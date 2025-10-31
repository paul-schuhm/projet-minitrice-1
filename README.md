# Git - Évaluation : - Projet *Minitrice* versionné avec Git

<hr>

Module Git (14h)

Date de dernière modification : 31/25

ESGI1

Auteur(s): Paul Schuhmacher, Fabien Rozar

Version: 2

<hr>

Ce projet consiste à créer un programme capable de réaliser les 4 opérations arithmétiques élémentaires (`+`, `-`, `*` et `/`) entre deux nombres positifs. L'historique de développement du projet sera suivi avec git.

## Objectifs

Ce projet sert de support pour l'évaluation du module Git et doit être réalisé **seul/e ou à deux**.

Ce projet a pour but d'évaluer votre capacité à utiliser git et à manipuler des branches git [en suivant un git worfklow précis](#branching-model-à-utiliser). Dans le cas où le travail est réalisé à deux, on attend que chaque membre du groupe contribue de manière *égale* au dépôt. Aussi, le nombre de commits par personne devrait être *sensiblement* le même.

## Comment rendre votre travail

> Merci de **lire attentivement** les consignes !

**Publier** votre travail **sur un dépôt git sur Github** et communiquer **l'URL du dépôt par email**. 

Le dépôt git contiendra les sources et un fichier `README` donnant les instructions pour installer et lancer le projet.

**Pour chaque groupe**, envoyer **un seul e-mail** à l’adresse suivante : <a href="mailto:pschuhmacher@myges.fr?subject=git-evaluation_groupe-<numéro>">pschuhmacher@myges.fr</a>, **ayant le sujet suivant** : 

`git-evaluation_groupe-<numéro>` 

où **`<numéro>`** est votre numéro de groupe. Par exemple, si j'appartiens au groupe `2`, j'enverrai donc un e-mail avec le sujet `git-evaluation_groupe-2`.

> Répartissez vous des numéros de groupe unique au besoin.

Dans l'e-mail, indiquer :

- **La composition du groupe** (Nom et prénom de chaque membre du groupe);
- **L'URL de votre dépôt Github** qui héberge votre projet.

Vous devez rendre votre travail **avant la date butoir fixée ensemble sous peine de pénalité** : 1 point le premier jour de retard, 2 points le deuxième jour de retard, et ainsi de suite jusqu'à un minimum de 0.

Merci de vérifier que le dépôt est **public** !

> Vous êtes encouragé·e à **mettre votre collègue en copie du mail** de rendu.


## Bien démarrer

Ce dépôt contient :

- Le sujet au format Markdown;
- Un dossier `test` comprenant des données pour tester votre programme;
- Un fichier `good-expression.txt` comprenant des expressions à évaluer.

