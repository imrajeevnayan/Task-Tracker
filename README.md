Task Tracker
Task Tracker is a modern, user-friendly task management application built with Spring Boot and a responsive single-page frontend. It enables users to perform CRUD operations (Create, Read, Update, Delete) on tasks through a clean, intuitive UI powered by Tailwind CSS (via CDN) and Inter font. The app emphasizes server-side and client-side validation, accessibility, and a smooth user experience with animations.
Features

CRUD Operations: Add, view, edit, and delete tasks effortlessly.
Validation: Enforces title (required, max 100 characters) and description (max 500 characters) constraints.
Responsive UI: Adapts seamlessly to mobile and desktop using Tailwind CSS.
Animations: Includes fade-in task cards, hover effects, and modal transitions.
Accessibility: Implements ARIA attributes for screen reader compatibility.
H2 Database: Uses an in-memory database for task persistence.
Task Count: Displays total tasks in the header.
API-Driven: Backend REST API supports integration with external tools.

Demo
Coming soon: A live demo will be hosted on a platform like Render or Heroku. Check Releases for updates!
Tech Stack

Backend:
Spring Boot 3.5.4
Java 21
Spring Data JPA
H2 Database (in-memory)
Spring Validation


Frontend:
HTML5 (index.html)
Tailwind CSS (via CDN)
Inter font (via Google Fonts)
JavaScript (for CRUD operations and dynamic UI)


Tools:
Maven (dependency management)
Spring Tool Suite 4 (STS 4)
Git (version control)



Prerequisites

Java 21: Download JDK 21
Maven: Included in STS 4 or install from maven.apache.org
Spring Tool Suite 4 (STS 4): Download
Git: Download
Internet: Required for Tailwind CSS CDN and Google Fonts

Setup Instructions

Clone the Repository:
git clone https://github.com/imrajeevnayan/Task-Tracker.git
cd Task-Tracker


Open in STS 4:

Go to File > Import > Maven > Existing Maven Projects.
Select the Task-Tracker folder > Finish.
Right-click project > Maven > Update Project > OK.


Run the Application:

Right-click TaskTrackerApplication.java > Run As > Spring Boot App.
Open http://localhost:8080 in a browser.



Usage

Access: Visit http://localhost:8080 to view the Task Tracker UI.

Create Task: Enter a title (required), optional description, and completion status, then click Add Task.

View Tasks: Tasks display with creation/update timestamps and completion status.

Edit Task: Click Edit to modify in a modal or Toggle to change completion status.

Delete Task: Click Delete to remove a task.

H2 Console: Access http://localhost:8080/h2-console (JDBC URL: jdbc:h2:mem:tasktracker, Username: sa, Password: blank) to query tasks with:
SELECT * FROM TASK;



For detailed setup, usage, and troubleshooting, see HELP.md.
Testing
Test the backend REST API using Postman or cURL:

Get All Tasks:
curl http://localhost:8080/api/tasks


Create Task:
curl -X POST http://localhost:8080/api/tasks -H "Content-Type: application/json" -d '{"title":"Test Task","description":"Test description","completed":false}'


Update Task (replace 1 with task ID):
curl -X PUT http://localhost:8080/api/tasks/1 -H "Content-Type: application/json" -d '{"title":"Updated Task","description":"Updated","completed":true}'


Delete Task (replace 1 with task ID):
curl -X DELETE http://localhost:8080/api/tasks/1


Validation Error:
curl -X POST http://localhost:8080/api/tasks -H "Content-Type: application/json" -d '{"title":"","description":"Test"}'

Expected response: {"title":"Title is required"}


Deployment
Coming soon: Instructions for deploying to platforms like Heroku, AWS, or Render. Planned steps include:

Configure a persistent database (e.g., PostgreSQL).
Compile Tailwind CSS for production using Tailwind CLI.
Package the app with mvn package to generate a JAR file.

Project Structure
Task-Tracker/
├── .gitignore
├── README.md
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


pom.xml: Defines Maven dependencies (Spring Boot, H2, Validation).
index.html: Single frontend file with Tailwind CSS and JavaScript.
HELP.md: Detailed documentation for setup and troubleshooting.
.gitignore: Excludes build outputs, IDE metadata, and logs.

Future Enhancements

Authentication: Implement Spring Security with JWT-based user authentication (planned).
Persistent Database: Transition to MySQL or PostgreSQL for production.
Search and Filter: Add a search bar and backend filtering for tasks.
Production CSS: Replace Tailwind CDN with compiled CSS via Tailwind CLI.
Pagination: Support large task lists with pagination or infinite scroll.

FAQ

Why aren’t styles loading?Ensure internet access for Tailwind CSS CDN and Google Fonts. Check browser console (F12) for errors. Fallback: Remove Google Fonts to use system fonts (font-sans).
Why do I get API errors?Verify TaskController.java endpoints and STS 4 logs. Run mvn clean install to resolve dependency issues.
Why isn’t README.md showing on GitHub?Ensure the file is named README.md (case-sensitive), committed, and pushed. Check .gitignore for *.md or README.md. Run git status to verify.

Contributing

Fork the repository: https://github.com/imrajeevnayan/Task-Tracker.
Create a branch: git checkout -b feature-name.
Commit changes: git commit -m "Add feature-name".
Push: git push origin feature-name.
Create a pull request on GitHub.

Changelog

Initial Release (August 2025):
Implemented CRUD operations with Spring Boot backend.
Built responsive UI with Tailwind CSS and JavaScript.
Added server-side/client-side validation.
Included HELP.md and README.md for documentation.



License
MIT License. See LICENSE for details.