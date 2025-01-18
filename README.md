# Learning Platform API

Une API backend pour une plateforme d'apprentissage en ligne construite avec Node.js et MongoDB.

## 🚀 Technologies Utilisées

- **Node.js** - Environnement d'exécution
- **Express.js** - Framework Web
- **MongoDB** - Base de données NoSQL
- **Mongoose** - ODM pour MongoDB
- **JWT** - Authentification par tokens
- **Bcrypt** - Hashage des mots de passe

## 📋 Fonctionnalités

- Authentification complète (inscription, connexion, gestion de profil)
- Gestion des cours (création, modification, suppression)
- Système d'inscription aux cours
- Suivi de la progression des étudiants
- Système d'évaluation et de commentaires

## 🛠️ Installation

1. Clonez le dépôt
```bash
git clone https://github.com/allaliHouda123/learning-platform-nosql.git
cd learning-platform-nosql
```

2. Installez les dépendances
```bash
npm install
```

3. Configurez les variables d'environnement
```bash
cp .env.example .env
# Modifiez les valeurs dans .env selon votre configuration
```

4. Lancez le serveur
```bash
npm run dev
```

## 📚 Structure du Projet

```
src/
├── config/         # Configuration (DB, env)
├── controllers/    # Logique métier
├── middleware/     # Middleware (auth, validation)
├── models/        # Modèles Mongoose
├── routes/        # Routes API
└── utils/         # Utilitaires

```

## 🔑 Points d'Accès API

### Authentification
- `POST /api/users/register` - Inscription
- `POST /api/users/login` - Connexion
- `GET /api/users/profile` - Profil utilisateur

### Cours
- `GET /api/courses` - Liste des cours
- `POST /api/courses` - Créer un cours (instructeur)
- `GET /api/courses/:id` - Détails d'un cours
- `PUT /api/courses/:id` - Modifier un cours
- `DELETE /api/courses/:id` - Supprimer un cours

### Inscriptions
- `POST /api/enrollments` - S'inscrire à un cours
- `GET /api/enrollments` - Voir ses inscriptions
- `PATCH /api/enrollments/:id/progress` - Mettre à jour sa progression

## 👥 Rôles Utilisateurs

- **Student** : Peut s'inscrire aux cours et suivre sa progression
- **Instructor** : Peut créer et gérer des cours
- **Admin** : Accès complet à toutes les fonctionnalités

## 🔐 Sécurité

- Authentification JWT
- Hashage des mots de passe avec Bcrypt
- Validation des données entrantes
- Protection CORS
- Headers de sécurité avec Helmet
