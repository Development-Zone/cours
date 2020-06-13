# HTML

HTML de Hyper text markup language est un langague de balisage ( **ce n'est pas pas language de programmation**) qui permet de structurer les donné d'une page web. 

le HTML est le code envoyé au navigateur internert qui va ensuite lire le code pour rendre le contenu de la page. 

bien sur le HTML seul ne fournis pas de style, il sera complémenter avec du CSS pour la mise en forme du style. 

donc nous avons le : 

- HTML, pour la structure des donnée 
- et le CSS pour la mise en forme du style. 

le HTML contient des balise, qui ont chacun des roles défini. 2 types de balise, les balise paire, et les balise orphelines. 

```html
<p>
    ceci est un paragraphe
</p>
```

dans cette exemple nous avons la balise qui elle contient une balise ouvrant et une balise fermant . 

voici le strict minimun pour une page HTML : 

```html
<!DOCTYPE html>
<html>
    <head>
    </head>

    <body>
    </body>

</html>
```

la premiere ligne `<!DOCUTPE html>` est le doctype, il indique au navigateur le type de documents et la version du language, l'occurence, c'est de HTML5. ht
les balise `<html>` va contenir l'ensemble de la page html. dans cette balise, elle doit obligatoirement avoir 2 balise : 

- `<head>` : cette balise contient les métadonné, information titre dans l'onglet, le logo dans l'onget, la description pour le référencement ( google ), divers message quand on partage le liens avec le protocole open graphe utilisé par discord, facebook ( vous avez pu remarquer que quand vous partager un lien, discord rajoute un bloc de text en bas )

- `<body>` : cette balise va contenir l'ensemble de la page ( c'est ensemble de la page visible )


## les différente type de balise 

il existe plusieurs type de balise: 

### les balise de type block 

les de type block sont comme des boite qu'ont peut modifier la largeur, hauteur, position via le CSS. voici quelque balise de type block : 

- div: la div est une balise générique de type block qui n'as pas de sens définir, a utiliser il on trouve pas de balise sémentique adapter a ce que on veut. 
- nav: balise qui représente le menu de navigation , a utiliser pour indiquer qui a un menu de navigation a l'intérieur des 2 balise 
- header: balise sémentatique qui indique le haut de la page, la partie qui contient le titre, le site 
- footer: balise sémentique qui répresente le pied de page, 
- article: balise à utiliser pour représenter un article le contenu entre les balise doivent etre un article ( comme un forum, ). 
- serction: balise sémentique qui représente une section de la page. 

d'autre balise de type block existe, mais les rémunrée tous serait trop long et on ne vas pas imiter le dico 

### les balise de type inline

les balise de type inline sont des balise qui vont mettre en valeur le text comme de emphasique. voici quelque balise de type inline : 

- strong : balise qui sert a indiquer que le text est important, mise en valeur forte ( **attention, cette balise n'as pas de role de mettre en gras. meme si c'est le comportement par défaut des navigateur** ) la mise en gras doit se faire dans le CSS. 
- em: mise en valeur normal
- mark: mise en valeur visuel 

## Mémento balise HTML

vous pouvez trouver le mémento de openclassroom des balise html [ici](https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3/1608357-memento-des-balises-html)

## Ressource utilise

pour apprendre le HTML, vous pouvez suivre excelent cours de Mathieu Nebra, Cofondateur de Openclassroom 

[apprendre le HTML et CSS](https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3)