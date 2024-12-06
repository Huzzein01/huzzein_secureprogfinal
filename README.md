# huzzein_secureprogfinal

User Information Collection and Dataset Management
This project is a web application that allows users to sign up by providing their name, email, and phone number. The application securely stores the information in a database and generates a downloadable CSV file for the dataset. It features input validation, database integration, and user-friendly functionality.

Features
Signup Form

Collects user name, email, and phone number.
Includes regex-based validation to ensure data accuracy:
Name: Only alphabets (no numbers or special characters).
Email: Valid formats ending in .com, .edu, or .gov.
Phone Number: Valid U.S. phone number format.
Dataset Management

Stores data in a MySQL database (user_data).
Automatically creates the database and table if they don’t exist.
Generates a downloadable CSV file of the collected user data.
Security Features

Prepared statements to prevent SQL injection.
User-friendly error handling to hide server details.
Responsive Dataset View

The dataset is displayed in a format that fits the screen, optimized for laptops.
Installation
Prerequisites
XAMPP or any other PHP and MySQL server environment.
Web browser for testing.
Setup Steps
Clone or download the project files into your web server’s root directory (e.g., htdocs for XAMPP).
Start your server using XAMPP or similar tools.
Open your browser and navigate to:
arduino
Copy code
http://localhost/index.php
File Descriptions
Core Files
index.php
The main page with the signup form.
db.php
Handles database creation and connection.
Ensures the user_data database and users table are automatically created.
Appends user data to a CSV file after signup.
register.php
Validates and processes user inputs from the signup form.
Inserts validated data into the database.
Redirects users to the dataset view page after successful signup.
download.php
Generates a CSV file of the dataset and triggers the download.
style.css
Defines the layout and styling for all pages, including a responsive dataset view.
Database Details
Database Name: user_data
Table Name: users
Columns:
id: Auto-increment primary key.
name: User's name.
email: User's email address.
phone: User's phone number.
signup_date: Timestamp of the signup.
Usage
Signup:

Open index.php and fill out the form.
Click the signup button to submit the details.
View Dataset:

After signing up, you are redirected to the dataset page.
View, download, or manage the data collected.
Security Measures
Input Validation: Prevents invalid or malicious data.
SQL Injection Protection: All database queries use prepared statements.
Error Handling: Hides sensitive server information from users.
Future Improvements
Add user authentication to restrict access to the dataset.
Improve the design for mobile responsiveness.
Add pagination for large datasets.
Credits
Developed by Huzzein Adebiyi
