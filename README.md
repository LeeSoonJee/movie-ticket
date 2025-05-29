Movie Ticket
Movie Ticket is a comprehensive web application designed for cinema management and ticket booking. Built with Spring Boot, Thymeleaf, and MySQL, it provides a robust admin interface for managing movies, showtimes, user accounts, and theaters, alongside a user-friendly front-end for ticket purchasing, including features like registration, login, password recovery, and PayPal payment integration.
Table of Contents

Overview
Features
Technologies
Prerequisites
Installation
Configuration
Running the Application
Troubleshooting
Contributing
License
Contact

Overview
Movie Ticket is a full-stack application tailored for cinema administrators and customers. Administrators can perform CRUD operations on movies, showtimes, theaters, and user roles, while customers can register, log in, recover passwords, browse movies and theaters, select seats, view booking history, and pay via PayPal. The application features a responsive interface powered by Bootstrap and Thymeleaf.
Features
Admin Features

Authentication
Secure admin login for system management.


User Account Management (CRUD)
Create, update, delete, and view user accounts.
Search accounts by role, creation date, or name.
Manage roles: Admin, User, Customer_Super.


Showtime Management (CRUD)
Add, edit, or remove movie showtimes.
Filter showtimes by date, month, or year.


Role Management
Create, update, or delete user roles.
Filter accounts by role.


Brand Management
Manage cinema brands (add, edit, delete).
Search brands by name and view brand lists.


Location Management
Administer theater locations (add, edit, delete).
Filter locations by province or city.


Movie Management
Add, edit, or delete movie details.
Search movies by title, genre, or release year.
Filter movies by duration or rating.


Theater Room Management
Manage theater rooms (add, edit, delete).
Filter rooms by name, theater, or seating capacity.
Administer seating arrangements (add, edit, delete seats).


Actor and Director Management
Add, edit, or delete actor and director profiles.


Showtime Schedule Management
View showtime schedules and movie durations.
Display status for past showtimes.


Ticket Booking Management
Process ticket bookings and cancellations.
View booking history with details: username, seat numbers, total cost, and seat count.
Search bookings by movie title, user, or time.



User Features

Registration and Login
User registration with email and password.
Secure login for customers.


Password Recovery
Forgot password functionality with email-based recovery.


Movie and Theater Filtering
Filter movies by title, genre, or release year.
Filter theaters by location or name.
Filter showtimes by date.


Booking History
View past and current ticket bookings with details (movie, seats, time, cost).


Seat Selection
Interactive seat selection interface for booking tickets.


Payment Integration
Secure ticket purchasing via PayPal.



Technologies

Java 17: Core programming language.
Spring Boot: Framework for building the application.
Thymeleaf: Server-side templating for dynamic UI.
JPA/Hibernate: ORM for database interactions.
MySQL: Relational database management system.
Bootstrap: Responsive front-end framework.
PayPal SDK: For secure payment processing.
Maven: Dependency management and build tool.
GitHub: Source code hosting and version control.

Prerequisites
Before setting up the project, ensure the following are installed:

Java 17 (JDK)
MySQL (version 8.0 or higher)
Maven (version 3.6 or higher)
Internet connection (for Bootstrap CDN and PayPal API, if used)

Installation

Clone the Repository
git clone https://github.com/NguyenTrieuDaiDuong/movie-ticket.git
cd movie-ticket


Set Up MySQL Database

Install and start MySQL Server.
Create a new database:CREATE DATABASE movie_ticket;




Install Maven Dependencies

Run the following command to download dependencies:mvn clean install





Configuration

Database Configuration

Open src/main/resources/application.properties and configure the MySQL connection:spring.datasource.url=jdbc:mysql://localhost:3308/movie_ticket
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect


Replace your_username and your_password with your MySQL credentials.


PayPal Configuration

Configure PayPal API credentials in application.properties:paypal.client.id=your_paypal_client_id
paypal.client.secret=your_paypal_client_secret
paypal.mode=sandbox  # or 'live' for production


Obtain credentials from PayPal Developer Dashboard.


Optional Configurations

Port: If port 8089 is in use, change it in application.properties:server.port=8088


Static Resources: Ensure Bootstrap CDN is accessible or use local static files in src/main/resources/static.



Running the Application

Start the Application

Run the Spring Boot application:mvn spring-boot:run


Alternatively, build and run the JAR file:mvn clean package
java -jar target/movie-ticket-0.0.1-SNAPSHOT.jar




Access the Application

Open a browser and navigate to: http://localhost:8088
Admin: Log in using admin credentials (check documentation or users table in the database).
Users: Register a new account or log in to access booking features.



Troubleshooting

MySQL Connection Issues: Verify MySQL Server is running and credentials in application.properties are correct.
Port Conflicts: Change the port in application.properties if 8080 is occupied.
Dependency Errors: Delete the .m2/repository folder and rerun mvn clean install.
PayPal Issues: Ensure PayPal API credentials are correct and the mode (sandbox or live) matches your environment.
UI Issues: Verify Bootstrap CDN connectivity or check local static files.

Contributing
We welcome contributions! To contribute:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Commit your changes (git commit -m "Add your feature").
Push to the branch (git push origin feature/your-feature).
Open a Pull Request.

For bug reports or feature requests, please create an issue on GitHub.
License
This project is licensed under the MIT License.
Contact
For inquiries or support, please contact [duongnguyen22394@gmail.com] (replace with your actual email).
