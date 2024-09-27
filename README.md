

# Installation du projet Laravel

Ce document explique comment installer et configurer un projet Laravel à partir de zéro en utilisant Composer, les migrations de base de données, et npm pour la gestion des ressources front-end.

## Prérequis

Avant de commencer, assurez-vous d'avoir installé les éléments suivants sur votre machine :
- **PHP** (version 8.0 ou supérieure)
- **Composer** (gestionnaire de dépendances PHP)
- **MySQL** (ou tout autre SGBD compatible)
- **Node.js** et **npm** (pour la gestion des packages front-end)

## Étapes d'installation



### 1. Installer les dépendances PHP

Utilisez Composer pour installer les dépendances du projet Laravel :

```bash
composer install
```

### 2. Créer le fichier de configuration `.env`

Copiez le fichier d'exemple `.env` pour créer votre propre fichier de configuration :

```bash
cp .env.example .env
```

### 3. Générer la clé d'application

Générez une clé d'application Laravel, qui est utilisée pour le chiffrement des données sensibles :

```bash
php artisan key:generate
```

### 4. Configurer la base de données

- Ouvrez le fichier `.env` nouvellement créé et configurez les informations de votre base de données.
  
  Exemple :
  ```env
  DB_CONNECTION=mysql
  DB_HOST=127.0.0.1
  DB_PORT=3306
  DB_DATABASE=nom_de_votre_base_de_donnees
  DB_USERNAME=nom_utilisateur
  DB_PASSWORD=mot_de_passe
  ```

### 5. Exécuter les migrations

Une fois la base de données configurée, exécutez les migrations pour créer les tables nécessaires :

```bash
php artisan migrate
```

### 6. Installer les dépendances npm

Installez les dépendances front-end du projet avec npm :

```bash
npm install
```

### 7. Lancer le serveur de développement Laravel

Pour voir le projet en action, lancez le serveur de développement Laravel avec la commande suivante :

```bash
php artisan serve
```

Cela devrait démarrer le serveur à l'adresse [http://127.0.0.1:8000](http://127.0.0.1:8000).

### 8. Compiler les fichiers front-end

Utilisez npm pour compiler et surveiller les fichiers front-end :

```bash
npm run dev
```

Cela compile vos fichiers JavaScript et CSS pour le développement.

### 9. Accéder à l'application

Votre application devrait maintenant être accessible à l'adresse suivante : [http://127.0.0.1:8000](http://127.0.0.1:8000).



