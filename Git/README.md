# Git

git est un systeme de versionning, qui permet de garder une trace de tous les modification et version d'un code. 
cela permet de garder une trace de tous les modications de code qu'ont appele **commit**. 

il existe plusieurs système de Versionning comme ( ajouter les noms des concurence ). 

git est un système distruber, chaque personne peut avoir ça propre copie et envoyé a une autre personne. 

donc avec git on peut revenir dans le code à un moment donné, revenir en arrière tester et faire des versions différent. savoir qui a fais la modification. 

git facilite la vie des dévellopeur, car il facilite le travail en équipe et le partage de code, la fusion de code ( merge ). 

## Lexique, les mots à connaitre 

**Commit** : Un commit est une modification du code, un commit va contenir plusieurs informations :
- Le nom de celui qui a crée
- La date du commit 
- Les modification effectuée
- Le numéro de SHA ( numéro unique qui permet d'identifier le commit) 

**Branche**: Les branches permettent de travailler sur des versions de code qui divergent de la branche principale (souvent appelé **master**) contenant votre code courant. 
( _une branche n'est ni plus ni moins qu'un alias qui correspondra à un numéro de SHA_ )

**SHA** : Code unique d'un commit, ce numéro permet d'etre sûr que le commit n'as pas été modifié, un nouveau SHA est généré a chaque commit, il ne peut pas y avoir deux SHA identiques. 

**Dépôt distant** : Souvent appelé _repo_ ou _repository_, un dépôt est un endroit de stockage de votre code, en l'occurence **Git**, GitHub est aussi un dépôt distant et une interface graphique.

**Merge** : Action de fusioner 2 branches, les modification de la branche éditée seront fusionnées a la branche voulue, souvent la branche principale.


## Les commandes

### A connaitre

Toutes ces commandes sont a entrer dans la CLI. (Command line interface, ce qui correspond au terminal ou invite de commande) 

**git init** : Initialise un projet git, cela crée un dossier .git dans le dossier de base de votre projet, ce dossier contiendra tous les commit, branches, etc... Il ne faut pas toucher a ce dossier a la main au risque de perdre vos données.

**git clone \<lien du repo\>** : Créé une copie d'un dépôt existant. 

**git add \<fichier\>** : Ajoute un fichier dans l'index* avant qu'il soit commité, l'index* et les modifications qui seront dans le commit lors de sa création. Remplacez \<fichier\> par "." pour ajouter tout vos fichiers.

> Index: considérez ceci comme une boite contenant le commit et ses modifications

**git commit -m "Message du commit"** : Crée un commit, cette action va enregistrer les modifications qui sont stockées dans l'index, ajoutés précédemant avec la commande _git add_. 

**git checkout \<SHA or branch\>** : Permet de se placer sur un commit en spéciant le numéro du SHA ou sur une branche via son nom. 

**git branch \<nom\>** : Crée une nouvelle branche. Pour voir la liste des branches existantes, ne spécifiez pas de nom.

### Pour travailer en équipe

**git push \<remote\> \<branch\>** : Permet d'envoyer le code d'une branche sur un repo. (en général github, framagit, gitlab). **remote** est l'adresse du dépôt ou son alias (souvent elle s'appele **origin**), **branch** est la branche sur laquelle vous voulez envoyer votre code.

**git fetch** : Permet de récuperer le code sur un dépôt distant sans appliquer les modification sur le repo local.

**git pull** : Permet de récuperer le code et faire un merge sur le repo local, cette commande est l'équivalent de **git fetch** suivi de **git merge**. 


## Le fichier gitignore

Ce fichier permet de dire a git quels fichiers/dossiers il va ignorer.

Tous les fichiers/dossiers contenu dans ce fichier ne seront ni commité ni versionné. 

Généralement on ignore les fichiers de configuration de notre projet car ils contiennent des informations privées.

### Creation et configuration

Créez un nouveau fichier dans le dossier de base de votre projet et nommez le ``.gitignore``.

Ensuite il vous suffit juste d'entrer le chemin d'accès du/des fichier(s) a ignorer.

Exemple :

Admettons que vos fichiers son organisé comme ceci

![gitignore](https://imgur.com/XeCS7ea.png)

Vous voulez ignorer le ficher apiKeys.js et le dossier build/

Ce que devra contenir votre ``.gitignore``.

```
apiKeys.js

build/
```

Voila, c'est aussi simple que ça. 

