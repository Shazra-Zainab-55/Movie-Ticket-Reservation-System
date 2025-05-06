Movie Ticket Booking System
This is a command-line-based Movie Ticket Booking System developed in Python with MySQL database integration. It allows users to view available shows, register, and book movie tickets. The project demonstrates core concepts of object-oriented programming, database integration, and SQL features like joins, triggers, stored procedures, and transactions.

🔍 Project Overview
The Movie Ticket Booking System simplifies the process of reserving seats for movie shows. It provides a backend logic for booking tickets, managing customer data, and updating seat availability. The system is built using the MVC (Model-View-Controller) architecture to ensure scalability and maintainability.

✅ Features
Customer registration and login (based on email)
View all available movie shows
Book tickets for selected shows
Auto-update of available seats after booking
Database integrity using triggers and transactions
🛠️ Tools & Technologies Used
Python
MySQL Workbench
MySQL Connector for Python
dotenv (to handle environment variables)
Git & GitHub (for version control)
Lucidchart / MS Visio (for ERD design)
🧩 Database Design (ERD)
Entities:

Customer (customer_id, name, phone, email)
Movie (movie_id, title, genre, duration)
Show (show_id, movie_id, start_time, available_seats)
Booking (booking_id, customer_id, show_id, seats_booked, booking_date)
Relationships:

A customer can have multiple bookings.
A movie can have multiple shows.
Each show belongs to one movie.
A booking links a customer and a show.
📊 SQL Concepts Used
DDL: Creating tables (Customer, Movie, Show, Booking)
DML: Inserting, updating, and deleting records
Joins: Fetching booking details by joining multiple tables
Stored Procedure: Automating booking logic
Trigger: Updating available seats after booking
Transactions: Booking operation managed as a transaction
Scalar & Table-Valued Functions: (optional use)
Select Queries: Using WHERE, GROUP BY, HAVING, ORDER BY
🗂️ Project Structure (MVC)
. ├── controller/ # Business logic (BookingController, ShowController, CustomerController) ├── model/ # DB access layer (BookingModel, ShowModel, CustomerModel) ├── config/ # DB connection setup (database.py) ├── views/ # CLI-based inputs/outputs ├── .env # Environment variables (DB credentials) ├── main.py # Entry point for the application

📸 Sample Output Screenshots
Show list before booking
Customer login/registration
Booking confirmation
Error on overbooking
Database view of successful booking
❗ Challenges Faced
Handling real-time updates to available seats
Integrating SQL triggers and stored procedures with Python
Maintaining MVC architecture in a CLI-based application
Managing transaction consistency and exception handling
✅ How to Run the Project
Clone the repository:

git clone https://github.com/yourusername/movie-ticket-booking-system.git cd movie-ticket-booking-system

Install dependencies:

pip install mysql-connector-python python-dotenv

Configure your database credentials in the .env file: DB_HOST=localhost DB_USER=root DB_PASSWORD=yourpassword DB_NAME=movie_booking

Run the main file: python main.py

📌 Future Enhancements
Add user authentication with password
Implement GUI using Tkinter or Web version using Flask/Django
Admin panel to manage shows and movies
Email confirmation for bookings
