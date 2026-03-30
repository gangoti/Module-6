# Exp.No:27  
## Operator Overloading

---

### AIM  
To write a Python program to perform division of two complex numbers using the binary '/' operator overloading. Class name: `Complex`, where the objects `Ob1 = Complex(10, 21)` and `Ob2 = Complex(2, 3)` represent complex numbers.

---

### ALGORITHM

1. **Start the Program.**
2. **Define the Complex class**:
   - Define the constructor `__init__()` to accept two parameters: `real` and `imag` (representing the real and imaginary parts of the complex number).
   - Assign these values to `self.real` and `self.imag` respectively.
3. **Define the `__truediv__()` method** to perform the division of two complex numbers:
   - Calculate the real part of the result as the division of `self.real` by `other.real`.
   - Calculate the imaginary part of the result as the division of `self.imag` by `other.imag`.
   - Return a new Complex object with the calculated real and imaginary parts.
4. **Define the `__repr__()` method** to represent the complex number as a string.
   - Return a string formatted to display the real and imaginary parts with one decimal place using `f"{self.real:.1f}, {self.imag:.1f}"`.
5. **Create two objects of the Complex class**:
   - `Ob1 = Complex(10, 21)` represents the complex number `10 + 21i`.
   - `Ob2 = Complex(2, 3)` represents the complex number `2 + 3i`.
6. **Perform the division operation**: Use the `/` operator to divide `Ob1` by `Ob2`. This will call the `__truediv__()` method.
7. **Print the result**: Print the result of the division, which will be formatted by the `__repr__()` method.
8. **End the Program.**

---

### PROGRAM
```
class Complex:
    def __init__(self, real, imag):
        self.real = real
        self.imag = imag

    # Overloading '/' operator
    def __truediv__(self, other):
        # Formula: (a+bi)/(c+di) = [(ac + bd) + (bc - ad)i] / (c^2 + d^2)
        a, b = self.real, self.imag
        c, d = other.real, other.imag
        denominator = c**2 + d**2

        real_part = (a * c + b * d) / denominator
        imag_part = (b * c - a * d) / denominator

        return Complex(real_part, imag_part)

    def __str__(self):
        return f"{self.real:.2f} + {self.imag:.2f}i"


# Creating objects
Ob1 = Complex(10, 21)
Ob2 = Complex(2, 3)

# Performing division
result = Ob1 / Ob2

# Displaying result
print("Result of (10 + 21i) / (2 + 3i):")
print(result)
```

### OUTPUT
<img width="818" height="196" alt="438288631-93dc2acc-d14d-4037-b279-15b1061de4a1" src="https://github.com/user-attachments/assets/3ea74e95-cc22-4d8b-a7f4-a35747cfa9fb" />


### RESULT
The program successfully demonstrates the division of two complex numbers using operator overloading.
