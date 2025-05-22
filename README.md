# 📋 Guide de Génération du Code de Départ - Budget Tracker MERN

> **Script de génération pour laboratoire pratique MERN**  
> Dr. El Hadji Bassirou TOURE - DMI/FST/UCAD  
> Département de Mathématiques et Informatique - FST/UCAD

## 🎯 Objectif du Script

Ce script `generate-starter-code.sh` génère automatiquement **tous les fichiers de base** avec des **TODOs à compléter** selon le lab PDF. Il ne lance pas l'application, mais crée le code de départ pour que les étudiants puissent suivre le laboratoire.

## 📋 Prérequis

### 🖥️ Logiciels requis

- **Bash** (Linux/macOS/WSL)
- **Git** (pour cloner le repository)
- **Éditeur de code** (VS Code recommandé)

### ✅ Vérification des prérequis

```bash
# Vérifier Bash
bash --version
# Doit afficher version 4.0+ ou plus

# Vérifier Git
git --version
# Doit afficher version 2.0+ ou plus
```

## 🏁 Génération du Code de Départ

### 1. Cloner le repository vide

```bash
# Cloner le repository (contient seulement les scripts)
git clone https://github.com/elbachir67/mern-budget-tracker-starter.git
cd mern-budget-tracker-starter
```

### 2. Générer le code de départ

```bash
# Rendre le script exécutable
chmod +x generate-starter-code.sh

# Générer tous les fichiers avec TODOs
./generate-starter-code.sh
```

### 3. Vérifier la génération

```bash
# Voir la structure générée
tree -I node_modules
# ou
find . -name "*.js" -o -name "*.json" | head -20
```

## 🔧 Ce que fait le script `generate-starter-code.sh`

### Phase 1 : Structure du Projet

- 📁 Crée la structure complète du projet MERN
- 📂 Organise les dossiers backend/frontend avec sous-dossiers
- 📝 Génère tous les fichiers nécessaires au développement

### Phase 2 : Backend avec TODOs

- 🔧 Génère `server.js` avec **TODO-SERVER-1**
- 🗄️ Crée `config/database.js` avec **TODO-DB-1**
- 👤 Génère les modèles avec **TODO-MODEL-1,2,3**
- 🔐 Crée l'authentification avec **TODO-AUTH-1,2**
- 📊 Génère les contrôleurs avec **TODO-CRUD-1, TODO-STATS-1**
- 🛣️ Crée les routes avec **TODO-ROUTES-1**

### Phase 3 : Frontend avec TODOs

- ⚛️ Génère `App.js` avec **TODO-ROUTER-1**
- 🔄 Crée le Context avec **TODO-CONTEXT-1**
- 🧩 Génère les composants avec **TODO-COMPONENT-1, TODO-FORM-1**
- 🎨 Configure Material-UI et styles de base

### Phase 4 : Configuration

- 🐳 Génère les Dockerfiles et docker-compose.yml
- ⚙️ Crée les package.json avec toutes les dépendances
- 🔧 Configure les variables d'environnement (.env)
- 📚 Génère README-TODOS.md avec guide complet

## 📂 Structure du Projet Générée

```
mern-budget-tracker-starter/
├── backend/                          # 🔧 API Node.js/Express
│   ├── config/
│   │   └── database.js              # TODO-DB-1: Connexion MongoDB
│   ├── controllers/
│   │   ├── categoryController.js    # TODO-CRUD-1: API catégories
│   │   └── statsController.js       # TODO-STATS-1: Agrégation MongoDB
│   ├── middleware/
│   │   └── auth.js                  # TODO-AUTH-2: Middleware JWT
│   ├── models/
│   │   ├── User.js                  # TODO-MODEL-1: Modèle utilisateur
│   │   ├── Category.js              # TODO-MODEL-2: Modèle catégorie
│   │   └── Transaction.js           # TODO-MODEL-3: Modèle transaction
│   ├── routes/
│   │   └── categories.js            # TODO-ROUTES-1: Routes REST
│   ├── utils/
│   │   └── generateToken.js         # TODO-AUTH-1: Génération JWT
│   ├── server.js                    # TODO-SERVER-1: Serveur Express
│   ├── package.json                 # Dépendances backend
│   ├── .env                         # Variables d'environnement
│   └── Dockerfile                   # Configuration Docker backend
├── frontend/                        # ⚛️ Application React
│   ├── public/
│   │   └── index.html              # Page HTML de base
│   ├── src/
│   │   ├── components/
│   │   │   ├── auth/
│   │   │   │   └── Login.js        # TODO-FORM-1: Formulaire connexion
│   │   │   ├── categories/         # (à créer selon lab)
│   │   │   ├── dashboard/          # (à créer selon lab)
│   │   │   ├── transactions/       # (à créer selon lab)
│   │   │   └── Navbar.js           # TODO-COMPONENT-1: Navigation
│   │   ├── contexts/
│   │   │   └── AuthContext.js      # TODO-CONTEXT-1: État global auth
│   │   ├── hooks/                  # (à créer selon lab)
│   │   ├── utils/                  # (à créer selon lab)
│   │   ├── App.js                  # TODO-ROUTER-1: Routage principal
│   │   ├── App.css                 # Styles de base
│   │   ├── index.js                # Point d'entrée React
│   │   └── index.css               # Styles globaux
│   ├── package.json                # Dépendances frontend
│   └── Dockerfile                  # Configuration Docker frontend
├── docker-compose.yml              # 🐳 Orchestration des services
├── README-TODOS.md                 # 📚 Guide des TODOs à compléter
├── generate-starter-code.sh        # 🔧 Ce script de génération
└── START.md                        # 📖 Ce guide
```

