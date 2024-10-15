
# CSC6302 Week 5 Project - Student Database with Toga GUI

This project is a student database application built using Python and Toga GUI. It allows users to manage student records, including displaying student information, adding new students, and calculating average grades from multiple tables in a relational database. The project integrates a business logic layer (BLL) with a data access layer (DAL) and a MySQL backend database.

## Features

- View all students along with their class subjects, grades, teacher names, and average grade.
- Add new students via the Toga GUI.
- Simple MySQL integration for data storage.
- Custom SQL procedures for student data manipulation.

## Prerequisites

Make sure you have the following installed on your system:

- Python 3.10+
- MySQL Server 9.0 or later

## Project Structure

```
Grandparent Directory: GitHub
|-- ./.DS_Store
|-- ./application
   |-- ./application/.DS_Store
   |-- ./application/clean.py
   |-- ./application/BLL
      |-- ./application/BLL/students.py
   |-- ./application/requirements.txt
   |-- ./application/Makefile
   |-- ./application/README.md
   |-- ./application/Connection.py
   |-- ./application/VIEW
      |-- ./application/VIEW/.DS_Store
      |-- ./application/VIEW/view.py
   |-- ./application/DAL
      |-- ./application/DAL/teacherDAL.py
      |-- ./application/DAL/classesDAL.py
      |-- ./application/DAL/studentDAL.py
   |-- ./application/main.py
   |-- ./application/python-path.txt
|-- ./.vscode
   |-- ./.vscode/settings.json
|-- ./togavenv
   |-- ./togavenv/.DS_Store
   |-- ./togavenv/bin
   |-- ./togavenv/include
   |-- ./togavenv/pyvenv.cfg
   |-- ./togavenv/lib
   |-- ./togavenv/share
|-- ./sql
   |-- ./sql/users.sql
   |-- ./sql/ddl.sql
   |-- ./sql/procedure_functions.sql
   |-- ./sql/query.sql
   |-- ./sql/dml.sql
   |-- ./sql/permissions.sql
```

## Installation and Setup

1. **Clone the Repository**
   ```bash
   [git clone https://github.com/yourusername/database_principles_csc6302.git](https://github.com/ajgalipeau/6302week5.git)
   cd <path>\6302week5
   ```

2. **Create a Virtual Environment**
   ```bash
   python3 -m venv togavenv
   source togavenv/bin/activate  # On Windows use `<path>\togavenv\Scripts\Activate.ps1` && ensure you give Powershell remote signing privileges 
   ```

3. **Install Required Packages**
   ```bash
   pip install -r application/requirements.txt
   # Preferred method - use the Makefile
   # or go to the application folder path
   make install
   ```

4. **MySQL Database Setup**
   - Ensure that MySQL is installed and running either in Code,Docker, MySQL Workbench, or your db tool of choice
   - Execute the SQL scripts in the `sql/` directory to create tables, add procedures, and insert sample data.

   ```bash
   mysql -u admin_user -p < sql/ddl.sql
   mysql -u admin_user -p < sql/dml.sql
   mysql -u admin_user -p < sql/users.sql
   mysql -u admin_user -p < sql/permissions.sql
   mysql -u admin_user -p < sql/procedure_functions.sql
   mysql -u admin_user -p < sql/query.sql
   ```

## Running the Application

1. **Start the Toga GUI**
   ```bash
   python3 application/main.py
   ```

   This will open the GUI window for the student database management application.

2. **Add a Student**
   - Fill out the form on the right panel of the GUI to add a new student.
   - Click "Add User" to submit the form.
   - The data table on the left will refresh to display the updated list of students.

## Makefile Commands

The `Makefile` includes a convenient command for cleaning up cache files:

- **Clean Cache Files**
  ```bash
  make clean
  ```
  This command will remove all `__pycache__` files and `.DS_Store` files from the project.

## License

Educational License

This project is licensed under the Educational License for the purposes of learning, academic exercises, and research.

Holder:  
Aaron Galipeau  
M.S. Computer Science Student  
Merrimack College  
Lecturer: Robert Sands  
Course: CSC6302 Database Principles

This license allows the project to be used, modified, and shared for educational purposes only. Commercial use or redistribution is strictly prohibited without prior written permission.
