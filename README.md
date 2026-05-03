# GreenQuiz

GreenQuiz est une application web éducative dédiée au Green IT.  
Le projet permet de créer, gérer et jouer des quiz autour des bonnes pratiques numériques responsables.  
L'architecture est volontairement simple et légère pour reduire l'empreinte technique (Flask, SQLite, front natif).  
L'objectif est de proposer une plateforme utile, maintenable et sobre en ressources.

## Site déployé

- Application en ligne : [https://greenproject-1f1e.onrender.com/](https://greenproject-1f1e.onrender.com/)

## Équipe et rôles

- `Membre 1` - Product Owner / Coordination projet
- `Membre 2` - Développement back-end (Flask, routes, logique metier)
- `Membre 3` - Développement front-end (templates, UI, UX)
- `Membre 4` - Qualité, tests et déploiement

> Remplacer les noms des membres par les noms réels de votre Équipe.

## Stack technique et justification Green IT

- `Python + Flask` : framework minimal, faible surcouche, moins de complexité et de dépendances.
- `SQLite` : base légère sans serveur dédié, adaptée a un projet pédagogique avec faible coût infra.
- `HTML/CSS/JS natifs` : pas de framework front lourd, moins de JavaScript execute et moins de transfert reseau.
- `Render` : déploiement simple et rapide, mutualisation de l'infrastructure.
- `Werkzeug security` : hash des mots de passe pour la sécurité sans service externe additionnel.

## Installation et lancement local

### 1) Cloner le projet

```bash
git clone <URL_DU_REPO>
cd GreenProject
```

### 2) Installer les dépendances

```bash
python -m pip install -r requirements.txt
```

### 3) Lancer l'application

```bash
python app.py
```

### 4) Ouvrir dans le navigateur

- `http://127.0.0.1:8000`

## Structure du dépôt (arborescence commentée)

```text
GreenProject/
|- app.py                    # Application Flask (routes, auth, logique quiz, init DB)
|- requirements.txt          # Dépendances Python
|- README.md                 # Documentation du projet
|- database/
|  |- greenquiz.sqlite       # Base SQLite locale
|- static/
|  |- assets/
|     |- style.css           # Styles globaux
|     |- app.js              # JS client (interactions UI)
|- templates/
|  |- base.html              # Layout principal
|  |- index.html             # Accueil + listing quiz publics
|  |- login.html             # Connexion
|  |- register.html          # Inscription
|  |- account*.html          # Espace personnel (profil/modification/suppression)
|  |- users_*.html           # Ecran admin de gestion utilisateurs
|  |- quizzes_*.html         # Création/édition/suppression quiz
|- docs/
|  |- rapport.pdf            # Rapport final (à déposer ici)
```

## Conventions de commit

Convention adoptée : `type(scope): message court`

Types utilisés :
- `feat` : nouvelle fonctionnalité
- `fix` : correction de bug
- `refactor` : amélioration interne sans changement fonctionnel
- `docs` : documentation
- `test` : ajout/modification de tests
- `chore` : maintenance technique

Exemples :
- `feat(auth): ajouter suppression de compte`
- `fix(deploy): utiliser PORT fourni par Render`
- `docs(readme): compléter la section installation`

## Lien vers le rapport PDF

- Rapport : [docs/rapport.pdf](docs/rapport.pdf)

> Si le PDF n'est pas encore versionné, ajouter le fichier `rapport.pdf` dans le dossier `docs/`.
