# Hospital Appointment System

A Java-based Hospital Appointment System developed as a desktop application using **Java 21** and **JavaFX 21**. The system provides separate interfaces and functionality for administrators, doctors, receptionists, and patients.

## 📌 Project Overview

The Hospital Appointment System is designed to simulate the management of a hospital and its appointment processes.

The application provides a graphical user interface (GUI) as well as a command-line interface (CLI). It manages hospitals, sections, doctors, patients, schedules, and appointments.

The project demonstrates important **Object-Oriented Programming (OOP)** concepts and Java programming techniques such as inheritance, interfaces, polymorphism, exception handling, collections, serialization, file handling, multithreading, and JavaFX GUI development.

## ✨ Features

* Hospital management
* Section management
* Doctor management
* Patient management
* Appointment/reservation management
* Doctor and patient information management
* Appointment scheduling
* Appointment date management
* Admin dashboard
* Doctor dashboard
* Receptionist interface
* Patient management interface
* Dark mode and light mode
* Modern JavaFX graphical interface
* Command-Line Interface (CLI)
* Data saving and loading using Java Serialization
* Data analytics/dashboard functionality
* Custom appointment restrictions and limits
* Exception handling for invalid operations
* Support for large amounts of data using Java collections
* Multithreading support

## 🛠️ Technologies Used

* **Java 21**
* **JavaFX 21**
* **Maven**
* **JUnit 4.12**
* **Java Collections**
* **Java Serialization**
* **JavaFX FXML**
* **Git & GitHub**

## 📂 Project Structure

```text
hospital-appointment-system/
│
├── .mvn/
│   └── wrapper/
│
├── JavaFX/
│   └── lib/
│
├── images/
│   ├── appointment.png
│   ├── console.png
│   ├── console2.png
│   ├── darkmode.png
│   ├── dashboard.png
│   ├── doctormenu.png
│   ├── logo.png
│   ├── macstyle.png
│   ├── mainmenu.png
│   └── modeselector.png
│
├── Softwaretests/
│   └── Java test files and test documentation
│
├── src/
│   └── main/
│       └── java/
│           ├── CRS/
│           ├── Enums/
│           ├── Exceptions/
│           ├── GUI/
│           ├── Hospital/
│           ├── Person/
│           ├── TextUI/
│           └── Main.java
│
├── data.ser
├── pom.xml
├── mvnw
├── mvnw.cmd
├── module-info.java
├── LICENSE
└── README.md
```

## 👥 Main User Roles

### Administrator

The administrator can manage:

* Hospitals
* Hospital sections
* Doctors
* System settings
* Application data
* Dashboard information

### Doctor

Doctors can:

* View their appointments
* View patient information
* Manage appointment-related information
* Access doctor dashboard features

### Receptionist

The receptionist interface provides functionality for handling patients and appointments.

### Patient

Patients can be managed through the system and can have appointments associated with doctors and hospital sections.

## 🧩 Main Java Packages

### `CRS`

Contains the core management classes responsible for handling the main system operations.

Important classes include:

* `CRS`
* `HospitalManager`
* `PatientManager`
* `DateManager`

### `Hospital`

Contains classes related to hospital operations:

* `Hospital`
* `Section`
* `Schedule`
* `Rendezvous`

### `Person`

Contains the main person-related classes:

* `Person`
* `Doctor`
* `Patient`

### `GUI`

Contains the JavaFX graphical user interface.

It includes separate interfaces for:

* Admin
* Doctor
* Receptionist
* Patient
* Universal/common operations

### `TextUI`

Contains the command-line interface and menu classes.

### `Exceptions`

Contains custom exceptions used to handle invalid operations, such as:

* `ChildOnlyException`
* `DailyLimitException`
* `DuplicateInfoException`
* `IDException`
* `RendezvousLimitException`

## 🧠 OOP Concepts Demonstrated

This project demonstrates several important Java and OOP concepts:

