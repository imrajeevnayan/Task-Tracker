Task Tracker - Help Documentation
Overview
Task Tracker is a Spring Boot application for managing tasks with a modern, responsive frontend. The application supports CRUD operations (Create, Read, Update, Delete) for tasks, with server-side and client-side validation, a beautiful UI using Tailwind CSS (via CDN), and accessibility features.

Backend: Spring Boot 3.5.4, Java 21, H2 in-memory database, Spring Data JPA, Spring Validation.
Frontend: Single index.html with embedded Tailwind CSS, Inter font, animations, and JavaScript for CRUD operations.
Features: Add, view, edit, toggle, and delete tasks; task count display; loading states; responsive design.

Prerequisites

Java 21: Install JDK 21.
Maven: Included in Spring Tool Suite 4 (STS 4) or install from maven.apache.org.
STS 4: Recommended IDE, download from spring.io/tools.
Git: Install from git-scm.com for cloning and version control.
Internet: Required for Tailwind CSS CDN and Google Fonts in index.html.

Setup Instructions

Clone the Repository:
git clone https://github.com/your-username/task-tracker.git
cd task-tracker

Replace your-username with your GitHub username.

Open in STS 4:

Launch STS 4.
Go to File > Import > Maven > Existing Maven Projects.
Select the task-tracker folder > Finish.
Right-click project > Maven > Update Project > OK to resolve dependencies.


Verify Project Structure:
task-tracker/
├── .gitignore
├── HELP.md
├── pom.xml
├── src/
│   ├── main/
│   │   ├── java/com/example/tasktracker/
│   │   │   ├── controller/TaskController.java
│   │   │   ├── model/Task.java
│   │   │   ├── repository/TaskRepository.java
│   │   │   ├── service/TaskService.java
│   │   │   ├── TaskTrackerApplication.java
│   │   ├── resources/
│   │       ├── static/index.html
│   │       ├── application.properties


Run the Application:

Right-click TaskTrackerApplication.java > Run As > Spring Boot App.
Access http://localhost:8080 in a browser.



Usage

Access the App:

Open http://localhost:8080 to view the Task Tracker interface.
The UI features a gradient background, task cards with hover effects, and a modal for editing tasks.


CRUD Operations:

Create: Enter a title (required, max 100 characters), description (optional, max 500 characters), and completion status. Click Add Task.
Read: Tasks load automatically with creation/update timestamps and completion status.
Update: Click Edit to modify a task in a modal or Toggle to change completion status.
Delete: Click Delete to remove a task.
Validation: Client-side and server-side validation ensures title is not empty and within length limits.


H2 Database Console:

Access http://localhost:8080/h2-console.
Use JDBC URL: jdbc:h2:mem:tasktracker, Username: sa, Password: (blank).
Run SELECT * FROM TASK; to view tasks.


Test with Postman:

Create Task:curl -X POST http://localhost:8080/api/tasks -H "Content-Type: application/json" -d '{"title":"Test Task","description":"Test","completed":false}'


Validation Error:curl -X POST http://localhost:8080/api/tasks -H "Content-Type: application/json" -d '{"title":"","description":"Test"}'

Expected response: {"title":"Title is required"}



Project Structure

pom.xml: Maven dependencies (Spring Boot, H2, Validation).
src/main/java/com/example/tasktracker/:
Task.java: Task entity with validation (@NotBlank, @Size).
TaskController.java: REST API endpoints (/api/tasks).
TaskService.java: Business logic for task operations.
TaskRepository.java: JPA repository for database access.
TaskTrackerApplication.java: Main Spring Boot application.


src/main/resources/static/index.html: Single frontend file with Tailwind CSS (CDN), Inter font, and JavaScript for CRUD.
src/main/resources/application.properties: Configures H2 database.
.gitignore: Excludes build outputs, IDE files, and logs.

Styling

Tailwind CSS: Loaded via CDN (https://cdn.tailwindcss.com).
Custom Styles: Embedded in index.html for spinner, modal transitions, and task card animations.
Typography: Inter font via Google Fonts.
Responsive Design: Adapts to mobile/desktop with Tailwind’s responsive classes.
Animations: Fade-in for tasks, hover effects for cards, and smooth modal transitions.

Troubleshooting

.gitignore Not Visible:
In STS 4, enable hidden files: Package Explorer > View Menu > Filters and Customization > Uncheck . resources*.
In terminal: ls -a to confirm .gitignore exists.


Styles Not Loading:
Ensure internet access for Tailwind CDN and Google Fonts.
Check browser console (F12) for errors.
Fallback: Remove Google Fonts link to use system fonts (font-sans).


API Errors:
Verify /api/tasks endpoints in TaskController.java.
Check STS 4 console logs for errors.
Run mvn clean install to resolve dependency issues.


Validation Issues:
Confirm spring-boot-starter-validation in pom.xml and @NotBlank in Task.java.
Test with Postman for server-side validation errors.


STS 4 Issues:
Refresh project: Right-click > Refresh or F5.
Clear IDE cache: Close STS 4, delete .metadata in workspace, restart.



Future Enhancements

Authentication: Add Spring Security for user login (JWT-based).
Persistent Database: Switch to MySQL or PostgreSQL.
Search and Filter: Add a search bar and backend filtering.
Production CSS: Replace Tailwind CDN with compiled CSS using Tailwind CLI.

Contributing

Fork the repository.
Create a branch: git checkout -b feature-name.
Commit changes: git commit -m "Add feature-name".
Push to GitHub: git push origin feature-name.
Create a pull request.

License
MIT License. See LICENSE for details.