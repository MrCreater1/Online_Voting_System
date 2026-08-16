
# 🗳️ Online Voting System

A web-based **Online Voting System** developed using **Java, Spring Boot, Thymeleaf, MySQL, HTML, CSS and Bootstrap**.

The application allows voters to register, log in, view their profile, and cast their vote online. An administrator can manage and monitor the voting system.

---

## 📌 Features

### 👤 Voter

- Voter registration
- Voter login
- User dashboard
- View voter details
- View voting status
- Cast vote
- Prevent multiple voting
- Logout

### 👨‍💼 Admin

- Admin login
- Admin dashboard
- View/manage voting information
- Monitor voters and voting activity
- Logout

---

## 🛠️ Technologies Used

### Backend

- Java
- Spring Boot
- Spring MVC
- Spring Data JPA
- Hibernate
- Maven

### Frontend

- HTML5
- CSS3
- Thymeleaf

### Database

- MySQL

### Tools

- IntelliJ IDEA
- MySQL Workbench
- Git
- GitHub

---

# 🚀 How to Run the Project

## 1. Requirements

Make sure the following are installed:

- Java JDK
- Maven
- MySQL
- Eclipse / Spring Tool Suite / IntelliJ IDEA
- Git (optional)

Check Java:

```bash
java -version
````

Check Maven:

```bash
mvn -version
```

---

## 2. Download the Project

Clone the repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Then open the project in your IDE.

---

## 3. Create the MySQL Database

Open MySQL Workbench or MySQL Command Line.

```sql
CREATE DATABASE online_voting;
```

---

## 4. Configure Database

Open:

```text
src/main/resources/application.properties
```

Update your MySQL username and password:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/online_voting
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

spring.thymeleaf.cache=false
```

Replace `YOUR_PASSWORD` with your MySQL password.

---

## 5. Run the Application

Run the main Spring Boot application from your IDE.

Or use:

```bash
mvn spring-boot:run
```

---

# 🌐 How to See the Project

After successfully starting the application, open your browser:

```text
http://localhost:8080/
```

This will open the **Online Voting home page**.

---

## 👤 Voter Registration

From the home page, click:

```text
Register
```

or open:

```text
http://localhost:8080/register
```

Create a new voter account.

---

## 🔐 Voter Login

Open:

```text
http://localhost:8080/signin
```

Enter your registered email and password.

After successful login, you will be redirected to the voter dashboard.

---

## 🗳️ Voter Dashboard

The dashboard allows voters to:

* View their details
* Check voting status
* Select a candidate
* Submit their vote

### Voting Flow

```text
Home
  ↓
Register
  ↓
Login
  ↓
User Dashboard
  ↓
Select Candidate
  ↓
Submit Vote
```

---

# 👨‍💼 Admin

The admin section can be accessed through the admin login configured in the application.

Example:

```text
http://localhost:8080/admin/
```

The exact admin URL may depend on the controller mappings in the project.

---

# 📂 Project Structure

```text
Online-Voting-System
│
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.example
│   │   │       ├── controller
│   │   │       ├── entity
│   │   │       ├── repository
│   │   │       └── service
│   │   │
│   │   └── resources
│   │       ├── static
│   │       │   ├── css
│   │       │   ├── js
│   │       │   └── image
│   │       │
│   │       ├── templates
│   │       │   ├── home.html
│   │       │   ├── signin.html
│   │       │   ├── register.html
│   │       │   │
│   │       │   ├── user
│   │       │   │   ├── base.html
│   │       │   │   ├── dashboard.html
│   │       │   │   └── about.html
│   │       │   │
│   │       │   └── admin
│   │       │       ├── base.html
│   │       │       └── dashboard.html
│   │       │
│   │       └── application.properties
│   │
│   └── test
│
├── pom.xml
└── README.md
```

> The exact package and file names may differ depending on your project structure.

---

# 🔄 Application Flow

```text
                    Online Voting System
                            │
                            ▼
                         Home Page
                            │
                  ┌─────────┴─────────┐
                  ▼                   ▼
               Register              Login
                  │                   │
                  ▼                   ▼
             Create Account      Authentication
                                      │
                              ┌───────┴────────┐
                              ▼                ▼
                            User             Admin
                              │                │
                              ▼                ▼
                       User Dashboard    Admin Dashboard
                              │
                              ▼
                         Select Candidate
                              │
                              ▼
                          Submit Vote
                              │
                              ▼
                       Voting Completed
```

---

# 🔐 Database

The application uses MySQL to store application data.

Database:

```text
online_voting
```

Tables are created/updated automatically by Hibernate when using:

```properties
spring.jpa.hibernate.ddl-auto=update
```

---

# ⚙️ Common Problems

## Port 8080 Already in Use

Change the port in `application.properties`:

```properties
server.port=8081
```

Then open:

```text
http://localhost:8081/
```

---

## MySQL Connection Error

Check:

```properties
spring.datasource.url
spring.datasource.username
spring.datasource.password
```

Make sure MySQL Server is running.

---

## Page Not Found

Check:

* Controller mapping
* Thymeleaf template name
* Template location
* Browser URL

For example:

```java
@GetMapping("/about")
public String about() {
    return "about";
}
```

normally corresponds to:

src/main/resources/templates/about.html




# 📸 Screenshots

You can add screenshots of the project here.

Example:

```text
screenshots/
├── home.png
├── register.png
├── login.png
├── user-dashboard.png
└── admin-dashboard.png
```

Then add them:

```markdown
![Home Page](screenshots/home.png)
```

---

# 🔮 Future Improvements

Possible improvements:

* JWT-based authentication
* Spring Security
* Password encryption
* Candidate management
* Election management
* Admin analytics dashboard
* Real-time election results
* Email verification
* OTP authentication
* AWS deployment
* Docker support
* REST API
* React.js frontend



# 📄 License

This project is developed for educational and academic purposes.


