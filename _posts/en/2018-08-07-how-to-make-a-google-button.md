---
layout: post_js_en
title: How to make a Google button with CSS
lang: en_US
image: /assets/meta/en/how-to-make-a-google-button.png
---

I personally like the Google buttons design; they are simple, lightweight, and modern at the same time. So, I decided to reproduce the Google buttons' design myself with some CSS.

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
        font-family: Arial, sans-serif;
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

<a href="#" class="google button">Google Search</a>

## Google Button Source Code

HTML
<pre><code class="xml">&#x3C;a href=&#x22;#&#x22; class=&#x22;google button&#x22;&#x3E;Google Search&#x3C;/a&#x3E;</code></pre>

CSS (775 bytes uncompressed)
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
}</code></pre>

And that’s it!
