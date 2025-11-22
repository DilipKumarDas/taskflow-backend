# TaskFlow Backend

TaskFlow Backend is a Spring Boot REST API that powers the TaskFlow application.  
It manages tasks, supports status updates, and exposes endpoints for CRUD operations.

---

## 🚀 Features

- Create a task  
- Retrieve all tasks  
- Retrieve a task by ID  
- Update a task  
- Update task status  
- Delete a task  
- CORS enabled for frontend integration  

---

## 🛠 Tech Stack

- **Java 21**
- **Spring Boot 3**
- **Spring Data JPA**
- **PostgreSQL**
- **Maven**
- **Docker**
- **Render Deployment**

---

## 📁 Project Structure

taskflow-backend/
├── src/main/java/com/sample/task_tracker/
│ ├── controller/
│ ├── entity/
│ ├── repository/
│ ├── service/
│ └── TaskTrackerApplication.java
├── src/main/resources/
│ └── application.properties
├── pom.xml
└── Dockerfile


---

## ▶️ Running Locally

### **1. Clone the repository**
```bash
git clone https://github.com/DilipKumarDas/taskflow-backend.git
cd taskflow-backend

2. Configure PostgreSQL

Update src/main/resources/application.properties:

spring.datasource.url=************
spring.datasource.username=***********
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update

3. Run the application

./mvnw spring-boot:run

🐳 Running with Docker
Build the image

docker build -t taskflow-backend .

Run the container

docker run -p 8080:8080 taskflow-backend

🌐 API Endpoints

Base URL:

/tasks

Method	    Endpoint	            Description
POST	     /tasks	                Create task
GET	       /tasks	                Get all tasks
GET	       /tasks/{id}	          Get task by ID
PUT	       /tasks/{id}	          Update task
PUT	       /tasks/{id}/{status}	  Update status
DELETE	   /tasks/{id}	          Delete task
