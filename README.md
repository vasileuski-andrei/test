# bank

The bank is a payment stub system that accepts payment information and pays for an order coming from the finance microservice.
After payment the payment receipt is saved in the database which can get by order id. The microservice has data validation, pagination and security.

Endpoints for all:
POST /api/v1/bank-payments - payments

GET /api/v1/payments-info - get payments by card number

GET /api/v1/payments-info/payment-receipt/{id} - get payment receipt by order id

Endpoints for admin:
> POST /api/v1/login - authentication
> POST /api/v1/admin/cards/change-status - change status of cards by filter
GET /api/v1/admin/clients - find all clients by filter, pagination
POST /api/v1/admin/clients - create new client using external service to get card info
DELETE /api/v1/admin/clients/{clientId} - delete client by id
GET /api/v1/admin/payments-info/all - get all payment info by filter, pagination
GET /api/v1/admin/payments-info/dates - get payments info between 2 dates, pagination

Technologies - Java 17, Spring Boot 2.7.11, Web, Validation, Security(JWT auth), Data-JPA, HQL and Querydsl-jpa, Eureka client, Webflux, Gradle, PostgreSQL, Liquibase, Docker, Lombok, Slf4j, JUnit, Mockito, MockMvc
