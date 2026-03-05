<p align="Center"><img src="../../includes/logo.png" alt="drawing" width="100"/></p>
<h3 align="Center">2Q2 - Développement Assembleur</h3>

# 🏋️‍♀️ Exercices 03 - Chaînes de caractères. 🏋️‍♀️

#### 📁 [Structures de projets & consignes à suivre](../../includes/rules.md)

## ↩ Question 01 - Reverso

Robert voit toujours tout à l'envers, aidez-le à voir ces phrases du bon côté en les inversants :

### Phrase 1

```plaintext
!sruetniop sel resilitu'd elitu siofrap tse lI
```

### Phrase 2

```plaintext
!!!OG ...1,2,3,4,5 snad tnednetne ednom el tuot euq ruop oloP ocraM iom-zeleppA
```

### Phrase 3

```plaintext
[VIDE]
```

Programmez un seul algorithme qui fonctionnera avec les 3 phrases. Placez-les en commentaires et décommentez la phrase à tester, simplement !

> 💡 Ajoutez un caractère de fin de ligne à la fin des chaînes de caractères `\0` pour C++ et `$` pour ASM8086.

> ⚠️ Le #3 devait simplement rien afficher à l'écran.

## 🤐 Question 02 - Zipper

Par mesure de sécurité, des données confidentielles ont été séparée, caractère par caractère, dans des variables différentes. Utilisez le principe du zipper afin de recréer l'information correctement en **mémoire** et affichez ensuite ce résultat à l'écran. Voici les données :

#### 🔒 Code secret 01
1. `J uscpbed esi ecus`;
2. `esi aal erusrc or!`;

> ⚠️ Un zipper est une fermeture éclair.  Le principe est de prendre une *dent* d'un premier côté et ensuite une autre d'un autre côté et ainsi de suite afin de refermer le tout.  Dans notre situation, le résultat sera une variable contenant le texte décodé.



### 2.2 🤐🤐🤐 DÉFI: Heavy Duty Zipper

En guise d'enrichissement personnel volontaire, assurez-vous que votre algorithme soit suffisament robuste afin de fonctionner avec ce message encodé :
#### 🔒 Code secret 02
1. `Mncd eberbse`;
2. `o oesml out`;

> ❓ Devez-vous faire un chargement à l'algorithme initial afin que cela fonctionne ?  Si oui, assurez-vous que votre nouvel algorithme ne *brise* pas le décodage du code secret 01.
  
> 💡 Dans le monde du développement, nous appelons cela des **test de régression**.

> ⚠️ Cet algorithme ne sera pas présent dans le solutionnaire. Présentez individuellement votre solution à l'enseignant sur une base volontaire afin de discuter de votre solution.

## 🔐 Question 03 - SKU Generator

Vous avez obtenu un contrat de programmation. Vous devez créer un générateur de code de produits (SKU) composé d'un nombre variable de **chiffres**.

```plaintext
Quelle est la taille du code que tu souhaite générer [0 à 9] ? 8
Code généré: 03948555
```

```plaintext
Quelle est la taille du code que tu souhaite générer [0 à 9] ? 6
Code généré: 837548
```

```plaintext
Quelle est la taille du code que tu souhaite générer [0 à 9] ? 0
```
> ⚠️ Afin de simplifier cette solution, nous présumerons que l'utilisateur entrera toujours un chiffre entre 0 et 9.

<hr><p align="Center"><img src="../../includes/end.png" alt="drawing" width="150"/></p>
