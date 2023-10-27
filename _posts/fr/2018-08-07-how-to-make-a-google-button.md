---
layout: post_js_fr
title: Comment faire un bouton Google avec du CSS
lang: fr_FR
---

Personnellement, j’aime le design des boutons google, ils sont simples, légers et modernes à la fois. J’ai donc décidé de reproduire moi-même le design des boutons google avec du CSS.

## Demo

<style>
  .button {
    display: inline-block;
    background-image: -moz-linear-gradient(top, #f5f5f5, #f1f1f1);
    -moz-border-radius: 2px;
    -moz-user-select: none;
    background-color: #f2f2f2;
    color: #757575;
    width: 152px;
    font-family: arial, sans-serif;
    font-size: 13px;
    border: 1px solid #f2f2f2;
    border-radius: 2px;
    cursor: default;
    font-weight: 700;
    text-align: center;
    line-height: 27px;
    min-width: 54px;
    padding: 0 16px;
    text-decoration: none;
  }
  .button:hover {
    background-color: #f8f8f8;
    background-image: linear-gradient(top, #f8f8f8, #f1f1f1);
    border: 1px solid #c6c6c6;
    color: #333;
    box-shadow: 0 1px 1px rgba(0, 0, 0, 0.1);
  }
  .button.default:active {
    box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
    color: #000;
  }
</style>

<a href="#" class="google button">Recherche Google</a>

## Code-source du bouton Google

HTML

<pre><code class="xml">&lt;a href="#&quot; class=&quot;google button&quot;&gt;Recherche Google&lt;/a&gt;</code></pre>

CSS (775 octets non compressés)

<pre><code class="css">.button {
    display: inline-block;
    background-image: -moz-linear-gradient(top, #f5f5f5, #f1f1f1);
    -moz-border-radius: 2px;
    -moz-user-select: none;
    background-color: #f2f2f2;
    color: #757575;
    width: 152px;
    font-family: arial, sans-serif;
    font-size: 13px;
    border: 1px solid #f2f2f2;
    border-radius: 2px;
    cursor: default;
    font-weight: 700;
    text-align: center;
    line-height: 27px;
    min-width: 54px;
    padding: 0 16px;
    text-decoration: none
}
.button:hover {
    background-color: #f8f8f8;
    background-image: linear-gradient(top, #f8f8f8, #f1f1f1);
    border: 1px solid #c6c6c6;
    color: #333;
    box-shadow: 0 1px 1px rgba(0, 0, 0, .1)
}
.button.default:active {
    box-shadow: inset 0 1px 2px rgba(0, 0, 0, .1);
    color: #000
}
</code></pre>

Et c’est tout !
