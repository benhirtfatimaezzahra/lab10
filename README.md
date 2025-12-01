# Lab10 – Indexation et Slicing NumPy

Application pratique de l'indexation et du slicing avec NumPy. Ce lab explore les techniques d'accès et de modification des éléments dans les tableaux 1D et 2D, ainsi que les concepts de vues et de copies.

Le programme démontre la différence entre vues (partage mémoire) et copies (indépendance), ainsi que les opérations de slicing avancées sur les tableaux NumPy.

---

## Fonctionnalités

### Indexation 2D
- **Accès par colonnes** : sélection de colonnes entières avec `[:, index]`
- **Modification in-place** : utilisation de `*=` pour modifier directement
- **Dernière colonne** : accès avec index négatif `[:, -1]`
- **Opérations vectorisées** : multiplication de colonnes entières

### Slicing et Blocs
- **Extraction de blocs** : sélection de sous-matrices avec `[lignes, colonnes]`
- **Slicing multi-dimensionnel** : `[1:, :2]` pour lignes 1+ et colonnes 0-1
- **Slicing 1D** : extraction de portions de vecteurs avec `[début:fin]`
- **Exclusion des extrémités** : `[1:-1]` pour ignorer premier et dernier éléments

### Vues vs Copies
- **Vue (view)** : partage la mémoire avec le tableau original
- **Copie (copy)** : tableau indépendant avec sa propre mémoire
- **Modification via vue** : les changements affectent le tableau original
- **Modification via copie** : les changements n'affectent pas l'original
- **Méthode `.copy()`** : création explicite de copies indépendantes

### Restauration de Données
- **Sauvegarde avant modification** : utilisation de `.copy()` pour backup
- **Restauration** : réaffectation depuis la copie sauvegardée
- **Préservation de l'original** : maintien des données initiales intactes

---

## Architecture
```
Lab10-Indexation.ipynb → Notebook Jupyter contenant :

1. Données initiales
   - A : tableau 1D de 5 éléments [10, 20, 30, 40, 50]
   - M : tableau 2D de 3×4 éléments

2. Exercise 8.1 : Dernière colonne × 10
   - Copie du tableau original
   - Accès à la dernière colonne avec [:, -1]
   - Multiplication in-place avec *=
   - Affichage du résultat

3. Exercise 8.2 : Bloc modifié (vue)
   - Extraction d'un bloc via slicing
   - Création d'une vue (partage mémoire)
   - Modification via la vue
   - Vérification de l'impact sur le tableau original

4. Exercise 8.3 : Bloc indépendant (copie)
   - Extraction d'un bloc avec .copy()
   - Création d'une copie indépendante
   - Modification de la copie
   - Vérification de l'indépendance

5. Exercise 8.4 : Vecteur slicing
   - Sauvegarde du vecteur original
   - Slicing pour exclure les extrémités [1:-1]
   - Mise à zéro des éléments centraux
   - Restauration du vecteur
```

---

## Installation

Cloner le projet :
```bash
git clone https://github.com/benhirtfatimaezzahra/Lab10.git
```

Installer NumPy (si nécessaire) :
```bash
pip install numpy
```

Ouvrir le notebook avec Jupyter :
```bash
cd Lab10
jupyter notebook Lab10-Indexation.ipynb
```

Ou utilisez JupyterLab :
```bash
jupyter lab Lab10-Indexation.ipynb
```

---


## Notes Techniques

### Concepts NumPy utilisés
- **Indexation 2D** : `array[lignes, colonnes]`
- **Index négatifs** : `-1` pour dernier élément, `-2` pour avant-dernier
- **Slicing** : `[début:fin]` pour extraire des portions
- **Slicing avec omission** : `[1:]` (début à fin), `[:2]` (début à 2), `[1:-1]` (sans extrémités)
- **Vue (view)** : `array[slice]` partage la mémoire
- **Copie (copy)** : `.copy()` crée un tableau indépendant
- **Modification in-place** : `*=`, `+=`, `[:] =` pour modifier sans réaffectation
- **All selector** : `:` pour sélectionner toutes les lignes ou colonnes



## Démonstration

<img width="1648" height="522" alt="image" src="https://github.com/user-attachments/assets/d68c4eb7-5007-4143-9838-827d56d497d4" />
<img width="1623" height="809" alt="image" src="https://github.com/user-attachments/assets/6bed88ca-c731-40cd-a5b1-2c55d7427852" />
<img width="1620" height="828" alt="image" src="https://github.com/user-attachments/assets/84f41953-09c1-437d-a755-03776f6461e4" />

---

## Auteur

**Nom :** Benhirt Fatima Ezzahra  
**Cours :** Introduction à Python  
**Date :** Décembre 2025  
**Encadré par :** Pr. Mohamed LACHGAR
