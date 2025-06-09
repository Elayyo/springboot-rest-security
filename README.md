# Spring Boot REST Security Demo

Dieses Projekt ist im Rahmen eines Udemy-Kurses entstanden, den ich selbständig zur Weiterbildung im Bereich Spring Boot und Spring Security bearbeitet habe.

## Projektbeschreibung

Die Anwendung ist ein einfaches CRUD-Backend für eine Mitarbeiterverwaltung (Employee Directory) mit REST-API und rollenbasierter Zugriffskontrolle. Die Benutzer- und Rollenverwaltung erfolgt über eine relationale Datenbank (MySQL) und nutzt Spring Security mit JDBC-Authentifizierung.

## Features

- REST-API für CRUD-Operationen auf Mitarbeiterdaten (`/api/employees`)
- Rollenbasierte Zugriffskontrolle:
  - **EMPLOYEE**: Lesen von Mitarbeiterdaten
  - **MANAGER**: Hinzufügen und Bearbeiten von Mitarbeitern
  - **ADMIN**: Löschen von Mitarbeitern
- Benutzer- und Rollenverwaltung in der Datenbank (BCrypt-verschlüsselte Passwörter)
- Beispiel-SQL-Skripte für Datenbank und Benutzerverwaltung

## Technologien

- Java 17
- Spring Boot 3
- Spring Data JPA
- Spring Security
- MySQL

## Setup

1. **Datenbank einrichten**  
   Die SQL-Skripte im Ordner `sql-scripts` ausführen, um die benötigten Tabellen und Testdaten anzulegen.

2. **Konfiguration**  
   In der Datei [`src/main/resources/application.properties`](src/main/resources/application.properties) die Zugangsdaten zur Datenbank anpassen.

3. **Build & Start**  
   Mit Maven bauen und starten:
   ```sh
   ./mvnw spring-boot:run
   ```
