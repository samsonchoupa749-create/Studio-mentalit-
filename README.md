# STUDIO MENTALITÉ — Version 1.0

## Ce que contient cette version
- Tableau de bord avec indicateurs.
- Six ateliers : littérature, cinéma, patrimoine, dessin/animation, carrière, communication.
- Gestion des projets, statuts et objectifs.
- Gestion des tâches, échéances et cases terminées.
- Documents/notes liés aux projets.
- Modèles de consignes IA à copier dans un assistant externe.
- Export et import des données au format JSON.
- Manifest, icônes et service worker pour une PWA.
- Interface responsive en français, adaptée au téléphone.

## Limites connues
- Ce n'est pas un APK Android : c'est une application web installable (PWA).
- L'installation sur l'écran d'accueil nécessite généralement une publication HTTPS.
- Les données sont stockées localement dans le navigateur, sans synchronisation automatique.
- Exporter régulièrement une sauvegarde est essentiel.
- L'IA n'est pas connectée automatiquement dans cette version : les consignes sont copiables vers un assistant IA de ton choix.
- Le service worker ne fonctionne pas en ouvrant simplement `index.html` depuis le gestionnaire de fichiers. Il faut charger le site via HTTPS (ou localhost).
- La première visite nécessite une connexion Internet. Après mise en cache, l'interface peut s'ouvrir hors ligne, mais une IA distante ne fonctionnera pas sans connexion.

## Publier gratuitement avec GitHub Pages depuis un téléphone
1. Ouvre https://github.com dans ton navigateur et connecte-toi ou crée un compte.
2. Crée un nouveau dépôt, par exemple `studio-mentalite`. Un dépôt public suffit pour GitHub Pages.
3. Téléverse le contenu du dossier `STUDIO_MENTALITE_V1` à la racine du dépôt. Il faut téléverser `index.html`, `manifest.json`, `sw.js` et le dossier `icons` avec les deux PNG. Ne téléverse pas seulement le ZIP.
4. Dans le dépôt, ouvre **Settings → Pages**.
5. Dans **Build and deployment**, choisis **Deploy from a branch**, puis la branche `main` et le dossier `/ (root)`, puis **Save**.
6. Attends que GitHub affiche l'adresse publiée. Elle ressemble généralement à `https://TON-PSEUDO.github.io/studio-mentalite/`. Utilise exactement l'adresse fournie par GitHub.
7. Ouvre cette adresse dans Chrome Android et attends que la page soit complètement chargée.
8. Dans Chrome, ouvre le menu ⋮. Choisis **Installer l'application** ou **Ajouter à l'écran d'accueil** (le libellé dépend de la version). Confirme. L'icône doit apparaître sur l'écran d'accueil.
9. Crée un projet test, ajoute une tâche et un document, puis exporte une sauvegarde.
10. Après un premier chargement en ligne, teste le mode avion. Si la page ne s'ouvre pas hors ligne, reconnecte-toi et recharge une fois l'application.

## Mises à jour
Après avoir remplacé les fichiers dans GitHub, le cache peut garder une ancienne version. Si une mise à jour ne s'affiche pas, ferme l'application, ouvre le site dans Chrome et recharge. Pour une version ultérieure, change `studio-mentalite-v1` dans `sw.js` vers `studio-mentalite-v2`.

## Confidentialité et sécurité
- N'y conserve pas de mots de passe, codes PIN, données bancaires ou informations hautement sensibles.
- Le stockage local peut être supprimé par les réglages du navigateur ou le système.
- Les sauvegardes JSON ne sont pas chiffrées : protège les fichiers exportés.
- Ne place jamais de clé API secrète dans `index.html`. Une connexion IA avec clé privée nécessiterait un serveur intermédiaire sécurisé.
- GitHub Pages héberge des fichiers statiques ; il ne fournit pas à lui seul une base de données privée ou un serveur pour cacher une clé API.

## Fichiers
- `index.html` : application.
- `manifest.json` : identité et paramètres installables.
- `sw.js` : cache hors ligne.
- `icons/icon-192.png`, `icons/icon-512.png` : icônes d'application.
