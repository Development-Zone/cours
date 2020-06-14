# Javascript 

Javascript est un langague de programmation interprété ( le code est interprété à la volé par un interprétateur ). 
Javascritp permet de rendre les page web plus dynamique, peut etre utilisé coté Serveur avec NodeJs, ou peut etre utilisé dans d'autre application ( comme des moteur de jeu ) 

pour le web javascript est incontournable, car javascript fais partir des langaguage que la majorité des navigateur connaissent. 

## Principe de base de la programmation 

un code se lit de haut en bas et le programme va executer chaque instruction de code dans l'ordre. 
meme si les **;** ne sont pas obligatoire à la fin des instruction, je vous conseil de mettre les **;** pour indiquer la fin de l'instruction. 
d'autres langague comme le **C** est obligatoire, et c'est une bonne habitude de mettre les ; en fin d'instruction, comme ça on perd pas l'habitude avec d'autre language plus stricte. 

### Les variables 

Les variables sont des espace mémoire ou on pourra stocker des valeurs lors de l'excution du programme. 
En javascript il existe plusieurs type de variables : 

- **Boolean** : variable qui peuvent contenir soit _true_ soit _false. 
- **Number** : variable qui pevent contenir des nombres.
- **String** : variable qui contiendra une suite de caractere. ( attention je ne parle pas des string que les dame porte ).

- **Array** : tableau qui contiendra ranger par index qui commence par 0 jusqu'a le nombre d'élément du tableau - 1 . ( comme un ascenseur ). 
- **Object** : un object contiendra d'autre variable organisé par clé/valeur. 

