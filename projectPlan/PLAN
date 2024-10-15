Current Development Plan for Time Management Application
1. Initial Setup (Completed)
Install Django: Django has been installed, and the initial project structure has been set up.
Project structure: You have set up the directory structure, including creating the input app and necessary files like models.py, views.py, admin.py, etc.
2. Create Models (Completed)
User Model (CustomUser): A custom user model has been created, extending Django’s AbstractUser to include three types of users:
Administrator: Full access to all tables and logs, including the ability to manage other users and rights.
Director: Can create and delete worker users, clients, and work types. Directors also have access to all work records.
Worker: Can create, edit, and delete their own work records and view only their own data.
Client Model: Stores client information, including client name and description.
Work Type Model: Stores different work types, allowing directors to add/edit these for work records.
Work Record Model: Tracks individual work sessions, linking a worker, client, work type, date, hours spent, and an optional comment field.
3. Backend Implementation (In Progress)
CRUD Functionality for Work Records:
Workers can create, edit, delete, and view their own work records.
Directors can review, edit, and delete work records from all workers.
Administrators have full access to all work records.
Views and Forms:
Implement forms for creating, editing, and deleting work records.
Set up views for displaying work records and handling CRUD operations.
Access Control:
Permissions will be enforced based on the user type:
Workers: Access to their own work records only.
Directors: Access to all work records, clients, and work types.
Administrators: Full access to all data, including user management.
Admin Interface:
Directors and administrators can manage clients, work types, and workers using the Django Admin interface.
4. Frontend (Upcoming)
Worker Views:
Create frontend templates for workers to view and manage their own time sheets.
Director Views:
Create frontend templates to display summarized data for directors, allowing them to view all workers' records.
Admin Interface:
The Django Admin interface will be used for administrators and directors to manage users, clients, work types, and records.
5. Testing and Deployment
Testing:
Perform unit testing for models, views, and forms.
Conduct manual testing of CRUD operations and permissions for all user roles.
Deployment:
Deploy the project on a server (e.g., Heroku or another hosting service).
Set up any necessary configurations for production (e.g., using PostgreSQL instead of SQLite).
Access Details
Workers: Can access their own work records through custom views.
Directors: Can access all workers’ records and manage clients/work types via the Django Admin interface.
Administrators: Have full access to all data and management via the Django Admin interface.