## 🎯 TODOs Générés - Vue d'Ensemble

Le script génère **14 TODOs principaux** répartis en 4 parties :

### 🏗️ PARTIE 1: Backend Fondamental (5 TODOs)

- `TODO-SERVER-1` → Configuration serveur Express
- `TODO-DB-1` → Connexion MongoDB avec Mongoose
- `TODO-MODEL-1` → Modèle User avec sécurité bcrypt
- `TODO-AUTH-1` → Génération tokens JWT
- `TODO-AUTH-2` → Middleware protection routes

### 📊 PARTIE 2: API REST et Données (5 TODOs)

- `TODO-MODEL-2` → Modèle Category (Transport, Alimentation...)
- `TODO-MODEL-3` → Modèle Transaction (montants FCFA)
- `TODO-CRUD-1` → API CRUD complète des catégories
- `TODO-ROUTES-1` → Configuration routes REST
- `TODO-STATS-1` → Statistiques avec agrégation MongoDB

### ⚛️ PARTIE 3: Frontend React (4 TODOs)

- `TODO-CONTEXT-1` → Context authentification global
- `TODO-COMPONENT-1` → Composant Navbar Material-UI
- `TODO-FORM-1` → Formulaire connexion avec validation
- `TODO-ROUTER-1` → Routage et navigation protégée

## 📚 Correspondance avec le Lab PDF

Chaque TODO généré correspond **exactement** à une section du lab PDF :

| TODO Généré        | Section Lab PDF                                       | Page | Durée estimée |
| ------------------ | ----------------------------------------------------- | ---- | ------------- |
| `TODO-SERVER-1`    | "TODO-SERVER-1 : Création du serveur Express de base" | p.15 | 10 min        |
| `TODO-DB-1`        | "TODO-DB-1 : Connexion à MongoDB"                     | p.18 | 8 min         |
| `TODO-MODEL-1`     | "TODO-MODEL-1 : Modèle User sécurisé"                 | p.20 | 12 min        |
| `TODO-AUTH-1`      | "TODO-AUTH-1 : Génération de tokens JWT"              | p.24 | 6 min         |
| `TODO-AUTH-2`      | "TODO-AUTH-2 : Middleware d'authentification"         | p.26 | 10 min        |
| `TODO-MODEL-2`     | "TODO-MODEL-2 : Modèle Category"                      | p.30 | 8 min         |
| `TODO-MODEL-3`     | "TODO-MODEL-3 : Modèle Transaction"                   | p.32 | 10 min        |
| `TODO-CRUD-1`      | "TODO-CRUD-1 : API complète des catégories"           | p.35 | 15 min        |
| `TODO-ROUTES-1`    | "TODO-ROUTES-1 : Routes des catégories"               | p.40 | 8 min         |
| `TODO-STATS-1`     | "TODO-STATS-1 : Statistiques avec agrégation"         | p.42 | 12 min        |
| `TODO-CONTEXT-1`   | "TODO-CONTEXT-1 : Configuration authentification"     | p.48 | 15 min        |
| `TODO-COMPONENT-1` | "TODO-COMPONENT-1 : Premier composant React"          | p.52 | 10 min        |
| `TODO-FORM-1`      | "TODO-FORM-1 : Formulaire de connexion"               | p.55 | 12 min        |
| `TODO-ROUTER-1`    | "TODO-ROUTER-1 : Configuration du routage"            | p.58 | 15 min        |

**Total estimé : ~2h30 de développement guidé**

## 🚀 Développement Guidé

### 📖 Méthodologie d'Apprentissage

1. **📚 Consultez le lab PDF** - Chaque TODO renvoie à une section précise
2. **🔍 Trouvez le fichier** correspondant dans la structure générée
3. **📋 Lisez l'objectif** et les instructions dans les commentaires
4. **📝 Copiez le code** depuis le lab PDF vers le fichier
5. **✅ Testez** immédiatement après chaque TODO
6. **➡️ Passez au suivant** une fois validé

