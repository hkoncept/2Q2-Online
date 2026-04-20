<p align="Center"><img src="../../includes/logo.png" alt="drawing" width="100"/></p>
<h3 align="Center">2Q2 - Développement Assembleur</h3>

# 🏋️‍♀️ Exercices 05 - Fichiers 🏋️‍♀️

<!--#
#### 📝 Lien vers les [notes de cours](https://slides.com/hkoncept/2q2-04/fullscreen?token=LZDfz3yW) !
-->

#### 🗄️ [Structures de projets & consignes à suivre](../includes/rules.md)

## 📁 Question 01 - Can you handle it ?

Afin de pouvoir lire ou écrire dans un fichier, le système d'exploitation (Windows 11) doit donner la permission à l'application. Cette permission s'enregistre dans un **handle** qui représente en fait, un jeton d'accès exclusif au fichier. Cela bloque donc toutes les autres applications d'avoir accès à ce fichier tant que vous n'invalidez pas le jeton en fermant le fichier.

Votre premier défi sera de créer une procédure `openfile` pure et réutilisable qui prendra en paramètre un nom de fichier et qui retournera un **handle** sur ce fichier avec les droits en lecture et en écriture. Si le fichier n'existe pas, il sera créé automatiquement. Pour toute autre erreur lors de l'ouverture ou de la création du fichier, un registre booléen nommé `CF` prendra la valeur `1` et un message d'erreur s'affichera à la console :

```plaintext
Erreur lors de l'ouverture du fichier !
```

Pour terminer, dans le `main`, ajoutez-y un tout petit test d'assurance qualité de votre créativité afin de prouver que la procédure `openfile` fonctionne bien. Testez :

1. L'ouverture correcte d'un fichier (existant ou non).
2. L'impossibilité d'ouvrir un fichier déjà ouvert.

> Astuce: Si la procedure `openfile` échoue vous en serez informés avec la valeur `1` du registre `CF`.

## 🫡 Question 02 - Say Goodbye !

Il est essentiel, pour le bon fonctionnement de toute application, qu'elle rende disponible un fichier qu'elle vient de terminer d'utiliser. Pour cela elle doit invalider son jeton (**handle**). On parle ici de fermer le fichier.

Écrivez une procédure réutilisable nommée `closefile` qui s'occupera d'effectuer cette opération. Cette procédure ne retounera rien mais affichera un message d'erreur à la console au besoin :

```plaintext
Erreur lors de la fermeture du fichier !
```

## ⚙️ Question 03 - SKU Loader

### Question 3.1

Chaque matin une entreprise reçoit de [nouveau produits](./includes/sku_20.dat) à charger en mémoire dans leur système de vente. et votre patron vous demande de charger les `sku` (toujours fixe de 6 caractères) en mémoire pour ensuite les afficher à l'écran sur 5 colonnes :

```plaintext
**************************************
         Liste des produits
**************************************
938475  093847  178493  000984  285745
909374  829385  983746  984012  119863
839485  102938  092847  983948  787364
098900  101010  879384  567398  789374
```

> Nous présumons ici que les `sku` seront toujours fixés à 6 caractères.

> ⚠️ Votre patron vous informe qu'il ne connaît pas le nombre de sku reçu par fichier de données.

### Question 3.2

Dans le monde de la programmation d'application, nous ne sommes jamais à l'abris des surprises. Les années ont passés et l'entreprise a prit beaucoup d'expension. Est-ce que le patron devra vous rappeler pour adapter votre code où il a survécu aux années ? Voici les [nouvelles données](./includes/sku_100.dat) journalière de l'entreprise.

## Question 04
Le propriétaire d'une entreprise nommée __ShaliExpress__ a besoin que ses employés puissent entrer des codes de produit (sku), un par ligne, dans un fichier nommé `sku.dat`.
### Spécifications

 - Le fichier doit se créer automatiquement s'il n'existe pas.
 - Les __sku__ entrés doivent être validés à la saisie (6 chiffres seulement).
 - La saisie se termine lors de l'appuie sur la touche ESC.
 - Les __sku__ de la base de donnée s'affichent alors à l'écran en format 5 colonnes.
 - Relancer le programme n'efface pas les sku précédents.

### Affichage requis
Ici il y avait déjà 15 __sku__ dans le fichier et un employé en entre 5 autres :
```plaintext
SKU : 098900
SKU : 101010
SKU : 879384
SKU : 567398
SKU : 789374
SKU : [Touche ESC appuyée]  

**************************************
         Liste des produits
**************************************
938475  093847  178493  000984  285745
909374  829385  983746  984012  119863
839485  102938  092847  983948  787364
098900  101010  879384  567398  789374
```
<hr><p align="Center"><img src="../../includes/end.png" alt="drawing" width="150"/></p>
