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
