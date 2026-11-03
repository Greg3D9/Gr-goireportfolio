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

## 11. Frise chronologique (aperçu 3D et réalité augmentée)

- Dans « À propos », le bouton **Frise chronologique** ouvre ton parcours en 3D : glisse avec le doigt ou utilise ‹ › pour passer d'une étape à l'autre.
- Sur iPhone et iPad (Safari), le bouton **Voir en réalité augmentée** pose la frise dans la pièce (environ 4 m de long, 1 m de haut) : marche le long, téléphone en main. Tu peux la réduire en pinçant.
- Pour changer les étapes : « À propos », « Modifier », rubrique « Frise chronologique » (8 étapes au maximum). Republie ensuite le portfolio pour que les visiteurs voient les changements.

## 12. Musique et petits sons

- La musique se lance à l'entrée dans l'espace propriétaire (sur iPhone, au premier toucher si tu étais déjà connecté).
- Dans la barre du bas : le bouton **♪ Musique** active ou coupe la musique.
- Les petits sons d'interface (un tic à chaque appui sur un bouton, une image ou un filtre) jouent quand la musique est **coupée** et se taisent quand elle joue.

## 13. Ouverture d'une œuvre

Quand tu touches une carte, l'image s'agrandit depuis sa place jusqu'à l'écran (environ une demi-seconde). Si ton iPhone est réglé sur « Réduire les animations », l'œuvre s'ouvre directement, sans mouvement.

## 14. Effet de relief

Quand tu penches ton iPhone, les images de la galerie bougent très légèrement. Au premier appui dans l'application, l'iPhone te demande l'autorisation d'utiliser les capteurs de mouvement : réponds « Autoriser ». Si tu refuses, l'effet reste coupé et l'application ne redemande pas. Pour le réactiver, ferme complètement l'application, puis dans Réglages > Safari > Avancé > Accès au mouvement et à l'orientation, vérifie que c'est activé.

## 15. Frise chronologique : nouveau look

Chaque étape est une carte sombre avec la période en grand, un numéro en filigrane, le titre, des pastilles pour les détails (lycée, ville, diplôme) et des points de progression. Dans la 3D et en réalité augmentée, les cartes sont encadrées et posées sur un socle, avec une bille sur le rail pour chaque étape. Pour avoir de jolies pastilles, sépare les détails par « · » dans le champ de détail de chaque étape.

## 16. Recadrer et retoucher les images

Quand tu ajoutes une photo (œuvre ou photo de profil dans « À propos »), un écran de retouche s'ouvre :
- **Recadrer** : tire les coins blancs, ou déplace le cadre avec le doigt. Choisis « Libre », « Original », 1:1, 4:5 ou 3:2. Pour la photo de profil, le format est fixé à 4:5.
- **Tourner** : boutons ↺ et ↻ (90°).
- **Redresser** : curseur de -15° à +15°, pratique pour un croquis photographié de travers. Les coins vides restent blancs, recadre pour les enlever.
- **Luminosité et contraste** : deux curseurs.
Pour plusieurs images d'un coup, l'écran s'ouvre pour chacune. « Garder tel quel » ajoute l'image sans la changer. Le bouton « Recadrer / retoucher l'image » du formulaire permet de recommencer. Les images GIF et SVG ne sont pas retouchées, pour ne pas perdre l'animation ou la qualité vectorielle.

## 17. Diaporama de veille (style fond d'écran)

Quand tu es connecté à ton espace propriétaire, tes œuvres s'affichent en plein écran après un moment sans toucher l'écran (1 minute par défaut). Un appui ou une touche n'importe où l'arrête. Dans la barre du bas, deux boutons :
- **▶ Diaporama** le lance tout de suite.
- **Veille : 1 min** change le délai (30 s, 1 min, 2 min, 5 min, ou non pour le couper).

Le style est celui d'un fond d'écran de designer : une mosaïque sans marges, avec des cases de tailles différentes, un grain fin et une légère vignette. Les œuvres se remplacent une à une en fondu lent, avec un zoom très doux. Toutes les 10 à 14 secondes, une œuvre s'agrandit au centre avec son numéro, son titre, sa catégorie et son année, puis retourne à sa place. En bas : « Grégoire · Portfolio » à gauche et l'heure à droite.

Le diaporama ne démarre pas pendant que tu remplis un formulaire ou que tu modifies ta page « À propos ». Il garde l'écran allumé s'il le peut (iPhone récent et iPad). Les visiteurs de ton site public ne le voient pas démarrer tout seul. Si tu as peu d'œuvres, il y a moins de cases, pour éviter les doublons.

## 18. Carte des œuvres

Dans le formulaire d'une œuvre, le champ « Lieu (facultatif) » te laisse écrire le nom du lieu et poser une épingle :
- **Placer sur la carte** ouvre une carte : touche pour poser l'épingle, cherche une adresse, ou appuie sur « Ma position ». Valide avec « Valider ce lieu ».
- Si ta photo contient sa position GPS, l'épingle est posée toute seule (vérifie-la). Sur iPhone, au moment de choisir la photo, touche « Options » et garde « Position » activée.
- Quand tu ajoutes plusieurs images d'un coup, elles reçoivent le même lieu.
Dès qu'une œuvre a une épingle, un bouton **Carte** apparaît en haut : une épingle ronde (avec la photo de l'œuvre) par lieu. Un appui ouvre la liste des œuvres de ce lieu. La fiche d'une œuvre affiche son lieu et un bouton « Voir sur la carte ». Le fond de carte (OpenStreetMap) a besoin d'une connexion. Hors connexion, les épingles restent visibles sur un fond gris.
Pense à republier ton portfolio (bouton « Publier le portfolio ») pour que tes visiteurs voient la carte.

