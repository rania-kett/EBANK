# Projet JEE - Digital Banking Backend

## Description
Application backend de gestion bancaire développée en **Java EE** permettant la gestion complète des clients, des comptes bancaires (courants/épargne) et des opérations financières (dépôts/retraits).

## Technologies Utilisées
- **Backend** : Java EE (JAX-RS, JPA, CDI)
- **Base de données** : MySQL
- **Build Tool** : Maven
- **Documentation API** : Swagger/OpenAPI
- **Serveur d'application** : WildFly/Payara

## Structure de la Base de Données
Base de données relationnelle MySQL avec les tables principales :
- `Client` - Informations des clients
- `Compte` - Comptes bancaires (courant/épargne)
- `Operation` - Historique des transactions
- Relations bien définies entre les entités

## API Endpoints

### **Gestion des Comptes Bancaires**
| Méthode | Endpoint | Description | Swagger |
|---------|----------|-------------|---------|
| **GET** | `/api/comptes` | Liste tous les comptes | Oui |
| **GET** | `/api/comptes/{id}` | Détails d'un compte par ID | Oui |
| **GET** | `/api/comptes/{id}/operations` | Opérations d'un compte | Oui |
| **GET** | `/api/comptes/{id}/page-operations` | Opérations paginées | Oui |
| **POST** | `/api/comptes` | Créer un nouveau compte | Oui |
| **POST** | `/api/comptes/{id}/depot` | Effectuer un dépôt | Oui |
| **POST** | `/api/comptes/{id}/retrait` | Effectuer un retrait | Oui |

### **Gestion des Clients**
| Méthode | Endpoint | Description | Swagger |
|---------|----------|-------------|---------|
| **GET** | `/api/clients` | Liste tous les clients | Oui |
| **GET** | `/api/clients/{id}` | Client par ID | Oui |
| **GET** | `/api/clients/search` | Recherche par mot-clé | Oui |

## Installation & Déploiement

### Prérequis
- Java JDK 17
- MySQL Server 5.7+
- Maven 3.6+
- Serveur d'application Java EE (WildFly 23+ recommandé)

### Étapes d'installation
1. **Cloner le projet**
   ```bash
   git clone [url-du-projet]
   cd digital-banking-backend
   ```

2. **Configurer la base de données**
   ```sql
   CREATE DATABASE digital_banking;
   CREATE USER 'bankadmin'@'localhost' IDENTIFIED BY 'password';
   GRANT ALL PRIVILEGES ON digital_banking.* TO 'bankadmin'@'localhost';
   FLUSH PRIVILEGES;
   ```

3. **Configurer les paramètres de connexion**
   - Modifier `src/main/resources/META-INF/persistence.xml`
   ```xml
   <jdbc-url>jdbc:mysql://localhost:3306/digital_banking</jdbc-url>
   <username>bankadmin</username>
   <password>password</password>
   ```

4. **Compiler et empaqueter**
   ```bash
   mvn clean package
   ```

5. **Déployer sur le serveur**
   - Copier le fichier `.war` génré dans le dossier `target/`
   - Déployer sur votre serveur WildFly/Payara

## Utilisation

### Accès aux interfaces
- **API REST** : `http://localhost:8080/digital-banking/api`
- **Swagger UI** : `http://localhost:8080/digital-banking/swagger-ui`
- **Base de données** : `localhost:3306/digital_banking`

### Exemple de requête API
```bash
# Liste des comptes
curl -X GET "http://localhost:8080/digital-banking/api/comptes"

# Détails d'un client
curl -X GET "http://localhost:8080/digital-banking/api/clients/1"
```

## Fonctionnalités Implémentées

### **Gestion des Comptes**
- [x] Création de comptes (courant/épargne)
- [x] Consultation des soldes
- [x] Historique des opérations
- [x] Opérations de dépôt/retrait
- [x] Pagination des transactions

### **Gestion des Clients**
- [x] Inscription des clients
- [x] Recherche multicritères
- [x] Consultation des détails
- [x] Association client-compte

### **Sécurité & Validation**
- [x] Validation des données
- [x] Gestion des erreurs
- [x] Contrôle des soldes
- [x] Journalisation des opérations

## Tests API avec Swagger
1. Accédez à l'interface Swagger : `http://localhost:8080/digital-banking/swagger-ui`
2. Explorez les endpoints disponibles
3. Testez les opérations directement depuis l'interface
4. Consultez les modèles de données

## Structure du Projet
```
src/
├── main/
│   ├── java/
│   │   ├── com/banking/entities/       # Entités JPA
│   │   ├── com/banking/services/       # Services métier
│   │   ├── com/banking/controllers/    # Contrôleurs REST
│   │   └── com/banking/config/         # Configuration
│   └── resources/
│       └── META-INF/
│           └── persistence.xml         # Config JPA
└── test/                               # Tests unitaires
```

## Auteur
**Réalisé par : Rania Kettani**


