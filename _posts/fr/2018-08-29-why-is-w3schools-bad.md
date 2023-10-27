---
layout: post_js_fr
title: Pourquoi w3schools est-il une mauvaise source d'information ?
lang: fr_FR
toc: true
---

En tant que développeur, j’utilise [Discord](https://discordapp.com/) tous les jours pour discuter avec des personnes et des amis au sujet de la programmation et je suis principalement dans des serveurs Discord en rapport à la programmation. J’ai surtout été dans un serveur Discord en particulier pendant quelques jours, serveur rassemblant environ 25.000 membres, et j’ai pu apercevoir des personnes partager des liens menants vers des tutoriels du site [w3schools](https://www.w3schools.com/), site qui est une mauvaise source d’information pour apprendre à programmer. J’ai donc décidé d’alerter un administrateur pour qu’il fasse quelque chose à ce sujet et il m’avait répondu que les tutoriels provenant du site w3schools sont parfois désuets et que cela n’est pas un gros problème en soi. Cependant, il est clair que c’est un gros problème parce que, en tant que débutant, quand on apprend quelque chose et qu’on le fait tout le temps, il est difficile d’arrêter de le faire et encore plus si personne ne vous en avertit. Avec tout ce que nous savons sur les meilleures pratiques de développement web, la capacité de w3schools à rester connu nous déconcerte tous.

Je ne suis pas le premier à dire que w3schools est mauvais ni le dernier à écrire sur le sujet ([cela a déjà été fait dans le passé](https://web.archive.org/web/20110412103745/http://w3fools.com)). Le problème est que maintenant, ceux qui conseillent l’utilisation de w3schools commencent à dire que ce site a résolu leurs problèmes. Et bien je vais vous montrer qu’il ne les a pas tous résolus.

## Exemple de mauvaises pratiques que w3schools vous fait apprendre

- HTML

  - Vous ne me croirez probablement pas, mais oui, w3schools recommande aux gens d’utiliser Notepad pour les utilisateurs de Windows et TextEdit pour les utilisateurs de Mac.

  « Les pages Web peuvent être créées et modifiées à l’aide d’éditeurs HTML professionnels.

  Cependant, pour apprendre le HTML, nous recommandons un éditeur de texte simple comme Notepad (PC) ou TextEdit (Mac).

  Nous croyons que l’utilisation d’un simple éditeur de texte est une bonne façon d’apprendre le HTML.

  Suivez les quatre étapes ci-dessous pour créer votre première page Web avec Notepad ou TextEdit. »

  [Voyez par vous-même](https://www.w3schools.com/html/html_editors.asp) _Qu’est-ce que les utilisateurs de Linux devraient utiliser alors ?_ 🤔

  Je recommande personnellement [VS Code](https://code.visualstudio.com/) ou [Sublime Text](https://www.sublimetext.com/) pour un éditeur de code simple. Pour un IDE, je recommande les [outils Jetbrains](https://www.jetbrains.com/).

  - Dans leur [tutoriel de formatage HTML](https://www.w3schools.com/html/html_formatting.asp), ils recommandent l’utilisation de la balise `<b>` qui est maintenant obsolète et devrait être remplacée par du CSS.
  - Dans leur [tutoriel sur les bases du HTML](https://www.w3schools.com/html/html_basic.asp), ils utilisent les attributs `width` et `height` dans une balise `<img>` au lieu d’utiliser du CSS. A peine mieux ici, ils inline du style dans la balise `<img>`.
  - Dans leur [tutoriel sur les éléments de titre HTML](https://www.w3schools.com/html/html_headings.asp), ils utilisent l’attribut `style` dans une balise `<h1>`. Même dans leurs tutoriels “[style HTML](https://www.w3schools.com/html/html_styles.asp)” et “[HTML CSS](https://www.w3schools.com/html/html_css.asp)” ils le font.
  - Dans leur [tutoriel des liens HTML](https://www.w3schools.com/html/html_links.asp) montrant comment changer les couleurs par défaut de la balise `<a>`, ils ont fait ceci
  <pre><code>&#x3C;style&#x3E;
    a:link {
        color: green;
        background-color: transparent;
        text-decoration: none;
    }
    a:visited {
        color: pink;
        background-color: transparent;
        text-decoration: none;
    }
    a:hover {
        color: red;
        background-color: transparent;
        text-decoration: underline;
    }
    a:active {
        color: yellow;
        background-color: transparent;
        text-decoration: underline;
    }
  &#x3C;/style&#x3E;
  </code></pre>

  _Notez que cette fois-ci ils ont utilisé une balise <code>&#x3C;style&#x3E;</code> !_

  Bien qu’ils auraient pu le faire comme ça
  <pre><code>&#x3C;style&#x3E;
    a {
        text-decoration: none;
        background-color: transparent
    }
    a:link {
        color: green
    }
    a:visited {
        color: pink
    }
    a:active,
    a:hover {
        color: red;
        text-decoration: underline
    }
    a:active {
        color: #ff0
    }
  &#x3C;/style&#x3E;
  </code></pre>

  - Dans leur [tutoriel de mise en page HTML](https://www.w3schools.com/html/html_layout.asp), ils recommandent l’utilisation de `float` au lieu de `flex`, ne parlent même pas de `grid` et, comme excuse, disent que `flex` n’est pas supporté par IE10 et moins. ![](/assets/images/ie11-desktop.png) ![](/assets/images/ie11-mobile.png) IE 11 Desktop fonctionne bien, mais pas la version mobile. Flex fonctionne partiellement sur IE 11 comme le dit [caniuse](https://caniuse.com/#search=flex). Cependant, ce n’est pas un vrai problème puisque IE ne représente que 2% de l’utilisation des navigateurs environ.
  - Dans leur [tutoriel sur le design Responsive](https://www.w3schools.com/html/html_responsive.asp), ils utilisent l’attribut `<media>` pour afficher différents contenus en fonction de la largeur du navigateur. Ne faites pas cela, utilisez plutôt les media queries dans un fichier CSS séparé.
  - Ils ont un [tutoriel sur le XHTML](https://www.w3schools.com/html/html_xhtml.asp) qui est mort depuis HTML5.

- CSS
  - Dans leur [tutoriel CSS Media Queries](https://www.w3schools.com/css/css3_mediaqueries.asp) et, ils utilisent l’attribut `<media>` pour afficher différents contenus en fonction de la largeur du navigateur. Ne faites pas cela, utilisez plutôt les media queries dans un fichier CSS séparé.
- JavaScript
  - Dans tous leurs tutoriels, y compris leur [tutoriel sur les variables JavaScript](https://www.w3schools.com/js/js_variables.asp) et “[Meilleures pratiques JavaScript](https://www.w3schools.com/js/js_best_practices.asp)”, ils utilisent `var` bien qu’aujourd’hui vous devriez utiliser `let` ou `const`. Dans ES2015, `let` et `const` ont été ajoutés et sont supportés par IE11 (IE11 représente presque 100% de l’utilisation actuelle d’IE). Vous pouvez écrire en ES2015 et convertir votre code en ES5 avec des outils tels que [babel](https://babeljs.io/). _Et pour être honnête, de nos jours, vous pouvez développer en ES2015, car IE ne représente que 2% de l’utilisation des navigateurs environ._
  - Dans tous leurs tutoriels, ils font de la concaténation bien qu’ils puissent faire de l’interpolation, ce qui est très facile en utilisant des modèles littéraux.
  - Dans tous leurs tutoriels où ils comparent des variables, ils utilisent `==` et `!=` au lieu d’utiliser `===` et `!==`.
  - Dans tous leurs tutoriels, ils montrent le plus souvent des fonctions traditionnelles au lieu de fonctions fléchées, même lorsque cela a plus de sens.
  - Dans leur [introduction à JavaScript](https://www.w3schools.com/js/tryit.asp?filename=tryjs_intro_lightbulb), ils montrent comment JavaScript peut modifier les valeurs des attributs HTML. Le problème est qu’ils inline le code JavaScript à l’intérieur d’un attribut `onclick`, ce qui est une mauvaise pratique, car ce n’est pas très lisible et c’est au même niveau qu’inline du CSS. Ils auraient dû utiliser une balise `<script>`.
  - Dans leur [tutoriel JavaScript Where To](https://www.w3schools.com/js/js_whereto.asp), ils ne mentionnent pas que lorsqu’on place du code JavaScript dans la balise `<head>`, vous devez utiliser l’attribut `defer` ou `async`.
  - Dans leur [tutoriel JavaScript Output](https://www.w3schools.com/js/js_output.asp), même s’ils ont averti que `document.write` ne devrait être utilisé que pour le débogage, honnêtement, cela ne devrait même pas être mentionné.
  - Dans leur [tutoriel sur les variables JavaScript](https://www.w3schools.com/js/js_variables.asp), il y a plusieurs exemples de rapports de plusieurs variables sur une même ligne sans assignation.
  - Dans leur [tutoriel sur les opérateurs JavaScript](https://www.w3schools.com/js/js_operators.asp), ils ne mentionnent pas l’opérateur `**`.
  - Dans leur [tutoriel sur les types de données JavaScript](https://www.w3schools.com/js/js_datatypes.asp), ils disent : “Vous pouvez considérer que c’est un bug dans JavaScript que le type de null est un objet. Il devrait être null.” C’était un bug au début, mais ce texte pourrait faire penser, à tort, que ce comportement changera un jour.
  - Pas de tutoriel/documentation sur l’API `fetch` moderne seulement sur [XMLHttpRequest](https://www.w3schools.com/js/js_ajax_intro.asp). _[Voyez pourquoi vous devriez utiliser fetch et non XMLHttp](https://blog.alexandrecipor.com/fr/fetch-api)_
  - Dans leur [tutoriel sur les objets en JavaScript](https://www.w3schools.com/js/js_objects.asp), ils auraient pu utiliser la syntaxe courte pour des créer une méthode dans un objet comme ceci
  <pre><code class="json">{
    firstName: &#x22;John&#x22;,
    lastName : &#x22;Doe&#x22;,
    id       : 1,
    method() {
      // code de la méthode ici
    }
  }
  </code></pre>
  - Dans leur [tutoriel sur les événements JavaScript](https://www.w3schools.com/js/js_events.asp), ils enseignent une mauvaise pratique consistant à utiliser des événements HTML au lieu d’utiliser des événements JavaScript avec la méthode `addEventListener`.
  - Dans leur [tutoriel sur les tableaux en JavaScript](https://www.w3schools.com/js/js_arrays.asp), ils auraient pu enseigner comment itérer sur un tableau comme ceci `for (const element of array) { ... }`
  - Dans leur [tutoriel JavaScript Hoisting](https://www.w3schools.com/js/js_hoisting.asp), il serait beaucoup plus facile d’utiliser `let` et `const`.
  - Dans leur [tutoriel sur les meilleures pratiques en JavaScript](https://www.w3schools.com/js/js_best_practices.asp) les déclarations en haut sont maintenant une mauvaise pratique, `let` et `const` devraient être utilisés à la place. Utiliser les paramètres par défaut fait maintenant partie de la syntaxe.
  - Dans leur [tutoriel de validation JavaScript](https://www.w3schools.com/js/js_validation.asp), `addEventListener` devrait, encore une fois, être utilisé.
  - Les classes JavaScript ne sont pas mentionnées.
  - Les promesses JavaScript ne sont pas mentionnées.
- PHP
  - Dans leur [introduction à PHP](https://www.w3schools.com/php/default.asp), PHP5 est suffisant pour montrer à quel point le tutoriel est dépassé.
  - Dans leur [tutoriel d’installation de PHP5](https://www.w3schools.com/php/php_install.asp), il n’y a pas vraiment d’explications sur la façon d’installer PHP, c’est comme dire “Regardez la doc et démerdez-vous avec elle, nous ne vous parlerons pas de php -S (serveur web interne php pour le développement)”.
  - Dans leur [tutoriel sur les variables en PHP](https://www.w3schools.com/php/php_variables.asp), ils utilisent `"` par défaut au lieu de `'` même sans interpolation. Ils utilisent des variables globales, ce qui est également une mauvaise pratique.
  - Dans leur [tutoriel sur les tableaux en PHP](https://www.w3schools.com/php/php_arrays.asp), ils utilisent l’ancienne syntaxe longue `array()` bien qu’ils devraient utiliser la syntaxe courte `[]`
  - Dans leur [tutoriel AJAX en PHP](https://www.w3schools.com/php/php_ajax_intro.asp), leurs codes JavaScript et PHP sont pleins de mauvaises pratiques et ils ne parlent même pas du fait que, de nos jours, vous devriez utiliser l’API `fetch` à la place d’AJAX. _[Voyez pourquoi vous devriez utiliser fetch et non XMLHttp.](https://blog.alexandrecipor.com/fr/fetch-api)_
  - Pas de tutoriel sur le hachage des mots de passe.
- Bootstrap
  - Dans leur [introduction a Bootstrap](https://www.w3schools.com/bootstrap/default.asp), ils utilisent Bootstrap 3, pas besoin d’aller plus loin.
- W3.JS
  - Leur bibliothèque [W3.JS](https://www.w3schools.com/w3js/default.asp) est lourde (12Ko) et ne fait pas beaucoup de choses. W3.JS est comme jQuery, lourd et inutile de nos jours, c’est pourquoi je ne recommande pas d’utiliser ces deux bibliothèques. En 2018, une bibliothèque qui permet d’interagir directement avec le DOM est assez anti-modèle maintenant qu’il existe des bibliothèques UX comme React ou VueJS.

## Pourquoi le site w3schools est-il lui-même mauvais ?

Pour cette partie, je vous recommande de lire [cet article](https://www.impressivewebs.com/w3schools-ugly-bad-good/).

## Fait amusant

Je me balader sur le [forum de w3schools](http://w3schools.invisionzone.com/) et j’ai trouvé ce [topic](http://w3schools.invisionzone.com/topic/57507-cloned-domain-from-w3schools/) disant que quelqu’un a cloné le site de w3schools. La version clonée est disponible [ici](https://www.quanzhanketang.com/) c’est une version ancienne du site de w3schools, donc vous pouvez explorer les tutoriels encore plus dépassés, vous pouvez aussi voir ce meme par vous-même

![](/assets/images/w3fools.png)

Ils utilisaient des tableaux HTML pour la mise en page et d’ailleurs ce n’est pas une lampe 😂 Et je suis sûr que vous pouvez trouver encore des choses drôles qu’ils faisaient il y a quelques années.

\*_PS:_- Si j’ai oublié quelque chose, vous pouvez [ouvrir une issue](https://help.github.com/articles/creating-an-issue/) sur le [dépôt GitHub](https://github.com/alexcpr/blog).

\*_TL;DR_- w3schools →🗑, utilisez plutôt [le MDN](https://developer.mozilla.org/en-US/) 🕶
