<p align="Center"><img src="../../includes/logo.png" alt="drawing" width="100"/></p>
<h3 align="Center">2Q2 - Développement Assembleur</h3>

# 🏋️‍♀️ Exercices 02 - Boucles & cie. 🏋️‍♀️

#### 📁 [Structures de projets & consignes à suivre](../../includes/rules.md)

## 4️⃣ Question 01 - ASCII

Créer deux variables x=5 et y=9. Calculer la différence entre y et x et affichez la réponse à l'écran.

#### Affichage requis:

```plaintext
4
```

## 🦘 Question 02 - Jump! Jump!

Reproduire ce code C++ en assembleur et le faire rouler avec 85 comme note tout comme 50.

```cpp
int seuil = 60;
int note = 85;
string message ="Vous avez avez obtenu un";
string succes = "succes";
string echec = "echec";
cout << message << " ";
if(note >= seuil) {
   cout << succes;
} else {
   cout << echec;
}
cout << "!";
```

#### Affichage requis:

```plaintext
Vous avez avez obtenu un succes!
```

```plaintext
Vous avez avez obtenu un echec!
```

## 🔠 Question 03 - Mr. Alpha Baitte

Écrivez l'alphabet à l'écran comme suit en affichant les caractères un à la fois :

> 🚫 Interdit d'utiliser la fonction d'affichage de chaîne de caractères (09h).

#### Affichage requis:

```plaintext
AaBbCcDdEeFfGgHhIiJjKkLlMmNnOoPpQqRrSsTtUuVvWwXxYyZz
```

> ⚠️ Réfléchissez à la structure globale avant de débuter le pseudo-code. Il est possible d'utiliser la représentation ASCII afin de créer la boucle : 'A' à 'Z'.

## 🚀 Question 04 - Rocketer

Programmez une simulation de lancement de fusée.

```plaintext
9
8
7
6
5
4
3
2
1
DÉCOLLAGE!!!
```

> ⚠️ Utilisez obligatoirement l'instruction `LOOP` au lieu de `JMP` afin de réaliser la boucle en ASM8086.

## 🎨 Question 05 - Pablo Picasso del Shawinigan

Recréez ce dessin à l'écran :

```plaintext
**********
*********
********
*******
******
*****
****
***
**
*
```

> 💡 En élaborant votre pseudo-code, utilisez des variables représentative de la réalité. Exemple: `line` pour le numéro de ligne (1 à 10) et `star` pour le numéro de l'étoile.

> ⚠️ L'apprentissage principal de cette question est de déterminer, avant de débuter la programmation, l'**équation** du nombre d'étoiles par ligne.

<hr><p align="Center"><img src="../../includes/end.png" alt="drawing" width="150"/></p>
