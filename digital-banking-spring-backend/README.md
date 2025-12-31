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
<img width="470" height="111" alt="image" src="https://github.com/user-attachments/assets/0e871314-de7e-4aa9-9cd8-bdefb64207fd" />


### Table bank_accounts
<img width="908" height="163" alt="image" src="https://github.com/user-attachments/assets/c5455912-701e-474a-bd9b-47a4bf5042d9" />


### Table account_operation
<img width="1091" height="212" alt="image" src="https://github.com/user-attachments/assets/bac3071f-70c5-486f-afed-09026cc4491b" />


## 🚀 Fonctionnalités principales

## 📖 Documentation API
Accéder à Swagger : `http://localhost:8085/swagger-ui.html`

Dans Swagger, vous pouvez :
- Tester tous les endpoints
- Voir les paramètres requis
- Exécuter des requêtes directement

<img width="1847" height="968" alt="image" src="https://github.com/user-attachments/assets/5d70a038-6a79-427e-8485-667ece53a0f3" />

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
