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


Add git in existing project:

```
    $ git remote add origin git@host:user/project_name.git
```

Supprimer un fichier suivi par git:

```
    $ git rm --cached /path/to/file # Pour un fichier
    $ git rm --cached -r /path/to/folder # Pour un dossier
```

Git permet de faire des branches, je pense qu’il faut en user et en abuser. Pour la simple raison que des gens vont probablement relire votre code derrière avec le système de Pull Request et même si une fonctionnalité n’est pas terminée, il pourra relire votre code en amont et vous faire des retours plus facilement.

De plus, vous aurez un historique bien plus clair des fonctionnalité qui ont été développées. Cela va permettre de bien séparer les développements même si vous travaillez seul, par exemple si vous avez besoin de rapidement corriger un bug, vous pourrez mettre en “pause” le développement en cours et corriger le bug de manière transparente pour votre avancement en cours.


```
 git branch --merged: Mergée
 git branch --no-merged: No Mergées
 ```

Version courte des status
```
    git status -u
```

```
    git add *.txt  # Tous les fichiers txt du dossier courant
    git add "*.txt" # Tous les fichiers txt du projet entier
```

Supprime un fichier du staging
```
    git reset folder/file # Enlève le fichier file du staging
```

Git reset hard est tres dangeureux..


Utiliser Git revert plutot que git reset hard:
Il faut bien faire la différence avec git reset. Git reset peut, entre autre, supprimer complètement un commit et donc modifier l’historique de git.

Le revert est plus souple et permet de garder un historique des modifications, il va tout simplement supprimer les modifications d’un commit mais dans un nouveau commit.

Si un fichier:
```
 git checkout file/to/path
 ```
Sinon:
```
 $ git checkout SHA-1 # Déplacer le HEAD sur le commit qui correspond au SHA-1
$ git checkout HEAD^ # Revient au commit précédent
$ git checkout HEAD~4 # Revient 4 commmits en arrière
```


Voir les logs sus form de graph
```
 git log --graph --oneline --decorate
```

Les logs sur une date:
```
    $ git log --after="2014-7-1"
    $ git log --before="2014-7-1"
    $ git log --after="2014-7-1" --before="2015-7-1"
```

Ou

```
    $ git log --after="yesterday"
    $ git log --before="1 week ago"
```


Par message:

```
    git log --grep="controller"
```

Visualisation

http://beta.gitflowchart.com/chart/github/Symfomany/tuto-git


Git kraken Visulisation 