# Bingo des doctorants

Une seule page (`index.html`) hébergée sur GitHub Pages, synchronisée entre
les téléphones et l'écran de projection par une base Firebase Realtime Database.

## 1. Créer la base (5 minutes, gratuit)

1. Aller sur https://console.firebase.google.com et créer un projet.
2. Menu **Build > Realtime Database > Créer une base de données** (région Europe).
3. Onglet **Règles**, coller puis publier :

   ```json
   { "rules": { ".read": true, ".write": true } }
   ```

   Toute personne qui a l'adresse de la base peut alors lire et écrire.
   C'est acceptable pour une animation d'un soir ; repasser les deux à
   `false` une fois la fête terminée.
4. **Paramètres du projet > Tes applications > Ajouter une application Web**,
   puis copier les valeurs de `firebaseConfig`.

## 2. Brancher la page

Dans `index.html`, remplacer les valeurs `A_COLLER` du bloc `FIREBASE_CONFIG`
(en haut du fichier) par celles du projet. `databaseURL` est indispensable.

## 3. Mettre en ligne

1. Créer un dépôt GitHub public et y déposer `index.html`.
2. **Settings > Pages > Deploy from a branch**, branche `main`, dossier `/ (root)`.
3. Le site est disponible à `https://<utilisateur>.github.io/<dépôt>/`.

## Utilisation

- **Préparer les grilles** : saisir les anecdotes et les grilles 3x3.
- Chaque doctorant ouvre le lien sur son téléphone et choisit son prénom.
- **Écran de projection et tirage** : à projeter ; cliquer sur le numéro tiré.
