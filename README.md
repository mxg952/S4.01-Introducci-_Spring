
# Spring Boot - S04T01

This repository contains the solutions for the **S04T01** task, an introduction to the Spring Boot framework, covering dependency management with Maven and Gradle, basic REST controller creation, and API testing with Postman.

## 📋 Task Overview

The objective of this project is to build two simple Spring Boot applications that demonstrate the use of:
1. **Maven** as a build and dependency management tool.
2. **Gradle** as a build and dependency management tool.

Each application exposes REST endpoints to handle HTTP GET requests using `@RequestParam` and `@PathVariable`.

## 🚀 Projects

### 1. Project 1: Maven-based Application (`S04T01N01`)
- **Location**: `/S04T01N01`
- **Port**: `9000`
- **Group**: `cat.itacademy.s04.t01.n01`
- **Dependencies**: Spring Web, Spring Boot DevTools

#### Endpoints:
- **GET** `http://localhost:9000/HelloWorld`
    - Returns: `"Hola, UNKNOWN. Estàs executant un projecte Maven"`
    - Uses `@RequestParam` with a default value.
- **GET** `http://localhost:9000/HelloWorld?nom={name}`
    - Returns: `"Hola, {name}. Estàs executant un projecte Maven"`
- **GET** `http://localhost:9000/HelloWorld2`
    - Returns: `"Hola, UNKNOWN. Estàs executant un projecte Maven"`
    - Uses `@PathVariable` (optional).
- **GET** `http://localhost:9000/HelloWorld2/{name}`
    - Returns: `"Hola, {name}. Estàs executant un projecte Maven"`

#### Key Maven Commands:
```bash
mvn compile    # Compile the project
mvn package    # Package the application (creates a JAR)
mvn clean      # Clean the target directory
mvn spring-boot:run  # Run the Spring Boot application
```

### 2. Project 2: Gradle-based Application (`S04T01N02`)
- **Location**: `/S04T01N02`
- **Port**: `9001`
- **Group**: `cat.itacademy.s04.t01.n02`
- **Dependencies**: Spring Web, Spring Boot DevTools

#### Endpoints:
- **GET** `http://localhost:9001/HelloWorld`
    - Returns: `"Hola, UNKNOWN. Estàs executant un projecte Gradle"`
    - Uses `@RequestParam` with a default value.
- **GET** `http://localhost:9001/HelloWorld?nom={name}`
    - Returns: `"Hola, {name}. Estàs executant un projecte Gradle"`
- **GET** `http://localhost:9001/HelloWorld2`
    - Returns: `"Hola, UNKNOWN. Estàs executant un projecte Gradle"`
    - Uses `@PathVariable` (optional).
- **GET** `http://localhost:9001/HelloWorld2/{name}`
    - Returns: `"Hola, {name}. Estàs executant un projecte Gradle"`

#### Key Gradle Commands:
```bash
gradle build     # Build the project
gradle assemble  # Assemble the JAR/WAR files
gradle clean     # Clean the build directory
gradle bootRun   # Run the Spring Boot application
```

## 🛠️ Setup & Execution

### Prerequisites
- **Java 11+**
- **IDE** (Eclipse recommended for this task)
- **Maven** (for Project 1)
- **Gradle** (for Project 2)
- **Postman** (for testing - Level 3)


### Running the Applications
1. Run each application from your IDE by right-clicking the main class (`*Application.java`) and selecting `Run As > Spring Boot App`.
2. Alternatively, use the command line:
   - **Maven**: `mvn spring-boot:run` (from the `S04T01N01` directory)
   - **Gradle**: `gradle bootRun` (from the `S04T01N02` directory)

## 📬 Postman Testing (Level 3)

Two Postman environments have been created and exported for testing the APIs.

### Environment Files (Exported as JSON)
1. **`Projecte Maven.postman_environment.json`**
    - Variables:
        - `servidor`: `http://localhost`
        - `port`: `9000`
2. **`Projecte Gradle.postman_environment.json`**
    - Variables:
        - `servidor`: `http://localhost`
        - `port`: `9001`

### How to Use:
1. Import the environment JSON files into Postman.
2. Select the desired environment from the top-right dropdown in Postman.
3. Use the following dynamic URLs in your requests:
    - `{{servidor}}:{{port}}/HelloWorld?nom=YourName`
    - `{{servidor}}:{{port}}/HelloWorld2/YourName`

### Screenshots:
- **Maven Project Test**: See `postman-maven-execution.png`
- **Gradle Project Test**: See `postman-gradle-execution.png`

## 📚 Resources & References

The following resources from the campus were instrumental in completing this task:

1.  **Baeldung: Changing the Spring Boot Port**
    - *Usage:* Essential for configuring `server.port` in the `application.properties` file for both projects.
    - Link: [https://www.baeldung.com/spring-boot-change-port](https://www.baeldung.com/spring-boot-change-port)

4.  **Baeldung: Difference between @RequestParam and @PathVariable**
    - Link: [https://www.baeldung.com/spring-requestparam-vs-pathvariable](https://www.baeldung.com/spring-requestparam-vs-pathvariable)

## 👨‍💻 Author

mxg952

## 📄 License

This project is created for educational purposes as part of the It Academy curriculum.