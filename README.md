# Cours Sur Linux

## Chapitre I
Ici nous allons decouvrir quelques consernants les differents console de linux
* <code> CTRL + ALT + F1</code>: terminal 1 (tty1);
* <code> CTRL + ALT + F2</code>: terminal 2 (tty2);
* <code> CTRL + ALT + F3</code>: terminal 3 (tty3);
* <code> CTRL + ALT + F4</code>: terminal 4 (tty4);
* <code> CTRL + ALT + F5</code>: terminal 5 (tty5);
* <code> CTRL + ALT + F6</code>: terminal 6 (tty6);
* <code> CTRL + ALT + F7</code>: retour au mode graphique
* <code> ALT + Impr.Ecran + K</code> pour faire retour en arrière

## Chapitre II
Ici, nous allons quelques commandes couramment utilisée sur linux
* <code>date</code> qui affiche la date du système
* <code>ls</code> qui liste tous les **fichiers** et **dossier** du dossier courant

## Options(paramètres)
* Les options(paramètres) nous permettent de rafiner nos recherche et ils sont placés après les commandes précedé par un tiret
**NB**: Attention à la case des paramètres
* Les paramètres longs sont précédés de deux tirets <code>commande --parametre</code> 
* On peut aussi combiner les paramètre <code>commande -daUh --parametre2 --parametre2</code>
  exemples <code>ls -l</code>

## Certains paramètres courts necessitent qu'on les associe une valeur

1. Pour les paramètres courts, on a : <code>commande -p 13</code>
2. Pour les paramètres longs, on a : <code>commande --parametre=13</code>

## Autocomplétion de commande
En linux, il existe tellement de commande, il arrive qu'on oublie certaines d'entre elles, donc il suffit taper le debut de la
commande et puis la touche <code>TAB</code> deux fois successivement automatiquement on aura la liste des commandes commençants par notre requêt

## La commande ls
Pour **l**i**s**t

* <code>pwd</code> nous affiche le dans lequel est 
* <code>which</code> pour connaitre l'emplacement d'une commande
* <code>ls --color=none</code> pour desactiver la coloration syntaxique par defaut
* <code>ls --color=auto</code> pour activer la coloration syntaxique par defaut
* **-a** le paramètre qui affiche les dossiers et fichiers cachés
* **-A** le paramètre qui permet de ne pas afficher les dossiers et fichiers cachés
* **-F** le paramètre qui permet d'afficher le type des éléments
* **-l** pour lister en détaile le contenu d'un dossier
* **-h** pour afficher leur taille en kilo octect
* **-t** trier par date de dernière modification
* **-tr** pour renverser le résultat de la commande précédente
* **-larth** pour combiner plusieurs de ces paramètres

## La commande cd
Pour **C**hange **D**irectory

* <code>cd</code> permet de se deplacer entre les dossiers de son système
* En fait pour ce deplacer entre les dossiers, on doit comprendre deux concepts clés
1. les **chemins relatifs** c'est à dire allez-y dans sous dossier en foction de notre emplacement courant
   exemple /home/damaro/Image à l'instant présent je me retrouve dans <code>/home/damaro</code> => <code>cd Image</code> ou
   <code>cd ./Image</code>, en réalité le point signifie le dossier courant
2. les **chemins absolus** c'est à dire doit obligatoirement commence par / qui veut dire d'aller à la racine qu'au dossier
   courant c'est ce genre de chemin qui marche pour n'importe quel dossier où on se 
   on peut aussi utiliser le tirde **~** pour aller dans /home/user

## La commande pwd
pour **P**rint **W**orking **D**irectory 

* <code>pwd</code> permet d'afficher le dossier dans lequel on se retrouve 

## La commande du
pour **D**isk **U**sage

* <code>du</code> cette commande affiche la taille occupée par un dossier 
* **-h** ce paramètre permet d'afficher la taille **Human Readable** qui peut être en Octect, kilo Octect, Mega Octect...
* *-a** ce paramètre permet d'afficher la taille des dossiers et fichier


## Manipuler les fichiers en Linux
Dans cette partie du tuto, nous allons voir comment:
1. afficher le contenu d'un fichier
2. deplacer un fichier
3. copier un ficier
4. supprimer un fichier

### 1 cat & less: afficher le contenu d'un fichier 
* <code>cat</code> la commande **cat** permet d'afficher tout le contenu d'un fichier d'un coups
* **-n** ce paramètre nous permet afficher les numéros de ligne du fichier
**NB** cette commande n'est pas adaptée aux minipulations des gros fichiers
** <code>less</code> permet d'afficher le contenu d'un fichier page par page dans console 