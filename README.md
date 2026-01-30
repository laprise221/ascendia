# 🚀 Ascendia - Plateforme de Gestion de Réseaux Sociaux

**Ascendia** est une application web centralisée permettant la gestion, la planification et l'analyse de publications sur plusieurs réseaux sociaux simultanément (Facebook, Instagram, Twitter/X). Elle intègre également des fonctionnalités d'IA pour recommander des contenus optimisés.

Ce projet a été réalisé dans le cadre de notre troisième année de Licence Informatique (L3 S6).

## 🎯 Objectifs du projet

- **Centralisation** : Gérer plusieurs comptes de réseaux sociaux depuis une interface unique.
- **Planification** : Programmer des posts à l'avance via un calendrier interactif.
- **Analyse** : Visualiser les statistiques d'engagement (likes, vues, partages) via des graphiques détaillés.
- **Intelligence Artificielle** : Génération et recommandation de posts assistée par IA.
- **Architecture Microservices** : Système modulaire pour une meilleure scalabilité et maintenabilité.

## 🛠️ Technologies utilisées

### Front-end
- **Framework** : React.js (Vite)
- **Styling** : Tailwind CSS
- **Visualisation** : Recharts, FullCalendar
- **Requêtes** : Axios

### Back-end
- **Runtime** : Node.js
- **Framework** : Express.js
- **Architecture** : Microservices (Gateway, Users, Posts, SocialAuth)
- **Authentification** : JWT, Passport.js (OAuth)
- **Base de données** : MongoDB (Mongoose)

### DevOps & Outils
- **Conteneurisation** : Docker, Docker Compose
- **Versionning** : Git, GitHub

## 📦 Installation et Lancement

### 1. Pré-requis
Assurez-vous d'avoir installé :
- [Node.js](https://nodejs.org/) (v16+)
- [Docker Desktop](https://www.docker.com/products/docker-desktop) (optionnel mais recommandé pour la base de données)
- Une instance MongoDB (locale ou Atlas)

### 2. Cloner le dépôt
```bash
git clone https://github.com/votre-username/ascendia.git
cd ascendia
```

### 3. 🔌 Côté Back-end (Microservices)

Vous pouvez lancer l'infrastructure via Docker (recommandé pour la DB et les services configurés) :

```bash
cd backend
docker-compose up --build
```
*Cela démarrera la Gateway, le service Users et la base de données MongoDB.*

Pour les services non inclus dans le Docker Compose actuel (Posts, SocialAuth), lancez-les manuellement dans de nouveaux terminaux :

**Service Posts :**
```bash
cd backend/services/posts
npm install
npm start
```

**Service SocialAuth :**
```bash
cd backend/socialAuth
npm install
npm start
```

### 4. 💻 Côté Front-end (React)

Dans un nouveau terminal :
```bash
cd frontend/reactJS
npm install
npm run dev
```
L'application sera accessible sur `http://localhost:5173` (port par défaut de Vite).

## 👥 Auteur

- **Aly Hachem Reda**

## 📄 Licence

Ce projet est à usage pédagogique dans le cadre de la Licence 3 Informatique.

---

## 🌐 Accès

Une fois lancé :
- **Frontend** : [http://localhost:5173](http://localhost:5173)
- **API Gateway** : [http://localhost:3000](http://localhost:3000)
