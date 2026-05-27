# 🇲🇱 Diaspora Mali Connect

> La plateforme internationale des Maliens du monde entier.

**Site:** Déployez sur Vercel en 5 minutes

---

## ✨ Fonctionnalités

- 👥 **Membres** — Annuaire, profils, carte de membre numérique
- 🏛 **Associations** — Inscription, validation, pages dédiées
- 🗓 **Événements** — Création, inscription, billetterie
- 📰 **Actualités** — Fil d'info diaspora malienne mondiale
- 💬 **Messages** — Messagerie privée entre membres
- 💝 **Cagnottes** — Collectes de fonds solidaires
- 📸 **Médias** — Photos, vidéos, podcasts
- 🌙 **Dark mode** — Clair et sombre
- 🌍 **5 langues** — FR · EN · Bambara · ES · AR
- 📱 **PWA** — Installable sur Android, iPhone, PC
- 🔄 **Scroll infini** — Sur toutes les listes
- 🔐 **Admin** — Dashboard sécurisé

---

## 🚀 Déploiement

### 1. Créer un projet Firebase
- [console.firebase.google.com](https://console.firebase.google.com) → Nouveau projet
- Activer **Realtime Database** (Start in test mode)
- Activer **Authentication** → Email/Password

### 2. Configurer
Dans `index.html`, remplacez `window.FIREBASE_CONFIG` avec vos vraies clés.

### Règles Realtime Database
```json
{
  "rules": {
    ".read": "auth != null",
    ".write": "auth != null",
    "members": {".read": "true"},
    "associations": {".read": "true"},
    "news": {".read": "true"},
    "posts": {".read": "true"},
    "events": {".read": "true"}
  }
}
```

### 3. Pousser sur GitHub
Uploadez les 7 fichiers sur GitHub.

### 4. Déployer sur Vercel
Importez le repo → Deploy (aucun build requis).

---

## 📁 Structure

```
diaspora-mali-connect/
├── index.html          ← Application complète
├── firebase-config.json← Config Firebase (référence)
├── manifest.json       ← PWA
├── sw.js               ← Service Worker
├── vercel.json         ← Déploiement
├── README.md
└── .gitignore
```

---

*Made with ❤️ for the Malian Diaspora — 🌍 Worldwide*
