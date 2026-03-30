# Exp.No:28  
## Abstraction

---

### AIM  
To write a Python program to define the abstract base class named `Polygon` and also define the abstract method. This base class is inherited by various subclasses. Implement the abstract method in each subclass. Create objects of the subclasses and invoke the `sides()` method.

---

### ALGORITHM

1. **Start the Program.**
2. **Import the ABC class** from the `abc` module to implement abstraction.
3. **Define the abstract base class Polygon**:
   - Inherit from `ABC` (Abstract Base Class).
   - Define an abstract method `sides()` with no implementation.
4. **Define the Triangle class** that inherits from `Polygon`:
   - Implement the `sides()` method to print `"Triangle has 3 sides"`.
5. **Define the Pentagon class** that inherits from `Polygon`:
   - Implement the `sides()` method to print `"Pentagon has 5 sides"`.
6. **Define the Hexagon class** that inherits from `Polygon`:
   - Implement the `sides()` method to print `"Hexagon has 6 sides"`.
7. **Define the Square class** that inherits from `Polygon`:
   - Implement the `sides()` method to print `"I have 4 sides"`.
8. **Create an object `t` of the Triangle class** and call the `sides()` method to print the number of sides.
9. **Create an object `s` of the Square class** and call the `sides()` method to print the number of sides.
10. **Create an object `p` of the Pentagon class** and call the `sides()` method to print the number of sides.
11. **Create an object `k` of the Hexagon class** and call the `sides()` method to print the number of sides.
12. **End the Program.**

---

### PROGRAM

```
from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def start(self):
        pass

    @abstractmethod
    def stop(self):
        pass

class Bike(Vehicle):
    def start(self):
        return "Bike is Started"

    def stop(self):
        return "Bike is stopped"

    def accelerate(self):
        return "Bike is accelrating @ 60kmph"

    def park(self):
        return "Bike is parked at two wheeler parking"

class Car(Vehicle):
    def start(self):
        return "Car is Started"

    def stop(self):
        return "Car is stopped"

    def accelerate(self):
        return "Car is accelrating @ 90kmph"

    def park(self):
        return "Car is parked at four wheeler parking"

# Create instances
bike = Bike()
car = Car()

# Invoke the methods
print("Bike Object")
print(bike.start())
print(bike.accelerate())
print(bike.park())
print(bike.stop())

print("\nCar Object")
print(car.start())
print(car.accelerate())
print(car.park())
print(car.stop())


```

### OUTPUT

<img width="1182" height="437" alt="438282449-7511df4d-81fb-4221-a821-a1cd79ac772d" src="https://github.com/user-attachments/assets/0c099562-22ef-4ffe-9462-3989df7d2fa4" />

### RESULT
The program successfully demonstrates the use of an abstract base class (VEHICLE) with two abstract methods (start() and stop()), which are implemented in the derived classes CAR and BIKE. Upon execution, the program correctly displays start and stop messages for both car and bike.
