# Task Tracker

Task Tracker is a modern, user-friendly task management application built with **Spring Boot** and a responsive frontend. It allows users to create, read, update, and delete tasks with a clean UI powered by **Tailwind CSS** (via CDN) and **Inter font**. The app features server-side and client-side validation, accessibility, and a smooth user experience with animations.

## Features
- **CRUD Operations**: Add, view, edit, and delete tasks.
- **Validation**: Ensures title (required, max 100 chars) and description (max 500 chars) meet requirements.
- **Responsive UI**: Adapts to mobile and desktop with Tailwind CSS.
- **Animations**: Fade-in task cards, hover effects, and modal transitions.
- **Accessibility**: ARIA attributes for screen reader support.
- **H2 Database**: In-memory database for task storage.
- **Task Count**: Displays total tasks in the header.

## Prerequisites
- **Java 21**: [Download JDK 21](https://www.oracle.com/java/technologies/downloads/#java21)
- **Maven**: Included in STS 4 or install from [maven.apache.org](https://maven.apache.org/)
- **Spring Tool Suite 4 (STS 4)**: [Download](https://spring.io/tools)
- **Git**: [Download](https://git-scm.com/)
- **Internet**: For Tailwind CSS CDN and Google Fonts

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/imrajeevnayan/Task-Tracker.git
   cd Task-Tracker