> Conseil : Cloner [ce dépôt](https://github.com/paul-schuhm/projet-minitrice-1) pour vous en servir comme point de départ. Une fois cloné vous pouvez supprimer le dossier `.git` et refaire un `git init` pour réinitialiser le dépôt.

## À rendre

**L'URL de votre dépôt git public**. 

- Le nom du dépôt doit être de la forme `git-evaluation_groupe-<numéro>` où **`<numéro>`** est votre numéro de groupe (assigné en classe). Par exemple, le groupe `2` doit créer un unique dépôt nommé `git-evaluation_groupe-2`.

Votre dépôt doit contenir *a minima* :

- Un fichier `README.md` avec les sections suivantes :
  - **Table des matières** (vous pouvez la générer automatiquement), pour naviguer facilement dans le document;
  - **Installation** : instructions pour installer et lancer votre programme. Si des logiciels tiers (ex: compilateur) doivent être installés, les procédures d'installation doivent être décrites ici. Il en va de même pour les bibliothèques;
  - **Exécution** : un exemple d'utilisation de votre programme, avec la sortie attendue, comme ce qui fait dans ce document;
  - **Remarques** : si vous voulez faire des remarques sur votre travail, difficultés rencontrées;
  - **Publication (optionnel)** : Le lien Youtube de votre vidéo Gource associée à l'activité de votre dépôt;
  - **Références/Liens utiles** : la liste des références (sites web, cours, livre, article, billet de blog, etc.)qui vous a été utile pour réaliser ce projet.
- Les exécutables `minitrice` et `generator` à la racine du dépôt. Dans le cas où ces programmes sont générés, à la fin de leur génération, ces programmes doivent être présents à la racine de votre dépôt.
- Un dossier `results` à la racine de votre dépôt. Vous y stockerez les résultats de votre programme `minitrice` sur les fichiers contenu dans le dossier `test`. Les noms de fichiers contenant les résultats correspondront au nom de fichier d'origine suffixé par `-result`, par exemple `00-addition-result.txt`.

Exemple de structure de dépôt attendue :

~~~bash
exemple-depot/
├── generator
├── minitrice
├── README.md
├── results
│   └── 00-addition-result.txt
└── test
    └── 00-addition.txt
~~~

> Pensez à bien **publier vos branches locales sur le dépôt** !

## Notation

Le projet est ramené sur une note sur **20**. Voici le barème détaillé :

- Présence d'un `README.md` **bien formé** ([Markdown correct](https://www.markdownguide.org/basic-syntax/), lisible, sans (trop de)fautes ou coquilles), **conforme à la consigne**  (sections demandées): **2 points**;
- **Respect des noms de programmes et fichiers** pour les travaux réalisés : **2 points**;
- **Exécution correcte** de votre programme sur les fichiers du répertoire `test` :  **2 points**;
- Présence du répertoire `results` contenant les différents fichiers de résultats avec le contenu attendu : **1 point**;
- Exécution correcte de votre programme sur les scénarios dans ce document : **2 points**;
- La création du programme `generator` et son exécution correcte : **1 point**;
- Le suivi du projet respecte [le workflow *GitFlow* vu en cours](#branching-model-à-utiliser) : **2 points**;
- Chaque message commit doit être concis (< 70 caractères) et **décrire correctement le travail réalisé par le commit**. Si la description doit être plus longue, le corps du message de commit est utilisé : **4 points**;
- L'historique de commits est nettoyé au besoin (avec `git rebase` interactif), les commits sont *atomiques* : **2 points**
- Pour chaque progression sur votre projet (*merge* d'une branche `feature` dans `main`), le projet est dans un état  **fonctionnel** (même s'il est incomplet) : **2 points**;
- **Bonus :** Publication de la vidéo générée par la commande [gource](https://gource.io/) correspondante à votre activité sur ce dépôt : **2 points**.

## Spécifications du projet

Le programme sera utilisable à travers un terminal. Vous utiliserez *votre langage de programmation favori*.

Le programme prend en entrée une chaîne de caractère qui contient 2 nombres positifs (entier ou rationnel) séparés par un caractère représentant l'une des opérations suivantes : `+`, `-`, `*` ou `/`. Après la validation d'une ligne, en appuyant sur la touche `Entrée`, votre programme affiche le résultat du calcul indiqué par la chaîne de caractère.

L'exécutable représentant le programme sera désigné par `minitrice` dans la suite de ce document. Il doit être utilisable de façon interactive ou en lisant l'entrée standard `STDIN`.

### Spécification 1 - Utilisation interactive

Un exemple d'utilisation :

~~~bash

1. $ ./minitrice
2. > 3+9
3. 12
4. > 
5. Fin des calculs
6. $ echo $?
7. 0
8. $ 
~~~

> Notez l'utilisation d'un `$` en début de ligne pour indiquer l'utilisation du prompt du terminal.  

- À la ligne `1`, le programme `minitrice` est appelé. Noterez l'utilisation d'un `$` en début de ligne pour indiquer l'utilisation du prompt du terminal.  
- À la ligne `2`, le calcul `3+9` est demande au programme. Noterez l'utilisation d'un `>` en début de ligne pour indiquer l'utilisation du prompt du programme `minitrice`.  
- À la ligne `3`, le programme affiche le résultat du calcul.  
- À la ligne `4`, on sort du programme `minitrice` grâce à la combinaison de touche `Ctrl + D` qui envoie [le signal `End-Of-File`](https://fr.wikipedia.org/wiki/End-of-file) au programme.  
- À la ligne `5`, le programme afficher un message de sorti `Fin des calculs`.  
- À la ligne `6`, de retour dans le terminal Unix, on demande le code de sortie (`$?`) suite à l'exécution du program `minitrice`.  
- À la ligne `7`, on voit le code de sortie `0`.  
- À la ligne `8`, on est de retour dans le terminal.  

Ce scénario décrit un exemple d'utilisation du programme à réaliser. 

> Vous noterez que malgré le fait qu'un signal soit utilisé pour sortir du programme, le code de sortie retourné est bien `0`, ce qui indique que le programme s'est exécuté normalement.

**Remarque :** Toutes les écritures du programme `minitrice` se font sur la sortie standard `STDOUT`.

### Spécification 2 - STDIN : utilisation de `echo`

Dans le but d'automatiser l'utilisation du programme `minitrice`, il doit pouvoir lire sur l'entrée standard `STDIN`. Dans [la tradition d'Unix](https://fr.wikipedia.org/wiki/Philosophie_d%27Unix), tout programme devrait présenter une interface *texte*, l'interface *universelle*. Cette interface permet au programme de recevoir des données en entrée depuis la sortie d'un autre programme sous forme de chaîne de caractères. Ainsi, le programme peut être *composé* avec d'autres programmes pour en fabriquer de nouveaux. Pour composer deux programmes, il faut utiliser [un pipe (ou tube)](https://en.wikipedia.org/wiki/Pipeline_(Unix)), représenté par le caractère `|`. Par exemple :

```bash
programme1 | programme2 | programme3
```

`programme3` lit son entrée depuis la sortie de `programme2`, et `programme2` lit son entrée depuis la sortie de `programme1`. On peut dire que `programme1 | programme2 | programme3` est un *nouveau* programme, *composé* à partir de 3 autres programmes. On pourrait écrire `alias programme4 = 'programme1 | programme2 | programme3'`.

Il y a généralement 2 utilitaires (programmes) pour envoyer des données à travers un pipe : `echo` et `cat`.

Un exemple d'utilisation :

```bash

1. $ echo "3+12" | ./minitrice
2. 15
3. $ echo $?
4. 0
5. $ 
```

- À la ligne `1`, on envoie la chaîne de caractère `"3+12"` dans le programme `minitrice` à l'aide d'un pipe;
- À la ligne `2`, le programme `minitrice` écrit son résultat;
- À la ligne `3`, de retour dans le terminal Unix, on demande le code de sortie suite à l'exécution du program `minitrice`;
- À la ligne `4`, on voit le code de sortie `0`;
- À la ligne `5`, on est de retour dans le terminal.  

Ce scénario décrit un exemple d'utilisation du programme à réaliser. On peut noter qu'il est plus court que le scénario interactif et qu'il n'y a pas de message à la sortie du programme.

### Spécification 3 - STDIN : utilisation de `cat`

Dans ce dépôt, vous trouverez le fichier `good-expression.txt` qui contient 10 expressions calculables avec les 4 opérations à gérer. En utilisant ce fichier :

<br>

~~~bash

 1. $ cat good-expression.txt | ./minitrice
 2. 4
 3. 11
 4. 35
 5. -4
 6. 12
 7. 90
 8. 4.0
1.  8.0
2.  10
3.  4
4.  $ echo $?
5.  0
6.  $ 

~~~

- À la ligne `1`, on envoie le contenu du fichier `good-expression.txt` dans le programme  `minitrice` à l'aide d'un pipe.
De la ligne `2` à `12`, le programme `minitrice` écrit le résultat des calculs sur la sortie standard `STDOUT`.  
- À la ligne `13`, de retour dans le terminal Unix, on demande le code de sortie suite à l'exécution du program `minitrice`.  
- À la ligne `14`, on voit le code de sortie `0`.  
- À la ligne `15`, on est de retour dans le terminal.  

Ce scénario décrit un exemple d'utilisation du programme à réaliser. On peut noter qu'avec la capacité de lecture sur le pipe, il possible au programme `minitrice` de traiter un grand nombre de données.

### Spécification 4 - Gestion d'erreurs

La gestion d'erreurs fait partie intégrante du travail du développeur·se. Si les cas limites ne sont pas traités, le programme est généralement inutilisable. La gestion des erreurs est identique que le programme `minitrice` soit utilisé en mode interactif ou en mode lecture depuis `STDIN`.

#### Erreur de syntaxe

Si la ligne de calcul comporte une erreur de syntaxe, voici le comportement du programme `minitrice` :

```bash

1. $ echo "3+*12" | ./minitrice
2. Erreur de syntaxe pour le calcul: "3+*12"
3. $ echo $?
4. 1
5. $ 
```

- À la ligne `1`, on envoie la chaîne de caractère "3+*12" dans le programme `minitrice` à l'aide d'un pipe.
- À la ligne `2`, le programme main écrit son message d'erreur en rappelant le calcul concerné.  
- À la ligne `3`, de retour dans le terminal Unix, on demande le code de sortie suite à l'exécution du program `minitrice`.  
- À la ligne `4`, on voit le code de sortie `1`.  
- À la ligne `5`, on est de retour dans le terminal.  

On peut noter que le message d'erreur rappelle la ligne de calcul qui a provoqué l'erreur. On peut aussi voir que le code de sortie est *différent* de `0`, ce qui indique que le programme ne s'est pas exécuté correctement.

#### Division par zéro

La division par zéro est un grand classique des erreurs à traiter dans le cadre de calcul. Voici le comportement du programme `minitrice` dans ce cas de figure :

```bash

1. $ echo "3/0" | ./minitrice
2. Division par zéro
3. $ echo $?
4. 1
5. $ 
```

- À la ligne `1`, on envoie la chaîne de caractère "3/0" dans le programme `minitrice` à l'aide d'un pipe.
- À la ligne `2`, le programme main écrit son message d'erreur.  
- À la ligne `3`, de retour dans le terminal Unix, on demande le code de sortie suite à l'exécution du program `minitrice`.  
- À la ligne `4`, on voit le code de sortie `1`.  
- À la ligne `5`, on est de retour dans le terminal.  

On peut noter que le message d'erreur ne donne pas d'information sur le calcul qui a provoqué ce message (ce qui est moins pratique pour débugguer). On peut aussi voir que le code de sortie est *différent* de 0, ce qui indique que le programme ne s'est pas exécuté correctement.

### Spécification 5 : Générateur d'expressions

Le programme `minitrice` ayant la capacité de lire des entrées depuis un pipe, `|`, il est maintenant possible de le relier à la sortie d'un autre programme : `generator`.

Le programme `generator` génère des expressions calculables de façon aléatoire. Deux nombres choisis aléatoirement dans l'intervale `[1, 1000]` sont utilisés pour générer les expressions. Le choix de l'opération à réaliser entre ces deux nombres est aussi aléatoire. Ce programme prend un entier comme premier argument qui désigne le nombre d'expression à générer. Exemple d'utilisation :

```bash

1. $ ./generator 2
2. 7-9
3. 84/12
4. $
```

- À la ligne `1`, le programme `generator` est appelé avec l'argument `2`. 
- À la ligne `2`, on voit que l'expression `7-9` a été générée.  
- À la ligne `3`, on voit que l'expression `84/12` a été générée.  
- À la ligne `4`, on est de retour dans le terminal.  

Le programme `generator` peut *être composé* avec le programme `minitrice` à l'aide d'un pipe (en imaginant que les mêmes expressions que précédemment soit générées) :

```bash

1. $ ./generator 2 | ./minitrice
2. -2
3. 7.0
4. $
```

### Spécification 6 : Formatage

- Les nombres que le programme `minitrice` doit supporter sont des nombres positifs de taille raisonnable : pas d'overflow ou d'erreur de calcul dû la taille des nombres manipulée. Donc pas de piège ici.
- Les espaces à gauche et à droite d'une ligne de calcul ne génèrent pas d'erreurs.
- Pour l'affichage du résultat de calcul, il doit être **arrondi à 2 chiffres après la virgule** lorsque sa partie décimale est grande.

### Branching model à utiliser

Pour versionner ce projet, **vous devez utiliser** le git workflow (ou *branching model*) [GitFlow](https://nvie.com/posts/a-successful-git-branching-model/) vu en cours :

- Une branche principale (`main`) représentant l'état de *référence*, fonctionnel du projet;
- Des branches de développement `feature/xyz`;
- Chaque contribution au projet se fait par un **merge** d'une branche `feature` sur `main`.

Pensez à bien conserver et pousser **toutes les branches locales (features) vers votre dépôt**. Le dépôt GitHub doit **contenir toutes les branches**.

### Visualisation avec gource (optionnel)

Pour [installer `gource`](https://gource.io/) sous GNU/Linux (Ubuntu/Debian), utiliser la commande suivante :

```bash
sudo apt install gource
```

Vous aurez aussi besoin du logiciel [`ffmpeg`](https://ffmpeg.org/) d'édition de flux vidéo pour convertir le fichier généré par `gource` :

```bash
sudo apt install ffmpeg
```

Pour apprendre à utiliser `gource`, veuillez consulter cet [article](https://dev.to/voieducode/my-gource-video-production-pipeline-5eb0). 

Voici un exemple de commande :

```bash
gource -s 2 -r 60 --file-font-size 8 --title git-evaluation --filename-time 2 --stop-at-end --hide date,usernames -o video1.ppm && \
  ffmpeg -y -r 60 -f image2pipe -vcodec ppm -i video1.ppm -vcodec libx264 -preset medium -pix_fmt yuv420p -crf 1 -threads 0 -bf 0 video2.mp4
```

Exécutez cette commande à la racine de votre dépôt. Vous devez obtenir comme résultat les fichiers `video1.ppm` et `video2.mp4`. Publier sur YouTube le fichier `video2.mp4`.

> Assurez-vous que votre dépôt et votre vidéo sont accessibles par n'importe qui (**public**) !

## Conseils

### Sur Windows

Pour les utilisateur·ices de Windows, installer [WSL2](https://learn.microsoft.com/fr-fr/windows/wsl/install) pour avoir accès à une distribution GNU/Linux de votre choix et à un shell Unix.

## Liens utiles

 - [A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model/), l'article original décrivant en détail le workflow *GitFlow*
 - [How to capture Control+D signal?](https://stackoverflow.com/questions/1516122/how-to-capture-controld-signal), discussion sur l'interception du signal `End Of File`;
 - [My Gource video production pipeline](https://dev.to/voieducode/my-gource-video-production-pipeline-5eb0), décrit un exemple d'utilisation de gource;
 - [Philosophie d'Unix](https://fr.wikipedia.org/wiki/Philosophie_d%27Unix), description de la philosophie Unix;
 - [Pipeline (Unix)](https://en.wikipedia.org/wiki/Pipeline_(Unix)), description du pipe;
 - [Pipe: How the System Call That Ties Unix Together Came About](https://thenewstack.io/pipe-how-the-system-call-that-ties-unix-together-came-about/), présente l'histoire de la création du pipe.
