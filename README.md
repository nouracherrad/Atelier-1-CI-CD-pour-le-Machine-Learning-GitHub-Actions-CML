
# Atelier 1 : CI/CD pour le Machine Learning avec GitHub Actions et CML

## Description
Ce projet illustre la mise en place d'une **boucle d'entraînement et de reporting automatisée** pour un modèle de Machine Learning.  
À chaque `git push`, le workflow GitHub Actions :  
- Entraîne automatiquement le modèle (`script.py`)  
- Génère les métriques de performance (`metrics.txt`)  
- Génère la matrice de confusion (`conf_matrix.png`)  
- Publie un **rapport automatisé** en commentaire sur GitHub via CML  


---

## Structure du dépôt

<img width="288" height="227" alt="image" src="https://github.com/user-attachments/assets/b4f7445e-f872-4e14-be91-2afeabee6557" />


---

## Prérequis

- Compte GitHub
- Git installé
- Python 3.11
- Visual Studio Code ou tout autre IDE

---

## Installation et utilisation

1. Cloner le dépôt :

bash
git clone https://github.com/nouracherrad/Atelier-1-CI-CD-pour-le-Machine-Learning-GitHub-Actions-CML.git
cd Atelier-1-CI-CD-pour-le-Machine-Learning-GitHub-Actions-CML
`


2. Installer les dépendances :

bash
pip install --upgrade pip
pip install -r requirements.txt


3. Lancer le script localement (facultatif) :

bash
python script.py


> Après un `git push` vers GitHub, le workflow CI/CD s'exécute automatiquement.

---

## Pipeline GitHub Actions + CML

* **Déclencheur** : `on: push`
* **Environnement** : runner Ubuntu + Python 3.11  + CML
* **Étapes** :

  1. Installation des dépendances
  2. Exécution du script (`script.py`)
  3. Génération de `metrics.txt` et `conf_matrix.png`
  4. Création de `report.md`
  5. Publication automatique des métriques et de la matrice de confusion sur GitHub via CML

---

## Résultats attendus

* Fichier `metrics.txt` avec F1-score train/test et autres métriques
* Image `conf_matrix.png` de la matrice de confusion
* Commentaire automatique sur GitHub avec :

  * Bloc `## Metrics`
 <img width="914" height="407" alt="image" src="https://github.com/user-attachments/assets/9597f574-838f-46a5-8483-c9987c262460" />

  * Bloc `## Confusion Matrix`
 <img width="922" height="415" alt="image" src="https://github.com/user-attachments/assets/058d3b49-f15b-4d66-bbf2-ebce63ffc487" />


---

## Auteur

* **Noura Cherrad**
* **Nissrine EL Fijaoui**



---

