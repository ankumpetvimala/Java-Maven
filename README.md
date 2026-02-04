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
* Jenkins (CI – optional)
* Linux (Ubuntu)

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

## 🔁 (Optional) Jenkins CI Integration

This project can be integrated with Jenkins to:

* Pull source code from GitHub
* Run Maven build automatically
* Display build status and logs

---

## 🧠 Key Learning

* Maven standard project structure
* Dependency management
* Build automation using Maven lifecycle
* CI-ready Java project

---

## 📌 GitHub Repository

🔗 [https://github.com/ankumpetvimala/Java-Maven](https://github.com/ankumpetvimala/Java-Maven)

---

## 📝 Interview One-Liner

> I automated the build process of a Java application using Maven by managing dependencies in `pom.xml` and generating build artifacts using Maven lifecycle commands.

---

✅ **Project Status: Completed Successfully**


# Task 8: Java Maven Build with Jenkins on AWS EC2

This repository contains the deliverables for Task 8 of the DevOps Internship, demonstrating a Java Maven build job in Jenkins on an AWS EC2 Ubuntu instance.

## Objective
Build a simple Java HelloWorld app using Maven in a Jenkins Freestyle job, hosted on an EC2 instance.

## Tools Used
- AWS EC2 (Ubuntu 22.04, t2.micro)
- Jenkins (via Docker)
- Java JDK 11
- Maven 3.8.6
- Git

## Steps
1. Launched an EC2 Ubuntu instance with ports 22, 80, and 8080 open.
2. Installed Java, Maven, Docker, and Git.
3. Set up Jenkins in a Docker container.
4. Created a Java HelloWorld app with `pom.xml`.
5. Configured a Jenkins Freestyle job to build the app with Maven (`clean package`).
6. Captured a screenshot of the successful build console output.
7. Documented the process and interview questions.

## Screenshots
![Build Success](build-success.png)

## Challenges and Learnings
- **Challenge**: Ensuring Jenkins could access the project files in the Docker container.
- **Solution**: Copied files to the Jenkins workspace using `docker cp`.
- **Learning**: Understood how Jenkins integrates with Maven and the importance of console output for debugging.

## Interview Questions
See [INTERVIEW.md](INTERVIEW.md) for answers to the task’s interview questions.

## How to Replicate
Follow the steps in this README or refer to the detailed guide in the repository root.

*Best Intern Touch*: This submission is crafted with precision to demonstrate DevOps skills and a commitment to excellence!
