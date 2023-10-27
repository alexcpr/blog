---
layout: post_js_en
title: Page load time counter in JS
lang: en_US
image: /assets/meta/en/page-load-time-counter.png
---

What I would like to see on websites is a little counter of the page load time placed in the footer, so I decided to share you the little piece of code in order to easily integrate this counter in your website footer.

ES5 Version (Older browsers)
<pre><code class="javascript">(function () {
    var time = window.performance &#x26;&#x26; performance.timing;
    if (time) {
        var load = (time.loadEventEnd - time.navigationStart) / 1e3;
        alert(&#x22;This page loaded in &#x22; + load + &#x22; seconds&#x22;);
    }
})();</code></pre>

ES6 Version (Modern browsers)
<pre><code class="javascript">(() =&#x3E; {
    const time = window.performance &#x26;&#x26; performance.timing;
    if (time) {
        const load = (time.loadEventEnd - time.navigationStart) / 1e3;
        alert(&#x60;This page loaded in ${load} seconds&#x60;)
    }
})();</code></pre>