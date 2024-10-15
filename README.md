# Time Management System

## Project Overview

This project is a **Time Management System** built with Django to help manage work records for a company. The system allows workers to log their work, directors to oversee their workers and clients, and administrators to manage the entire system. The goal is to automate and simplify the process of time tracking, work reporting, and client management.

### Key Features

- **Role-based access control**:
  - **Administrator**: Full access to manage users, work records, clients, work types, and system logs.
  - **Director**: Can manage workers, clients, work types, and view all work records.
  - **Worker**: Can create, edit, and delete their own work records.
- **CRUD operations** for managing:
  - Users (Workers and Directors).
  - Work records (time entries).
  - Clients.
  - Work types.
- **User Interface**:
  - Workers use a simple web interface to manage their own work records.
  - Directors and Administrators use the Django Admin interface to manage the system.
- **Dynamic Reporting**: Directors can view summaries of work done by workers.

---

## Application Structure

The system is structured into various components:

### Web Frontend
- **HTML, CSS, JavaScript** for dynamic user interaction.
- **Django templates** used to render data to the web interface.

### Server (Backend)
- Built with **Django (Python)**.
- Handles HTTP requests and connects to the database using Django ORM.
- Role-based access controls for different user types (Administrator, Director, Worker).

### Database
- **PostgreSQL** (or **SQLite** for development).
- Stores users, work records, clients, and work types.

---

## How to Set Up and Run

### Prerequisites

1. Python 3.x
2. Django
3. PostgreSQL (recommended) or SQLite for development

### Installation Steps

1. **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/time-management-system.git
    cd time-management-system
    ```

2. **Create a virtual environment:**
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows: env\Scripts\activate
    ```

3. **Install the dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4. **Set up the database:**
   - If using **PostgreSQL**, ensure it is installed and running.
   - Update the `DATABASES` setting in `settings.py` if needed.

5. **Apply migrations:**
    ```bash
    python manage.py makemigrations
    python manage.py migrate
    ```

6. **Create a superuser (admin):**
    ```bash
    python manage.py createsuperuser
    ```

7. **Run the development server:**
    ```bash
    python manage.py runserver
    ```

8. **Access the application**:
   - **Admin Interface**: Go to `http://127.0.0.1:8000/admin/` to log in with the superuser account.
   - **Worker Interface**: Workers can access custom views for managing work records at `http://127.0.0.1:8000/records/`.

---

## Application Flow

### Users

- **Workers**:
  - Can create, edit, view, and delete their own work records.
  - Access their interface via a web browser.
  
- **Directors**:
  - Can manage workers, clients, work types, and view all work records.
  - Access the system via the Django Admin interface and additional views.

- **Administrators**:
  - Have full control over the system, including user and data management.
  - Access via the Django Admin interface.

### System Components

- **Web Interface**:
  - Built using Django templates and basic HTML/CSS for worker interaction.
  
- **Django Framework**:
  - Handles all backend logic, routing, and authentication.
  
- **PostgreSQL Database**:
  - Stores all data (users, work records, clients, work types).

