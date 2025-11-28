# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
```
class Details:
    def getName(self, name):
        self.name = name

    def getAge(self, age):
        self.age = age


class Employee(Details):
    def getEmployeeDetails(self, emp_id, dept):
        self.employee_id = emp_id
        self.department = dept

    def showEmployee(self):
        print("\n--- Employee Details ---")
        print("Name:", self.name)
        print("Age:", self.age)
        print("Employee ID:", self.employee_id)
        print("Department:", self.department)


class Patient(Details):
    def getPatientDetails(self, pat_id, disease):
        self.patient_id = pat_id
        self.disease = disease

    def showPatient(self):
        print("\n--- Patient Details ---")
        print("Name:", self.name)
        print("Age:", self.age)
        print("Patient ID:", self.patient_id)
        print("Disease:", self.disease)


name = input("Enter Employee Name: ")
age = int(input("Enter Employee Age: "))
emp_id = input("Enter Employee ID: ")
dept = input("Enter Department: ")

emp = Employee()
emp.getName(name)
emp.getAge(age)
emp.getEmployeeDetails(emp_id, dept)
emp.showEmployee()

name = input("\nEnter Patient Name: ")
age = int(input("Enter Patient Age: "))
pat_id = input("Enter Patient ID: ")
disease = input("Enter Disease: ")

pat = Patient()
pat.getName(name)
pat.getAge(age)
pat.getPatientDetails(pat_id, disease)
pat.showPatient()
```
## Sample Output
```
Enter Employee Name: John
Enter Employee Age: 32
Enter Employee ID: E101
Enter Department: HR

--- Employee Details ---
Name: John
Age: 32
Employee ID: E101
Department: HR

Enter Patient Name: David
Enter Patient Age: 45
Enter Patient ID: P201
Enter Disease: Fever

--- Patient Details ---
Name: David
Age: 45
Patient ID: P201
Disease: Fever
```
