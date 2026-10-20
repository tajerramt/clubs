# Clubs ENS Marrakech — déploiement GitHub Pages

Fichiers : `index.html` (l'application), `firebase-config.js` (à remplir), `firestore.rules` (règles de sécurité), `logo.jpg`.
GitHub Pages héberge la page ; Firebase (gratuit) stocke les données et gère les connexions.

## 1. Créer le projet Firebase (console.firebase.google.com)
1. **Ajouter un projet** (Google Analytics non nécessaire).
2. **Authentication > Commencer > Email/Mot de passe** : activer.
3. **Firestore Database > Créer une base** (mode production, région `eur3` ou `europe-west`).
4. Onglet **Règles** de Firestore : colle le contenu de `firestore.rules`, puis **Publier**.
5. **Paramètres du projet > Tes applications > Web (</>)** : enregistre l'app, copie la configuration dans `firebase-config.js`.

## 2. Publier sur GitHub
1. Crée un dépôt GitHub, puis **Add file > Upload files** : envoie les 4 fichiers à la racine.
2. **Settings > Pages > Deploy from a branch > main / (root)** : enregistre.
3. Ton lien sera `https://TON-PSEUDO.github.io/NOM-DU-DEPOT/`.
4. Firebase **Authentication > Paramètres > Domaines autorisés** : ajoute `TON-PSEUDO.github.io`.

## 3. Premier lancement
1. Ouvre le lien, clique **Créer mon compte**, puis va dans **Mon espace**.
2. Si l'annuaire est vide, clique **Ajouter les 20 clubs de l'ENS** (une seule fois).
3. Choisis ton club, puis envoie le lien aux autres présidents.

## Bon à savoir
- Seuls les comptes connectés voient les données (emails et téléphones protégés), mais n'importe qui peut créer un compte avec le lien : ne le diffuse qu'aux présidents.
- Chaque club n'est modifiable que par le compte qui l'a choisi ; les autres présidents ne peuvent pas modifier ses événements.
- La clé dans `firebase-config.js` est publique par conception : la sécurité repose sur les règles Firestore.
