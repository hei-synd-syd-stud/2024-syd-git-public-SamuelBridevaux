# Answers of Samuel Bridevaux SamuelBridevaux

## Basics

### Task 1

Après le clonage du dépôt Git, on trouve :

1. **Dossier `.git`** : contient l'historique complet du projet, y compris les commits, branches, et les métadonnées du projet pour le suivi de version. Ce dossier permet d'utiliser les fonctionnalités Git.
2. **Dossier `img`** : un dossier pour stocker des images liées au projet.
3. **Fichier `answers.md`** : fichier Markdown pour noter les réponses.

### Task 2

On voit les modifications apporté dans answers.md et on voit aussi que le fichier README.md a été ajouté. On voit aussi que les modifications n'ont pas été commit.

### Task 3

On voit que le fichier README.md est prêt à être commit.

Les logs n'ont pas changé.

### Task 4

Le fichier README.md (vide) est prêt à être commit. Par contre les modifications apportées dans le README.md ne sont pas prêtes à être commit.

### Task 5

On voit cela dans la console :

```sh
$ git log --oneline
410e57b (HEAD -> main) ADD: README file.
5da930b (origin/main, origin/HEAD) Initial commit
```

1. **410e57b** est le début de l'identifiant unique (ou *hash*) du commit. Chaque commit dans Git est représenté par un identifiant SHA-1 unique, ce qui permet de le distinguer des autres commits. Dans notre cas, on voit seulement le "short hash" Cela permet de retrouver précisément le commit dans l’historique et de revenir dessus si nécessaire.

2. **HEAD** est pointeur qui représente le commit actuellement "checkouté" (celui sur lequel on est positionné). Dans ce cas, HEAD est sur la branche `main`.
   
   **main** : C'est le nom de la branche actuelle. Ici, cela signifie que le commit `f878da5` est le dernier commit de la branche `main`.
   
   Donc, `(HEAD -> main)` indique que `HEAD` et `main` pointent tous les deux sur le commit `f878da5`, ce qui signifie qu’on est sur la branche `main` et que ce commit est le plus récent sur cette branche.

3. Après les parenthèses, on voit le message de commit : `"ADD: README file."`. Ce message décrit brièvement les modifications apportées dans ce commit.

### Task 6

Lors du checkout commit sur le initial commit, les fichiers du projet sont revenus à l’état du tout premier commit, donc seuls les fichiers présents à ce moment-là étaient visibles.

Ensuite, lorsque j'ai checkout sur le main, tous les fichiers et modifications ajoutés depuis le commit initial ont été restaurés, ramenant le projet à son état le plus récent.

## Gitgraph

### Task 7

![Gitgraph](img/gitgraph.svg)

1. **develop** : Nom de la branche `develop`, qui est une branche secondaire par rapport à la branche principale `main`.

2. **baa6795** : Identifiant du commit. Chaque commit possède un identifiant unique, ici, il commence par "baa6795".

3. **Merge branch 'feature-auth' into 'develop'** : Message de commit indiquant qu'une fusion (*merge*) de la branche `feature-auth` vers la branche `develop` a été réalisée.

4. **ByteMe Bob bob.byteme@hevs.ch** : Auteur du commit de fusion, ici "ByteMe Bob" avec son adresse e-mail.

5. Tag `v1.0.0`, utilisé pour marquer une version spécifique dans l'historique du dépôt.

6. Merge la branche `feature-auth` dans `develop`

7. Création de la branche `feature-auth`, qui est une branche secondaire. Ici, le commit d'id **c93cfcc** ajoute l'athentification utilisateur fait par "CodeQueen Carol"

8. Merge la branche `develop` dans `main` par "Silvan Zahno" avec l'identifant de commit **7725aa3**.

9. Ligne de la branche `develop` avec les commits suivant :
   
   - `b205e38` : Préparation pour la publication, par "Silvan Zahno".
   - `e209ecc` : Ajout du frontend, par "Silvan Zahno".
   - `79bc77a` : Ajout du backend, par "Silvan Zahno".

10. Ligne de la branche `main` et en bas le commit initial avec l'id **e83fbdc** fait par "Silvan Zahno".

Ce schéma montre un historique Git avec des branches, des commits, des fusions, et un tag pour la version.