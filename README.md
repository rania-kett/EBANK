#  EBank – Application Bancaire Full Stack

##  Description générale

**EBank** est une application bancaire **full stack** permettant la gestion des clients, des comptes bancaires et des opérations financières.
Elle repose sur une architecture **Frontend Angular + Backend Spring Boot (Java JEE)** avec une communication sécurisée via des **API REST**.

Le projet est divisé en deux parties :

* **EBank Frontend** : Application web développée avec Angular
* **EBank Backend** : API REST développée en Java avec Spring Boot

---

##  EBank – Frontend

###  Vue d’ensemble

Application web frontend développée avec **Angular 17.0.7**, conçue pour interagir avec l’API Spring Boot du backend.
Elle offre une interface moderne et sécurisée pour la gestion des opérations bancaires.

###  Fonctionnalités

* Authentification sécurisée
* Gestion des clients
* Gestion des comptes bancaires
* Liaison clients – comptes
* Navigation sécurisée avec contrôle d’accès
* Interface réactive et intuitive

###  Captures d’écran

* Page d’authentification
* Tableau de bord administrateur
* Gestion des clients
* Gestion des comptes


###  Informations techniques

* **Framework** : Angular 17.0.7
* **Langage** : TypeScript
* **Build tool** : Angular CLI
* **Serveur de développement** : `ng serve`
* **URL locale** : [http://localhost:4200/](http://localhost:4200/)
* **Hot Reload** : Activé

###  Architecture et composants

#### Modules

* **Customers** : Gestion complète des clients
* **Accounts** : Supervision des comptes bancaires
* **Customers-Accounts** : Liaison clients / comptes
* **Login** : Authentification sécurisée

#### Services

* **Customers Service**
* **Accounts Service**
* **Auth Service**

#### Sécurité

* Intercepteurs HTTP
* Garde d’authentification
* Garde d’autorisation basée sur les rôles
  
<img width="995" height="343" alt="image" src="https://github.com/user-attachments/assets/e1b2e594-e17c-4cb5-867f-5bc3a0d283a1" />

#### Routage

* Routes publiques
* Routes protégées
* Navigation fluide et modulaire

###  Qualité & Tests

* Tests unitaires des composants
* Validation des services
* Tests des intercepteurs
* Tests des gardes de routage
* Vérification des mécanismes de sécurité

###  Lancement du Frontend

```bash
npm install
ng serve
```

➡️ Accès via : [http://localhost:4200/](http://localhost:4200/)

---

##  EBank – Backend

###  Description

Application backend développée en **Java (Spring Boot / JEE)** pour la gestion des opérations bancaires via des **API REST sécurisées**.

###  Technologies utilisées

* **Java JEE / Spring Boot**
* **Spring Data JPA**
* **Spring Security**
* **MySQL**
* **Swagger (OpenAPI)**

###  Base de données

Base de données relationnelle **MySQL** avec les tables principales suivantes :

* **customers**
* **bank_accounts**
* **account_operation**


###  Fonctionnalités principales

* Gestion des clients
* Gestion des comptes bancaires
* Consultation des opérations financières
* Recherche par mot-clé
* Accès sécurisé aux ressources

###  Documentation API (Swagger)

Swagger est intégré pour tester et documenter les API.

➡️ Accès Swagger :
[http://localhost:8085/swagger-ui.html](http://localhost:8085/swagger-ui.html)

Avec Swagger, vous pouvez :

* Tester tous les endpoints
* Visualiser les paramètres requis
* Exécuter des requêtes REST
* Vérifier les réponses API

###  Tests

* Tests de la couche DAO
* Validation des endpoints REST
* Vérification des requêtes via Swagger

---

##  Sécurité

* Authentification basée sur Spring Security
* Gestion des rôles utilisateurs
* Protection des endpoints sensibles
* Sécurisation des routes côté frontend et backend

---

##  Communication Frontend – Backend

* API REST JSON
* HTTP Client Angular
* Gestion des tokens via intercepteurs
* Architecture scalable et modulaire

---

##  Technologies globales

* Angular 17
* TypeScript
* RxJS
* Angular Router
* Java Spring Boot
* MySQL
* Swagger / OpenAPI
* REST API

---

###  Réalisé par: RANIA KETTANI

