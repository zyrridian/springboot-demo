# springboot-demo

This is a simple Spring Boot demo application backed by a MySQL database using Docker Compose.

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- [Java 17+](https://adoptopenjdk.net/)
- [Maven](https://maven.apache.org/install.html)
- [Docker](https://www.docker.com/)

---

## 🧰 Setup & Run

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/springboot-demo.git
cd springboot-demo
```

### 2. Install Dependencies

Run the following Maven command to build the project and skip running tests:

```bash
mvn clean install -DskipTests
```

### 3. Start Docker Containers

This will spin up the MySQL database defined in your `docker-compose.yml`:

```bash
docker-compose up --build
```

---

## 🧪 Testing the API

### Create a User

```bash
curl -X POST http://localhost:8080/api/users -H "Content-Type: application/json" -d "{\"name\": \"Alice\", \"email\": \"alice@example.com\"}"
```

### Get All Users

```bash
curl http://localhost:8080/api/users
```

---

## 📝 Notes

- If you face any DB connection issues, ensure MySQL container is fully started and the DB credentials in your `application.properties` match those in `docker-compose.yml`.
- Ports and endpoints can be configured as needed.

---

