# 🚒 Application SDIS – Gestion opérationnelle des secours

## 🧭 Présentation générale

**SDIS** est une application web développée dans le cadre du **BTS SIO – option SLAM**.  
Elle a pour objectif de modéliser et de gérer les activités d’un **Service Départemental d’Incendie et de Secours (SDIS)**, ici inspiré du SDIS du Finistère.

Ce projet a une vocation pédagogique : il illustre les principes fondamentaux du développement web en **PHP**, l’organisation d’un projet MVC simplifié, l’utilisation d’une **base de données MySQL**, et la gestion des sessions utilisateurs.

---

## ⚙️ Fonctionnalités principales

- 👨‍🚒 **Gestion du personnel**
  - Fiches pompiers (identité, grade, habilitations)
  - Gestion des plannings et disponibilités

- 🚒 **Gestion des véhicules**
  - Suivi des entretiens et de l’état de chaque véhicule
  - Gestion des inventaires et disponibilités

- 🔥 **(À venir)** Gestion des interventions
  - Mobilisation automatique des véhicules et pompiers en fonction des habilitations et disponibilités

---

## 🧑‍💻 Technologies utilisées

| Composant | Technologie |
|------------|-------------|
| **Langage serveur** | PHP 8.2+ |
| **Base de données** | MySQL 8 |
| **Front-end** | HTML5, CSS3, Bootstrap 5 |
| **Scripts** | JavaScript (validation formulaire + preview image) |
| **Serveur local** | MAMP (macOS) ou XAMPP (Windows) |
| **Normes de code** | PSR-12, PHPDoc |

---

## 📂 Structure du projet

```
DSCPompier2025/
├── include/
│   ├── entete.php
│   ├── pied.php
│   ├── connection.php
│   ├── mesFonctions.php
│   ├── svg.php
├── images/
│   └── imagesCarte/
├── css/
│   └── styles.css
├── js/
│   └── app.js
├── index.php
├── README.md
└── .env
```

---

## 🔐 Configuration de la base de données

Le fichier **`.env`** contient les informations de connexion à la base MySQL.  
⚠️ Ce fichier ne doit **jamais être versionné** (ajouté à `.gitignore`).

Exemple :
```ini
DB_HOST=127.0.0.1
DB_PORT=8888
DB_NAME=DSC
DB_USER=userDSC
DB_PASS=IciVotreMotDePasse!
```

---

## 🚀 Installation et exécution

1. **Cloner le projet**
   ```bash
   git clone https://github.com/SebInfo/DSCPompier2025.git
   cd DSCPompier2025
   ```

2. **Configurer l’environnement**
   - Copier le fichier `.env.example` vers `.env`
   - Modifier les paramètres selon ta configuration MAMP/XAMPP

3. **Créer la base de données**
   - Importer le fichier `test.sql` (ou `schema.sql`) dans phpMyAdmin.

4. **Lancer le serveur local**
   - Sous MAMP, placer le projet dans le dossier `htdocs`
   - Accéder à : [http://localhost:8888/DSCPompier2025](http://localhost:8888/DSCPompier2025)

---

## 🧩 Bonnes pratiques et outils

- **Qualité du code**
  - Analyse : `phpcs --standard=PSR12 ./include`
  - Correction auto : `phpcbf ./include`
- **Documentation**
  - Tous les fichiers PHP incluent un en-tête PHPDoc conforme PSR-19.
- **Sécurité**
  - Variables sensibles dans `.env`
  - Connexion PDO avec gestion d’erreurs
  - Cookies configurés en mode `HttpOnly` + `SameSite=Lax`

---

## 👤 Auteur

**Sébastien Inion** et **Léo Letanneur**
> Projet réalisé dans le cadre du BTS SIO (option SLAM)  
> Lycée — 2025

---

## 📜 Licence

Ce projet est distribué sous licence **MIT**.  
Vous êtes libre de l’utiliser, le modifier et le redistribuer à condition de conserver la mention de l’auteur original.

---

## 🧠 Remarques pédagogiques

Ce projet illustre :
- Les bases de la programmation orientée serveur (PHP + MySQL)
- L’importance de la modularisation (`include/`, `require_once`)
- Le respect des standards du code (PSR-12)
- Les notions de sessions, cookies et formulaires sécurisés



