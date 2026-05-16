<p align="Center"><img src="../../includes/logo.png" alt="drawing" width="100"/></p>
<h3 align="Center">2Q2 - Développement Assembleur</h3>

# 🏋️‍♀️ Exercices 05 - Fichiers 🏋️‍♀️

> Représentera votre travail pratique #2 (10%)

<!--#
#### 📝 Lien vers les [notes de cours](https://slides.com/hkoncept/2q2-04/fullscreen?token=LZDfz3yW) !
-->

#### 🗄️ [Structures de projets & consignes à suivre](../../includes/rules.md)

## 📁 Question 01 - Can you handle it ?

Afin de pouvoir lire ou écrire dans un fichier, le système d'exploitation (Windows 11) doit donner la permission à l'application. Cette permission s'enregistre dans un **handle** qui représente en fait, un jeton d'accès exclusif au fichier. Cela bloque donc toutes les autres applications d'avoir accès à ce fichier tant que vous n'invalidez pas le jeton en fermant le fichier.

Votre premier défi sera de créer une procédure `openfile` pure et réutilisable qui prendra en paramètre un nom de fichier et qui retournera un **handle** sur ce fichier avec les droits en lecture et en écriture. Si le fichier n'existe pas, il sera créé automatiquement. Pour toute autre erreur lors de l'ouverture ou de la création du fichier, rertournez simplement la valeur zéro dans le handle et gérer cette valeur dans le main :

```plaintext
; Dans le main
Erreur lors de l'ouverture du fichier !
```

Pour terminer, dans le `main`, ajoutez-y un tout petit test d'assurance qualité de votre créativité afin de prouver que la procédure `openfile` fonctionne bien. Testez :

1. L'ouverture correcte d'un fichier (existant ou non).
2. L'impossibilité d'ouvrir un fichier à cause d'un erreur dans le passage de la valeur d'entrée.

Pour ouvrir un fichier en lecture & écriture en C++ :

```cpp
#include <fstream>
fstream file(filename, ios::app);
```

## 🫡 Question 02 - Say Goodbye !

Il est essentiel, pour le bon fonctionnement de toute application, qu'elle rende disponible un fichier qu'elle vient de terminer d'utiliser. Pour cela elle doit invalider son jeton (**handle**). On parle ici de fermer le fichier.

Écrivez une procédure réutilisable nommée `closefile` qui s'occupera d'effectuer cette opération. Cette procédure ne retounera rien mais affichera un message d'erreur à la console au besoin :

```plaintext
Erreur lors de la fermeture du fichier !
```

## ⚙️ Question 03 - SKU Reader

### Question 3.1

Chaque matin une entreprise reçoit de [nouveau produits](./includes/sku_20.dat) à charger en mémoire dans leur système de vente. et votre patron vous demande d'afficher les `sku` (toujours fixe de 6 caractères) à l'écran sur 5 colonnes :

```plaintext
**************************************
         Liste des produits
**************************************
938475  093847  178493  000984  285745
909374  829385  983746  984012  119863
839485  102938  092847  983948  787364
098900  101010  879384  567398  789374
**************************************
```

> Nous présumons ici que les `sku` seront toujours fixés à 6 caractères.

> ⚠️ Votre patron vous informe qu'il ne connaît pas le nombre de sku reçu par fichier de données. Votre algorithme doit donc fonctionner aussi avec ces [données](./includes/sku_25.dat).

## BONUS ⚙️ Question 04 - SKU Loader

Reprennant votre solution précédente, faites en sorte que les données soient toutes enregistrées en mémoire avant de les afficher à l'écran.

<hr><p align="Center"><img src="../../includes/end.png" alt="drawing" width="150"/></p>
