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

* ** <code>less</code> permet d'afficher le contenu d'un fichier page par page dans console 

* <code>Espace</code> : affiche la suite du fichier. La toucheEspacefait défiler le fichier vers le bas d'un « écran » de console. C'est celle que j'utilise le plus souvent.

* <code>Entrée</code>: affiche la ligne suivante. Cela permet donc de faire défiler le fichier vers le bas ligne par ligne.

* <code>head</code> cette commande permet d'afficher les 10 premières lignes d'un fichier par defaut
* <code>tail</code> cette commande permet d'afficher les 10 dernières lignes d'un fichier par defaut

* **-n nbre** retourne nbre premières ou dernières ligne d'un fichier selon **head** ou **tail**

### 2 touch & mkdir: création d'un fichier et dossier

* <code>touch</code> cette commande permet de créer un fichier
* <code>mkdir</code> cette commande permet de créer un dossier
* **-p** cette option permet à la commande **mkdir** de créer de dossier intermediaires
  ex: mkdir dossier/sousdossier/lion

### 3 cp & mv: copier et deplacer un fichier ou un dossier

* <code>cd</code> cette commande permet de copier un fichier dans un dossier
* <code>mv</code> cette commande permet de deplacer un fichier dans un dossier
* **-R** avec la commande **cp** permet de copier un dossier avec son contenu dans un autre
* <code>*</code> avec la commande **cp** permet de copier avec les extensions

### 3 rm: supprimer des fichiers et dossiers

* <code>rm</code> suivi du nom du fichier ou dossier à supprimer
* **-i** pour demander la confirmation 
* **-f** pour forcer la suppression
* **-v** pour dire ce la commande est entrain  de faire
* **-r** pour supprimer un dossier ses contenus
* **NB** il faut jamais utiliser cette commande rm -rf /* pour dir supprimer avec force mon dossier racine et ses sous dossiers 

## 5 ln: créer des liens entre fichiers
Elle crée de types de liens:
* liens **Symboliques**
* liens **Physiques**

* lien **physique** <code>ln fichier fichier2</code> fichier doit avoir exister
* lien **symbolique** <code>ln -s fichier fichier</code> même remarque

## Les droits d'accèss 
**sudo** qui signifie **S**uper **U**ser **DO**
* <code>sudo su</code> cette commande, nous permet de devenir **super utilisateur** du Système
il se distingue par l'utilisateur normal **~** par **#** pour quitter <code>CTRL + D</code>

### Gestion des utilisateurs

1. ajouter un utilisateur
*   <code>adduser</code> cette commande nous permet d'ajouter un utilisateur
*   <code>passwd</code> cette commande nous permet de changer de mot de passe d'utilisateur
2. suppression d'un utilissateur
*   <code>deluser</code> cette commande nous permet de supprimer utilisateur
*   <code>addgroup</code> cette commande nous permet d'ajouter group 
*   <code>usermod</code> cette commande nous permet de modifier un user
*   **-l** ce parametre de la commande **usermod** permet de renommer un user
*   **-g** ce parametre de la commande **usermod** permet de de changer le d'un user
*   **-G** ce parametre de la commande **usermod** permet de d'ajouter un user à plusieur group
*   ex: usermod -g amis mawatta; usermod -G amis,mawatta mawatta
*   <code>delgroup</code> cette commande nous permet de supprimer un group

## Gestion des propriétaire d'un fichier
* <code>chown user fichier</code> pour changer de proprietaire d'un fichier
* <code>chgrp user fichier</code> pour changer de group proprietaire d'un fichier
* <code>chow user:group fichier</code> pour changer proprietaire et groupe du fichier
* **-R** modifier également pour les sous dossiers

## chmod: modifie les droits d'accèss 
* x->1 w->2 r->4 rwx->7
* un fichier peut avoir trois droits propriétaire groupe et les autres
* un propriétaire peut avoir le droit de lecture <code>r->4</code>, droit d'écriture <code>w->2</code> et droit d'execution <code>x->1</code> pour <code>rwx->7</code>
* un groupe peut avoir le droit de lecture <code>r->4</code>, droit d'écriture <code>w->2</code> et droit d'execution <code>x->1</code> pour <code>rwx->7</code>
* et les autres peuvent avoir le droit de lecture <code>r->4</code>, droit d'écriture <code>w->2</code> et droit d'execution <code>x->1</code> pour <code>rwx->7</code>
* si le propriétaire, le groupe et les autre ont tous les droits ça donne ça <code>700 + 70 + 7 => 777</code> ou <code>rwrrwxrwx</code>
* si le propriétaire n'a que le droit de lecture, le groupe et les autre ont tous les droits ça donne ça <code>400 + 70 + 7 => 477</code> ou <code>r--rwxrwx</code>

* si le propriétaire n'a que le droit de lecture, le groupe n'a que le droit d'ecriture et les autre ont tous les droits ça donne ça <code>400 + 20 + 7 => 427</code> ou <code>r---w-rwx</code> etc...

* ou encore propriétaire designé par u, groupe par g et les autre o
* ajouter le droit d'ecriture au propriétaire par <code>chmod u+w fichier</code>
* retirer le droit d'execution aux autres par <code>chmod o-x fichier</code>
* ajouter le droit de lecture au group par <code>chmod g+r fichier</code>

* + signifie ajouter un droit
* - signifie retirer un droit
* Exemple chmod u+w, g+r, o-x rapport.txt
* Exemple chmod ugo+x rapport.txt c'est à dire ajouter le droit d'execution au propriétaire, groupe et les autres au fichier rapport.txt
* Exemple chmod u=rwx,g=r,o=- rapport.txt: ajouter les droits au propriétaire, seulement de lecture au groupe et retirer tous les droits autres au fichier rapport.txt
* **-R** le paramètre pour affectation recursive