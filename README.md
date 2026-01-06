# Day-Care-Pet-Management

🐶🐱 **Day Care Pet Management System**

## 📌 **Project Overview**

The Pet Day Care Management System is a Java console application that helps staff manage pets during periods when their owners are at work, travelling, or on vacation.


The system eliminates paper-based records and sticky notes by providing a structured, user-friendly digital solution that is designed to evolve into a future mobile application.


It offers comprehensive pet management features, including adding, updating, deleting, searching, sorting, and reporting, while ensuring capacity and pricing rules are strictly applied.

###🧩 **Core Features**

####📝 **Pet Registration**

•	Register a new pet as either a Dog or Cat


•	Record important details:


  Name, age, sex, owner

  
  Days attending per week

  
  Neutered status

  
  Dog breed or cat favourite toy
  
####📋 **Pet Management**

•	View all pets currently in the day care


•	Update pet details


•	Remove pets safely with index validation


•	Enforce day care capacity limits

####📊 **Reports & Insights**

•	List all pets


•	View dogs or cats only

•	Identify dangerous dogs


•	List indoor cats and count them


•	Show neutered animals


•	Calculate total weekly income using polymorphism

####🔍 **Search & Sort**

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

##🏗️ **Project Structure**

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

##🏗️ **System Architecture**

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

##🧠 **Object-Oriented Design**

Abstraction & Inheritance


•	Pet is an abstract superclass
•	Dog and Cat extend Pet
•	Shared behaviour is defined once and reused

Polymorphism
•	All pets are stored as Pet
•	Each pet calculates its own weekly fee automatically
•	New animals (e.g. Rabbit) can be added without changing existing logic

Encapsulation
•	All fields are defined as private or protected and accessed via public getter and setter methods
•	Business rules are isolated in the correct classes

##🧪 **Input Validation and Error Handling **

•	All numeric and textual user input is validated using the ScannerInput utility
•	Menu options are checked to ensure selections fall within valid ranges
•	Access to collections is safeguarded through index validation
•	Day care capacity constraints are enforced when adding new pets
•	File input/output operations are enclosed in exception handling blocks to prevent system failures
This ensures the system behaves predictably even when users make mistakes.

##💾 **Persistence (Save & Load)**

Pet data is saved and loaded using Java object serialization:
•	All data is stored in a file called pets.dat
•	The Pet class implements the Serializable interface, enabling all subclasses to be saved and restored
•	The system safely handles scenarios where the data file is missing or cannot be read

##▶️** How to Run**

1.	Open the project using an IDE (IntelliJ, Visual Studio, Eclipse, etc.)
2.	Verify that Java version 15 or higher is installed
3.	Run the main.Driver class
4.	Use the console menu instructions to interact with the application
Show console screen
```
-------- Pet Day Care --------
1) Pets CRUD Menu
2) Reports Menu
3) Search Pets
4) Sort Pets
10) Save all
11) Load all
0) Exit

==>>
```
6.	2 submenus

## **Sample Usage **

•	Register new pets (dogs or cats) with validated input data
•	View reports detailing day care activity and statistics
•	Search for and sort pets using a variety of criteria
•	Save pet data before exiting the application and reload it later

## **Assumptions & Constraints **

•	The application is limited to two pet categories: dogs and cats
•	Dog breeds and cat toys are chosen from predefined selections
•	Pricing rules are fixed and implemented within the model classes
•	All sorting operations are implemented manually, without relying on built-in library sort methods

🚀 Future Expansion

The system is designed to support:

•	New animal types (e.g. Rabbits)
•	Mobile app interface
•	Advanced analytics and reporting

Author
Boun Chun
Pet Day Care Management System
Version 1.0













