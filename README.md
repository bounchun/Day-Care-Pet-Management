# Day-Care-Pet-Management

🐶🐱 Day Care Pet Management System
## 📌 Project Overview

The Pet Day Care Management System is a Java console application that helps staff manage pets during periods when their owners are at work, travelling, or on vacation.
The system eliminates paper-based records and sticky notes by providing a structured, user-friendly digital solution that is designed to evolve into a future mobile application.
It offers comprehensive pet management features, including adding, updating, deleting, searching, sorting, and reporting, while ensuring capacity and pricing rules are strictly applied.

###🧩 Core Features

####📝 Pet Registration

•	Register a new pet as either a Dog or Cat
•	Record important details:
  Name, age, sex, owner
  Days attending per week
  Neutered status
  Dog breed or cat favourite toy
  
####📋 Pet Management

•	View all pets currently in the day care
•	Update pet details
•	Remove pets safely with index validation
•	Enforce day care capacity limits

####📊 Reports & Insights

•	List all pets
•	View dogs or cats only
•	Identify dangerous dogs
•	List indoor cats and count them
•	Show neutered animals
•	Calculate total weekly income using polymorphism

####🔍 Search & Sort

•	Search pets by:
o	Name
o	Owner
o	Breed (dogs)
o	Favourite toy (cats)
•	Sort pets by:
o	Name
o	Age
o	Owner
o	Days attending

##🏗️ Project Structure

```
src/
├── main/
│   └── Driver.java
├── controllers/
│   └── DayCare.java
├── models/
│   ├── Pet.java
│   ├── Dog.java
│   └── Cat.java
└── utils/
    ├── ScannerInput.java
    ├── Utilities.java
    ├── DogBreedUtility.java
    └── CatToyUtility.java

```

##🏗️ System Architecture

```
Driver (Console UI)
        ↓
DayCare (Controller / Business Logic)
        ↓
Pet (Abstract Model)
   ↳ Dog
   ↳ Cat
```
The system is implemented using a layered architectural approach: 
•	Driver
Coordinates all user interactions, including menu presentation and navigation.
•	DayCare (Controller)
Manages the core business logic such as pet management, reporting, searching, sorting, and data persistence.
•	Models (Pet, Dog, Cat)
Define the domain entities and encapsulate pet-specific data and behaviour.
•	Utilities
Provide reusable helper methods for input processing, validation, and data formatting.

















