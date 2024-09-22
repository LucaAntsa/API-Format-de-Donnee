# API-Format-de-Donnee

---Exemple----
# Gestion des Absences et Présences

Dans ce projet de gestion des absences et présences des étudiants, nous allons voir comment ajouter, mettre à jour, supprimer et lister les absences et les présences, ainsi que vérifier des conditions spécifiques (comme l'ajout au processus COR pour les absences non justifiées).

## Outils utilisés :
- **Spring Boot**
- **Lombok**
- **JDBC pur**
- **PostgreSQL**

## Étapes de configuration

### 1. Créer un projet Spring Boot avec Maven

Créez un projet Maven Spring Boot en utilisant des outils comme **Spring Initializr** ou **IntelliJ IDEA**, et incluez les dépendances pour Spring Boot, Lombok et PostgreSQL.

### 2. Configurer la connexion avec la base de données

Dans IntelliJ IDEA :
- Allez dans le dossier `src/main/resources`.
- Ouvrez le fichier `application.properties` et ajoutez les informations de connexion à la base de données PostgreSQL.

### 3. Créer un package repository

Dans le dossier `src/main/java`, créez un package nommé `repository` pour gérer la connexion avec la base de données et les opérations associées.

### 4. Créer les packages pour les contrôleurs, entités et services

- **Controller** : pour gérer les endpoints relatifs aux absences et présences.
- **Entity** : pour définir les entités telles que l'absence et la présence.
- **Service** : pour implémenter la logique métier liée aux absences et présences.

### 5. Exécuter l'application Spring Boot

Lancez l'application Spring Boot pour démarrer les services de gestion des absences et présences.

---

## Endpoints pour la gestion des absences

### Absences

- **Ajouter une absence** : `POST` `/absences/add` – Ajouter une nouvelle absence pour un étudiant.
- **Mettre à jour une absence** : `PUT` `/absences/update/{id}` – Mettre à jour les détails d'une absence existante.
- **Supprimer une absence** : `DELETE` `/absences/delete/{id}` – Supprimer une absence en utilisant son ID.
- **Lister toutes les absences** : `GET` `/absences/all` – Obtenir la liste de toutes les absences.
- **Vérifier l'ajout au processus COR** : `POST` `/absences/check-cor/{etudiantId}` – Vérifier si un étudiant doit être ajouté au processus COR après trois absences injustifiées consécutives.

---

## Endpoints pour la gestion des présences

### Présences

- **Ajouter une présence** : `POST` `/presences/add` – Ajouter une nouvelle présence ou absence pour un étudiant.
- **Mettre à jour une présence** : `PUT` `/presences/update/{id}` – Mettre à jour les détails d'une présence existante.
- **Supprimer une présence** : `DELETE` `/presences/delete/{id}` – Supprimer une présence en utilisant son ID.
- **Lister toutes les présences** : `GET` `/presences/all` – Obtenir la liste de toutes les présences.

---

## Remarque

La spécification détaillée de l'API se trouve dans le fichier de configuration sous format **YAML**, qui est situé dans le répertoire principal du projet.
