# Build-Automation-Using-Maven

📌 Project Overview

This project demonstrates Build Automation using Apache Maven for a Java Web Application.
The application is structured as a Maven project and uses GitHub for source code management along with GitHub Actions for CI/CD workflow automation.

The workflow automates:

Building the project using Maven
Packaging the application into a .war file
Uploading/copying the generated artifact automatically

📂 Project Structure
Build-Automation-Using-Maven/
│── .github/
│   └── workflows/
│       └── maven.yml
│
│── src/
│   └── main/
│       └── webapp/
│
│── pom.xml
│── README.md

⚙️ Technologies Used
Java
Maven
GitHub Actions
Apache Tomcat
Git & GitHub


🚀 Maven Build Lifecycle

Maven follows a standard build lifecycle:

mvn validate
mvn compile
mvn test
mvn package
mvn install
Important Command

To build the WAR file:

mvn clean package



Generated file location:

target/*.war
📦 Maven Dependencies

Dependencies are managed inside the pom.xml file.

Example:

<dependencies>
    <dependency>
        <groupId>javax.servlet</groupId>
        <artifactId>javax.servlet-api</artifactId>
        <version>4.0.1</version>
        <scope>provided</scope>
    </dependency>
</dependencies>


🔄 GitHub Actions Workflow

The project contains a GitHub Actions workflow inside:

.github/workflows/
Workflow Features
Automatically triggers on push
Builds Maven project
Generates WAR artifact
Copies WAR file instead of JAR

Example workflow step:

- name: Build with Maven
  run: mvn clean package

- name: Copy WAR File
  run: cp target/*.war deployment/


  
▶️ How to Run Project
Step 1: Clone Repository
git clone https://github.com/dipali-nagesh/Build-Automation-Using-Maven.git
Step 2: Move into Project Directory
cd your-repository
Step 3: Build Project
mvn clean install
Step 4: Deploy WAR File

Copy the generated WAR file from:

target/

to Apache Tomcat webapps folder.

📸 GitHub Repository Screenshot




The repository includes:

.github/workflows
src/main/webapp
pom.xml
README.md

which represent a Maven-based web application structure.

✅ Features
Automated Maven Build
WAR Packaging
CI/CD with GitHub Actions
Easy Deployment
Organized Project Structure


📚 Learning Outcome

By completing this project, you will learn:

Maven Project Structure
Build Automation
Dependency Management
CI/CD Pipeline Setup
GitHub Actions Workflow
WAR Deployment Process


👩‍💻 Author

Dipali Nageshwar
