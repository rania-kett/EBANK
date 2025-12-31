# EBank - Backend

## Description
Application backend pour système bancaire développée en Java (JEE). Gère les clients, comptes bancaires et opérations financières.

## Technologies
- **Backend**: Java JEE
- **Base de données**: MySQL
- **API**: REST
- **Documentation**: Swagger

## 📊 Base de données

### Tables principales
<img width="1054" height="116" alt="image" src="https://github.com/user-attachments/assets/4cb1b506-8951-48e8-9818-a5c13bd661e3" />


### Table customers
![Table customers](images/table-customers.png)
*Exemple de données clients avec id, email et nom*

### Table bank_accounts
![Table bank_accounts](images/table-accounts.png)
*Comptes bancaires avec solde, type et client associé*

### Table account_operation
![Table operations](images/table-operations.png)
*Historique des opérations avec dates et montants*

## 🚀 Fonctionnalités principales

### 📋 Gestion des comptes
**Liste des comptes**
- `GET /api/accounts` - Voir tous les comptes

![Liste des comptes API](images/api-accounts-list.png)
*Exemple de réponse JSON avec tous les comptes*

**Détails d'un compte**
- `GET /api/accounts/{id}` - Voir un compte spécifique

![Détails compte API](images/api-account-detail.png)
*Détails d'un compte avec ses informations*

**Opérations d'un compte**
- `GET /api/accounts/{id}/operations` - Historique des transactions

![Opérations compte API](images/api-account-operations.png)
*Liste des opérations d'un compte spécifique*

### 👥 Gestion des clients
**Liste des clients**
- `GET /api/customers` - Voir tous les clients

**Recherche client**
- `GET /api/customers/search` - Rechercher par nom/email

**Détails client**
- `GET /api/customers/{id}` - Voir un client spécifique

## 📖 Documentation API
Accéder à Swagger : `http://localhost:8080/swagger-ui.html`

Dans Swagger, vous pouvez :
✅ Tester tous les endpoints
✅ Voir les paramètres requis
✅ Exécuter des requêtes directement

![Swagger Interface](images/swagger-interface.png)
*Interface Swagger avec exemples de requêtes*

## 📝 Structure des données

### Client
```json
{
  "id": 1,
  "firstName": "Jean",
  "lastName": "Dupont",
  "email": "jean.dupont@email.com"
}
Compte bancaire
json
{
  "id": "04f14e04-cfa3-410a-bcc3-075a6b79d7c1",
  "balance": 710196.79,
  "accountType": "CHECKING"
}
Opération
json
{
  "type": "CREDIT",
  "amount": 30425.06,
  "date": "22-12-2023:14-35-55"
}
⚙️ Installation rapide
1. Prérequis
Java 11+

MySQL

Maven

2. Configuration base de données
sql
CREATE DATABASE digital_banking;
Modifier application.properties :

text
spring.datasource.url=jdbc:mysql://localhost:3306/digital_banking
spring.datasource.username=root
spring.datasource.password=votre_mot_de_passe
3. Lancer l'application
bash
mvn spring-boot:run
🔧 Utilisation
Test rapide avec cURL
Voir tous les comptes :

bash
curl http://localhost:8080/api/accounts
Voir un compte spécifique :

bash
curl http://localhost:8080/api/accounts/04f14e04-cfa3-410a-bcc3-075a6b79d7c1
Faire un dépôt :

bash
curl -X POST http://localhost:8080/api/accounts/{id}/operations \
  -H "Content-Type: application/json" \
  -d '{"type":"CREDIT", "amount":500}'
