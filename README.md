# Template API Symfony

## Français

Ce projet est un template Symfony avec une configuration prête à l'emploi pour développer des API modernes.

---
## Objectif du projet
Ce template vise à fournir une base solide pour le développement d'API modernes avec Symfony et un frontend React (Next.js), le tout conteneurisé avec Docker.

---
## Fonctionnalités

- **Symfony Framework** : Base du projet pour le développement backend.
- **API Platform** : Intégré pour faciliter la création d'API RESTful.
- **Next.js** : Framework React pour le développement frontend.
- **Docker** : Conteneurisation pour un environnement de développement reproductible.

---
## Technologies utilisées

- PHP 8.4
- Symfony 7+
- API Platform
- Node.js / Next.js
- Docker / Docker Compose
- Nginx
- MySQL
- PhpMyAdmin 
---

## Prérequis

Avant de commencer, assurez-vous d'avoir les outils suivants installés sur votre machine :

- **PHP** >= 8.4
- **Composer**
- **Node.js** et **npm**
- **Docker** et **Docker Compose**
- **Git**

---

## Arborescence du projet

Voici une vue simplifiée de l'arborescence du projet :
```
├── .docker/
│   ├── php/                # Configuration PHP
│       ├── Dockerfile
│       └── php.ini
│   ├── nginx/              # Configuration Nginx
│       └── nginx.conf
├── backend/                # Code source du backend Symfony
│   ├── config/             # Fichiers de configuration Symfony
│   ├── src/                # Code PHP du projet
│   ├── .env                # Fichier d'environnement
│   └── composer.json       # Dépendances PHP (uniquement API Platform)
├── frontend/               # Code source du frontend Next.js
│   ├── Dockerfile          # Configuration Docker pour Next.js
│   ├── src/                # Code source React (Next.js)
│   ├── public/             # Fichiers statiques accessibles publiquement
│   └── package.json        # Dépendances Node.js
├── docker-compose.yml      # Configuration Docker globale
├── LICENSE                 # Licence du projet
└── README.md               # Documentation du projet

```

---

## Explication des composants

### Backend
Le backend est construit avec **Symfony**, un framework PHP robuste. 
Il est actuellement vide. Seul le package `api-platform` est installé via la commande suivante : 
```bash
composer require api
```

### Frontend
Le frontend est construit avec **Next.js**, un framework JavaScript moderne pour créer des interfaces utilisateur dynamiques. Il est conçu pour interagir avec le backend via des appels API.

---

## Tutoriel d'utilisation

### 1. Cloner le dépôt
Exécutez la commande suivante pour cloner le projet :
```bash
git clone git@github.com:Baptistedev-web/Template-API.git
cd Template-API
```

### 2. Lancer Docker
Assurez-vous que Docker et Docker Compose sont installés. 
Ensuite, démarrez les conteneurs :
```bash
docker-compose up -d --build
```

### 3. Installer les dépendances PHP
   Accédez au conteneur PHP et installez les dépendances avec Composer :
```bash
docker-compose exec php composer install
```

### 4. Installer les dépendances Node.js
   Accédez au conteneur Node.js et installez les dépendances avec npm :
```bash
docker-compose exec frontend npm install
```

### 5. Configuration de l'environnement
   Copiez le fichier .env en .env.local et ajustez les variables si nécessaire :
   ```bash
   cp backend/.env backend/.env.local
   ```

### Contribution
Les contributions sont les bienvenues ! 
Veuillez soumettre une pull request ou ouvrir une issue pour toute suggestion ou amélioration.

### Licence
Ce projet est sous licence MIT. 
Consultez le fichier LICENSE pour plus d'informations.


## English
This project is a Symfony template with a ready-to-use configuration for developing modern APIs.

## Project Goal
This template aims to provide a solid foundation for developing modern APIs using Symfony and a React (Next.js) frontend, all containerized with Docker.
---
## Features
- **Symfony Framework**: Project base for backend development.
- **API Platform**: Integrated to facilitate the creation of RESTful APIs.
- **Next.js**: React framework for frontend development.
- **Docker**: Containerization for a reproducible development environment.

---
## Technologies Used

- PHP 8.4
- Symfony 7+
- API Platform
- Node.js / Next.js
- Docker / Docker Compose
- Nginx
- MySQL
- PhpMyAdmin

---
## Prerequisites
Before you begin, ensure you have the following tools installed on your machine:
- **PHP** >= 8.4
- **Composer**
- **Node.js** and **npm**
- **Docker** and **Docker Compose**
- **Git**

---
## Project Structure
Here is a simplified view of the project structure:
```
├── .docker/
│   ├── php/                  # PHP configuration
│       ├── Dockerfile
│       └── php.ini
│   ├── nginx/                # Nginx configuration
│       └── nginx.conf
├── backend/                  # Symfony backend source code
│   ├── config/               # Symfony configuration files
│   ├── src/                  # PHP project source code
│   ├── .env                  # Environment variables file
│   └── composer.json         # PHP dependencies (only API Platform)
├── frontend/                 # Next.js frontend source code
│   ├── Dockerfile            # Docker configuration for Next.js
│   ├── src/                  # React (Next.js) source code
│   ├── public/               # Public static files
│   └── package.json          # Node.js dependencies
├── docker-compose.yml        # Global Docker configuration
├── LICENSE                   # Project license
└── README.md                 # Project documentation

```
---
## Explanation of Components
### Backend
The backend is built with **Symfony**, a robust PHP framework.
It is currently empty. Only the `api-platform` package is installed via the following command:
```bash
composer require api
```
### Frontend
The frontend is built with **Next.js**, a modern JavaScript framework for creating dynamic user interfaces.
It is designed to interact with the backend via API calls.
---

## Usage Tutorial
### 1. Clone the repository
Run the following command to clone the project:
```bash
git clone git@github.com:Baptistedev-web/Template-API.git
cd Template-API
```
### 2. Start Docker
Make sure Docker and Docker Compose are installed.
Then, start the containers:
```bash
docker-compose up -d --build
```
### 3. Install PHP dependencies
Access the PHP container and install dependencies with Composer:
```bash
docker-compose exec php composer install
```
### 4. Install Node.js dependencies
Access the Node.js container and install dependencies with npm:
```bash
docker-compose exec frontend npm install
```
### 5. Environment Configuration
Copy the .env file to .env.local and adjust the variables if necessary:
```bash
cp backend/.env backend/.env.local
```
### Contribution
Contributions are welcome!
Please submit a pull request or open an issue for any suggestions or improvements.

### License
This project is licensed under the MIT License.
See the LICENSE file for more information.