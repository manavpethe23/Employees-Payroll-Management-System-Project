# 💼 Payroll Management System (Java)

This is a simple **Payroll Management System** implemented in Java using **OOP concepts** such as **Abstraction, Inheritance, Polymorphism, and Encapsulation**.  
The project demonstrates how to manage **full-time and part-time employees**, calculate their salaries, add/remove employees, and display employee details.  

---

## 📌 Features
- Add new employees (Full-Time or Part-Time)  
- Remove employees by ID  
- Calculate salary automatically  
- Display all employee details with salary  
- Uses **abstraction (abstract class Employee)** and **polymorphism (method overriding)**  

---

## 📂 Project Structure
## 📊 UML Class Diagram
classDiagram
    class Employee {
        - String name
        - int id
        + getName() String
        + getId() int
        + calculateSalary() double*
        + toString() String
    }

    class FullTimeEmployee {
        - double monthlySalary
        + calculateSalary() double
    }

    class PartTimeEmployee {
        - int hoursWorked
        - double hourlyRate
        + calculateSalary() double
    }

    class PayrollSystem {
        - ArrayList<Employee> employeeList
        + addEmployee(Employee e)
        + removeEmployee(int id)
        + displayEmployee()
    }

    class Main {
        + main(String[] args)
    }

    Employee <|-- FullTimeEmployee
    Employee <|-- PartTimeEmployee
    PayrollSystem --> Employee
    Main --> PayrollSystem
