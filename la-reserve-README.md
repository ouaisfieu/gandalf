# 🔵 La Réserve

> **Ce qui existe déjà mais n'a jamais été reconnu.**

La Réserve est un système ARG (Alternate Reality Game) permettant de créer des **actions de détournement institutionnel**. Chaque action génère une page web autonome publiable n'importe où.

[![Version](https://img.shields.io/badge/version-1.0-blue.svg)]()
[![License](https://img.shields.io/badge/license-CC%20BY--SA%204.0-green.svg)]()
[![PWA Ready](https://img.shields.io/badge/PWA-ready-purple.svg)]()

---

## 📦 Structure du projet

```
la-reserve/
├── hub.html              ← 🏠 Page d'accueil / Hub
├── la-reserve-v10.html   ← 💻 Version Desktop complète
├── la-reserve-app.html   ← 📱 Version Mobile PWA
├── manifest.json         ← ⚙️ Manifest PWA
├── sw.js                 ← 🔄 Service Worker
├── offline.html          ← 📴 Page hors ligne
└── README.md             ← 📖 Documentation
```

---

## 🚀 Démarrage rapide

### Option 1 : Ouvrir directement
```bash
# Téléchargez les fichiers et ouvrez dans un navigateur
open hub.html
```

### Option 2 : Serveur local
```bash
# Python
python -m http.server 8000

# Node.js
npx serve .

# Puis visitez http://localhost:8000
```

### Option 3 : Déploiement
```bash
# Uploadez les fichiers sur :
# - GitHub Pages
# - Netlify
# - Vercel
# - N'importe quel hébergeur statique
```

---

## 💻 Version Desktop

Interface complète avec toutes les fonctionnalités avancées.

### Fonctionnalités

| Fonctionnalité | Description |
|----------------|-------------|
| 📝 Éditeur Markdown | Barre d'outils, raccourcis clavier, aperçu |
| 👥 Recrues | 4 types : réelle, fictive, moi-même, fonction |
| 📅 Timeline | 8 types d'événements avec badges colorés |
| 🎨 6 Thèmes | Clair, Sombre, Disco, Néon, Retro, Console |
| ✒️ 6 Typographies | Élégant, Organique, Editorial, Littéraire, Poétique, Brut |
| 📁 Gestionnaire fichiers | Import/Export/Prévisualisation multi-format |
| 💡 Templates | 5 modèles de démarrage |
| 📖 README intégré | Documentation accessible dans l'app |

### Thèmes disponibles

| Thème | Ambiance |
|-------|----------|
| ☀️ Clair | Lumineux et aéré |
| 🌙 Sombre | Mode nuit élégant |
| 🪩 Disco | Couleurs vives et festives |
| 💜 Néon | Cyberpunk néon |
| 👾 Retro | Pixel art 8-bit |
| 💻 Console | Terminal hacker |

---

## 📱 Version Mobile (PWA)

Application installable fonctionnant hors ligne.

### Installation

**iOS (Safari) :**
1. Ouvrir `la-reserve-app.html`
2. Partager (📤) → "Sur l'écran d'accueil"

**Android (Chrome) :**
1. Ouvrir `la-reserve-app.html`
2. Menu (⋮) → "Ajouter à l'écran d'accueil"

### Fonctionnalités mobile

- 🎨 Interface native avec navigation par onglets
- 📴 Mode hors ligne (Service Worker)
- 💾 Sauvegarde automatique (LocalStorage)
- 📤 Partage natif (Web Share API)
- 📱 Génération QR Code
- 🌓 Thème clair/sombre

---

## 📁 Formats supportés

### Import

| Format | Extension | Usage |
|--------|-----------|-------|
| JSON | `.json` | Données complètes |
| Markdown | `.md` | Description avec frontmatter |
| YAML | `.yaml` `.yml` | Configuration |
| CSV | `.csv` | Timeline ou recrues |
| TXT | `.txt` | Description simple |
| HTML | `.html` | Réimporter une page |

### Export

| Format | Extension | Usage |
|--------|-----------|-------|
| HTML | `.html` | Page web autonome |
| JSON | `.json` | Backup / Import |
| Markdown | `.md` | Documentation |
| YAML | `.yaml` | Configuration |
| CSV | `.csv` | Tableur |
| TXT | `.txt` | Texte brut |
| PDF | `.pdf` | Impression |
| PNG | `.png` | Capture (via navigateur) |

### Exemples de formats

<details>
<summary>📦 JSON</summary>

```json
{
  "id": "LR-ABC123DEF",
  "titre": "Coordinateur·rice de silences",
  "pseudo": "Anonyme",
  "lieu": "Bruxelles",
  "type": "silence",
  "statut": "en-cours",
  "description": "# Mon action\n\nDescription en **Markdown**...",
  "recrues": [
    { "nom": "Jean", "type": "fictive", "role": "Complice" }
  ],
  "timeline": [
    { "date": "2025-01-15", "type": "creation", "description": "Début" }
  ],
  "theme": "clair",
  "style": "elegant",
  "createdAt": "2025-01-15T10:30:00.000Z"
}
```
</details>

<details>
<summary>📝 Markdown avec frontmatter</summary>

```markdown
---
title: "Mon action"
pseudo: "Anonyme"
type: silence
statut: en-cours
---

# Mon action

Description de l'action en **Markdown**...
```
</details>

<details>
<summary>📊 CSV (Timeline)</summary>

```csv
date,type,description
"2025-01-15","creation","Création du projet"
"2025-01-20","soumission","Envoi à l'ASBL"
"2025-02-01","silence","Aucune réponse"
```
</details>

<details>
<summary>⚙️ YAML</summary>

```yaml
id: LR-ABC123DEF
titre: "Mon action"
pseudo: "Anonyme"
type: silence

recrues:
  - nom: "Jean"
    type: fictive
    role: "Complice"

timeline:
  - date: 2025-01-15
    type: creation
```
</details>

---

## 🔧 Fonctionnalités techniques

### PWA (Progressive Web App)

- **Service Worker** : Cache offline, sync en arrière-plan
- **Manifest** : Icônes, splash screen, raccourcis
- **Installable** : Comportement natif sur mobile

### Stockage

- **LocalStorage** : Brouillons et préférences
- **Aucun serveur** : 100% local, données privées

### Accessibilité

- Contraste suffisant (WCAG)
- Navigation clavier
- Labels ARIA
- Responsive (mobile-first pour l'app)

---

## 📖 Guide d'utilisation

### Créer une action

1. **Ouvrir** la version Desktop ou Mobile
2. **Choisir** un template (optionnel)
3. **Remplir** les informations de base
4. **Rédiger** la description en Markdown
5. **Ajouter** des recrues et événements
6. **Prévisualiser** le résultat
7. **Exporter** en HTML

### Raccourcis clavier (Desktop)

| Raccourci | Action |
|-----------|--------|
| `Ctrl+B` | Gras |
| `Ctrl+I` | Italique |
| `Ctrl+S` | Sauvegarder |
| `Tab` | Indenter |

### Types de recrues

| Type | Icône | Description |
|------|-------|-------------|
| Réelle | 👤 | Personne existante |
| Fictive | 🎭 | Personnage inventé |
| Moi-même | 🪞 | Vous sous un autre rôle |
| Fonction | 💼 | Rôle abstrait |

### Types d'événements

| Type | Icône | Usage |
|------|-------|-------|
| Création | 🚀 | Début de l'action |
| Soumission | 📨 | Envoi d'un document |
| Réponse | 📬 | Réception d'une réponse |
| Silence | 🔇 | Absence de réponse |
| Validation | ✅ | Acceptation |
| Refus | ❌ | Rejet |
| Basculement | 🌟 | Passage dans le réel |
| Autre | 📝 | Événement divers |

---

## 🌐 Publication

### GitHub Pages (gratuit)

```bash
# 1. Créer un dépôt GitHub
# 2. Uploader les fichiers
# 3. Settings → Pages → Source: main
# 4. URL: https://username.github.io/repo/
```

### Netlify / Vercel

```bash
# Glisser-déposer le dossier sur netlify.com ou vercel.com
# Déploiement automatique
```

### IPFS (décentralisé)

```bash
ipfs add -r la-reserve/
# Accès via gateway IPFS
```

---

## 🗺️ Roadmap / Évolutions futures

### 🔜 Court terme (v1.1)

- [ ] **Synchronisation cloud** optionnelle (Firebase/Supabase)
- [ ] **Galerie publique** d'actions partagées
- [ ] **Mode collaboratif** (partage de brouillons)
- [ ] **Notifications push** (rappels timeline)
- [ ] **Export image** (canvas/html2canvas)
- [ ] **Mode impression** optimisé

### 🔮 Moyen terme (v2.0)

- [ ] **API REST** pour intégrations tierces
- [ ] **Plugins système** (extensions utilisateur)
- [ ] **Thèmes custom** (éditeur de thèmes)
- [ ] **Médias embarqués** (images base64 dans HTML)
- [ ] **Signature cryptographique** (preuve d'authenticité)
- [ ] **Historique/versioning** des actions
- [ ] **Mode présentation** (diaporama timeline)

### 🚀 Long terme (v3.0)

- [ ] **Fédération** (réseau décentralisé ActivityPub)
- [ ] **NFT/blockchain** (certification immuable)
- [ ] **IA assistante** (aide à la rédaction)
- [ ] **Cartographie** (visualisation géographique)
- [ ] **Analyse de sentiments** (impact mesurable)
- [ ] **Application native** (Electron/Tauri)
- [ ] **Extensions navigateur** (capture rapide)

### 💡 Idées communautaires

- **Système de badges** (gamification)
- **Templates communautaires** (partage de modèles)
- **Mode "campagne"** (plusieurs actions liées)
- **Intégration réseaux sociaux** (auto-publication)
- **Webhooks** (notifications externes)
- **Statistiques** (dashboard d'impact)
- **Export vidéo** (animation de la timeline)
- **Mode anonyme renforcé** (Tor, encryption)

---

## 🤝 Contribuer

Le projet est ouvert aux contributions :

1. **Fork** le dépôt
2. **Créer** une branche (`git checkout -b feature/ma-feature`)
3. **Commiter** (`git commit -m 'Add ma feature'`)
4. **Pusher** (`git push origin feature/ma-feature`)
5. **Pull Request**

### Guidelines

- Code commenté en français
- CSS mobile-first
- Pas de dépendances externes (sauf polices)
- Tests sur Chrome, Firefox, Safari

---

## 📄 Licence

**CC BY-SA 4.0** (Creative Commons Attribution-ShareAlike)

Vous pouvez :
- ✅ Partager et adapter librement
- ✅ Usage commercial autorisé
- ⚠️ Attribution requise
- ⚠️ Partage sous même licence

---

## 🙏 Crédits

- **Polices** : Google Fonts (Inter, Space Grotesk, Playfair Display, etc.)
- **Icônes** : Emojis natifs
- **Inspiration** : ARG, net.art, détournement situationniste

---

## 📞 Contact

Pour questions, suggestions ou contributions :
- **Issues GitHub** : Signaler un bug ou proposer une feature
- **Discussions** : Échanger avec la communauté

---

<p align="center">
  <strong>La Réserve</strong><br>
  <em>Ce qui existe déjà mais n'a jamais été reconnu.</em><br>
  <br>
  Système ouvert depuis 2025
</p>
