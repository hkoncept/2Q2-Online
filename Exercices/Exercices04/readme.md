<p align="Center"><img src="../../includes/logo.png" alt="drawing" width="100"/></p>
<h3 align="Center">2Q2 - Développement Assembleur</h3>

# 🏋️‍♀️ Exercices 04 - Procédures 🏋️‍♀️

#### 📁 [Structures de projets et consignes à suivre](../../includes/rules.md)

## 🚀 Question 01 - La NASA

La NASA vous a octroyé un contrat de programmation pour une procédure d'affichage du décompte pré-lancement d'une fusée, nommée `display`. Cette procédure doit afficher `Attention: X`, où X est le chiffre passé en paramètre (numérique). La procédure affichera `Décollage !!!` lorsque le chiffre passé en paramètre sera égal à zéro (`0`).

La procédure `main` fera une boucle en passant à la fonction `display` la valeur de 9 à 0.

### Affichage attendu :

```plaintext
Attention: 9
Attention: 8
Attention: 7
Attention: 6
Attention: 5
Attention: 4
Attention: 3
Attention: 2
Attention: 1
Décollage !!!
```

### Règles à respecter :

1. Effectuez le passage du paramètre (le chiffre du décompte) par la pile.
2. Il est permis de continuer d'utiliser des variables globales pour les messages à afficher.

## 🎲 Question 02 - Dice

Créer un algorithme qui affichera le résultat d'un jet d'un dé à l'écran à chaque appuie de la touche d'espacement. L'algorithme se servira de la procédure `random` qui retounera une valeur numérique aléatoire. L'appuie de la touche `ESC` terminera l'algorithme.

```plaintext
Vous avez obtenu un 6.
Vous avez obtenu un 2.
Vous avez obtenu un 1.
Vous avez obtenu un 3.
```

1. Effectuez le passage des paramètres par la pile.

> ⚠️ Avez-vous pensé à rendre votre procédure réutilisable en paramétrant les valeurs `min` et `max` ?

> 💡 Astuce : Déclarez les contantes MIN et MAX en 16 bits afin d'être en mesure de les placer facilement sur la pile.

> 🏆 Mini Challenge : Faites en sorte que l'utilisateur puisse quitter le programme en appuyant sur `ESC`.

## 📦 Question 03 - SKU Generator

Créer un algorithme qui affiche un SKU d'exactement 6 chiffres généré aléatoirement à chaque appuie de la touche d'espacement. Votre algorithme devra comporter une procédure `generate_sku` qui reçoit en paramètre l'emplacement où écrire le SKU généré. Cette procédure appelera à son tour la procédure `random` créée précédement.

```plaintext
SKU: 939485
SKU: 002948
SKU: 109586
```

1. Effectuez le passage des paramètres d'entrée par la pile.
2. Aucun accès direct aux variables globales ne doit être fait, seul l'adresse mémoire passé en paramètre au besoin.
3. Conservez chacune des procédures **pures**.

> 🏆 Mini Challenge : Faites en sorte que l'utilisateur puisse quitter le programme en appuyant sur `ESC`.

## ⚡ Question 04 - Power !

Demandez une base (entre 1 et 9) ainsi qu'une puissance (entre 1 et 5) à l'utilisateur.
Dans une procédure **power**, effectuez le calcul et retournez le résultat.
Affichez ensuite le résultat dans le registre BX.

```plaintext
Entrez la base : 2
Entrez l'exposant : 8
; Valeur du registre BX : 256
```

```plaintext
Entrez la base : 9
Entrez l'exposant : 5
; Valeur du registre BX : 59049
```

### Règles à respecter :

1. Effectuez le passage des paramètres par la pile.
2. Aucun accès direct aux variables globales ne doit être fait, seul l'adresse mémoire passé en paramètre au besoin.
3. Conservez chacune des procédures **pures**.

## ⚡⚡⚡ DÉFI Question 05 - SuperPower !

Affichez maintenant le résultat à l'écran.

```plaintext
Entrez la base : 9
Entrez l'exposant : 5
Résultat : 59049
```

> ⚠️ Vous aurez besoin d'une procédure dédiée à l'affichage d'une valeur numérique à l'écran.

### Règles à respecter :

1. Effectuez le passage des paramètres par la pile.
2. Aucun accès direct aux variables globales ne doit être fait, seul l'adresse mémoire passé en paramètre au besoin.
3. Conservez chacune des procédures **pures**.

<hr><p align="Center"><img src="../../includes/end.png" alt="drawing" width="150"/></p>
