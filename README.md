
# 🪐 Le Déchiffreur d’Artefact

## 🎮 Présentation

**Genre :** Jeu d’énigmes interactif en terminal / Bash  
**Objectif :** Tu es une équipe d’archéologues ayant découvert un artefact extraterrestre. Chaque module représente une étape de l’infiltration et de l’activation de l’artefact. Résous les énigmes pour progresser.

Chaque module affiche une **narration immersive** et demande au joueur d’interagir via le terminal.

---

## ⚙️ Installation et pré-requis

Avant de lancer le jeu, rends tous les scripts Bash exécutables :

```bash
# depuis la racine du projet, rend tous les scripts .sh exécutables
find . -type f -name "*.sh" -exec chmod +x {} \;

# ou depuis un dossier de module
chmod +x *.sh
```

## 🔁 Ordre d’utilisation d’un module

Chaque module (ou palier) contient deux scripts principaux :

- **`setupX.sh`** : Initialise le module
  - Réinitialise le dossier et les fichiers nécessaires.
  - Génère les indices ou éléments à manipuler.
  - Affiche la narration immersive et les consignes.

- **`verificationX.sh`** : Vérifie votre solution
  - Demande au joueur de saisir sa réponse dans le terminal.
  - Vérifie si la réponse est correcte.
  - Affiche un message de réussite ou d’erreur.

### Étapes pour jouer un module

1. **Rendre les scripts exécutables si ce n'est pas deja fait.**  
1. **Lancer le script de setup pour préparer le module.**
2. **Suivre les instructions affichées et résoudre l’énigme.**
3. **Valider votre solution avec le script de vérification.**
4. **En cas d’erreur, réessayer directement ou bien relancer setupX.sh pour réinitialiser le module et réessayer.**

## 🗂️ Structure des modules
| Module | Nom                       | Objectif                                               | Mécanique principale                                                                                                  |
| ------ | ------------------------- | ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- |
| 1      | Neutralisation des défenses | Trouver le mot secret                                  | Lire les fichiers du journal, résoudre une opération mathématique et identifier la bonne page contenant le mot secret |
| 2      | Le Cercle des Runes       | Identifier la rune correcte                            | Chaque rune a 3 battements ; seule la rune dont la somme des battements est un nombre premier est correcte            |
| 3      | Le Verrou des permissions       | Déverrouiller la clé d’accès                           | Ouvrir le fichier `cle_access`, convertir le code binaire en décimal, puis saisir la clé dans le terminal             |
| 4      | La Chambre des Échos      | Bloquer un compte corrompu et créer un utilisateur sûr | Simuler la gestion d’utilisateurs et de permissions                                                                   |
| 5      | L'éveil du coeur de l'artefact     | Calculer le code final                                 | Observer une suite de Fibonacci affichée et saisir la somme des nombres comme code d’activation final                 |

## 💡 Conseils pour jouer

- Toujours exécuter setupX.sh avant verificationX.sh pour remettre le module dans son état initial.
- Saisir les réponses directement dans le terminal lorsque le script de vérification le demande (mot secret, rune, clé binaire, code Fibonacci…).
- Si vous faites une erreur, relancez setupX.sh pour tout réinitialiser proprement.
- Chaque module peut être rejoué autant de fois que nécessaire (valeurs aléatoires).

## 🔗 Commandes Bash utiles

- Lire un fichier : cat fichier.txt
- Chercher un mot dans un fichier : grep "mot" fichier.txt
- Déplacer/copier un fichier : mv source destination / cp source destination
- Créer un fichier vide : touch fichier.txt
- Modifier les permissions : chmod 740 fichier.sh
- Éditer un fichier : vi fichier.txt

## Amusez-vous bien et déchiffrez l’artefact jusqu’au bout !
