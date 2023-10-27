---
layout: post_fr
title: Réparer le clic droit sur les icônes de la barre des tâches
lang: fr_FR
toc: true
---

Quand j’utilise Windows 10, je suis parfois confronté au problème que je ne peux pas faire un clic droit sur mes icônes de la barre des tâches, mais j’ai trouvé quelques solutions pour résoudre cela.

_NB: Cela fonctionne également sur Windows 7 et 8._

## Solution 1 : Utilisation de Maj + clic droit

Tout ce que vous avez à faire est de maintenir la touche **Maj** tout en faisant un clic droit sur n’importe quelle icône de votre barre des tâches et après cela, vous pourrez faire un clic droit normalement sur les icônes de votre barre des tâches. Mais gardez à l’esprit que même si cette méthode fonctionne, elle devrait être considérée comme une solution de contournement plutôt qu’un correctif.

## Solution 2 : Redémarrer l’Explorateur Windows

1. Appuyez sur **Ctrl + Maj + Esc** pour ouvrir le **Gestionnaire de tâches**.
2. Dans le **Gestionnaire de tâches**, localisez le processus **Windows Explorer**, **cliquez avec le bouton droit** dessus et choisissez **Redémarrer**.

![Image](/assets/images/fix-right-click-on-taskbar-icons-1.png)

Voyez maintenant si le correctif a été efficace en cliquant avec le bouton droit de la souris sur un icône dans la barre des tâches.

## Solution 3 : Redémarrage du service Serveur de modèle de données

1\. Appuyez sur la touche **Windows + R** pour ouvrir la fenêtre exécuter. Ensuite, tapez “**services.msc**” et appuyez sur **Entrée** pour ouvrir la fenêtre Services.

![Image](/assets/images/fix-right-click-on-taskbar-icons-2.png)

2\. Dans la fenêtre **Services**, faites défiler la liste **Services locaux** et localisez **Serveur de modèle de données**.

3\. Cliquez avec le bouton droit de la souris sur **Serveur de modèle de données** et choisissez **Redémarrer**, puis attendez que le service soit redémarré.

![Image](/assets/images/fix-right-click-on-taskbar-icons-3.png)

4\. Cliquez avec le bouton droit de la souris sur n’importe quoi dans votre barre des tâches pour voir si la solution a été efficace.
