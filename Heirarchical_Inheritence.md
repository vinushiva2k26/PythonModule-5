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

```python
class Details:
    def getName(self):
        self.name = input("Enter Name: ")

    def getAge(self):
        self.age = int(input("Enter Age: "))

class Employee(Details):
    def getEmployeeDetails(self):
        self.employee_id = input("Enter Employee ID: ")
        self.department = input("Enter Department: ")

    def display(self):
        print("Employee Details")
        print("Name:", self.name)
        print("Age:", self.age)
        print("Employee ID:", self.employee_id)
        print("Department:", self.department)

class Patient(Details):
    def getPatientDetails(self):
        self.patient_id = input("Enter Patient ID: ")
        self.disease = input("Enter Disease: ")

    def display(self):
        print("Patient Details")
        print("Name:", self.name)
        print("Age:", self.age)
        print("Patient ID:", self.patient_id)
        print("Disease:", self.disease)

e = Employee()
e.getName()
e.getAge()
e.getEmployeeDetails()

p = Patient()
p.getName()
p.getAge()
p.getPatientDetails()

e.display()
p.display()
```

## Output

```text
Enter Name: Vinu
Enter Age: 20
Enter Employee ID: E101
Enter Department: CSE
Enter Name: Ravi
Enter Age: 35
Enter Patient ID: P201
Enter Disease: Fever

Employee Details
Name: Vinu
Age: 20
Employee ID: E101
Department: CSE

Patient Details
Name: Ravi
Age: 35
Patient ID: P201
Disease: Fever
```

## Result

Thus, the Python program was successfully executed to demonstrate Hierarchical Inheritance by collecting and displaying Employee and Patient details using a common base class.

