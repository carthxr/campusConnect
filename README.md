# Plateforme Régionale d'Offres — DTeam

> Application web de mise en relation locale (emplois, stages, alternances) entre candidats, entreprises et écoles par région et secteur d'activité. *(Projet scolaire - DTeam)*

## Stack Technique

* **Frontend :** HTML5, CSS3, JavaScript
* **Backend :** PHP 8
* **Base de données :** MySQL (`phpMyAdmin`)

## Fonctionnalités de l'application

### 1. Inscription & Authentification (Stepper en 2 étapes)

* **Étape 1 (Identité) :** Prénom, nom, date de naissance, email unique et mot de passe haché (`password_hash`).

* **Étape 2 (Localisation & Secteur) :** Secteur d'activité et adresse (Région et Code postal obligatoires).

### 2. Fil d'Actualité & Recherche (Accueil)

* **Tri intelligent :** Offres priorisées selon la **Région**, la proximité du **Code postal** et le **Secteur** de l'utilisateur

* **Filtres :** Recherche par mot-clé, type de contrat (`Stage`, `Alternance`, `CDD`, `CDI`), région, code postal et secteur

* **Interactions :** Consultation détaillée et système de **Like** (1 max par utilisateur/offre avec compteur)

### 3. Profil & Organisations (Entreprise / École)

* **Gestion du profil :** Mise à jour des informations personnelles et affichage de l'âge.

* **Organisations :** Création ou rattachement (autocomplétion) à une **Entreprise** (SIREN à 9 chiffres requis) ou une **École**

* **Gestion des offres (CRUD) :** Création, modification et suppression des annonces réservées aux membres de l'organisation

## Installation & Lancement rapide

1. **Cloner le projet** dans le dossier de votre serveur local (`htdocs` ou `www`) :

   ```
   git clone <https://github.com/carthxr/campusConnect.git>
   cd <campusConnect>
   
   ```

2. **Base de données (`phpMyAdmin`)** :

   * Créer une base `campusConnect_db`
   * Importer le fichier `database/schema.sql`.

3. **Configuration** (`config/db.php`) :

   ```
   <?php
   $pdo = new PDO('mysql:host=localhost;dbname=campusConnect_db;charset=utf8', 'root', '');
   
   ```

4. **Accès** : Lancer Apache/MySQL et ouvrir `http://localhost/<campusConnect>/`


## Auteur

* **Développeur :** CARPENTIER Arthur - Organisation **DTeam**