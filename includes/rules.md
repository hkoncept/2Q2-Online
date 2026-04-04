## Structure de la solution C++
Créez une solution C++ globale nommée `2Q2-Solutions` que vous utiliserez pour toutes les solutions aux exercices.  À l'aide de Windows, créez un dossier `Projets` à l'intérieur de `2Q2-Solutions`.

Créez ensuite un __projet Visual Studio__ par page d'exercices (exemple: `Exercices01`) en vous assurant de le créer dans le dossier `Projets` et ajoutez-y un fichier principal nommé `main.cpp`.  Créez finalement une fonction de type `void` pour chaque question dans cette page d'exercices, exemple :

```cpp
void question01() {
   // Votre code ici
}
```



## Consignes à suivre
1. Lire la question et, sur 'papier', réinterpréter la demande en vos mots. Exemple: _Je dois générer des mots de passe aléatoirement_.
2. Décortiquer votre idée générale en 3 à 5 sections afin de simplifier l'écriture du _pseudo-code_ en C++.
   1. LECTURE: Demander la taille du mot de passe à l'utilisateur.
   2. GÉNÉRATION: Créer le mot de passe aléatoire en utilisant l'horloge.
   3. AFFICHAGE: Afficher le mot de passe à l'écran.
3. N'oubliez pas que votre code C++ devra être transcodé en ASM8086 par la suite.  Afin de conserver la plus grande corrélation possible, utilisez les types de variables 8 et 16 bits pures en C++ :
   1. DB (8 bits) --> `uint8_t`
   2. DW (16 bits) --> `uint16_t`

> ⚠️ Utiliser les version __signées__ de ces variables pour les boucles (`int8_t` et `int16_t`).

4. Déployez votre code sur plusieurs lignes vous aidera à trancoder en ASM8086.
   - Exemple, ce code :
   ```cpp
   cout << "Impossible d'ouvrir le fichier " << FILENAME << "!";
   ```
   - Deviendra :
   ```cpp
   const uint8_t message[] = "Impossible d'ouvrir le fichier ";
   //...
   cout << message;
   cout << FILENAME;
   cout << "!";
   ```
## Création des fichiers ASM8086
1. Dans `2Q2-Solutions\Projets\ExercicesXX`, créez un dossier nommé `ASM8086` où vous placerez les code assembleurs de vos solutions.
2. Créer une copie de la dernière version du [template ASM8086](https://www.cshawi.info/2q2.html#t4) en le réenregistrant selon cette nomenclature `E`[Numéro de l'exercice]`Q`[Numéro de la question]`.ASM` (exemple: `E01Q02.ASM` pour la deuxième question de l'exercices 01).
3. Transcrire votre _pseudo-code_ C++ en ASM8086 et y ajouter le C++ en prenant bien soin de conserver une corrélation ligne par ligne (autant que possible).
   - Les variables ainsi que les procédures doivent être codées dans la section appropriée.
   - Toutes les données numériques entières doivent être en `hexadécimales` (exemple: `30` en décimal devriendra `21h` en hex).
   - Les étiquettes doivent être en minuscules et tout le reste en majuscule.
   - Les instructions, commentaires et le code C++ doivent débuter **exactement** sur la colonne telle qu'indiquée en haut du _template_.

## Remise d'une série d'exercices :
Pour chacunes des séries d'exercices, remettez votre solution globale complète :
1. Fermez l'application Visual Studio.
2. Assurez-vous de supprimer tous les dossiers compilés ainsi que le dossier caché `.vs`.
3. Compressez le répertoire racine `2Q2-Solutions`.
4. Observez la taille du fichier `2Q2-Solutions.zip`, s'il fait plus de 500ko, revenez au point #1.
5. Remettez le fichier `2Q2-Solutions.zip` sur Omnivox dans la section des travaux au nom de l'exercice.