### 🏃‍♂️ Développement Rapide (Ordre Recommandé)

#### Phase 1: Backend Core (45 min)

```bash
# 1. Serveur Express de base
code backend/server.js        # TODO-SERVER-1 (10 min)

# 2. Base de données
code backend/config/database.js    # TODO-DB-1 (8 min)

# 3. Modèle utilisateur sécurisé
code backend/models/User.js        # TODO-MODEL-1 (12 min)

# 4. Authentification JWT
code backend/utils/generateToken.js # TODO-AUTH-1 (6 min)
code backend/middleware/auth.js     # TODO-AUTH-2 (10 min)

# Test de validation Phase 1
curl http://localhost:5000/api/health
```

#### Phase 2: API Métier (45 min)

```bash
# 5-6. Modèles de données
code backend/models/Category.js     # TODO-MODEL-2 (8 min)
code backend/models/Transaction.js  # TODO-MODEL-3 (10 min)

# 7-8. API REST complète
code backend/controllers/categoryController.js # TODO-CRUD-1 (15 min)
code backend/routes/categories.js              # TODO-ROUTES-1 (8 min)

# 9. Statistiques avancées
code backend/controllers/statsController.js    # TODO-STATS-1 (12 min)

# Test de validation Phase 2
curl -X POST http://localhost:5000/api/categories
```

#### Phase 3: Frontend React (60 min)

```bash
# 10. État global d'authentification
code frontend/src/contexts/AuthContext.js  # TODO-CONTEXT-1 (15 min)

# 11-12. Composants de base
code frontend/src/components/Navbar.js     # TODO-COMPONENT-1 (10 min)
code frontend/src/components/auth/Login.js # TODO-FORM-1 (12 min)

# 13. Routage et navigation
code frontend/src/App.js                   # TODO-ROUTER-1 (15 min)

# Test de validation Phase 3
# Ouvrir http://localhost:3000
```

### 🔧 Installation et Lancement

Après avoir complété les TODOs, installez et lancez l'application :

```bash
# Installation des dépendances
cd backend && npm install
cd ../frontend && npm install

# Option 1: Lancement avec Docker (recommandé)
docker-compose up --build

# Option 2: Lancement manuel
# Terminal 1: Backend
cd backend && npm run dev

# Terminal 2: Frontend
cd frontend && npm start

# Terminal 3: MongoDB (si pas Docker)
mongod --dbpath ./data
```

### 📊 URLs de Test

Une fois l'application lancée :

- **Frontend React** : http://localhost:3000
- **Backend API** : http://localhost:5000
- **Health Check** : http://localhost:5000/api/health
- **MongoDB** : mongodb://localhost:27017

## ✅ Validation par Checkpoint

### Checkpoint 1 - Backend Fondamental

```bash
# Tester l'API de base
curl http://localhost:5000/api/health
# Doit retourner: {"message": "API Budget Tracker fonctionne !"}

# Tester l'inscription
curl -X POST http://localhost:5000/api/auth/register \
  -H "Content-Type: application/json" \
  -d '{"name":"Test User","email":"test@ucad.edu.sn","password":"password123"}'
```

### Checkpoint 2 - API Complète

```bash
# Tester la création de catégorie (avec token)
curl -X POST http://localhost:5000/api/categories \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer VOTRE_TOKEN" \
  -d '{"name":"Transport UCAD","type":"expense","color":"#ff6b6b"}'

# Lister les catégories
curl -H "Authorization: Bearer VOTRE_TOKEN" \
  http://localhost:5000/api/categories
```

### Checkpoint 3 - Application Complète

- ✅ Interface web accessible sur http://localhost:3000
- ✅ Inscription et connexion fonctionnelles
- ✅ Navigation entre pages sans erreurs
- ✅ Données affichées en temps réel
- ✅ Aucune erreur dans la console navigateur/serveur

## 🔍 Dépannage et Debugging

### Problèmes Courants et Solutions

#### ❌ "TODO non complété" dans les logs

```bash
# Vérifier quels TODOs restent à compléter
grep -r "TODO-" backend/ frontend/ --include="*.js"

# Consulter README-TODOS.md pour guidance
cat README-TODOS.md
```

#### ❌ Erreur de connexion MongoDB

```bash
# Vérifier que MongoDB fonctionne
docker-compose ps
# ou si installation locale
mongosh --eval "db.adminCommand('ping')"

# Vérifier la variable MONGO_URI
cat backend/.env | grep MONGO_URI
```

#### ❌ Erreur d'importation React

```bash
# Vérifier que les composants existent
ls frontend/src/components/
ls frontend/src/contexts/

# Vérifier la syntaxe import/export
grep -n "export\|import" frontend/src/App.js
```

#### ❌ Erreur JWT "Token invalide"

