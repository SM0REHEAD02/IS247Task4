# Dockerized Java App with GitHub Actions CI/CD  
**Automatically build, push, and deploy a Java app to Docker Hub using GitHub Actions.**  

## 📌 Overview  
This project demonstrates:  
- Dockerizing a simple Java application (`HelloWorld.java`).  
- Automating builds/pushes to Docker Hub via GitHub Actions.  
- Using GitHub Secrets for secure credential management.  

## 🛠️ Prerequisites  
1. Docker Hub account ([sign up here](https://hub.docker.com/)).  
2. GitHub repository with Java code and `Dockerfile`.  

## 🔧 Setup  
### 1. Dockerfile  
```dockerfile
FROM openjdk:23
WORKDIR /app
COPY src/ /app/
RUN javac *.java
CMD ["java", "HelloWorld"]
