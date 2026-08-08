# 📚 Book's Club — suivi de lecture

Une app de suivi de lecture personnelle, à héberger sur GitHub Pages et à ajouter sur ton écran d'accueil iPhone (exactement comme pour ton app de suivi de sport).

Toutes les données (livres, journal, streak, objectifs) sont stockées **uniquement dans le navigateur de ton téléphone** (aucun serveur, aucun compte). Pense à faire un export de temps en temps depuis les paramètres de l'app (⚙️ → "Exporter mes données") pour ne rien perdre si tu changes de téléphone ou vides les données Safari.

## Fonctionnalités

- **Journal** : calendrier mensuel, tu coches chaque jour si tu as lu ou non (+ le livre, les pages, une note). Tu peux remplir un jour manqué plus tard, la streak se recalcule automatiquement sur les vraies dates.
- **Objectifs** : objectif de nombre de livres par an (modifiable, historisé par année), streak actuelle + record, pages lues (année et total), heatmap d'assiduité sur 12 mois, statistiques par genre.
- **Palier lifetime** (façon Book Nova) : 15 paliers de badges (1, 5, 10, 25, 50, 75, 100, 150, 200, 300, 500, 750, 1000, 1500, 2000 livres lus), avec barre de progression vers le prochain palier.
- **PAL (pile à lire)** : liste de livres à lire + bouton "🎲 Choisis ma prochaine lecture" qui tire un livre au hasard dans ta pile.
- **Sagas en cours** : suivi de séries tome par tome, avec barre de progression.
- **Lus** : bibliothèque des livres terminés, recherche, note en étoiles, avis. Ajouter un livre déjà lu avec une date de fin l'ajoute automatiquement à l'objectif de l'année correspondante.
- **Bonus** : mode sombre, export/import JSON (sauvegarde), design mobile pensé pour un usage "app" via écran d'accueil.

## 1. Mettre le projet sur GitHub

1. Va sur [github.com/new](https://github.com/new) et crée un nouveau repo, par exemple `books-club` (public, sans README ni licence).
2. Sur ton Mac, dans le dossier reçu (`booksclub`), ouvre le Terminal et lance :

   ```bash
   cd chemin/vers/booksclub
   git remote add origin https://github.com/TON-NOM-UTILISATEUR/books-club.git
   git branch -M main
   git push -u origin main
   ```

   (Le dossier contient déjà un historique git avec les commits prêts — pas besoin de refaire `git init` ni `git commit`.)

## 2. Activer GitHub Pages

1. Sur la page du repo GitHub → **Settings** → **Pages** (menu de gauche).
2. Dans "Build and deployment", choisis **Source : Deploy from a branch**.
3. Branch : **main**, dossier **/ (root)** → **Save**.
4. Attends 1 à 2 minutes, GitHub te donne une URL du type :
   `https://TON-NOM-UTILISATEUR.github.io/books-club/`

## 3. Ajouter l'app sur ton iPhone

1. Ouvre cette URL dans **Safari** sur ton iPhone.
2. Appuie sur l'icône de partage (le carré avec la flèche vers le haut).
3. Choisis **"Sur l'écran d'accueil"**.
4. Valide → l'icône "Book's Club" apparaît sur ton écran d'accueil et s'ouvre en plein écran comme une vraie app.

## Mettre à jour l'app plus tard

Si tu veux ajouter une fonctionnalité ou changer un détail, demande-moi les modifications, je te renvoie les fichiers mis à jour : il te suffira de les repousser sur GitHub (`git add -A && git commit -m "update" && git push`) et de recharger la page sur ton iPhone (l'icône sur l'écran d'accueil se met à jour toute seule au prochain chargement avec réseau).

## Fichiers du projet

- `index.html` — toute l'application (HTML + CSS + JS, un seul fichier)
- `manifest.json` — permet l'ajout à l'écran d'accueil avec une belle icône
- `icon-192.png`, `icon-512.png` — icône de l'app
