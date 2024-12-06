# Liberia UniPortal

## Overview

This application is a JavaFX-based Database Management System that allows the college administration to keep track of students with information such as their id number, first name, last name, department, major, school email and school id photo.

---

## Setup Instructions

### Prerequisites

- **JavaFX**: Required to be setup in your development environment.
- **MySQL Server**: Required for database use.
- **Azure Blob Storage**: Must have access to blob storage for file uploads.

### Installation

1. Clone the repository and open it in your IDE.
2. Configure the database connection in `DbConnectivityClass.java` with your own database credentials.
3. Update `StorageUploader.java` with your Azure connection string.

### Account Creation

**First-time Registration**: Create an account.
**Subsequent Logins**: Log in with your credentials.

### Username Requirements
- Must be at least 8 characters long.
- Must contain at least 1 lowercase letter.

### Password Requirements
- Must be at least 8 characters long.
- Must contain at least 1 lowercase letter.
- Must contain at least 1 uppercase letter.
- Must contain at least 1 special character (*.!@#$%^&(){}[-]:;<>,.?/~_+=|).

## Features

### Database Integration
   - Creates a database for the user.
   - Supports CRUD operations on user records.

### User Management
- **Add User (`addNewRecord`)**: Adds a new user by validating form inputs and saving them to the database.
- **Edit User (`editRecord`)**: Updates the selected user's details in the database.
- **Delete User (`deleteRecord`)**: Removes the selected user record from the database.
- **Clear Form (`clearForm`)**: Resets all input fields.

### Data Import & Export
- **Import Data (`importCSV`)**: Reads user records from a CSV file, validates, and inserts them into the database.
- **Export Data (`exportCSV`)**: Exports the current user records to a CSV file.

### Reporting
- **Generate PDF (`generateReport`)**: Creates a PDF report showing the number of students in each major.

### Themes
- **Light Theme (`lightTheme`)**: Applies the light theme to the application.
- **Dark Theme (`darkTheme`)**: Applies the dark theme to the application.

## Project Structure

- **DAO**
  - `DbConnectivityClass.java`: Handles database interaction using JDBC.
  - `StorageUploader.java`: Manages the file uploads to Azure Blob Storage.
- **Model**
  - `Person.java`: Represents a user entity in the system.
- **Service**
  - `UserSession.java`: Manages the active user session.
  - `MyLogger.java`: Logs important application events and errors.
- **Main Application**
  - `MainApplication.java`: Entry point for the application.
- **Controllers**
  - `DB_GUI_Controller.java`: Manages the user data operations.
  - `LoginController.java`: Manages user login.
  - `SignUpController.java`: Manages new user registration.
  - `SpalshScreenController.java`: Controls the splash screen.
- **CSS**
  - `darkTheme`
  - `lightTheme`
- **Images**
  - `Pictures`
- **view (FXML)**
  - `about`
  - `db_interface_gui`
  - 'help'
  - `login`
  - `signUp`
  - `splashscreen`  

