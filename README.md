##Project Overview: Payroll System

## Overview

The Payroll System is designed to manage and calculate the salaries of different types of employees within an organization. It supports both full-time and part-time employees, offering flexibility and accurate payroll processing.

## Project Components

### 1. Employee Class (Abstract)
- Attributes:
  - `name` (String): Name of the employee.
  - `id` (int): Unique identifier for the employee.
- Constructor:
  - Initializes the `name` and `id` attributes.
- Methods:
  - `getName()`: Returns the name of the employee.
  - `getId()`: Returns the ID of the employee.
  - `calculateSalary()`: Abstract method to be implemented by subclasses to calculate the employee's salary.
  - `toString()`: Returns a string representation of the employee, including name, ID, and calculated salary.

### 2. FullTimeEmployee Class
- Attributes:
  - `monthlySalary` (double): Monthly salary of the full-time employee.
- Constructor:
  - Initializes `name`, `id`, and `monthlySalary` attributes using the superclass constructor.
- Methods:
  - `calculateSalary()`: Returns the monthly salary. This method demonstrates polymorphism by providing a specific implementation of the abstract method in the Employee class.

### 3. PartTimeEmployee Class
- Attributes:
  - `hoursWorked` (int): Number of hours worked by the part-time employee.
  - `hourlyRate` (double): Hourly rate of the part-time employee.
- Constructor:
  - Initializes `name`, `id`, `hoursWorked`, and `hourlyRate` attributes using the superclass constructor.
- Methods:
  - `calculateSalary()`: Returns the total salary calculated as `hoursWorked * hourlyRate`. This method also demonstrates polymorphism.

### 4. PayrollSystem Class
- Attributes:
  - `employeeList` (ArrayList<Employee>): List to store employee objects.
- Constructor:
  - Initializes the `employeeList` as an empty ArrayList.
- Methods:
  - `addEmployee(Employee employee)`: Adds an employee to the `employeeList`.
  - `removeEmployee(int id)`: Removes an employee with the specified ID from the `employeeList`.
  - `displayEmployee()`: Displays details of all employees in the `employeeList` by calling the `toString()` method of each employee.

### 5. Main Class
- Main Method:
  - Creates an instance of `PayrollSystem`.
  - Adds a `FullTimeEmployee` and a `PartTimeEmployee` to the payroll system.
  - Displays initial employee details.
  - Removes an employee by ID.
  - Displays remaining employee details.

## Sample Output

Upon running the program, the following output is produced:

Initial Employee Details:
Employee [name=vikas,id=1,salary=70000.0]
Employee [name=Alexander,id=2,salary=4000.0]
Remove Employees
Remaining Employee Details
Employee [name=vikas,id=1,salary=70000.0]