## 19. Effet au défilement

Dans la galerie, les cartes situées plus bas arrivent en glissant quand tu fais défiler, et les images bougent très légèrement dans leur cadre. Si ton iPhone est réglé sur « Réduire les animations », l'effet est coupé.

## 20. Si la page d'accueil reste noire sur un ordinateur

Sur certains PC Windows, les animations sont désactivées (Réglages > Accessibilité > Effets visuels > Effets d'animation). L'application respecte ce réglage : depuis la version 54, la page d'accueil s'affiche alors directement en entier, sans animation, avec le bouton « Entrer ». Si une animation ne démarre pas pour une autre raison, l'accueil s'affiche aussi tout seul après 3 secondes.

## 21. Orientation des pièces 3D

Les fichiers SolidWorks ou CATIA n'ont pas toujours le même « haut » que l'iPhone, et la pièce peut se retrouver couchée en réalité augmentée. Dans la visionneuse 3D de ton espace propriétaire, le bouton **Orientation** ouvre un panneau :
- **Poser sur la base (auto)** cherche la plus grande face plane de la pièce et la met en bas.
- **Basculer ↻ avant**, **Basculer ↻ côté** et **Pivoter ↻** tournent la pièce d'un quart de tour dans chaque sens, pour régler à la main.
- **Origine** annule les changements.
- **Enregistrer** retient l'orientation pour cette pièce, pour l'aperçu et pour la réalité augmentée. Pense à republier le portfolio pour que tes visiteurs la voient aussi.
Le bouton « Réalité augmentée » utilise toujours l'orientation affichée à l'écran, même avant d'enregistrer : tu peux donc essayer avant de valider.

## 22. Cartes à collectionner et booster

Un bouton **Booster** (violet et rose) est dans la barre du haut, à côté de « Galerie » et « À propos ». Un appui ouvre un paquet de 5 cartes, tirées parmi tes œuvres. Le visiteur retourne les cartes une par une.

Cinq raretés, de la plus courante à la plus rare : Neutre, Normal, Rare, Ultra rare, Légende. L'étiquette est en haut à droite de l'image de la carte, et l'effet holographique brillant est plus fort pour les raretés élevées (il bouge quand on penche le téléphone ou qu'on glisse le doigt).

- **Collection** : le classeur du visiteur. Les cartes trouvées s'affichent, les autres sont des cases avec un « ? ». Il reste sur l'appareil du visiteur.
- **Voir la carte** : bouton sur la fiche de chaque œuvre. On peut enregistrer la carte en image.
- **Pour toi** : dans le formulaire d'une œuvre, choisis la rareté et les trois stats (précision, créativité, difficulté). Sans choix, une rareté est attribuée automatiquement et reste la même. Republie ton portfolio pour que les visiteurs voient tes choix.

## 23. Échange de cartes par QR code

Deux amis peuvent s'échanger une carte, sans serveur. La carte donnée disparaît de la collection du donneur et apparaît chez l'autre.

1. **Le donneur** ouvre « Booster », puis « Collection », touche une de ses cartes et appuie sur **Donner cette carte**. Un QR code s'affiche (valable 15 minutes).
2. **L'ami** le scanne avec l'**appareil photo** de son téléphone : l'application s'ouvre et lui montre la carte. Il appuie sur **Accepter** : la carte entre dans sa collection.
3. Son téléphone affiche alors un **QR de confirmation**. Le donneur le scanne à son tour.
4. C'est seulement à ce moment-là que la carte quitte la collection du donneur.

Sans appareil photo, le bouton « Partager le lien » envoie le même code par message, et « Recevoir » (dans la Collection) ou « J'ai un code » permet de coller un lien reçu.

Limites à connaître :
- Chaque code ne marche qu'une fois par appareil et expire au bout de 15 minutes. Comme il n'y a pas de serveur, rien n'empêche techniquement quelqu'un de bidouiller son propre téléphone. Pour un jeu entre amis, c'est suffisant.
- Les collections restent dans le navigateur de chaque téléphone. Le donneur doit scanner la confirmation dans la **même application** que celle où il a créé l'offre (même téléphone, même navigateur ; l'application installée sur l'écran d'accueil et Safari ont des collections séparées).
- Si l'ami possède déjà la carte, il peut l'accepter : elle ne sera pas en double, mais elle aura quitté la collection du donneur.

## 24. Succès à débloquer

Dans la Collection, le bouton **Succès** ouvre la liste des 5 badges. Un badge gagné devient une médaille dorée ; les autres sont grisés avec un cadenas. Au moment où un badge est débloqué, une annonce brillante « Succès débloqué ! » descend du haut de l'écran.

- **Premier booster** : ouvrir son premier paquet et retourner une carte.
- **Chasseur de Légende** : obtenir une carte de rareté Légende.
- **Échangeur** : réussir un échange de carte (en donnant ou en recevant).
- **Collectionneur** : posséder la moitié des cartes du portfolio.
- **Collection complète** : posséder toutes les cartes (à partir de 3 œuvres).

Les succès sont enregistrés sur l'appareil du visiteur, comme sa collection. Si tu ajoutes des œuvres, « Collectionneur » et « Collection complète » se recalculent : un badge déjà gagné reste gagné.