* Classes and Objects
* Encapsulation
* Inheritance
* Polymorphism
* Method Overloading
* Interfaces
* Enumerations
* Exception Handling
* Collections
* File I/O
* Serialization and Deserialization
* Multithreading
* Streams
* JavaFX GUI programming

## 💾 Data Storage

The application uses **Java Serialization** to save and load application data.

The serialized data is stored in:

```text
data.ser
```

This allows information to persist between application sessions.

## 🧪 Testing

The project contains a `Softwaretests` directory with Java test classes and testing documentation.

The tests cover different parts of the system, including:

* Hospital management
* Patient management
* Doctor management
* Appointment management
* Date management
* Exception handling
* Boundary value testing
* Equivalence partitioning
* Decision table testing
* Negative testing
* State transition testing

JUnit is included in the Maven configuration for testing.

## ⚙️ Requirements

Before running the project, install:

* **JDK 21 or later**
* **Maven**
* **JavaFX 21**

You can verify your Java installation with:

```bash
java -version
```

The project is configured to use Java 21.

## 🚀 How to Run

### Method 1 — Using Maven

Clone the repository:

```bash
git clone <YOUR-GITHUB-REPOSITORY-URL>
```

Open the project directory:

```bash
cd hospital-appointment-system
```

Run the application using Maven:

```bash
mvn clean javafx:run
```

### Windows Maven Wrapper

If Maven is not installed, you can use the included Maven wrapper:

```bash
mvnw.cmd clean javafx:run
```

### Linux / macOS

```bash
./mvnw clean javafx:run
```

## 🔄 Application Flow

```text
Start Application
       │
       ▼
   Main Menu
       │
       ▼
   Select Mode
       │
 ┌─────┼──────────────┐
 ▼     ▼              ▼
Admin Doctor     Receptionist
 │     │              │
 ▼     ▼              ▼
Manage  Manage       Manage
Hospital Patients    Patients
Doctor  Appointments Appointments
Section
       │
       ▼
 Save / Load Data
       │
       ▼
    data.ser
```

## 📦 Maven Dependencies

The project uses the following major dependencies:

* JavaFX Controls 21
* JavaFX FXML 21
* JavaFX Web 21
* JavaFX Swing 21
* JUnit 4.12 for testing

These dependencies are configured in `pom.xml`.

## 📁 Important Files

| File               | Purpose                                      |
| ------------------ | -------------------------------------------- |
| `pom.xml`          | Maven project configuration and dependencies |
| `src/main/java/`   | Main Java source code                        |
| `module-info.java` | Java module configuration                    |
| `data.ser`         | Serialized application data                  |
| `images/`          | Application screenshots and images           |
| `Softwaretests/`   | Test classes and testing documentation       |
| `.gitignore`       | Git ignore configuration                     |
| `mvnw`             | Maven wrapper for Linux/macOS                |
| `mvnw.cmd`         | Maven wrapper for Windows                    |
| `LICENSE`          | Project license                              |

## 🎯 Learning Objectives

The project provides practical experience in:

1. Developing a Java desktop application.
2. Applying Object-Oriented Programming concepts.
3. Creating graphical interfaces using JavaFX.
4. Managing data using Java collections.
5. Implementing file handling and serialization.
6. Handling application errors using custom exceptions.
7. Writing and organizing unit tests.
8. Using Maven for project and dependency management.
9. Designing a system with multiple user roles.
10. Using Git and GitHub for source-code management.

## 🔮 Future Improvements

Possible improvements for the system include:

* Database integration using MySQL or PostgreSQL
* User authentication and authorization
* Password protection
* Cloud-based data storage
* Online appointment booking
* Email/SMS appointment notifications
* REST API integration
* Improved reporting and analytics
* Deployment as a standalone executable

## 👨‍💻 Author

**Nitin**

Java Project — Hospital Appointment System

## 📄 License

This project is distributed under the MIT License. See the `LICENSE` file for more information.
