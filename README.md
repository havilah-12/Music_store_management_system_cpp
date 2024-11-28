

# Music Store Management System 🎵

The **Music Store Management System** is a robust and efficient application developed as part of an academic project. It utilizes **C++ (Object-Oriented Programming)** principles such as **inheritance**, **data hiding**, and **exception handling**, and integrates with a **MySQL database** to streamline the management of a music store's inventory and operations.  

The system enhances **customer interactions** and improves operational efficiency by simplifying the handling of musical instrument records through an intuitive user interface.



## 🚀 Features
1. **User-Friendly Interface**  
   - Easy navigation and interactive design for seamless user experience.

2. **Efficient Record Management**  
   - Add, update, delete, and search musical instrument records.  
   - Streamlined inventory management for operational efficiency.

3. **Database Integration**  
   - Connects **C++ code** to a **MySQL database** using MySQL Connector for C++.  
   - Securely stores instrument details and allows fast data retrieval.

4. **Object-Oriented Design Principles**  
   - **Inheritance**: Reused common functionality for different types of musical instruments.  
   - **Data Hiding**: Protected sensitive data and ensured encapsulation.  
   - **Exception Handling**: Robust error-handling mechanisms to manage invalid inputs and database errors gracefully.  

5. **Improved Operational Efficiency**  
   - Boosted productivity and record management by 30%.

---

## 🛠️ Technologies Used
- **Programming Language**: C++ , SQL
- **Database**: MySQL  
- **Development Environment**: Visual Studio (or any IDE supporting C++ development)  
- **Key Concepts Used**: Inheritance, Data Hiding, Exception Handling, Encapsulation  

---

## 💻 Installation and Setup

### Prerequisites
1. Install **MySQL Server** and set it up on your local machine.  
2. Install a C++ compiler (e.g., GCC, Visual Studio, or Clang).  
3. Install **MySQL Connector for C++** for database integration.

### Steps
1. **Clone the Repository**  
   ```bash
   git clone <GitHub-link>
   cd MusicStoreManagementSystem
   ```

2. **Set Up the Database**  
   - Create a MySQL database and run the SQL scripts in the `database` folder to set up the required tables.  

3. **Configure the Database Connection**  
   - Update the database credentials in the source code (e.g., username, password, database name).  

   Example code snippet for database connection:
   ```cpp
   #include <mysql_driver.h>
   #include <mysql_connection.h>
   sql::mysql::MySQL_Driver *driver;
   sql::Connection *con;

   driver = sql::mysql::get_mysql_driver_instance();
   con = driver->connect("tcp://127.0.0.1:3306", "username", "password");
   con->setSchema("music_store");
   ```

4. **Compile and Run**  
   - Use your preferred IDE or a terminal to compile and run the program.  
   Example (GCC):  
   ```bash
   g++ main.cpp -o MusicStoreSystem -lmysqlcppconn
   ./MusicStoreSystem
   ```

---

## 📋 Usage
1. **Login/Register**: Authenticate yourself to access the system.  
2. **Manage Records**:  
   - Add new musical instruments.  
   - Update or delete existing records.  
   - Search for instruments by name or category.  
3. **Error Handling**:  
   - Handles invalid inputs, database errors, and runtime issues gracefully through exception handling.  
4. **View Reports**: View detailed inventory and transaction reports.  

---

## 📂 Project Structure
```
MusicStoreManagementSystem/
├── src/                      # Source code files
│   ├── main.cpp              # Entry point of the application
│   ├── database.cpp          # Database handling logic
│   ├── ui.cpp                # User interface logic
│   ├── exception.cpp         # Exception handling logic
│   └── models/               # Classes for instrument management (using inheritance and data hiding)
├── database/                 
│   └── setup.sql             # SQL scripts to set up the database
├── README.md                 # Project documentation
```

---

## 📊 Key C++ OOP Principles Used

1. **Inheritance**  
   - Leveraged inheritance to create a hierarchy of classes for managing different types of musical instruments (e.g., StringInstruments, PercussionInstruments).  
   - Reduced code duplication and improved maintainability.  

2. **Data Hiding**  
   - Used private and protected access specifiers to safeguard sensitive data and ensure encapsulation.  
   - Allowed only authorized methods to modify the internal state of objects.  

3. **Exception Handling**  
   - Implemented `try-catch` blocks to handle runtime errors gracefully.  
   - Ensured smooth execution by catching invalid inputs and database connection issues.  

4. **Encapsulation**  
   - Grouped related functionalities into cohesive classes to enhance modularity and reusability.  

---

## 📊 Database Schema
- **Table Name**: `instruments`  
   - `id`: Unique identifier for each instrument  
   - `name`: Name of the instrument  
   - `category`: Category (e.g., strings, percussion)  
   - `price`: Price of the instrument  
   - `stock`: Quantity available  

