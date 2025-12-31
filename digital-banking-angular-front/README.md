# EBank - Frontend

## Vue d'ensemble
Application web frontend développée avec Angular 17.0.7, conçue pour interagir avec une API Spring Boot backend. Cette application permet une gestion complète des opérations bancaires incluant la gestion des clients, des comptes, et un système d'authentification sécurisé.

## Captures d'écran

### 1. Page d'authentification
<img width="1216" height="379" alt="image" src="https://github.com/user-attachments/assets/8bf2c156-c369-4e48-9fda-f1ed1388bdc8" />


### 2. Tableau de bord des clients
<img width="1587" height="619" alt="Admin (2)" src="https://github.com/user-attachments/assets/e6596000-cf09-4e25-b0a2-ace142e93fa2" />

### 3. Gestion des clients
<img width="891" height="307" alt="image" src="https://github.com/user-attachments/assets/9376278a-5fc3-4b9a-a87e-838945cde6d9" />

## 4. Gestion des comptes
<img width="1352" height="545" alt="image" src="https://github.com/user-attachments/assets/af1dbe38-df62-4a3d-938f-d11448dc9649" />

## Informations techniques
- **Framework**: Angular 17.0.7
- **Build**: Angular CLI
- **Serveur de développement**: `ng serve`
- **URL locale**: `http://localhost:4200/`
- **Hot-reload**: Activé pour les modifications de fichiers sources

## Architecture et composants

### Modules d'interface
- **Gestion des clients** (`Customers`) : Interface de gestion complète des clients
- **Gestion des comptes** (`Accounts`) : Interface pour la supervision des comptes bancaires
- **Relations clients-comptes** (`Customers-Accounts`) : Interface de liaison entre clients et leurs comptes
- **Authentification** (`Login`) : Interface de connexion sécurisée pour les utilisateurs

### Services
- **Service clients** (`Customers-Services`) : Gestion des opérations clientèles
- **Service comptes** (`Accounts-Services`) : Administration des comptes bancaires
- **Service d'authentification** (`Auth-Service`) : Gestion sécurisée des sessions utilisateurs

### Système de sécurité
- **Intercepteurs HTTP** : Gestion avancée des requêtes entrantes et sortantes
- **Garde d'authentification** : Protection des routes nécessitant une connexion
- **Garde d'autorisation** : Contrôle d'accès basé sur les rôles utilisateurs

### Routage
Architecture de navigation intuitive avec :
- Routes publiques accessibles à tous les utilisateurs
- Routes protégées sécurisées par les gardes d'authentification et d'autorisation
- Navigation fluide entre les différents modules

## Qualité et tests
Tous les composants de l'application ont subi une validation rigoureuse :
- Tests unitaires des composants
- Validation des services et intercepteurs
- Vérification des mécanismes de sécurité
- Tests d'intégration des gardes de routage

## Lancement du projet

### Installation des dépendances
```bash
npm install
```

### Démarrage du serveur de développement
```bash
ng serve
```
L'application sera accessible à l'adresse : `http://localhost:4200/`

### Fonctionnalités du serveur de développement
- Rechargement automatique lors des modifications de code
- Messages d'erreur en temps réel
- Optimisation des performances de développement

## Caractéristiques principales
- Interface utilisateur moderne et réactive
- Communication sécurisée avec l'API backend
- Gestion d'état efficace
- Expérience utilisateur optimisée
- Architecture modulaire et scalable

## Technologies utilisées
- Angular 17
- TypeScript
- RxJS pour la programmation réactive
- Angular Router pour la navigation
- HTTP Client pour les communications API

### Réalisé par : RANIA KETTANI
