# Portfolio de Grégoire — mettre l'application en ligne et l'installer

Ce dossier est un site prêt à publier. Il suffit de le mettre en ligne (gratuit), puis d'ouvrir l'adresse sur chaque appareil et d'installer l'application.

## 1. Mettre le dossier en ligne (une seule fois)

Il faut une adresse en **https**, sinon l'installation ne marche pas. Trois options gratuites, de la plus simple à la plus technique :

**Netlify Drop (le plus simple)**
1. Va sur app.netlify.com/drop.
2. Glisse le dossier `pwa` (décompressé) dans la page.
3. Netlify te donne une adresse du type `https://nom-au-hasard.netlify.app`. Garde-la.

**Cloudflare Pages**
1. Crée un compte sur pages.cloudflare.com, choisis « Upload assets ».
2. Envoie le dossier, donne un nom au projet. L'adresse est `https://ton-nom.pages.dev`.

**GitHub Pages**
1. Crée un dépôt public, envoie-y le contenu du dossier.
2. Dans Settings → Pages, choisis la branche principale. L'adresse est `https://ton-pseudo.github.io/nom-du-depot/`.

## 2. Installer

**Android (Chrome)** : ouvre l'adresse, touche le bouton « Installer » en haut de l'application (ou menu ⋮ → « Installer l'application »).

**iPhone / iPad (Safari uniquement)** : ouvre l'adresse, touche Partager → « Sur l'écran d'accueil ».

**Windows / Mac (Chrome ou Edge)** : ouvre l'adresse, clique « Installer » dans l'application (ou l'icône d'installation à droite de la barre d'adresse). L'application apparaît dans le menu Démarrer comme un vrai logiciel, avec sa propre fenêtre.
Le bouton « Installer » est toujours visible tant que l'application n'est pas installée. S'il ne lance rien, il te montre la marche à suivre pour ton navigateur (Chrome et Edge : icône dans la barre d'adresse ; Safari sur Mac : Fichier → Ajouter au Dock ; Firefox ne gère pas l'installation).

Après la première ouverture, elle fonctionne aussi sans connexion.

## 3. Où sont mes dessins ?

Tes œuvres et ton style sont enregistrés **sur l'appareil**, dans l'application. Chaque appareil a donc sa propre collection : ce que tu ajoutes sur le téléphone n'apparaît pas automatiquement sur l'ordinateur.

Pour les copier d'un appareil à l'autre, ou pour te protéger d'une perte :
- Ouvre **Style → Sauvegarde → Exporter** : un fichier `.json` est téléchargé.
- Sur l'autre appareil, **Style → Sauvegarde → Importer**, et choisis ce fichier.

Fais une sauvegarde de temps en temps. Vider les données du navigateur ou désinstaller l'application efface les œuvres de cet appareil.

## 4. Mettre à jour

Si le fichier `index.html` change, renvoie le dossier au même endroit. Dans `sw.js`, change `portfolio-ambre-v1` en `v2` pour forcer la mise à jour sur les appareils.

## 5. Nouveautés

**Page « À propos »** : bouton « À propos » en haut. Ajoute ta photo, ta bio, tes logiciels et ton e-mail (le bouton « Me contacter » ouvre ton mail). Les boutons de partage envoient l'adresse du portfolio, ou celle de la page À propos (`adresse/#apropos`).

**Modèles 3D** : dans « Ajouter une œuvre », choisis un fichier `.glb`, `.gltf` ou `.stl` (export SolidWorks ou CATIA possible en STL ou GLB). Sans image, l'aperçu est créé automatiquement. Dans la visionneuse, le bouton « Voir en 3D » permet de tourner la pièce au doigt et de zoomer en pinçant.

Les fichiers de la 3D sont intégrés à `index.html` : il n'y a rien d'autre à envoyer que les fichiers du dossier.

## 6. Outils 3D et carte QR

Dans la visionneuse, bouton « Voir en 3D », puis :
- **Éclater** (ou un toucher bref sur la pièce) : les pièces d'un assemblage s'écartent, puis se rassemblent. Un STL est découpé automatiquement en pièces quand ses volumes sont séparés.
- **Plan** : trois vues (face, côté, dessus) avec cotes et cartouche, en projection européenne. Le bouton d'unité (mm, cm, m) change l'unité des cotes ; « PNG » télécharge le plan.
- **Réalité augmentée** (iPhone, Safari) : pose la pièce à l'échelle réelle sur ton bureau. L'unité choisie dans « Plan » sert à régler l'échelle (un STL est en mm par défaut).

**Carte QR** : « À propos », puis « Carte QR ». Choisis le portfolio ou la page À propos, puis télécharge la carte de visite (85 × 54 mm, 300 dpi) ou le QR seul. Le QR pointe vers l'adresse où tu ouvres l'application : ouvre-la depuis l'adresse en ligne avant de le créer.

## 7. Musée et mockups

**Musée** : bouton « Galerie » en haut. Tu entres dans une salle d'exposition : tes dessins sont dans des cadres avec cartel, tes modèles 3D tournent sur des socles. Pour te déplacer :
- glisse le doigt pour regarder autour de toi ;
- maintiens ▲ pour avancer, ▼ pour reculer (ordinateur : flèches ou Z Q S D) ;
- touche une œuvre : tu t'en approches et tu la vois de face ; son titre apparaît en bas, « Ouvrir » la montre en grand ;
- ‹ et › font la visite œuvre par œuvre ;
- « Mouvement » (iPhone : accepte l'autorisation) : le téléphone devient ta tête, tu regardes en tournant sur toi-même ;
- « Pas » (essai) : marche pour avancer dans la salle. La position réelle dans ta pièce ne peut pas être suivie par un navigateur iPhone : la détection des pas est approximative.

**Mockup** : ouvre une pièce, puis « Créer un mockup ». Choisis une photo (mug, t-shirt, affiche…), puis place les 4 coins sur la zone à imprimer : le dessin suit la perspective. « Mug » enroule le dessin autour du cylindre, « Vêtement » reprend les plis et les ombres du tissu, « Affiche » pose l'image à plat. Les curseurs affinent l'enroulement, la courbe des bords, les plis, les ombres et l'opacité. « Fond blanc : retiré » enlève le blanc du dessin. « Enregistrer » exporte l'image (sur iPhone : menu de partage, puis « Enregistrer l'image »).

## 8. Rendu 3D : matières et éclairage

Dans la visionneuse 3D, touche « Rendu ». Choisis une **matière** (aluminium, acier poli, or, cuivre, plastique mat ou brillant avec la couleur de ton choix, bois, verre, caoutchouc) et un **éclairage** (studio, extérieur, soir). L'ombre au sol et le fond s'adaptent. « Fond transparent » exporte un PNG détouré. « Exporter l'image » enregistre un rendu en haute définition (sur iPhone : menu de partage, puis « Enregistrer l'image »).

Le bois est un motif calculé (il n'utilise pas de texture de ton modèle). La réalité augmentée utilise toujours les matières d'origine de la pièce.

## 9. Publier pour tes visiteurs (QR code et partage)

Tes œuvres sont enregistrées sur ton appareil. Une personne qui ouvre ton site (ou scanne ton QR code) ne les voit donc pas, tant que tu ne les as pas publiées.

1. Sur l'appareil où se trouvent tes œuvres, ouvre **Style → Sauvegarde → Publier le portfolio** (depuis Safari, pas depuis l'icône). Un fichier `portfolio-en-ligne-….zip` est créé : enregistre-le dans Fichiers.
2. **Décompresse** ce fichier. Tu obtiens des fichiers tous au même niveau : `index.html`, `sw.js`, `manifest.webmanifest`, `portfolio-data.json`, et un fichier `f-….png` (ou `.stl`, `.glb`) par œuvre. Il n'y a **aucun dossier à envoyer** : le dossier `icons` n'est utile que la toute première fois.
3. **GitHub** : dans ton dépôt, « Add file → Upload files », sélectionne **tous ces fichiers** (sans le dossier `icons`), puis « Commit changes ». Si un fichier du même nom existe déjà, il est remplacé.
   **Netlify** : glisse le dossier décompressé sur la page Deploys de ton site.
4. Attends 1 à 2 minutes, puis scanne ton QR code avec un autre téléphone.

Les visiteurs voient une version en lecture seule, sans boutons de modification. Chaque fois que tu ajoutes ou changes une œuvre, publie à nouveau et renvoie les fichiers. Sur un nouvel ordinateur, le bouton « Espace propriétaire » en bas de page permet d'importer ta sauvegarde pour modifier ton portfolio.

## 10. Mot de passe de l'espace propriétaire

- La première fois que tu entres dans l'espace propriétaire sur un appareil, l'application te demande de **choisir ton mot de passe** (4 caractères minimum, à saisir deux fois). Il n'y a aucun mot de passe par défaut.
- Ensuite, il est demandé à chaque ouverture de l'application, et quand tu appuies sur « Espace propriétaire » depuis le site visiteur. « Retour au site » ouvre la version visiteur.
- Pour le changer : bouton **Style**, section « Sauvegarde », « Changer le mot de passe ».
- Il est enregistré **sur l'appareil seulement**, sous forme brouillée. Chaque appareil a donc son propre mot de passe.
- Limite : le site est statique. Le mot de passe empêche d'ouvrir ton écran d'édition, mais ce que fait un visiteur reste sur son appareil et ne modifie jamais le site en ligne, qui ne change que lorsque tu renvoies les fichiers sur GitHub.
- **Oublié ?** Efface les données du site dans le navigateur (Safari : Réglages › Safari › Avancé › Données de sites web). Cela efface aussi les œuvres enregistrées sur cet appareil : récupère-les avec « Espace propriétaire » depuis le site publié, ou avec une sauvegarde exportée.