une type de variable **undefined** est une variable ou on connais pas encore le type de la variable, ( ex d'une variable sans mettre de valeur ) 

dans c'est variable ont peut les classer en 2 catégorie, les variable par valeur, et les variable par référence. ( pour bien connaitre ce concept je vous conseil d'apprendre le C ou C++ et d'apprendre les pointeurs ) . Les variable : Boolean, Number et String sont des variable par valeur. 

les Array et les Object sont des des variable par références. 

### Déclaration de variabble 

en javascript pour déclarer les variable, il faut utiliser un de c'est mot clé : **const** , **let** , **var** ( var est le plus ancien, priviliégé **let**).
voici la syntaxe pour déclarer une variable : 

```javascript
let myVariable; 
```
dans cette exemple on déclare une variable qui à le nom myVariable, mais comme on à pas affecter de valeur, c'est une variable **undefined**. 

ont peut modifier la valeur d'une variable en utiisant le symbole d'affectation : **=** . comme ceci : 
```js
myVariable = 69;
```
dans cette exemple, nous attribuons la valeur **69** dans notre variable **myVariable**. 

nous pouvons aussi bien affecter la variable lors de sa déclaration comme ceci : 
```js
let myVariable = 69; 
```
cette facon de faire est plus rapide, est elle est obligatoire de faire pour les constant, car on ne peut pas modifié les constant après la déclaration. 

#### déclaration de variable pour chaque type de variable 

##### déclaration d'un boolean 

voici la déclaration d'un boolean 
```js
let myBoolean = true; 
```

la valeur est soit vrai ( _true_ ) soit faux ( _false_ )

##### déclaration d'un number 

voici la déclaration d'un number 
```js
const PI = 3.14159256359; 
```

ici les valeur décimale sont séparer par un point et non la virgule. comme vous avez pu le remarquer, je l'ai déclarer en constant, cette valeur ne pourra pas etre modifié par la suite. 

##### déclaration d'un string 

voici la déclaration d'un string ( ou chaine de caractère ) 
```js
let hello = "Hello World"; 
```

on peut aussi déclarer avec des simples quotes comme ceci : 
```js
let hello = 'Hello World'; 
```
##### déclaration d'un tableau 

voici la déclaration d'un tableau vide : 
```js
let myArray = []; 
``` 

le tableau myArray, contient un tableau qui ne contient aucun élément. 
pour ajouter un élément dans le tableau, faut une utiliser des méthode qu'on véra plus tard dans le cours. 

déclaration d'un tableau avec des élément lors de la déclaration : 
```js 
let langage = ["PHP", "Javascript", "Python", "Pascal", "Rust", "Go"]; 
```
si nous voulons modifié une valeur du tableau nous pouvons y acceder via son index ( la position dans le tableau ).
exemples si on veut modifié **Javascript** par **JS**, la valeur javascript est le 2eme élément du tableau, mais comme sur un tableau on commence à compter à partir de 0, sont index est 1. nous allons modifié comme ceci : 
```js
langage[1] = "JS"; 
```
la valeur **Javascript** est remplacer par **JS**. 

remarque: avec javascript nous pouvons mélanger les type dans un tableau, ce qui n'est pas autorisé dans des autres langage. 
(perso, je ne vois pas l'utilité de mélangé les type dans un tableau, en général on met des élément qui réprésente la meme choses ).

##### déclaration d'un object 

voici la déclaration d'un object vide : 
```js
let myObject = {}; 
```

nous avons déclarer un object vide, nous pouvons ajouter une valeur avec la notation pointé. comme ceci : 
```js
let myObject.myAttribut = 42; 
```
avec cette notation, nous pouvons ajouter, acceder au attributs de l'object. 

voici la déclaration d'un object avec affectation : 
```js
let student = {
    firstname: "Arthur", 
    lastname: "Dupont", 
    age: 30, 
    country: "France"
}
```

on peut acceder au attributs ( or key ) de la variable student via la notation pointé, 


### Les Fonctions

Les fonctions permet de réutiliser un bloc d'instruction. afin de simplier le code. Pour du code qui est utilisé souvent. 
une fonction peut recevoir des arguments en parametre, et peut retourner une valeur de retour à la fin de la fonction. 

une fonction se déclare avec le clé **function**.

dans cette exemple, je vais crée une fonction qui calcul le taux d'alcoolémique d'un individu, voici la déclaration de fonction : 

```js
function tauxAlcool(cl, weight, isMan, percentAlcool)
{
    let coeffIndividu = isMan ? 0.7 : 0.6 ; 
    let tauxAlcool = (cl * ( percentAlcool / 100 ) * 0.8) - ( coeffIndividu * weight ) ;
    return tauxAlcool;
}
```
dans l'exemple nous avons déclarer une fonctions qui prend 4 argument : 
- **cl** : la quantité d'alcool que l'individu a bu
- **weight** : le poids de l'individu exprimer en kilo. 
- **isMan** : un boolean a renseigner pour indiquer le sex de l'individu, **true** pour une homme, **false** pour une femme.
- **percentAlcool** : pourcentage du taux ( indiquer sur la bouteille d'alcool ) . ( 13% pour une bouteille de champagne engénéral ) 

cette fonction retourne une valeur qui est le taux d'alcoolémique( grace au mot clé **return** ). 

ce morceau de code ne sert a rien tant que la fonctionn n'est pas appeler. 

voici comment on execute une fonction : 
```js
let tauxRobert = tauxAlcool(30, 70, true, 13)
```

dans cette exemple, robert à bu 30 cl de boisson alcoolisé, il pese 70 kilo, et bien sur c'est une homme( d'ou la raison du **true**). 
il a bu une boisson avec une boison alcoolisé à 13% ( Champagne ) 

cette fonction peuvent etre appeler autant de fois que néccessaire. 


### Les structure de control

Dans un programme, les structure de control est primodial, c'est qui donne la logique du programme. et permet au programme de prendre des décisions. 


#### Les conditions

Les conditions permet de choisir un bloc de code en fonction d'une condition. 


##### la structure if

voici une condition avec un simple **if** : 
```js
let ageArthur = 30; 

if ( ageArtur >= 18 ) 
{
    console.log("Arthur est majeur"); 
}
```

comme la condition est vrai, le message **Arthur est majeur** sera afficher dans la console. 

##### la structue else-if 

voici une condition avec un **else-if** : 
```js
let ageArthur = 15; 

if ( ageArthur >=18 )
{
    console.log("Arthur est majeur" ); 
} 
else
{
    console.log("Arthur est mineur" ) ; 
}
```

comme  la condition dans le if ne passse passe pas, le message affiché sera : **Arthur est mineur** . 


