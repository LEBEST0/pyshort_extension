# PyShort — Raccourcisseur d'URLs

## 📋 Description

**PyShort** est une extension de navigateur qui permet de raccourcir rapidement les URLs directement depuis votre navigateur Chrome. En un simple clic droit, transformez vos liens longs et complexes en URLs courtes et partageables.

## ✨ Fonctionnalités

- **Raccourcir un lien** : Clic droit sur n'importe quel lien pour le raccourcir
- **Raccourcir la page actuelle** : Clic droit sur la page pour raccourcir l'URL de la page courante
- **Copie automatique** : Les URLs raccourcies s'affichent dans un toast intégré à la page
- **Notification de succès** : Confirmation visuelle lors du raccourcissement réussi
- **Configuration personnalisée** : Possibilité de spécifier un serveur API personnalisé

## 🚀 Installation

### Depuis le code source

1. Clonez ce repository :
   ```bash
   git clone https://github.com/LEBEST0/pyshort_extension.git
   ```

2. Ouvrez Chrome et accédez à `chrome://extensions/`

3. Activez le **Mode de développement** (coin supérieur droit)

4. Cliquez sur **Charger l'extension non empaquetée** et sélectionnez le dossier du projet

## 📂 Structure du projet

```
pyshort_extension/
├── manifest.json      # Configuration de l'extension
├── background.js      # Service worker (gestion des clics et requêtes API)
├── popup.html         # Interface du popup
├── popup.js          # Logique du popup
├── icons/            # Icônes de l'extension
│   ├── icon16.png
│   ├── icon48.png
│   └── icon128.png
└── README.md         # Documentation
```

## 🛠️ Configuration

### Serveur API personnalisé

Par défaut, l'extension utilise le serveur :
```
https://url-short-1-vaqx.onrender.com
```

Pour utiliser un serveur API différent, vous pouvez le configurer dans le popup de l'extension.

### Permissions requises

L'extension utilise les permissions suivantes :
- `activeTab` : Accès à l'onglet actif
- `contextMenus` : Ajout d'options au menu contextuel
- `storage` : Stockage des préférences
- `clipboardWrite` : Écriture dans le presse-papiers
- `clipboardRead` : Lecture du presse-papiers
- `notifications` : Affichage des notifications
- `scripting` : Injection de scripts dans les pages web

## 📖 Utilisation

1. **Raccourcir un lien** :
   - Clic droit sur un lien
   - Sélectionnez "🔗 Raccourcir ce lien"
   - L'URL raccourcie s'affiche dans un toast

2. **Raccourcir la page courante** :
   - Clic droit sur la page (pas sur un lien)
   - Sélectionnez "🔗 Raccourcir cette page"
   - L'URL raccourcie s'affiche dans un toast

3. **Copier l'URL** :
   - Cliquez sur le bouton "Copier" dans le toast
   - L'URL courte est copiée dans votre presse-papiers

## 🧩 Compatibilité
 
| Navigateur | Statut |
|---|---|
| Google Chrome | ✅ Supporté |
| Microsoft Edge | ✅ Supporté |
| Mozilla Firefox | ⚙️ Supporté avec adaptation mineure |
| Safari | ❌ Non testé |

 L'adaption pour Mozilla Firefox consiste à remplacer chrome. par browser. dans les fichiers JS. 
---
## 🔧 Architecture

### background.js
- Gestion du menu contextuel Chrome
- Communication avec l'API de raccourcissement
- Injection du toast dans les pages web

### popup.html / popup.js
- Interface de configuration
- Gestion des paramètres utilisateur
- Affichage des statistiques

## ⚙️ Technologies

- **JavaScript** 
- **HTML** 
- **Chrome Extension**

## 🐛 Dépannage

**"Serveur inaccessible"**
- Vérifiez que l'API est accessible
- Assurez-vous d'avoir une connexion Internet
- Vérifiez l'URL du serveur configuré

**Toast n'apparaît pas**
- Vous êtes peut-être sur une page protégée (ex: `chrome://`)
- Une notification système s'affichera à la place

## 📝 Licence

Ce projet est ouvert à tous. Consultez le fichier LICENSE pour plus de détails.

## 👤 Auteur

Développé par [LEBEST0](https://github.com/LEBEST0)

## 🤝 Contribution

Les contributions sont bienvenues ! N'hésitez pas à :
- Signaler des bugs
- Proposer des améliorations
- Créer des pull requests

---

**Dernière mise à jour** : Mars 2026
