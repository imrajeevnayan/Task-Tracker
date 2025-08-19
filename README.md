# Task Tracker 🌟

**Task Tracker** is a sleek, modern task management application built with **Spring Boot** and a responsive single-page frontend. It empowers users to manage tasks efficiently with full CRUD operations, a polished UI powered by **Tailwind CSS**, and thoughtful features like validation, accessibility, and animations. 🚀

---

## ✨ Features

- 📋 **CRUD Operations** – Create, read, update, and delete tasks easily.
- ✅ **Validation** – Ensures title (required, max 100 chars) and description (max 500 chars) meet standards.
- 📱 **Responsive Design** – Works great on both mobile and desktop devices.
- 🎨 **Animations** – Smooth transitions, fade-in cards, and interactive modals.
- ♿ **Accessibility** – ARIA attributes ensure screen reader compatibility.
- 💾 **In-Memory Database** – Uses H2 for quick development/testing.
- 🔢 **Task Counter** – Displays total number of tasks.
- 🌐 **REST API** – Fully API-driven backend, ideal for integration.

---

## 🎥 Demo

Live demo coming soon on Render or Heroku. Stay tuned in [Releases](https://github.com/imrajeevnayan/Task-Tracker/releases). 📽️

---

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

** Open in STS 4**

Go to: File > Import > Maven > Existing Maven Projects

Select the Task-Tracker folder > Click Finish

Right-click project > Maven > Update Project > Click OK

3 **Run the Application **

Right-click TaskTrackerApplication.java > Run As > Spring Boot App

Open your browser at: http://localhost:8080
 🌍
 
 
** 🚀 Usage **

Access: Visit http://localhost:8080

Create Task: Fill title (required), description, and status → Click Add Task

Edit Task: Click Edit or Toggle to modify

Delete Task: Click Delete 🗑️

H2 Console: http://localhost:8080/h2-console

JDBC URL: jdbc:h2:mem:tasktracker

Username: sa

Password: (blank)
```
SELECT * FROM TASK;
```


** 🧪 Testing the API **

Use Postman or cURL:

Get all tasks

curl http://localhost:8080/api/tasks


Create a task

curl -X POST http://localhost:8080/api/tasks \
-H "Content-Type: application/json" \
-d '{"title":"Test Task","description":"Test description","completed":false}'


Update a task (replace 1 with task ID)

curl -X PUT http://localhost:8080/api/tasks/1 \
-H "Content-Type: application/json" \
-d '{"title":"Updated Task","description":"Updated","completed":true}'


Delete a task

curl -X DELETE http://localhost:8080/api/tasks/1


Validation error example

curl -X POST http://localhost:8080/api/tasks \
-H "Content-Type: application/json" \
-d '{"title":"","description":"Test"}'


Expected Response:

{"title":"Title is required"}

 ** 🌐 Deployment  **

Deployment to Heroku/Render is planned.

Upcoming Steps:

Switch to persistent DB (e.g., PostgreSQL)

Compile Tailwind for production (using Tailwind CLI)

Package app:

mvn package

📂 Project Structure
```
Task-Tracker/
├── .gitignore
├── README.md
├── HELP.md
├── pom.xml
├── src/
│   └── main/
│       ├── java/com/example/tasktracker/
│       │   ├── controller/TaskController.java
│       │   ├── model/Task.java
│       │   ├── repository/TaskRepository.java
│       │   ├── service/TaskService.java
│       │   └── TaskTrackerApplication.java
│       └── resources/
│           ├── static/index.html
│           └── application.properties
```
🔮 Future Enhancements

🔐 Add authentication with Spring Security (JWT)

💾 Use persistent DB (MySQL/PostgreSQL)

🔍 Search & filter tasks

🎨 Replace Tailwind CDN with compiled CSS

📄 Add pagination or infinite scroll

❓ FAQ

Q: Why aren’t styles loading?
A: Ensure internet access (for Tailwind CDN & Google Fonts). Check browser console.

Q: API errors?
A: Check controller logs in STS 4 or run mvn clean install.

Q: README not showing on GitHub?
A: Ensure the file is named README.md, committed and pushed. Also check .gitignore.

🤝 Contributing

Fork: https://github.com/imrajeevnayan/Task-Tracker

Create a branch:

git checkout -b feature-name


Commit changes:

git commit -m "Add feature-name"


Push to GitHub:

git push origin feature-name


Open a pull request on GitHub 🌟

📜 Changelog

Initial Release (August 2025):

✅ Full CRUD with Spring Boot

🎨 Responsive UI with Tailwind & JS

🧪 Validation & testing support

📖 Added HELP.md and README.md

📄 License

MIT License – See LICENSE
 for full details.