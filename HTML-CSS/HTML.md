# HTML

HTML de Hyper Text Markup Language est un langague de balisage (**ce n'est pas pas language de programmation**) qui permet de structurer les données d'une page web. 

Le HTML est le code envoyé au navigateur internet qui va ensuite le lire pour le traduire et le rendre visible a l'utilisateur.

Bien sûr le HTML seul ne fournis pas de style, il sera complémenté avec du CSS pour la mise en forme du style. 

Donc nous avons : 

- Le HTML, pour la structure des données.
- Le CSS pour la mise en forme du style.

Le HTML contient des balises, qui ont chacun des rôles définis. Il y a deux types de balises, les balises paires, et les balises orphelines. 

```html
<p>
    Ceci est un paragraphe dans une balise paire
</p>
```

Dans cet exemple nous pouvons voir deux balises, une ouvrante ``<p>`` et une fermante ``</p>``.

Une balise orpheline ressemble a ceci : ``<br>``. Cette balise permet de sauter une ligne, car oui, il ne vous suffit pas juste de cliquer "Entrée" pour faire ceci.

certaine balise peuvent comporter des attributs, prenont l'exemple de la balise ``<a>`` ( a comme anchor, ). cette balise doit avoir un attributs renseigné. 

```html
<a href="page1">Lien vers la page 1</a>
```

dans cette exemple, la balise a posede un attributs donc la key est **href** et la valeur est **page1**. certaine balise peuvent avoir des attributs a renseigner comme la balise ``<img>`` : 

```html
<img src="img/photo1.jpg" alt="photo" >
```

dans cettte balise image, elle contient 2 attributs : src et alt. src permet d'indiquer le chemin de la photo donc la le chemin est **img/photo1.jpg**. 
alt est un attributs qui permet de donnée une descript sur image quand elle ne peut pas etre afficher ( navigateur pour aveugles, navagateur ne supportant pas le rendu graphique), cette attributs est aussi utilisé par le bot google pour le référencement web. ( les bot google est un grand aveugle ). 

voici 2 attributs a connaitre qu'ont peut mettre sur n'importe quel balise : 
**id** : id lui renseigne un identifiant unique sur la balise. 
**class** : class lui renseigne une classe. les classe sont majoritairement utilisé dans le css pour regrouper les balise de la meme classe. ca permet distinguer un certain groupe de balise qui auront le meme style CSS. 

Voici le strict minimun pour une page HTML : 

```html
<!DOCTYPE html>
<html>
    <head>
    </head>

    <body>
    </body>

</html>
```

La premiere ligne `<!DOCYTPE html>` est le doctype, il indique au navigateur le type de documents et la version du language, en l'occurence HTML5.
Les balises `<html>` vont contenir l'ensemble de la page html. dans cette balise, il doit obligatoirement y avoir 2 balises : 

- `<head>` : Contient les métadonnées, information principale de votre page, titre, le logo, la description (pour le référencement sur google ou autre), les informations pour l'embed (bloc qui va afficher les informations de votre page) avec le protocole open graphe utilisé par discord ou facebook. 

![embed](https://imgur.com/ejZCUkG.png)

- `<body>` : Contient l'ensemble de la page, donc tous ce qui sera visible sur la page.


## Les autres type de balise 

Il existe plusieurs autres type de balises.

### Les balises de type block 

Les balises de type block sont comme des boites qu'ont peut modifier: Largeur, Hauteur, position, tout ça via le CSS.

- nav: balise qui représente le menu de navigation.
- header: balise sémantique qui indique le haut de la page.
- div: la div est une balise générique de type block qui n'as pas de sens défini. A utiliser si on ne trouve pas de balise sémantique adapté a ce que l'on cherche. 
- article: balise à utiliser pour représenter un article, le contenu entre les balise doivent etre un article (comme un forum, ou un blog). 
- section: balise sémantique qui représente une section de la page. 
- footer: balise sémantique qui répresente le pied de page.

### Les balises de type inline

Les balise de type inline sont des balise qui vont agir sur le text.

- ``strong`` : balise qui sert a indiquer que le text est important, mise en valeur forte  la mise en gras doit se faire dans le CSS ou en utilisant la balise suivante. 
- ``b`` : sert a attirer l'attention sur le contenu n'aura aucune importance, c'est juste pour *attirer l'attention sur ce mot*
- ``em`` ou ``i`` : indiquer le text pour le mettre en valeur 
- ``mark`` : indiquer le text pour indiquer une certaine importance
- ``u`` : indiquer le text pour indiquer une certaine importance

**attention, cette c'est balise cité, ne sont pas des balise pour de la mise en forme. si vous voulez mettre en forme, c'est dans le CSS qui faut le faire**

## Mémento balises HTML

Vous pouvez trouver le mémento de openclassroom des balises HTML [ici](https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3/1608357-memento-des-balises-html)

## Ressources utilisées

Pour apprendre le HTML, vous pouvez suivre cet excellent cours de Mathieu Nebra, Cofondateur de Openclassroom.

[apprendre le HTML et CSS](https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3)