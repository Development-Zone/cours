# Git

Git est un système de versionning, qui permet de garder une trace de toutes les modifications et versions d'un code. 
Ces modifications sont appelées **commit**. 

Il existe plusieurs autres systèmes de versionning comme GitHub, SVN (Subversion), Bitbucket, Perforce, ou Mercurial. 

Git est un système distribué, chaque personne peut avoir sa propre copie et la partager à une autre personne. 

Git permet donc de parcourir l'historique des version d'un projet, de revenir en arrière, tester et faire des versions différentes, et même de connaître l'auteur de ces modifications. 

Il facilite la vie des développeurs car il facilite le travail en équipe et le partage de code ainsi que la fusion de code (appelée **merge**). 

## Lexique, les mots à connaitre 

**Commit** : Un commit est une modification du code, il contient plusieurs informations :
- Le nom de l'auteur du commit
- La date de création du commit 
- Les modifications effectuées
- Le numéro de SHA ( numéro unique qui permet d'identifier le commit) 

**Branche**: Les branches permettent de travailler sur des versions de code qui divergent de la branche principale (souvent appelée branche **master**). On trouve en général une branche master et une branche dev, qui sert à tester de nouvelles fonctionnalités sans affecter le programme principal.
(_une branche n'est ni plus ni moins qu'un alias qui correspondra à un numéro de SHA_)

**SHA** : Code unique d'un commit, il permet d'être sûr qu'il n'a pas été modifié. Un nouveau SHA est généré à chaque commit. Il ne peut pas y avoir deux SHA identiques. 

**Dépôt distant** : Souvent appelé _repo_ ou _repository_, un dépôt est un endroit de stockage de votre code, en l'occurence **Git**. GitHub est aussi un dépôt distant et une interface graphique très utilisée.

**Merge** : Action de fusionner 2 branches, les modifications de la branche éditée seront fusionnées à la branche voulue, souvent la branche principale.


## Les commandes

### À connaitre

Toutes ces commandes sont à entrer dans la CLI. (Command line interface, ce qui correspond au terminal ou invite de commande) 

**git init** : Initialise un projet git, cela crée un dossier .git dans le dossier de base de votre projet, ce dossier contiendra tous les commit, branches, etc... Il ne faut pas éditer ce dossier au risque de perdre vos données.

**git clone \<lien du repo\>** : Permet de créer une copie d'un dépôt existant. 

**git add \<fichier\>** : Ajoute un fichier dans l'index* avant qu'il soit commité. Remplacez \<fichier\> par "." pour ajouter tout vos fichiers.

> Index: considérez ceci comme une boite contenant le commit et ses modifications

**git commit**: Crée un commit, cette action va enregistrer les modifications qui sont stockées dans l'index, ajoutés précédemment avec la commande _git add_.
Cette commande va ouvrir un éditeur de texte dans le terminal, le commit sera pris en compte après avoir renseigné le nom du commit et l'avoir sauvegardé.

**git checkout \<SHA or branch\>** : Permet de se placer dans un commit en spécifant le numéro du SHA ou dans une branche via son nom. 

**git merge _\<branche1\>_ _[\<branche2\>]_** : Permet de fusionner les commits de la branche1 dans la branche2, si la branche2 n'est pas renseignée, c'est la branche actuelle qui sera pris en tant que branche 2. (le paramètre _branche2_ est facultatif). Si il y a eu des modifications au même endroit dans les deux branches, cela peut causer des conflits lors du merge. Git vous proposera alors quelle version choisir et vous demandera de résoudre les conflits manuellement avant le merge. 

###  pour obtenir des information 

**git status** : Permet d'obtenir des information sur l'état du repo. On peut obtenir l'état de l'index, le numéro de la branche actuel ou du commit (SHA) actuel et d'autre information (c'est une commande beaucoup utilisée).

**git log** : Affiche la liste des commits de la branche actuelle.

**git show _[\<SHA\>]_** : Permet d'afficher des informations détaillées sur un commit. Le numéro de SHA est facultatif : si il n'est pas renseigné, c'est le dernier commit qui sera pris.

**git diff _[\<SHA1\>]_ _[\<SHA2>]_** : Cette commande affiche les différences de code entre 2 commits, si rien n'est renseigné dans les SHA, la différence entre l'état du travail actuel et du dernier commit sera affichée. Si il n'y a que le SHA1 de renseigner, c'est la différence entre l'état de travail et le commit renseigné SHA1 qui sera affichée. 

**git blame _\<file\>_** : Affiche le code d'un fichier en indiquant qui a édité les lignes, cette commande est utilisée pour retrouver l'auteur d'une modification en cas de bugs par exemple (cette commande n'est utile que si on travaille à plusieurs).




### Pour travailler en équipe : 
**git branch \<nom\>** : Crée une nouvelle branche. Si aucun nom n'est spécifié, c'est la liste totale des branches qui sera affichée.

**git push \<remote\> \<branch\>** : Permet d'envoyer le code d'une branche sur un repo (en général Github, Framagit ou Gitlab). **remote** est l'adresse du dépôt ou son alias (souvent elle s'appelle **origin**), et **branch** est la branche sur laquelle le code va être transféré.

**git fetch** : Permet de récupérer le code sur un dépôt distant sans appliquer les modifications sur le repo local.

**git pull** : Permet de récupérer le code et d'en faire un merge sur le repo local. Cette commande est l'équivalent de **git fetch** suivi de **git merge**.


## Le fichier .gitignore

Ce fichier permet d'indiquer à git quels fichiers/dossiers il devra ignorer lors de transferts.

Tous les fichiers/dossiers contenu dans ce fichier ne seront ni commités ni versionnés.

Généralement on ignore les fichiers de configuration de notre projet car ils contiennent des informations privées.

### Création et configuration

Créez un nouveau fichier dans le dossier de base de votre projet et nommez le ``.gitignore``.

Ensuite il vous suffit simplement d'entrer le(s) chemin d'accès du/des fichier(s) à ignorer.

Exemple :

Admettons que vos fichiers sont organisés comme ceci :

![gitignore](https://imgur.com/XeCS7ea.png)

Vous voulez ignorer le ficher apiKeys.js ainsi le dossier build/

Votre fichier ``.gitignore`` devra alors contenir :

```
apiKeys.js

build/
```

## Conclusion

Ce court texte d'introduction à l'utilisation de Git vous a donc appris les définitions des principaux mots clés utilisés dans le versionning, les principales commandes propres à git ainsi que quelques précisions qui vous seront utiles.
Pour passer au cours suivant, [cliquez ici](INSÉRER COURS 2 ICI).