```bash
# Vérifier la variable JWT_SECRET
cat backend/.env | grep JWT_SECRET

# Tester la génération de token
node -e "console.log(require('./backend/utils/generateToken')('test123'))"
```

### Commandes de Debug Utiles

```bash
# Voir tous les processus Node.js
ps aux | grep node

# Nettoyer et redémarrer proprement
docker-compose down -v
docker system prune
./generate-starter-code.sh  # Regénérer si nécessaire

# Vérifier les dépendances
cd backend && npm list
cd frontend && npm list

# Logs détaillés
DEBUG=* npm run dev  # Backend avec logs détaillés
REACT_APP_DEBUG=true npm start  # Frontend avec logs
```

## 🎓 Conseils Pédagogiques

### 📚 Pour les Enseignants

1. **Progression modulaire** : Chaque TODO peut être fait indépendamment
2. **Validation immédiate** : Tester après chaque TODO complété
3. **Code review** : Comparer avec le lab PDF section par section
4. **Debugging guidé** : Utiliser les messages d'erreur pour enseigner

### 👨‍💻 Pour les Étudiants

1. **Ne pas copier-coller aveuglément** : Comprendre chaque ligne
2. **Tester fréquemment** : Un TODO à la fois
3. **Lire les erreurs** : Elles indiquent souvent le problème exact
4. **Consulter la doc** : Links vers documentation officielle dans le lab

### 🔄 Workflow Recommandé

```bash
# 1. Lire la section théorique du lab PDF
# 2. Comprendre l'objectif du TODO
# 3. Implémenter le code étape par étape
# 4. Tester immédiatement
# 5. Debug si nécessaire
# 6. Passer au TODO suivant
```

## 📁 Structure des Fichiers TODO

Chaque fichier généré contient :

```javascript
// TODO-XXX-Y: Titre explicite
//
// OBJECTIF: Description claire de ce qui doit être fait
//
// QUE FAIT CE CODE: Explication du fonctionnement attendu
//
// INSTRUCTIONS: Renvoi vers la section précise du lab PDF
//
// ÉTAPES À COMPLÉTER:
// 1. Première étape détaillée
// 2. Deuxième étape détaillée
// 3. etc.
//
// RAPPEL: Le code complet est dans le lab PDF à la section TODO-XXX-Y

console.log("🚧 TODO-XXX-Y: Description à implémenter");

// Code temporaire de placeholder - À REMPLACER
```

Cette structure garantit que les étudiants :

- ✅ Comprennent l'objectif avant de coder
- ✅ Savent exactement où trouver la solution
- ✅ Ont des étapes claires à suivre
- ✅ Peuvent identifier facilement les TODOs restants

## 🎯 Fonctionnalités Finales Attendues

Une fois tous les TODOs complétés, l'application aura :

### 🔐 Authentification Sécurisée

- Inscription avec validation email/password
- Connexion avec tokens JWT
- Protection automatique des routes privées
- Persistance de session avec localStorage

### 💰 Gestion Budgétaire Complète

- Catégories personnalisées (Transport UCAD, Alimentation...)
- Transactions en FCFA avec validation métier
- CRUD complet via API REST sécurisée
- Statistiques en temps réel avec agrégation MongoDB

### 📊 Interface Moderne et Responsive

- Dashboard avec métriques financières
- Graphiques interactifs (camembert, historique)
- Formulaires avec validation Material-UI
- Navigation fluide avec React Router
- Design adaptatif mobile/desktop

### 🚀 Architecture Production-Ready

- Docker pour portabilité et déploiement
- Variables d'environnement sécurisées
- Structure modulaire et maintenable
- Gestion d'erreurs centralisée
- Code documenté et testable

---

## 🆘 Support et Ressources

### 📖 Documentation de Référence

- **Lab PDF** : Source principale avec code complet
- **README-TODOS.md** : Guide détaillé des TODOs
- **Commentaires de code** : Instructions dans chaque fichier

### 🔗 Ressources Externes

- [Documentation React](https://react.dev)
- [Documentation Express](https://expressjs.com)
- [Documentation MongoDB](https://docs.mongodb.com)
- [Material-UI Components](https://mui.com/components)

### 💬 En Cas de Blocage

1. 📚 Relire la section théorique correspondante dans le lab
2. 🔍 Vérifier la syntaxe et les imports
3. 🧪 Tester les endpoints avec curl/Postman
4. 📝 Consulter les logs d'erreur détaillés
5. 🤝 Demander de l'aide avec le contexte précis

---

**🎓 Bon développement et bon apprentissage !**  
_Dr. El Hadji Bassirou TOURE - DMI/FST/UCAD_

> 💡 **Rappel** : Ce script génère le code de départ avec TODOs.  
> Pour une application complète fonctionnelle, suivez le lab PDF étape par étape !
