---
layout: post_js_en
title: Create gists from Command Line
lang: en_US
image: /assets/meta/en/create-gist-from-cli.png
---

## Installation

1\. Install <code>pretty-diff</code> npm package
<pre><code class="bash">npm install -g pretty-diff</code></pre>


2\. Add your github username into git global configuration
<pre><code class="bash">git config --global github.user "YourGitHubUsernameHere"</code></pre>


3\. Create a [Personal Access Token](https://github.com/settings/tokens) (don’t forget to check the “Create gist” checkbox) in order to <code>pretty-diff</code> to work. Once you have created the token, run this command
<pre><code class="bash">git config --global gist-diff.token "YourPersonalAccessTokenHere"</code></pre>

Now you’re ready to use <code>gist-diff</code>!

## Creating a Gist

Now you can just run <code>gist-diff</code> command in order to create a gist with the content of <code>git diff</code>

<pre><code class="bash">gist-diff</code></pre>

When <code>gist-diff</code> has created the gist it will open the gist URL in your browser.