# One-To-Many JPA Relationship Demo

A simple Java application demonstrating parent-child relationship management using JPA with EclipseLink and MySQL.

## Overview

This project showcases:

- JPA entity relationship mapping (One-to-Many)
- DAO pattern implementation
- CRUD operations with JPA

## Project Structure

```
src/main/
├── java/
│   ├── dao/             # Data Access Object interfaces
│   ├── daoImpl/         # DAO implementations
│   ├── models/          # JPA entity classes
│   └── Main.java        # Application entry point
└── resources/
    └── META-INF/
        └── persistence.xml  # JPA configuration
```

## Entities

- **Parent**: Entity with one-to-many relationship to children
- **Child**: Entity with many-to-one relationship to parent

## Technologies Used

- Java
- Jakarta Persistence API (JPA)
- EclipseLink (JPA Provider)
- MySQL
- Maven

## Database Configuration

The application connects to a MySQL database with the following settings (configurable in `persistence.xml`):

- Database name: `entity5`
- Username: `root`
- Password: ` ` (empty)

## Getting Started

1. Clone the repository
2. Create MySQL database named `entity5`
3. Run the application using Maven:

```bash
mvn clean install
mvn exec:java -Dexec.mainClass="Main"
```

## Features

- Create, read, update, and delete Parents and Children
- Manage parent-child relationships
- Automatic table creation with EclipseLink

## Implementation Details

The application uses:

- Entity annotations for JPA mapping
- DAO pattern for database operations
- Transaction management for data consistency

## Requirements

- Java 23+
- MySQL 8.0+
- Maven 3.6+
