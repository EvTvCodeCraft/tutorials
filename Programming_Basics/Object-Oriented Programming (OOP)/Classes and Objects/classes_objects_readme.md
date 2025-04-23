# 🧠 Understanding Classes and Objects in Object-Oriented Programming (OOP)

Classes and objects are **fundamental building blocks** in Object-Oriented Programming (OOP). They enable developers to create organized, modular, and scalable code by modeling real-world entities and their behaviors. This guide explores these concepts step by step.

---

## 🟢 Level 1: Introduction to Classes and Objects

- A **class** is a **blueprint** or **template** for creating objects. It defines the **attributes (properties)** and **methods (behaviors)** that its instances will have.

- An **object** is an **instance** of a class. It represents a **specific, concrete entity** with its own unique state and behavior, based on the structure defined by the class.

Classes and objects let you translate real-world entities into structured code components, which simplifies the design of complex systems.

---

## 🔵 Level 2: Class Definition

A class definition typically includes:

- **Class Name**: A descriptive name that reflects the real-world entity (e.g., `Car`, `Person`).

- **Attributes (Properties)**: Variables that store the state of an object (e.g., `make`, `model`, `year`).

- **Methods (Behaviors)**: Functions defined inside a class that operate on its attributes and represent its actions (e.g., `start_engine`, `stop_engine`).

---

## 🟡 Level 3: Object Creation

You create objects by **instantiating** a class. Each object has its own set of attribute values.

**Example (Python):**

```python
# Class definition
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def start_engine(self):
        print("Engine started.")

# Object creation
my_car = Car("Toyota", "Camry", 2022)
my_car.start_engine()  # Output: Engine started.
```

Here, `my_car` is an instance of the `Car` class with its own data.

---

## 🟣 Level 4: Encapsulation

**Encapsulation** is the concept of bundling data and methods that operate on the data within a class, and **restricting access** to some components.

- `public`: Accessible from anywhere.
- `private`: Prefixed with `_` or `__`, accessible only inside the class.
- `protected`: Prefixed with `_`, intended to be accessed within the class and its subclasses.

Encapsulation ensures that internal object details are **hidden** from the outside world and accessed only through well-defined interfaces (getters/setters), helping maintain data integrity.

---

## 🔴 Level 5: Inheritance

**Inheritance** allows a class to **reuse** the properties and behaviors of another class. The derived (child) class inherits from a base (parent) class and can extend or override its behavior.

**Example:**

```python
class ElectricCar(Car):
    def __init__(self, make, model, year, battery_capacity):
        super().__init__(make, model, year)
        self.battery_capacity = battery_capacity

    def charge_battery(self):
        print("Battery is charging.")
```

Here, `ElectricCar` inherits the properties and methods of `Car`, adding its own specific features.

---

## 🟠 Level 6: Polymorphism

**Polymorphism** enables you to use a unified interface to interact with objects of different classes. It allows code to be more generic and adaptable.

**Example:**

```python
def get_vehicle_info(vehicle):
    return f"{vehicle.make} {vehicle.model} ({vehicle.year})"
```

The `get_vehicle_info` function works with any object that has the expected attributes, whether it's a `Car`, `ElectricCar`, or any subclass thereof.

---

## ✅ Conclusion

Classes and objects form the **foundation of OOP**, helping developers create structured, reusable, and scalable code by modeling real-world entities and their interactions.

> As you deepen your OOP skills, mastering classes and objects is your first step toward designing robust and maintainable software systems.

---
