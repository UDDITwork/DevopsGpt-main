# 🚀 DevOpsGPT: Your AI-Powered DevOps Companion

![DevOpsGPT Banner](https://img.shields.io/badge/DevOpsGPT-v1.0-blue?style=for-the-badge&logo=spring)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Stars](https://img.shields.io/github/stars/pearch001/DevopsGpt.svg?style=social)](https://github.com/pearch001/DevopsGpt)

Welcome to **DevOpsGPT**, a cutting-edge Spring Boot application that harnesses the power of AI to streamline DevOps, cloud computing, and software engineering tasks. With intelligent responses, Retrieval-Augmented Generation (RAG), and advanced dialogue management, DevOpsGPT is your go-to tool for smarter workflows.

---

## ✨ Features

- **💬 Standard Chat**: Get instant AI-powered answers to your DevOps queries.
- **🔍 Retrieval-Augmented Generation (RAG)**: Context-aware responses backed by relevant documents.
- **🧠 Advanced Chat**: Engage in stateful conversations with enhanced reasoning.
- **📄 Document Ingestion**: Seamlessly process and store documents for RAG-based queries.
- **🩺 Health Check**: Verify the application's status with a simple ping endpoint.

---

## 🛠️ Technologies Used

| Technology       | Purpose                              |
|------------------|--------------------------------------|
| **Java 21**      | Core programming language            |
| **Spring Boot**  | Application framework                |
| **Maven**        | Dependency management and build tool |
| **AWS SDK**      | Integration with AWS services        |
| **Spring AI**    | AI client for chat and vector store  |
| **SLF4J**        | Logging framework                    |

---

## 📋 Prerequisites

Before diving in, ensure you have the following:

- **Java 21**: [Download and install](https://www.oracle.com/java/technologies/javase/jdk21-archive-downloads.html).
- **Maven**: [Install Maven](https://maven.apache.org/install.html) for dependency management.
- **AWS Credentials**: Configure credentials for AWS services like EC2.
- **IDE**: We recommend [IntelliJ IDEA](https://www.jetbrains.com/idea/) for a smooth development experience.

---

## ⚙️ Installation

Get DevOpsGPT up and running in a few simple steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/pearch001/DevopsGpt.git
   cd DevopsGpt
   ```

2. **Build the Project**:
   ```bash
   mvn clean install
   ```

3. **Run the Application**:
   ```bash
   mvn spring-boot:run
   ```

🎉 Your DevOpsGPT instance should now be live and ready to assist!

---

## 🔧 Configuration

### AWS SDK Setup
Configure your AWS credentials in `application.properties`:

```properties
aws.region=us-east-1
aws.accessKeyId=your-access-key-id
aws.secretAccessKey=your-secret-access-key
```

### Logging Configuration
DevOpsGPT uses SLF4J for logging. Customize logging in `application.properties`:

```properties
logging.level.root=INFO
logging.file.name=devopsgpt.log
```

Logs are written to the console by default and saved to `devopsgpt.log`.

---

## 🌐 API Endpoints

### 🩺 Health Check
- **Endpoint**: `GET /api/ping`
- **Response**: `"Pong! DevOpsGPT is running."`

### 💬 Standard Chat
- **Endpoint**: `POST /api/chat`
- **Request Body**:
  ```json
  {
    "sessionId": "unique-session-id",
    "message": "Your query here"
  }
  ```
- **Response**:
  ```json
  {
    "reply": "AI response",
    "sessionId": "unique-session-id"
  }
  ```

### 🔍 RAG Chat
- **Endpoint**: `POST /api/chat/rag`
- **Request Body**:
  ```json
  {
    "sessionId": "unique-session-id",
    "message": "Your query here"
  }
  ```
- **Response**:
  ```json
  {
    "reply": "Context-aware AI response",
    "sessionId": "unique-session-id"
  }
  ```

### 🧠 Advanced Chat
- **Endpoint**: `POST /api/chat/advanced`
- **Request Body**:
  ```json
  {
    "sessionId": "unique-session-id",
    "message": "Your query here"
  }
  ```
- **Response**:
  ```json
  {
    "response": "Enhanced AI response",
    "sessionId": "unique-session-id"
  }
  ```

---

## 📂 Document Ingestion

DevOpsGPT uses the `VectorStoreIngestor` service to process documents for RAG queries. Ensure your documents are correctly formatted and placed in the designated resource directory.

---

## 🛠️ Troubleshooting

### Common Issues

#### `UnsatisfiedDependencyException`
- **Cause**: Missing or misconfigured beans.
- **Solution**: Verify all required beans are defined and dependencies are included in `pom.xml`.

#### `ClientEndpointProvider` Error
- **Cause**: Incompatible AWS SDK version.
- **Solution**: Check the AWS SDK version in `pom.xml` and ensure compatibility.

#### `commons-logging.jar` Conflict
- **Solution**: Exclude `commons-logging` from dependencies in `pom.xml`:

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter</artifactId>
    <exclusions>
        <exclusion>
            <groupId>commons-logging</groupId>
            <artifactId>commons-logging</artifactId>
        </exclusion>
    </exclusions>
</dependency>
```

---

## 🤝 Contributing

We welcome contributions to make DevOpsGPT even better! Follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix: `git checkout -b feature/your-feature`.
3. Commit your changes: `git commit -m "Add your feature"`.
4. Push to your branch: `git push origin feature/your-feature`.
5. Submit a pull request with a detailed description of your changes.

---

## 📜 License

DevOpsGPT is licensed under the [MIT License](https://opensource.org/licenses/MIT). See the `LICENSE` file for details.

---

## 📬 Contact

Have questions or need support? Reach out to [pearch001](https://github.com/pearch001) on GitHub.

---

<p align="center">
  <img src="https://img.shields.io/badge/Powered%20by-Spring%20Boot-green?style=flat-square&logo=spring" alt="Spring Boot">
  <img src="https://img.shields.io/badge/AI-Driven-blue?style=flat-square" alt="AI Driven">
</p>
