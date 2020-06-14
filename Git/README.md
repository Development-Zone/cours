# Git

git est un systeme de versionning, qui permet de garder une trace de tous les modification et version d'un code. 
cela permet de garder une trace de tous les modications de code qu'ont appele **commit**. 

il existe plusieurs système de Versionning comme ( ajouter les noms des concurence ). 

git est un système distruber, chaque personne peut avoir ça propre copie et envoyé a une autre personne. 

donc avec git on peut revenir dans le code à un moment donné, revenir en arrière tester et faire des versions différent. savoir qui a fais la modification. 

git facilite la vie des dévellopeur, car il facilite le travail en équipe et le partage de code, la fusion de code ( merge ). 

## Lexique, les mots à connaitre 

**Commit** : un commit est une modification du code, un commit va contenir plusieurs information, le nom de celui qui a crée , la date du commit, les modification effectuer, le numéro de SHA ( numéro unique qui permet d'identifier le commit) 

**Branches**: une branches est une version différents du code, par défaut quand on crée un projet, nous avons la branche **master** qui est la branche principale. je vois une branche comme une dimension parallèle, la branche est une version différent d'une réalité ou les commit sont des point temporel. 
( j'espere mon explication avec dimension parallèle vous a aider a comprendre ) 
( _une branche n'est ni plus ni moins qu'un alias qui correspondra à un numéro de SHA_ )

**SHA** : numéro unique qu'un commit contient, ce numéro est utile et permet d'etre sur que le commit n'as pas était modifié, vu a chaque nouveau commit un SHA est généré et ne peut pas avoir 2 SHA identique 

**depot distant** : depot comme Github, Framagit afin de stocker le code sur un serveur en commun. comme git est basé sur un distribuer, nous utilisons un depot commun afin de faciliter le partage. 

**merge** : action de fusioner 2 branche , les modification d'une branche sont mis dans une autre branche. 


## les commande de git 

### les principaux a connaitre 

tous les commande sont a rentrer dans la CLI ( Command line interface , ce qui correspond au terminal ou invite de commande) 

**git init** : initialise un projet git, cela crée le dossier .git dans le dossier, ce dossier contiendra tous les commit, branche, c'est un dossier qu'ont ne manipule pas directement 

**git clone _adresse_** : crée une copie d'un projet existant. 

**git add _file1_** : ajoute un fichier dans l'index avant qui soit commité, l'index et les modification qui seront dans le commit lors de la création du commit 

**git commit** : crée un commit, cette action va enregistrer les modification qui sont stocker dans l'index, ajouté précédemant avec la commande _git add_ cette commande va ouvrir un editeur de text dans le terminal, le commit sera effectif avec après renseigner le nom du commit et sauvegarde le fichier dans l'éditeur 

**git checkout _SHA or branch_** : cette commande permet de se placer sur un commit ou autre branch en spéciant le numéro du SHA ou le nom de la branche 

**git branch _name_** : permet de crée une nouvelle branche, dans mon exemple avec le voyage dans le temps c'est comme si on crée une nouvelle dimension parallèle. _name_ est a remplacer par le nom de la branche qu'on veut. 

**git merge _branch1_ _[branch2]_** : permet de fusioner les commit de la branch1 dans la branch2, si la branch2 n'est pas renseigné, c'est la branche actuel qui sera pris en tant que branche 2. ( le parametre _branch2_ est facultatif ). si au niveau des 2 branche, il a eu des modification au meme endroit, lors de la merge, cela causera des conflits. git vous propsera quel version choisir et vous demandera de résoudre les conflits manuellement avant le merge. 

###  pour obtenir des information 

**git status** : donne des information sur l'état du repo , elle donne l'état de l'index, le nombre de la branche actuel ou du commit ( SHA ) actuel et d'autre information. ( c'est une commande que j'utilise souvent ) 

**git log** : affiche la liste des commit de la branche actuel 

**git show _[SHA]_** : affiche le détail de commit, le numéro de SHA est facultatif, si il n'est pas renséigné, c'est le dernier commit qui sera pris.

**git diqff _[SHA1]_ _[SHA2]_** : cette commande affiche les différence de code entre 2 commits, si rien n'est renséigné dans les SHA, il donnera la différence entre l'état du travail actuel et du dernier commit. si il y a que le SHA1 de renseigner, on aura la différence de l'état de travail avec le commit renseingé SHA1. 

**git blame _file_** : affiche le code d'un fichier en indiquant qui a éditer les lignes, cette commande est utilise si on veut retrouver le coupable d'un bug et de le blamer. ( cette commande est utile que si on travaill à plusieurs)



### pour travailer en équipe : 

**git push _remote_ _branch_** : action qui permet d'envoyer le code d'une branche sur une repo. (en général github, framagit, gitlab ). **remote** est l'adresse du depot ou son alias ( souvent elle s'appele **origin**)

**git pull** : cette action va récuper le code est faire un merge sur le repo local, cette commande est l'équivalent de **git fetch** suivi de **git merge**. 

**git fetch** : action qui consiste a récuperer le code sur un depot distant sans appliquer les modification sur le repo local 


