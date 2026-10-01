# Government Welfare Scheme Recommendation System

A full-stack web application that helps users discover government welfare schemes based on their eligibility criteria. Built using **Spring Boot, React, and MySQL**, the system provides user authentication, welfare scheme management, eligibility evaluation, personalized scheme recommendations, and notification services through RESTful APIs.

## 🚀 Features

* **User Authentication** — Provides authentication functionality for users accessing the application.
* **Scheme Management** — Supports managing government welfare scheme information.
* **Eligibility Checking** — Evaluates user eligibility against predefined scheme criteria.
* **Recommendation Engine** — Identifies relevant welfare schemes based on eligibility information.
* **Notification Service** — Provides notification-related functionality to communicate relevant scheme information.
* **RESTful APIs** — Exposes backend functionality through REST APIs.
* **Relational Database** — Uses MySQL to persist application data.
* **Full-Stack Architecture** — Integrates a React frontend with a Spring Boot backend.

## 🛠️ Tech Stack

| Technology  | Purpose                                    |
| ----------- | ------------------------------------------ |
| Java        | Backend programming                        |
| Spring Boot | Backend application and REST APIs          |
| React       | Frontend user interface                    |
| MySQL       | Relational database                        |
| Maven       | Backend dependency and build management    |
| REST APIs   | Communication between frontend and backend |

## 🏗️ Architecture

The application follows a client-server architecture.

```text
                ┌──────────────────────┐
                │      React UI        │
                │   Frontend Client    │
                └──────────┬───────────┘
                           │
                      HTTP / REST
                           │
                ┌──────────▼───────────┐
                │    Spring Boot       │
                │     REST APIs        │
                └──────────┬───────────┘
                           │
                ┌──────────▼───────────┐
                │   Business Logic     │
                │                      │
                │ • Authentication     │
                │ • Scheme Management  │
                │ • Eligibility        │
                │ • Recommendations    │
                │ • Notifications      │
                └──────────┬───────────┘
                           │
                ┌──────────▼───────────┐
                │       MySQL          │
                │   Persistent Data    │
                └──────────────────────┘
```

## ⚙️ Core Modules

### 1. User Management

Handles user-related operations and supports authentication functionality.

### 2. Welfare Scheme Management

Manages scheme information used by the application to identify potentially relevant government benefits.

### 3. Eligibility Evaluation

Evaluates eligibility criteria against user information to determine which schemes may apply.

### 4. Recommendation Engine

Uses eligibility evaluation results to identify and recommend relevant welfare schemes to users.

### 5. Notification Service

Handles notification-related operations within the application.

## 🔄 Application Workflow

1. A user accesses the application through the React frontend.
2. The frontend communicates with the Spring Boot backend through REST APIs.
3. The backend processes user requests and retrieves relevant information from MySQL.
4. The eligibility module evaluates the user's details against scheme criteria.
5. The recommendation module identifies relevant schemes based on the evaluation.
6. The application returns the results to the frontend, where users can view relevant scheme information.

## 📋 Prerequisites

Ensure the following tools are installed:

* Java Development Kit (JDK)
* Maven
* MySQL Server
* Node.js and npm
* Git

## 🖥️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/HagaluruChitra/Goverment_welfare_scheme_recommendation_system.git
cd Goverment_welfare_scheme_recommendation_system
```

### 2. Configure MySQL

Start your MySQL server and create a database for the application.

```sql
CREATE DATABASE welfare_system;
```

Update the database connection settings in your Spring Boot configuration, such as `application.properties`.

Example configuration:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/welfare_system
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}
```

Configure `DB_USERNAME` and `DB_PASSWORD` in your environment before starting the application. Adjust the database name and configuration to match your actual project settings.

### 3. Run the Backend

From the backend project directory, run:

```bash
./mvnw spring-boot:run
```

On Windows, use:

```bash
mvnw.cmd spring-boot:run
```

If the Maven wrapper is unavailable, use:

```bash
mvn spring-boot:run
```

### 4. Run the Frontend

Navigate to the React frontend directory:

```bash
cd frontend
```

Install dependencies and start the development server:

```bash
npm install
npm run dev
```

Use the actual frontend directory and start command defined by your project. For example, some React applications use `npm start` instead of `npm run dev`.

## 🔐 Configuration and Security

* Keep database credentials outside source control.
* Store secrets in environment variables or a suitable secrets manager.
* Do not commit passwords, API keys, or private configuration files.
* Validate user input on the backend.
* Ensure authentication and authorization checks are applied to protected operations.

## 🧪 Testing

Run backend tests using the Maven wrapper:

```bash
./mvnw test
```

On Windows:

```bash
mvnw.cmd test
```

Review the test results before deploying changes.

## 🔮 Future Enhancements

* Advanced recommendation ranking based on user profiles and scheme criteria.
* Expanded automated testing for eligibility and recommendation logic.
* Improved search and filtering for welfare schemes.
* Administrative dashboards and scheme analytics.
* Multilingual support for broader accessibility.
* Deployment with Docker and a cloud hosting platform.

These are potential enhancements, not claims about features already implemented.

## 🎯 Project Objective

The goal of this project is to simplify the discovery of government welfare schemes by bringing scheme information, eligibility evaluation, and personalized recommendations into one accessible application.

## 👩‍💻 Author

**Chitra Hagaluru**

GitHub: [HagaluruChitra](https://github.com/HagaluruChitra)

## 📄 License

Add a license file if you intend to distribute this project under an open-source license.
