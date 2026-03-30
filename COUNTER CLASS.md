# Exp.No:30  
## COUNTER CLASS

---

### AIM  
To write a Python program to create a `Counter` class that can increment the value of a counter.

---

### ALGORITHM

1. **Start the Program.**
2. **Define the `Counter` class.**
   - Initialize the `current` variable with 0.
3. **Define the `increment()` method** to increment the value of `current` by 1.
4. **Define the `value()` method** to return the current value of `current`.
5. **Define the `reset()` method** to reset the `current` value back to 0.
6. **Create a `counter` object** of the `Counter` class.
7. **Call the `increment()` method** three times to increment the counter.
8. **Call the `value()` method** and print the result to show the current counter value.
9. **End the program.**

---

### PROGRAM

```
class Counter:
    def __init__(self):
        self.count = 0

    def increment(self):
        self.count += 1

    def display(self):
        print("Current Counter Value:", self.count)


# Example usage
counter = Counter()

# Increment and display
counter.increment()
counter.increment()
counter.display()  # Should show 2

counter.increment()
counter.display()  # Should show 3
```

### OUTPUT

<img width="818" height="254" alt="438285662-aaf60e57-c2c7-4a99-84a4-78e9defaebb8" src="https://github.com/user-attachments/assets/42136ae9-12d5-4867-ad72-40ecad5cfbc3" />

### RESULT
The program successfully creates a Counter class. Each call to increment() increases the counter value by 1, and display() correctly shows the current count.
