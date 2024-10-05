# README - Entity-Relationship Model

## Description
This file describes the Entity-Relationship (ER) model for the ApartaApp database, which includes the entities, their attributes, and the relationships between them. The goal is to represent the structure of the database clearly and concisely.

## Entities and Attributes

### 1. **Owner**
- **OwnerID**: Unique identifier for the owner.
- **Name**: Name of the owner.
- **Age**: Age of the owner.
- **Children**: Number of children of the owner.
- **Pets**: Number of pets of the owner.

### 2. **Apartment**
- **ApartmentID**: Unique identifier for the apartment.
- **Number**: Number of the apartment.
- **Block**: Block where the apartment is located.
- **Area**: Area of the apartment in square meters.
- **Rooms**: Number of rooms in the apartment.

### 3. **PublicServices**
- **ServiceID**: Unique identifier for the public service.
- **Name**: Name of the public service (water, electricity, gas, etc.).

### 4. **Reservations**
- **ReservationID**: Unique identifier for the reservation.
- **ApartmentNumber**: Number of the reserved apartment.
- **Owner**: Owner of the apartment.
- **Date**: Date of the reservation.
- **CommonSpace**: Common space reserved.

### 5. **CommonSpace**
- **CommonSpaceID**: Unique identifier for the common space.
- **Name**: Name of the common space (e.g., pool, gym, etc.).

### 6. **ApartmentPublicService** (Intermediate Entity)
- **ApartmentID**: Identifier for the apartment.
- **ServiceID**: Identifier for the public service.

## Relationships
- **Owner 1 --- N Apartment**: An owner can have multiple apartments.
- **Apartment 1 --- N ApartmentPublicService N --- 1 PublicServices**: An apartment can have multiple public services, and a service can be available in multiple apartments (resolved by the intermediate entity).
- **Apartment 1 --- N Reservations**: An apartment can have multiple reservations.
- **Reservations N --- 1 CommonSpace**: A reservation can be associated with a single common space, but a common space can be reserved multiple times.

## ER Diagram
The ER diagram visualizes the entities and their relationships. This diagram includes the entities, attributes, and the 1:N and N:M relationships. An intermediate entity, **ApartmentPublicService**, is used to break down the many-to-many relationship between **Apartment** and **PublicServices**.

## Conclusion
This ER model provides a clear structure for the ApartaApp database, allowing for efficient management of data related to owners, apartments, public services, and reservations.

