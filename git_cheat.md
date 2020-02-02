# Github Cheat Sheet
---
## Se connecter à Github avec SSH
---
## Créer un repo local
---
1. Dans le terminal, changer le CWD pour le root du repo local
2. > git init

## Ajouter un fichier au repo
---
Afin de keep track des changements et d'inclure un fichier aux commits, il faut l'ajouter au repo à l'aide de
> git add fichier.xyz

## Vérifier l'état du repo et de ses fichiers
---
Utile pour s'assurer d'avoir bien ajouter un fichier au repo
> git status

## Commits !
---
Un commit sert à enregistrer les différences entre l'état actuel du repo et son état lors du dernier commit.
Ils permettent de garder différentes versions du repo accessibles. Il est donc possible de revenir à un commit antérieur.

### Ajouter un fichier pour le prochain commit
C'est ce qu'on appelle staging environment. On doit indiquer quels fichiers doivent être inclus dans le prochain commit. La commande est la même que pour ajouter un fichier au repo :
> git add fichier.xyz

Si on est paresseux, il est possible d'utiliser :
> git add *

### Faire le commit
Enfin quand les changements ont été apportés et sauvegardés, puis ajoutés au prochain commit, on peut procéder à ce dernier. Le commit devrait toujours être accompagné par un message décrivant la nature du commit. Le message peut être inclus directement dans la commande :
> git commit -m "message"

Si on omet -m et son argument, on sera prompté à écrire un message dans vim (?).

## Branches !
---
La branches principales, nommée Master, contient le projet dans son état idéalement le plus stable. Afin de développer le projet sans crainte de créer des boulversements indésirables au Master, il est possible de travailler sur une branches différentes du projet.

### Créer et se déplacer sur une nouvelle branche
> git checkout -b <branch>

### Vérifier sa position dans l'arborescence du projet
> git branch

## Github
---
Tout ce qui est expliqué plus haut se passe localement. Cependant si on veut travailler avec plusieurs autres collaborateurs, il est impératif d'utiliser un service comme celui de Github. Le repo, en plus d'exister localement existe aussi sur Github.

### Créer un repo Github
Se connecter au site web de Github et créer un nouveau repo à partir du site.

### Ajouter un commit actuel au repo Github
Un ou plusieurs commits ayant déjà été fait localement, il est temps de les envoyer en ligne. Pour se faire on utilisera la commande :
> git push origin branch_name
