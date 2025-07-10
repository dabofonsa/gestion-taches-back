# Gestionnaire de Tâches

## Description du projet

Ce projet est une application fullstack pour la gestion de tâches :  
- Frontend : Application React pour créer, modifier, supprimer et afficher des tâches.  
- Backend : API NestJS pour gérer les tâches, connectée à une base de données MySQL (MySQL Workbench) via Prisma.  

L’application permet de manipuler les tâches avec un CRUD complet et une interface utilisateur simple et intuitive.


## Installation et mise en place

### Prérequis
- Node.js & npm  
- MySQL 8.0

### Backend 
1. Cloner le dépôt le backend dans votre dossier local: `git clone https://github.com/dabofonsa/gestion-taches-back.git`
2. Installer les dépendances avec `npm install`  
3. Configurer la base de données MySQL dans le fichier `.env` (nom_SGBD, utilisateur, mot de passe, hôte, port, nom de la base)
    - Exemple: `DATABASE_URL="mysql://fonsa:fonsa@localhost:3306/testdeveloppement"`
5. Lancer MySQL localement 
6. Exécuter la migration Prisma avec la commande :  `npm prisma migrate dev --name init`
7. Démarrer le serveur backend : `npm run start`

## Choix techniques
### Backend
- NestJS : Framework Node.js structuré, supportant TypeScript, et idéal pour API REST.
- Prisma : Pour gérer les migrations et les requêtes SQL avec MySQL de manière typée et simple.
- MySQL 8.0 : Base de données relationnelle stable, facile à utiliser avec Prisma.
- Structure modulaire : Organisation claire des modules, contrôleurs, et services pour faciliter la maintenance.
- Gestion des erreurs et validation : Validation des données reçues pour sécuriser l’API.
- Endpoints REST : CRUD complet pour les tâches, notamment création, édition, suppression, récupération.
- Postman: Permet de tester les requetes HTTP CRUD.
- 
## Fonctionnalités réalisées:
-Implémentation du model de données, des services et des controlleurs pour gérer les taches
- Connection du backend avec la base de données local MySQL via Prisma
- Création, afficher, édition et suppression des tâches côté backend avec POSTMAN
- Tester les requêtes HTTP sur POSTMAN.

## Difficultés et points d’attention:
- Comprendre la structure NestJS et Prisma pour la gestion des migrations et des modèles.
- La synchronisation des données entre frontend et backend, notamment lors de la modification inline.
- Configuration CORS entre frontend et backend pour éviter les erreurs de requêtes.
- Respecter la consigne d’utiliser uniquement yarn et non npm.

## Bonus réalisé
- Ajout d’un système de tri par date de création et un filtre par priorité des tâches.
