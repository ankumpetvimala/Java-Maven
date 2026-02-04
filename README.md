# DevOps Project : Build Automation Using Maven

## 📌 Objective

Automate the build process of a Java application using **Apache Maven**. The project demonstrates Maven project creation, dependency management, build lifecycle execution, and artifact generation.

---

## 🧩 Problem Statement

Create a Maven-based Java project, understand the `pom.xml` structure, add dependencies, build the project using Maven commands, and verify the generated build output.

---

## 🛠️ Tools & Technologies

* Java (JDK 11 / 17)
* Apache Maven
* Git & GitHub
* AWS EC2 (Ubuntu 22.04, t2.micro)
* Jenkins (via Docker)
* Maven 3.8.6
  

---

## 📂 Project Structure

```
Java-Maven/
├── pom.xml
├── src/
│   ├── main/
│   │   └── java/com/example/App.java
│   └── test/
│       └── java/com/example/AppTest.java
├── target/
├── README.md
└── screenshots/
```

Maven follows a standard directory structure which helps in automatic compilation and testing.

---
## Steps
1. Launched an EC2 Ubuntu instance with ports 22, 80, and 8080 open.
2. Installed Java, Maven, Docker, and Git.
3. Set up Jenkins in a Docker container.
4. Created a Java HelloWorld app with `pom.xml`.
5. Configured a Jenkins Freestyle job to build the app with Maven (`clean package`).
6. Captured a screenshot of the successful build console output.
7. Documented the process


## ⚙️ Task 1: Create a Maven Project

The Maven project was created using standard Maven archetype conventions, ensuring proper folder structure for source and test code.

---

## 📄 Task 2: Understand `pom.xml`

The `pom.xml` (Project Object Model) is the heart of a Maven project.

### Key Elements:

* **groupId** – Organization or package name
* **artifactId** – Project name
* **version** – Application version
* **packaging** – Type of artifact (jar)
* **dependencies** – External libraries

Example:

```xml
<groupId>com.example</groupId>
<artifactId>Java-Maven</artifactId>
<version>1.0-SNAPSHOT</version>
```

---

## 📦 Task 3: Add Dependency

JUnit dependency was added for unit testing.

```xml
<dependency>
  <groupId>junit</groupId>
  <artifactId>junit</artifactId>
  <version>4.13.2</version>
  <scope>test</scope>
</dependency>
```

Maven automatically downloads required libraries from Maven Central.

---

## 🚀 Task 4: Build the Project Using Maven

The project was built using the following command:

```bash
mvn clean package
```

### Maven Lifecycle:

* `clean` → Removes previous builds
* `compile` → Compiles source code
* `test` → Runs unit tests
* `package` → Generates JAR file

---

## ✅ Task 5: Verify Build Output

After a successful build, Maven generates output inside the `target/` directory.

```bash
ls target/
```

Expected output:

```
Java-Maven-1.0-SNAPSHOT.jar
```

This confirms the build was successful.

---

## 📊 Expected Outcome (Achieved)

* Maven project created successfully
* Dependencies managed via `pom.xml`
* Build lifecycle executed without errors
* JAR artifact generated

---

## 📌 GitHub Repository

🔗 [https://github.com/ankumpetvimala/Java-Maven](https://github.com/ankumpetvimala/Java-Maven)

---

✅ **Project Status: Completed Successfully**

## Screenshots
![Build Success] <img width="1366" height="768" alt="Build sucess" src="https://github.com/user-attachments/assets/44d18d6e-4842-4242-8f78-e402531fbae8" /> 
<img width="1366" height="768" alt="Hello snapshot" src="https://github.com/user-attachments/assets/3efad0c3-a32c-473b-805e-309d3fcf7a97" />




## 🧠 Challenges and Key Learning

* **Challenge**: Ensuring Jenkins could access the project files in the Docker container.
* **Solution**: Copied files to the Jenkins workspace using `docker cp`.
* **Learning**: Understood how Jenkins integrates with Maven and the importance of console output for debugging.
* Maven standard project structure
* Dependency management
* Build automation using Maven lifecycle
* CI-ready Java project




