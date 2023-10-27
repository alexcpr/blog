---
layout: post_js_en
title: Why is w3schools a bad information source?
lang: en_US
toc: true
---

As a developer, I’m using <a href="https://discordapp.com/">Discord</a> every day to talk with people and friends about programming stuff, but I am mainly in programming Discord servers and I was, especially in a Discord server for a few days, which have ~25K members and I saw some people referring people to <a href="https://www.w3schools.com/">w3schools</a>, which is a bad information source to learn programming. So, I decided, to alert a staff to do something about it, and the staff said that w3schools is sometimes outdated, but that it’s not a big problem. However, in fact, it is a big problem because as a starter when you learn something and do it all the time it’s hard to stop doing it even more if nobody alerts you about it. With everything we know about web development best practices, w3schools ability to remain that known, baffles us all.

I’m not the first one saying that w3schools is bad and writing about it. <a href="https://web.archive.org/web/20110412103745/http://w3fools.com">This has already been done in the past</a >, the problem is that now they say that w3schools resolved these issues, well, I will show you they didn’t resolve all of them.

## Example of bad practices that w3schools makes you learn

- HTML

  - You probably won't believe me, but yes w3schools recommend to people to use Notepad for Windows users and TextEdit for Mac users.

  « Web pages can be created and modified by using professional HTML editors.

  However, for learning HTML we recommend a simple text editor like Notepad (PC) or TextEdit (Mac).

  We believe using a simple text editor is a good way to learn HTML.

  Follow the four steps below to create your first web page with Notepad or TextEdit. »

  <a href="https://www.w3schools.com/html/html_editors.asp">See it by yourself</a> <em>What does Linux users should use, though</em> 🤔

  I personally recommend <a href="https://code.visualstudio.com/">VS Code</a> or <a href="https://www.sublimetext.com/">Sublime Text</a> for simple code editor. For an IDE I recommend the <a href="https://www.jetbrains.com/">Jetbrains tools</a>

  - In their [HTML Formatting tutorial](https://www.w3schools.com/html/html_formatting.asp), they recommend the use of `<b>` tag, which is deprecated and should be replaced by CSS.
  - In their [HTML Basics tutorial](https://www.w3schools.com/html/html_basic.asp), they use `width` and `height` attributes in an `<img>` tag instead of using CSS. Barely better [here](https://www.w3schools.com/html/html_assets/images.asp), they inline style into the `<img>` tag.
  - In their [HTML Headings tutorial](https://www.w3schools.com/html/html_headings.asp), they inline style in an `<h1>` tag. Even in their [HTML Styles tutorial](https://www.w3schools.com/html/html_styles.asp) and [HTML CSS tutorial](https://www.w3schools.com/html/html_css.asp), they do so.
  - In their [HTML Links tutorial](https://www.w3schools.com/html/html_links.asp), showing how to change default `<a>` colors they did this.

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

  _Note that this time they used a <code>&#x3C;style&#x3E;</code> tag!_

  Although they could have just done it like this
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

  - In their [HTML Layout tutorial](https://www.w3schools.com/html/html_layout.asp), they recommend `float` over `flex` and doesn't even talk about `grid`, using the excuse that `flex` isn't supported by IE10 and lower.
    ![IE 11 Desktop](/assets/images/ie11-desktop.png)
    ![IE 11 Mobile](/assets/images/ie11-mobile.png)
    IE 11 Desktop works fine, but mobile doesn't. Flex works partially on IE 11, as [caniuse says](https://caniuse.com/#search=flex). However, it's not a real problem since IE only represents ~2% of browser usage.
  - In their [HTML Responsive tutorial](https://www.w3schools.com/html/html_responsive.asp), they use the `<media>` attribute to show different content depending on the browser width. It's better to use media queries in a separate CSS file.
  - They have a [tutorial about XHTML](https://www.w3schools.com/html/html_xhtml.asp), which is obsolete since HTML5.

- CSS:
  - In their [CSS Media Queries tutorial](https://www.w3schools.com/css/css3_mediaqueries.asp), they use the `<media>` attribute to show different content depending on the browser width. It's better to use media queries in a separate CSS file.
- JavaScript:
  - In all their tutorials, including their [JavaScript Variables tutorial](https://www.w3schools.com/js/js_variables.asp) and "JavaScript Best Practices," they use `var`, although nowadays you should be using `let` or `const`. `let` and `const` have been added since ES2015, and they are supported by IE11 (which represents almost 100% of current IE usage). You can write in ES2015 and convert your code to ES5 with tools such as [Babel](https://babeljs.io/).
  - They mostly use string concatenation instead of string interpolation, which is very easy using template literals.
  - They use `==` and `!=` instead of `===` and `!==` in variable comparisons.
  - They primarily show traditional functions instead of arrow functions, even when arrow functions would make more sense.
  - In their [JavaScript introduction](https://www.w3schools.com/js/tryit.asp?filename=tryjs_intro_lightbulb), they show how JavaScript can modify HTML attribute values, but they inline the JavaScript inside an `onclick` attribute, which is a bad practice. They should have used a `<script>` tag.
  - In their [JavaScript Where To tutorial](https://www.w3schools.com/js/js_whereto.asp), they don't mention that when placing JavaScript code in the `<head>`, you must use the `defer` or `async` attribute.
  - In their [JavaScript Output tutorial](https://www.w3schools.com/js/js_output.asp), they mention that `document.write` should be used for debugging only, but it shouldn't even be mentioned.
  - In their [JavaScript Variables tutorial](https://www.w3schools.com/js/js_variables.asp), they provide examples of reporting several variables on the same line without assignment.
  - In their [JavaScript Operators tutorial](https://www.w3schools.com/js/js_operators.asp), they don't mention the `**` operator.
  - In their [JavaScript Data Types tutorial](https://www.w3schools.com/js/js_datatypes.asp), they state, "You can consider it a bug in JavaScript that `typeof null` is an object. It should be null." It was a bug in the beginning, but this text could lead to the mistaken belief that this behavior will change someday.
  - There is no tutorial/documentation about the modern `fetch` API, only about [XMLHttpRequest](https://www.w3schools.com/js/js_ajax_intro.asp). [See why you should be using fetch and not XMLHttpRequest](https://blog.alexandrecipor.com/en/fetch-api).
  - In their [JavaScript Objects tutorial](https://www.w3schools.com/js/js_objects.asp), they could have used short syntax for object methods like this:
  <pre><code class="json">{
      firstName: &#x22;John&#x22;,
      lastName : &#x22;Doe&#x22;,
      id       : 1,
      method() {
          // code of the method here
      }
  }
  </code></pre>
  - In their [JavaScript Events tutorial](https://www.w3schools.com/js/js_events.asp), they teach a bad practice of using HTML events instead of using JavaScript events with the `addEventListener` method.
  - In their [JavaScript Arrays tutorial](https://www.w3schools.com/js/js_arrays.asp), they could have taught `for...of` to iterate over an array like this: `for (const element of array) { ... }`.
  - In their [JavaScript Hoisting tutorial](https://www.w3schools.com/js/js_hoisting.asp), it would be much easier using `let` and `const`.
  - In their [JavaScript Best Practices tutorial](https://www.w3schools.com/js/js_best_practices.asp), declarations on top are now considered a bad practice, and `let` and `const` should be used. Using Parameter Defaults is now part of the syntax.
  - In their [JavaScript Validation tutorial](https://www.w3schools.com/js/js_validation.asp), `addEventListener` should be used, again.
  - JavaScript Classes and Promises aren't mentioned.
- PHP:
  - In their [PHP Introduction](https://www.w3schools.com/php/default.asp), PHP5 is used, which shows how outdated the tutorial is.
  - In their [PHP Installation tutorial](https://www.w3schools.com/php/php_install.asp), PHP5 is still used, and there is no real explanation on how to install PHP. It's like saying, "Look at the documentation and figure it out; we won't tell you about `php -S` (the PHP internal web server for development)."
  - In their [PHP Variables tutorial](https://www.w3schools.com/php/php_variables.asp), they use double quotes by default instead of single quotes, even without interpolation. They use global variables, which is considered a bad practice.
  - In their [PHP Arrays tutorial](https://www.w3schools.com/php/php_arrays.asp), they use the old long syntax `array()` instead of the short syntax `[]`.
  - In their [PHP Ajax tutorial](https://www.w3schools.com/php/php_ajax_intro.asp), their JavaScript and PHP code are full of bad practices, and they don't discuss the fact that nowadays you should use the `fetch` API instead of AJAX. [See why you should be using fetch and not XMLHttpRequest](https://blog.alexandrecipor.com/en/fetch-api).
  - There is no tutorial about hashing passwords.
- Bootstrap:
  - In their [Bootstrap Introduction](https://www.w3schools.com/bootstrap/default.asp), they use Bootstrap 3, so there's no need to go further.
- W3.JS:
  - Their [W3.JS](https://www.w3schools.com/w3js/default.asp) library is heavy (12KB) and doesn't offer many features. W3.JS is like jQuery, heavy and less useful nowadays. In 2018, a library that allows direct interaction with the DOM is considered outdated, given the availability of modern UX libraries like React or VueJS.

## Why is the W3Schools site itself bad?

For more insights, you can read [this article](https://www.impressivewebs.com/w3schools-ugly-bad-good/).

## Fun Fact

I was looking at the [w3schools forum](http://w3schools.invisionzone.com/) and I found this [thread](http://w3schools.invisionzone.com/topic/57507-cloned-domain-from-w3schools/) saying that someone cloned the w3schools site. The cloned version is available [here](https://www.quanzhanketang.com/). This is an outdated version of the w3schools site, so you can explore even more outdated tutorials. You can also see this meme by yourself:

![W3Fools Meme](/assets/images/w3fools.png)

They were using HTML tables for layout, and by the way, this is not a lamp 😂. I'm sure you can still find some funny things they were doing a few years ago.

**PS:** If I forgot something, you can [open an issue](https://help.github.com/articles/creating-an-issue/) on the [GitHub repository](https://github.com/alexcpr/blog).

**TL;DR** w3schools → 🗑, use [the MDN](https://developer.mozilla.org/en-US/) instead 🕶
