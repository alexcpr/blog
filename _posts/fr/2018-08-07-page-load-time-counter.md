---
layout: post_js_fr
title: Compteur de temps de chargement d'une page en JS
lang: fr_FR
---

 Ce que j’aimerais voir sur les sites web est un petit compteur du temps de chargement de la page placé dans le footer de la page, alors j’ai décidé de vous partager le petit morceau de code afin d’intégrer facilement ce compteur dans le footer sur votre site web.

Version ES5 (Navigateurs anciens)
<pre><code class="javascript">(function () {
    var time = window.performance &#x26;&#x26; performance.timing;
    if (time) {
        var load = (time.loadEventEnd - time.navigationStart) / 1e3;
        alert(&#x22;Cette page a &#xE9;t&#xE9; charg&#xE9;e en &#x22; + load + &#x22; secondes&#x22;);
    }
})();</code></pre>

ES6 Version (Navigateurs modernes)
<pre><code class="javascript">(() =&#x3E; {
    const time = window.performance &#x26;&#x26; performance.timing;
    if (time) {
        const load = (time.loadEventEnd - time.navigationStart) / 1e3;
        alert(&#x60;Cette page a &#xE9;t&#xE9; charg&#xE9;e en ${load} secondes&#x60;)
    }
})();</code></pre>