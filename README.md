# CS-320-Software-Test-Automation
## CS 320 Portfolio Project

This repository has my work from CS 320 Software Testing and Automation.  
It shows the Contact Service project and my testing summary and reflection.

### Files Included

**Project One – Contact Service**
- Contact.java  
- ContactService.java  
- ContactTest.java  
- ContactServiceTest.java  

**Project Two**
- Project-Two-Submission.docx

---

## Project Summary

In Project One I created three parts of a system which are Contact, Task, and Appointment. Each one has a class to store the data and a service class that manages the data. The purpose was to make sure the system only accepts valid information and does not allow bad data.

For the Contact object, the ID cannot be null and cannot be longer than 10 characters. First and last names are required and must be 10 characters or less. The phone number must be exactly 10 digits and the address cannot be more than 30 characters. The ContactService allows adding, deleting, and updating contacts.

The Task object also has rules. The ID cannot be null or longer than 10 characters. The name cannot be more than 20 characters and the description cannot be more than 50 characters. The TaskService allows adding, deleting, and updating tasks.

The Appointment object requires an ID, a future date, and a description that is not longer than 50 characters. The AppointmentService allows adding and deleting appointments.

All validation is done inside the constructors and setters so invalid objects cannot be created. The service classes also prevent duplicate IDs and stop actions on items that do not exist.

---

## Summary of Tests

I created unit tests using JUnit to make sure the program works correctly and also fails when it should. I tested both valid and invalid inputs.

My tests checked:
- boundary values like maximum lengths  
- null and invalid inputs  
- duplicate IDs  
- updating and deleting records  
- making sure data cannot be changed accidentally from outside the class  

These tests help show that the program works in normal situations and also handles errors safely.

---

## Reflection

### How can I ensure that my code, program, or software is functional and secure?

I make my code functional and secure by validating all inputs and writing tests. The constructors and setters make sure invalid data cannot be created. The service classes prevent duplicate IDs and stop deleting items that are not in the system. I also used defensive copying for the appointment date so outside code cannot change the internal data. Unit testing helps find problems and makes the software more reliable.

### How do I interpret user needs and incorporate them into a program?

I look at what the user needs and turn those needs into rules the program must follow. For example, if a user wants to store contacts, the program must require an ID, check phone number length, and prevent missing information. These needs become validation rules in the classes and operations in the service classes. Tests help confirm that the program behaves the way the user expects.

### How do I approach designing software?

I design software by separating responsibilities. The model classes handle data and validation, the service classes manage operations like add and delete, and the test classes check that everything works correctly. This makes the code easier to understand and maintain. Designing the program with testing in mind helped me confirm each part works by itself and together.
