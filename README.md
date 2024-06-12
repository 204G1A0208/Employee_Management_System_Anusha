# Employee_Management_System
## Project Overview
The Employee Management System Database is designed to efficiently manage and organize employee information, departmental data, project assignments, performance reviews, and salary records. It provides a comprehensive structure for tracking employee roles, project involvement, departmental oversight, and historical salary changes. The system facilitates streamlined operations and reporting through well-defined relationships between employees, departments, projects, and performance metrics.
## Database Schema
### Tables and Their Contents
#### Employees
* employee_id: A unique identifier for each employee (Primary Key).
* name: The name of the employee.
* department_id: A foreign key linking to the department the employee belongs to.
* job_title: The job title of the employee.
* hire_date: The date the employee was hired.
* salary: The current salary of the employee.
#### departments
* department_id: A unique identifier for each department (Primary Key).
* department_name: The name of the department.
* manager_id: A foreign key referencing the employee who manages the department.
* location: The location of the department.
* phone_number: The contact phone number for the department.
* budget: The budget allocated to the department.
#### project
* project_id: A unique identifier for each project (Primary Key).
* project_name: The name of the project.
* start_date: The date the project started.
* end_date: The date the project ended or is expected to end.
* budget: The budget allocated for the project.
* department_id: A foreign key linking the project to the department responsible for it.
#### project_assignments
* assignment_id: A unique identifier for each assignment (Primary Key).
* project_id: A foreign key linking to the project table.
* employee_id: A foreign key linking to the employees table.
* role: The role of the employee in the project.
* assignment_date: The date the employee was assigned to the project.
* status: The current status of the assignment (e.g., active, completed).
#### performance_review
* review_id: A unique identifier for each review (Primary Key).
* employee_id: A foreign key linking to the employee being reviewed.
* review_date: The date the review was conducted.
* rating: The performance rating given to the employee.
* comments: Any comments provided by the reviewer.
* reviewer_id: A foreign key linking to the employee who conducted the review.
#### salaries
* salary_id: A unique identifier for each salary record (Primary Key).
* employee_id: A foreign key linking to the employee whose salary is recorded.
* salary_amount: The amount of salary.
* effective_date: The date when the salary became effective.
* end_date: The date when the salary ended, if applicable.
* salary_reason: The reason for the salary change (e.g., promotion, annual increment).
### Relationships:
* employees - departments: An employee belongs to one department.
* employees - project_assignments: An employee can be assigned to multiple projects.
* departments - project: A department can manage multiple projects.
* performance_review - employees: Employees can receive multiple performance reviews.
* salaries - employees: Employees can have multiple salary records over time.



