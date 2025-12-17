# DigitalOcean Nexus Deployment Demo Project

## Project Overview

This project demonstrates the deployment of Nexus on a DigitalOcean server and the process of publishing artifacts from Java Gradle and Maven projects.

**Technologies Used:** DigitalOcean, Linux, Java, Gradle, Maven, Nexus

## Setup and Configuration

### 1. DigitalOcean Droplet

* Created Ubuntu Droplet on DigitalOcean.
* Configured a new Linux user `demo` for secure access.

### 2. Nexus Installation

* Installed Nexus Repository Manager on the Droplet.
* Configured Nexus from scratch.
* Created a user in Nexus with appropriate permissions.

### 3. Java Projects

#### Gradle Project

* Project located in `gradle-app/java-app`.
* Built JAR using `gradle build`.
* Uploaded built artifact to Nexus.

#### Maven Project

* Project located in `maven-app`.
* Built JAR using `mvn package`.
* Uploaded built artifact to Nexus.

## Repository Structure

```
.digitalocean-nexus-deployment/
├─ gradle-app/
│  └─ java-app/
├─ maven-app/
├─ .gitignore
└─ README.md
```

* `gradle-app/java-app`: Java Gradle project for Nexus deployment.
* `maven-app`: Java Maven project for Nexus deployment.
* `.gitignore`: Excludes build artifacts and IDE files.
* `README.md`: Project documentation.

## Notes

* The repository contains only source code and configuration.
* Build artifacts (JARs, `build/`, `target/`) are excluded via `.gitignore`.
* The server/Droplet does not need to be active for reviewers to assess the project.

## How to Run Locally

1. Clone the repository.
2. Navigate to the project folder (`gradle-app/java-app` or `maven-app`).
3. Build the project:

   * Gradle: `./gradlew build` (Linux/macOS) or `gradlew.bat build` (Windows)
   * Maven: `mvn package`
4. Deploy the JAR to your Nexus instance if desired.

---

**End of Nexus Deployment Demo Project**
