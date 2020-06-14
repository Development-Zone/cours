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

La premiere ligne `<!DOCUTPE html>` est le doctype, il indique au navigateur le type de documents et la version du language, en l'occurence HTML5.
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

### Les balise de type inline

Les balise de type inline sont des balise qui vont mettre en valeur le text comme en **gras**, _italique_, __barré__ ou <u>souligné</u>. 

- strong : balise qui sert a indiquer que le text est important, mise en valeur forte (**attention, cette balise n'as pas le role de mettre en gras. meme si c'est le comportement par défaut des navigateur**) la mise en gras doit se faire dans le CSS ou en utilisant la balise suivante. 
- b : sert a indiquer que le texte doit être en gras mais n'aura aucune importance, c'est juste pour *attirer l'attention sur ce mot*
- em : mettre le texte en italique
- mark : surligner le texte, par défaut, il sera surligné en jaune, libre a vous de changer ceci dans le CSS.

## Mémento balise HTML

Vous pouvez trouver le mémento de openclassroom des balises HTML [ici](https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3/1608357-memento-des-balises-html)

## Ressource utilise

Pour apprendre le HTML, vous pouvez suivre cet excellent cours de Mathieu Nebra, Cofondateur de Openclassroom.

[apprendre le HTML et CSS](https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3)