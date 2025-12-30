w# Projet JEE - Partie Backend

Ce projet est la partie **backend** d’une application de gestion bancaire. Il est développé avec **Spring Boot 3**, utilise **Spring Data JPA** pour l’accès à la base de données et expose des **web services RESTful**. L’API est documentée via **Swagger**.

## Technologies utilisées

* Java 17 
* Spring Boot 3
* Spring Data JPA
* Hibernate
* MySQL / H2 (base de données)
* Spring Web (REST API)
* Springdoc OpenAPI (Swagger UI)

## Structure du projet

```
src/main/java
├── org.sid.ebankingbackend
│   ├── entities
│   │   ├── Customer.java
│   │   ├── BankAccount.java
│   │   ├── SavingAccount.java
│   │   ├── CurrentAccount.java
│   │   └── AccountOperation.java
│   │
│   ├── repositories
│   │   ├── CustomerRepository.java
│   │   ├── BankAccountRepository.java
│   │   └── AccountOperationRepository.java
│   │
│   ├── services
│   │   ├── BankAccountService.java
│   │   └── CustomerService.java
│   │
│   ├── dtos
│   │   ├── CustomerDTO.java
│   │   └── BankAccountDTO.java
│   │
│   ├── controllers
│   │   ├── CustomerRestController.java
│   │   └── BankAccountRestController.java
│   │
│   └── EbankingBackendApplication.java
```

## Étapes réalisées

1. **Création du projet Spring Boot**
   Utilisation de Spring Initializr avec les dépendances **Spring Web** et **Spring Data JPA**.

2. **Création des entités JPA**

   * `Customer`
   * `BankAccount` (classe abstraite)
   * `SavingAccount` et `CurrentAccount` (héritage de BankAccount)
   * `AccountOperation`

3. **Création des repositories Spring Data**

   * `CustomerRepository`
   * `BankAccountRepository`
   * `AccountOperationRepository`

4. **Tests de la couche DAO**

   * Insertion, mise à jour et récupération d’objets via les repositories.

5. **Couche Service et DTOs**

   * `BankAccountService` et `CustomerService` pour la logique métier.
   * DTOs (`CustomerDTO`, `BankAccountDTO`) pour exposer uniquement les données nécessaires via l’API.

6. **Création des contrôleurs REST**

   * `CustomerRestController` et `BankAccountRestController` pour gérer les endpoints REST.

7. **Tests des web services REST**

   * Vérification avec **Postman** ou Swagger UI.

## Swagger UI

Une fois le projet lancé, la documentation des API est disponible à l’URL suivante :

```
http://localhost:8085/swagger-ui.html
```

Swagger permet de tester facilement toutes les routes REST exposées par le backend.
<img width="912" height="425" alt="image" src="https://github.com/user-attachments/assets/cad840f0-d08e-4e4f-a9cc-fbde5be6b53e" />


## Auteur
**Réalisé par : Rania Kettani**


