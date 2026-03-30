# Exp.No:29  
## Encapsulation

---

### AIM  
To write a Python program to create a class `Student` with the private members `name` and `age`, and add getter and setter methods to initialize and modify the `age` variable.

---

### ALGORITHM

1. **Start the Program.**
2. **Define the `Student` class.**
   - Inside the `Student` class, define the `__init__` method to initialize `name` and the private member `__age`.
3. **Define a getter method** `get_age` to return the value of the private member `__age`.
4. **Define a setter method** `set_age` to set a new value to the private member `__age`.
5. **Create an object `stud`** of the `Student` class with the name 'Jessa' and age 14.
6. **Print the name and the age** of `stud` using the getter method.
7. **Use the setter method** `set_age` to change the age of `stud` to 16.
8. **Print the name and the updated age** of `stud` using the getter method.
9. **End the program.**

---

### PROGRAM

```

class Student:
    def __init__(self, name, age):
        self.__name = name
        self.__age = age

    # Getter for age
    @property
    def age(self):
        return self.__age

    # Setter for age
    @age.setter
    def age(self, age):
        if age > 0 and isinstance(age, int):
            self.__age = age
        else:
            print("Please enter a valid age")

    # Method to print student details
    def print_details(self):
        return f"Name: {self.__name} {self.__age}"

# Create an instance
s = Student(" Jessa Salary:", 10000)
print(s.print_details())
# Change age using setter
s.age = 10000
print(s.print_details())
```

### OUTPUT
<img width="1189" height="211" alt="438280734-c8694416-d90b-4d7f-9f8e-d2a1c49c3066" src="https://github.com/user-attachments/assets/4c5e2506-30f0-43db-93ca-7c06e525b101" />


### RESULT

The program successfully creates an Employee class and uses a public method show() to display the details of the employee.
