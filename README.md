Task Tracker
Task Tracker is a modern, user-friendly task management application built with Spring Boot and a responsive frontend. It allows users to create, read, update, and delete tasks with a clean UI powered by Tailwind CSS (via CDN) and Inter font. The app features server-side and client-side validation, accessibility, and a smooth user experience with animations.
Features

CRUD Operations: Add, view, edit, and delete tasks.
Validation: Ensures title (required, max 100 chars) and description (max 500 chars) meet requirements.
Responsive UI: Adapts to mobile and desktop with Tailwind CSS.
Animations: Fade-in task cards, hover effects, and modal transitions.
Accessibility: ARIA attributes for screen reader support.
H2 Database: In-memory database for task storage.
Task Count: Displays total tasks in the header.

Prerequisites

Java 21: Download JDK 21
Maven: Included in STS 4 or install from maven.apache.org
Spring Tool Suite 4 (STS 4): Download
Git: Download
Internet: For Tailwind CSS CDN and Google Fonts

Setup Instructions

Clone the Repository:git clone https://github.com/imrajeevnayan/Task-Tracker.git
cd Task-Tracker


Open in STS 4:
Go to File > Import > Maven > Existing Maven Projects.
Select the Task-Tracker folder > Finish.
Right-click project > Maven > Update Project > OK.


Run the Application:
Right-click TaskTrackerApplication.java > Run As > Spring Boot App.
Open http://localhost:8080 in a browser.



Usage

Access: Visit http://localhost:8080 to see the Task Tracker UI.
Create Task: Enter a title and optional description, check completion status, and click Add Task.
View Tasks: Tasks display with creation/update timestamps and completion status.
Edit Task: Click Edit to modify in a modal or Toggle to change completion.
Delete Task: Click Delete to remove a task.
H2 Console: Access http://localhost:8080/h2-console (JDBC URL: jdbc:h2:mem:tasktracker, Username: sa, Password: blank) to view tasks.

For detailed documentation, see HELP.md.
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


pom.xml: Maven dependencies (Spring Boot, H2, Validation).
index.html: Single frontend file with Tailwind CSS and JavaScript.
HELP.md: Detailed setup and troubleshooting guide.

Future Enhancements

Authentication: Add Spring Security for user login (planned).
Persistent Database: Switch to MySQL or PostgreSQL.
Search and Filter: Add task search functionality.
Production CSS: Replace Tailwind CDN with compiled CSS.

Contributing

Fork the repository.
Create a branch: git checkout -b feature-name.
Commit changes: git commit -m "Add feature-name".
Push: git push origin feature-name.
Create a pull request.

Troubleshooting

Styles Not Loading: Ensure internet access for CDN.
API Errors: Check TaskController.java and STS 4 logs.
Git Issues: Resolve conflicts with git pull origin main --rebase.
STS 4: Refresh project (F5) or clear .metadata in workspace.

License
MIT License. See LICENSE for details.