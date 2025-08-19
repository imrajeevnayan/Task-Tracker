# Task-Tracker

![HTML](https://img.shields.io/badge/HTML-blue?style=for-the-badge) ![License](https://img.shields.io/badge/license-MIT-blue.svg?style=for-the-badge) ![GitHub stars](https://img.shields.io/github/stars/imrajeevnayan/Task-Tracker?style=for-the-badge) ![GitHub forks](https://img.shields.io/github/forks/imrajeevnayan/Task-Tracker?style=for-the-badge)

**Task Tracker** is a sleek, modern task management application built with **Spring Boot** and a responsive single-page frontend. It empowers users to manage tasks efficiently with full CRUD operations, a polished UI powered by **Tailwind CSS**, and thoughtful features like validation, accessibility, and animations. 🚀
## ✨ Features

- 📋 **CRUD Operations** – Create, read, update, and delete tasks easily.
- ✅ **Validation** – Ensures title (required, max 100 chars) and description (max 500 chars) meet standards.
- 📱 **Responsive Design** – Works great on both mobile and desktop devices.
- 🎨 **Animations** – Smooth transitions, fade-in cards, and interactive modals.
- ♿ **Accessibility** – ARIA attributes ensure screen reader compatibility.
- 💾 **In-Memory Database** – Uses H2 for quick development/testing.
- 🔢 **Task Counter** – Displays total number of tasks.
- 🌐 **REST API** – Fully API-driven backend, ideal for integration.


## 🎥 Demo

Live demo coming soon on Render or Heroku. Stay tuned in [Releases](https://github.com/imrajeevnayan/Task-Tracker/releases). 📽️

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



## 📁 Project Structure

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

## 🛠️ Built With

- **HTML** - Primary programming language

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Development Process

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Add tests for your changes
5. Ensure all tests pass
6. Commit your changes (`git commit -m 'Add some amazing feature'`)
7. Push to the branch (`git push origin feature/amazing-feature`)
8. Open a Pull Request

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
- 📝 Language: HTML

---

⭐️ If you found this project helpful, please give it a star!

