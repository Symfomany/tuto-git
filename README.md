# Git Utilisation

## Démonstration avec VSCode

Doc: https://git-scm.com/book/fr/v1/D%C3%A9marrage-rapide-Param%C3%A9trage-%C3%A0-la-premi%C3%A8re-utilisation-de-Git

Ressources:
https://github.com/dictcp/awesome-git


Git in 15 minutes
https://try.github.io/levels/1/challenges/2

Free Books Git
https://www.git-tower.com/learn/

Git CheatSheet
https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf


Bonne référence en français:
http://alx.github.io/gitbook/3_comparer_les_commits_-_git_diff.html

------------------------------------------------------------------------------------------------------

+ Initialisation avec git init
+ Git add for tricked
+ Git status for changements detected
+ Github sync avec remote
+ Historique avec git log (tricks: git log ./css)
Tricks de git log:
```
    git log --pretty=oneline
    git log --stat: avec les stats de diff (git diff combined)
    git log --stat --topo-order --graph: ça c'est cool
```
+ git diff avec HEAD pour la différences avec le dernier commit (en entete) ou entre 2 branches: git diff master..test


Pour aller plus loin:

+ Github Desktop: opérations de lecture et non d'écriture pour moi


Commande utilse dans git diff:
```
    git diff HEAD -- ./lib :limite le chemin des différence
    git diff --stat : montre jusrte les différences
```

Créer une branche: 

```
    git branch html
    git checkout html
    tricks: git checkout -b html: créer et swicth
```