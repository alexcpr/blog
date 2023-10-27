---
layout: post_js_fr
title: Créer des gists en ligne de commande
lang: fr_FR
---

## Installation

1\. Installer le paquet npm <code>pretty-diff</code>
<pre><code class="bash">npm install -g pretty-diff</code></pre>


2\. Ajoutez votre nom d’utilisateur github dans la configuration globale de git 
<pre><code class="bash">git config --global github.user "VotreNomDutilisateurGitHubIci"</code></pre>


3\. Créez un [jeton d'accès personnel](https://github.com/settings/tokens) (n’oubliez pas de cocher la case “Créer un gist”) afin de faire fonctionner <code>pretty-diff</code>. Une fois que vous avez créé le jeton, exécutez cette commande
<pre><code class="bash">git config --global gist-diff.token "VotreTokenPersonnelIci"</code></pre>

Vous êtes maintenant prêt à utiliser <code>gist-diff</code>!

## Créer un Gist

Maintenant vous pouvez simplement exécuter la commande <code>gist-diff</code> afin de créer un gist avec le contenu de <code>git diff</code>

<pre><code class="bash">gist-diff</code></pre>

Lorsque <code>gist-diff</code> a créé le gist, il ouvrira l’URL du gist dans votre navigateur 