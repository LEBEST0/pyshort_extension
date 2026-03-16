🚀 Installation
Depuis le Chrome Web Store

Bientôt disponible

En mode développeur (installation manuelle)

1- Téléchargez ou clonez ce dépôt
https://github.com/LEBEST0/pyshort_extension.git

2- Ouvrez Chrome et allez sur chrome://extensions/

3- Activez le Mode développeur ( en haut à droite)

4- Cliquez sur "Charger l'extension non empaquetée"

5- Sélectionnez le dossier extension/ du projet

L'icône PyShort apparaît dans votre barre d'outils 🚀


📁 Structure des fichiers

extension/
├── manifest.json       # Configuration et permissions
├── popup.html          # Interface du bouton (2 onglets)
├── popup.js            # Logique du popup
├── background.js       # Service worker (clic droit + toast)
└── icons/
    ├── icon16.png
    ├── icon48.png
    └── icon128.png


🔗 Projets liés
Projet            Description
PyShort-cli       Interface ligne de commande — pip install pyshort-cli 
PyShort           BackendAPI REST FastAPI déployée sur Render


📄 Licence
Ce projet est sous licence MIT — vous êtes libre de l'utiliser, le modifier et le distribuer.
