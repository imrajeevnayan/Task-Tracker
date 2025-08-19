# Task-Tracker

**Task Tracker**  is a modern, user-friendly task management application built with Spring Boot and a responsive frontend. It allows users to create, read, update, and delete tasks with a clean UI powered by Tailwind CSS (via CDN) and Inter font. The app features server-side and client-side validation, accessibility, and smooth animations. 🚀

## ✨ Features

- 📋 **CRUD Operations** – Create, read, update, and delete tasks easily.
- ✅ **Validation** – Ensures title (required, max 100 chars) and description (max 500 chars) meet standards.
- 📱 **Responsive Design** – Works great on both mobile and desktop devices.
- 🎨 **Animations** – Smooth transitions, fade-in cards, and interactive modals.
- ♿ **Accessibility** – ARIA attributes ensure screen reader compatibility.
- 💾 **In-Memory Database** – Uses H2 for quick development/testing.
- 🔢 **Task Counter** – Displays total number of tasks.
- 🌐 **REST API** – Fully API-driven backend, ideal for integration.

## 🖼️ Project Screenshot

Here's what Task Tracker looks like in action:

![Task Tracker Screenshot](Screenshot.png)


## 🎥 Demo

Live demo  on Render. Click here [Live Link](https://task-tracker-2ez1.onrender.com/). 📽️

## 🛠️ Tech Stack

### Backend
- Spring Boot 3.5.4
- Java 21
- Spring Data JPA
- H2 Database (in-memory)
- Spring Validation

### Frontend
- HTML5 (`index.html`)
- Tailwind CSS (via CDN)
- Inter font (via Google Fonts)
- JavaScript

### Tools
- Maven
- Spring Tool Suite 4 (STS 4)
- Git

---

## 📋 Prerequisites

- [Java 21](https://jdk.java.net/21/)
- [Maven](https://maven.apache.org/)
- [Spring Tool Suite 4](https://spring.io/tools)
- [Git](https://git-scm.com/)
- Internet access (for Tailwind CSS and Google Fonts)

---

## ⚙️ Setup Instructions

1. **Clone the Repository**

```bash
git clone https://github.com/imrajeevnayan/Task-Tracker.git
cd Task-Tracker
```
 ** Create a Dockerfile in the project root:**
 
 ```
 # Build stage
FROM maven:3.9.9-eclipse-temurin-21 AS build
WORKDIR /app
COPY pom.xml .
COPY src ./src
RUN mvn clean package -DskipTests

# Package stage
FROM eclipse-temurin:21-jre-alpine
WORKDIR /app
COPY --from=build /app/target/task-tracker-0.0.1-SNAPSHOT.jar app.jar
ENV PORT=8080
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "app.jar"]

 ```


## 📁 Project Structure

```
Task-Tracker/
├── .gitattributes
├── .gitignore
├── .mvn
    └── wrapper
    │   └── maven-wrapper.properties
├── LICENSE
├── README.md
├── Screenshot.png
├── mvnw
├── mvnw.cmd
├── pom.xml
└── src
    ├── main
        ├── java
        │   └── com
        │   │   └── example
        │   │       └── tasktracker
        │   │           ├── TaskTrackerApplication.java
        │   │           ├── controller
        │   │               └── TaskController.java
        │   │           ├── model
        │   │               └── Task.java
        │   │           ├── repository
        │   │               └── TaskRepository.java
        │   │           └── service
        │   │               └── TaskService.java
        └── resources
        │   ├── application.properties
        │   └── static
        │       └── index.html
    └── test
        └── java
            └── com
                └── example
                    └── tasktracker
                        └── TaskTrackerApplicationTests.java


```
### Open in STS 4

- Go to: File > Import > Maven > Existing Maven Projects
-  Select the Task-Tracker folder > Click Finish
- Right-click project > Maven > Update Project > Click OK
- Run the Application
- Right-click TaskTrackerApplication.java > Run As > Spring Boot App
- Open your browser at: http://localhost:8080
 🌍
 
### 🚀 Usage

- Access: Visit http://localhost:8080
- Create Task: Fill title (required), description, and status → Click Add Task
- Edit Task: Click Edit or Toggle to modify
- Delete Task: Click Delete 🗑️
- H2 Console: http://localhost:8080/h2-console
- JDBC URL: jdbc:h2:mem:tasktracker
- Username: sa
- Password: (blank)


### 🧪 Testing the API

Use Postman or cURL:

Get all tasks
```
curl http://localhost:8080/api/tasks
```


- Create a task
```
curl -X POST http://localhost:8080/api/tasks \
-H "Content-Type: application/json" \
-d '{"title":"Test Task","description":"Test description","completed":false}'
```

- Update a task (replace 1 with task ID)
```
curl -X PUT http://localhost:8080/api/tasks/1 \
-H "Content-Type: application/json" \
-d '{"title":"Updated Task","description":"Updated","completed":true}'
```

- Delete a task

```
curl -X DELETE http://localhost:8080/api/tasks/1
```


- Validation error example
```
curl -X POST http://localhost:8080/api/tasks \
-H "Content-Type: application/json" \
-d '{"title":"","description":"Test"}'
```

- Expected Response:
```

{"title":"Title is required"
```
### 🌐 Deployment

- Deployment to Heroku/Render is planned.

- Upcoming Steps:

- Switch to persistent DB (e.g., PostgreSQL)

- Compile Tailwind for production (using Tailwind CLI)

## Package app:
``mvn package``

#🔮 Future Enhancements

- 🔐 Add authentication with Spring Security (JWT)

- 💾 Use persistent DB (MySQL/PostgreSQL)

- 🔍 Search & filter tasks

- 🎨 Replace Tailwind CDN with compiled CSS

- 📄 Add pagination or infinite scroll

## 🛠️ Built With

- **JAVA** - Primary programming language

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Development Process

- Fork the repository
- Create your feature branch (`git checkout -b feature/amazing-feature`)
- Make your changes
- Add tests for your changes
- Ensure all tests pass
- Commit your changes (`git commit -m 'Add some amazing feature'`)
- Push to the branch (`git push origin feature/amazing-feature`)
- Open a Pull Request

### Code Style

- Follow the existing code style
- Run the linter before submitting: `npm run lint`
- Write meaningful commit messages
- Add tests for new features

### Reporting Issues

- Use the GitHub issue tracker
- Provide detailed information about the bug
- Include steps to reproduce the issue
- Add relevant labels



## 📄 License

This project is licensed under the MIT License License - see the [LICENSE](LICENSE) file for details.

### License Summary

The MIT License license is a permissive license that allows for commercial use, modification, distribution, and private use.

## 👥 Authors

- **imrajeevnayan** - *Project Creator* - [@imrajeevnayan](https://github.com/imrajeevnayan)

## 🙏 Acknowledgments

- Thanks to all contributors who have helped shape this project
- Inspired by the open-source community
- Built with ❤️ and modern development practices

## 📊 Project Stats

- ⭐ Stars: 0
- 🍴 Forks: 0
- 🐛 Issues: 0
- 📝 Language: JAVA

---

⭐️ If you found this project helpful, please give it a star!

