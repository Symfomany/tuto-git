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


Tuto Github
https://www.grafikart.fr/tutoriels/divers/git-github-131

Git Workflow Grakifart
https://www.grafikart.fr/tutoriels/divers/git-workflow-478

Ouverture sur Github Project
https://github.com/Symfomany/tuto-git/projects/2

Bonnes pratiques
https://guillaumebriday.fr/comment-jutilise-git-mes-astuces-et-bonnes-pratiques


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


Démo de branche:

Modifier du HTML puis
```
    git push origin html
```
Aller sur Github pour voir la modif et préparer la PR

---------------------
Créer une branche: 

```
    git branch html
    git checkout html
    tricks: git checkout -b html: créer et swicth
```

Voir les modifications entre 2 branches:

```
    git diff master..css
```

Pusher sur la branche css et merge sur master

```
    git merge css
```

*Attention: La master étant la brabche la plus haute et la plus en avance, 
il faut que toutes les autres branches AVANT TOUS CHANGEMENT puisse se mettre à jour par rapport à la master.*


Article interessante pour demystifié git add, commit :
https://git-scm.com/book/fr/v2/Utilitaires-Git-Reset-d%C3%A9mystifi%C3%A9

HEAD --- Index --- Working Files

Modification: git add dessus pour le monter dans notre index.



Revenir en arriere sur un commit:

```
    git reset 9183c5024d3853f14efadf907f2d3aa46dcb3694 --hard
    git push --force origin master : (ne pas oublier le force car on force sur une branche plus avancée a revenir en arriere)
```

ou juste un fichier

```
    git checkout -- unfichier
```

Le plus important, cela va permettre de vous identifier en tant qu’auteur du commit :

```
    $ git config --global user.name "John Doe"
    $ git config --global user.email johndoe@example.com
```


Ajouter une clé ssh

Selon les recommandations de Github et Gitlab, il est préférable d’utiliser le port https, et cela peut être utilisé avec ssh : https://help.github.com/articles/which-remote-url-should-i-use/.


Add Git Lens for Vscode
http://gitlens.amod.io/
