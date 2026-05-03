# GreenQuiz

GreenQuiz est une application web ?ducative d?di?e au Green IT.  
Le projet permet de cr?er, g?rer et jouer des quiz autour des bonnes pratiques num?riques responsables.  
L'architecture est volontairement simple et l?g?re pour reduire l'empreinte technique (Flask, SQLite, front natif).  
L'objectif est de proposer une plateforme utile, maintenable et sobre en ressources.

## Site d?ploy?

- Application en ligne : [https://greenproject-1f1e.onrender.com/](https://greenproject-1f1e.onrender.com/)

## ?quipe et r?les

- `Membre 1` - Product Owner / Coordination projet
- `Membre 2` - D?veloppement back-end (Flask, routes, logique metier)
- `Membre 3` - D?veloppement front-end (templates, UI, UX)
- `Membre 4` - Qualit?, tests et d?ploiement

> Remplacer les noms des membres par les noms r?els de votre ?quipe.

## Stack technique et justification Green IT

- `Python + Flask` : framework minimal, faible surcouche, moins de complexit? et de d?pendances.
- `SQLite` : base l?g?re sans serveur d?di?, adapt?e a un projet p?dagogique avec faible co?t infra.
- `HTML/CSS/JS natifs` : pas de framework front lourd, moins de JavaScript execute et moins de transfert reseau.
- `Render` : d?ploiement simple et rapide, mutualisation de l'infrastructure.
- `Werkzeug security` : hash des mots de passe pour la s?curit? sans service externe additionnel.

## Installation et lancement local

### 1) Cloner le projet

```bash
git clone <URL_DU_REPO>
cd GreenProject
```

### 2) Installer les d?pendances

```bash
python -m pip install -r requirements.txt
```

### 3) Lancer l'application

```bash
python app.py
```

### 4) Ouvrir dans le navigateur

- `http://127.0.0.1:8000`

## Structure du d?p?t (arborescence comment?e)

```text
GreenProject/
|- app.py                    # Application Flask (routes, auth, logique quiz, init DB)
|- requirements.txt          # D?pendances Python
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
|  |- quizzes_*.html         # Cr?ation/?dition/suppression quiz
|- docs/
|  |- rapport.pdf            # Rapport final (? d?poser ici)
```

## Conventions de commit

Convention adopt?e : `type(scope): message court`

Types utilis?s :
- `feat` : nouvelle fonctionnalit?
- `fix` : correction de bug
- `refactor` : am?lioration interne sans changement fonctionnel
- `docs` : documentation
- `test` : ajout/modification de tests
- `chore` : maintenance technique

Exemples :
- `feat(auth): ajouter suppression de compte`
- `fix(deploy): utilis?r PORT fourni par Render`
- `docs(readme): compl?ter la section installation`

## Lien vers le rapport PDF

- Rapport : [docs/rapport.pdf](docs/rapport.pdf)

> Si le PDF n'est pas encore versionn?, ajouter le fichier `rapport.pdf` dans le dossier `docs/`.
