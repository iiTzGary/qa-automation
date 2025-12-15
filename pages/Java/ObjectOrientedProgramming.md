# Object-Oriented Programming (OOP) in Java

## Class
**Blueprint of an object**

## Object
**Instance of a class**

---

## 1️⃣ Encapsulation

Encapsulation is about hiding the internal state of an object and exposing behavior through methods.

In Java, this is done using **private variables** and **public getters and setters**.

For example, a user’s password should not be accessed directly, only through controlled methods.

It improves security, prevents invalid data, and makes the code easier to maintain.

In automation, **Page Object Model (POM)** uses encapsulation to hide web elements and expose actions.

### Example

```java
class User {
    private String password;

    public void setPassword(String password) {
        this.password = password;
    }

    public String getPassword() {
        return password;
    }
}
```

---

## 2️⃣ Inheritance

Inheritance allows one class to reuse the properties and methods of another class.

A child class extends a parent class using the `extends` keyword.

For example, a `LoginTest` class can extend a `BaseTest` class and reuse WebDriver setup logic.

### 🎯 Why it matters

- Reduces code duplication
- Promotes reuse
- Overusing inheritance can cause tight coupling, so **composition is often preferred**

### Example

```java
class Animal {
    void eat() {
        System.out.println("Eating...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Barking...");
    }
}

Dog dog = new Dog();
dog.eat();   // inherited
dog.bark();  // own method
```

---

## 3️⃣ Polymorphism

Polymorphism means the same method call can behave differently depending on the object.

In Java, this is commonly achieved through **method overriding** and **interfaces**.

For example, a `WebDriver` reference can point to `ChromeDriver` or `FirefoxDriver`, but the same `get()` method is used.

It allows flexible, extensible code and is heavily used in frameworks like **Selenium** and **Spring**.

### Example

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

Animal animal = new Dog();
animal.sound(); // Dog barks
```

---

## 4️⃣ Abstraction

Abstraction means showing what an object does while hiding how it does it.

In Java, abstraction is achieved using **abstract classes** and **interfaces**.

For example, a `Payment` interface defines a `pay()` method, but each implementation decides how to process the payment.

### 🎯 Why it matters

- Reduces complexity
- Allows loose coupling between components

### Abstract Class Example

```java
abstract class Vehicle {
    abstract void move();
}

class Bike extends Vehicle {
    void move() {
        System.out.println("Bike is moving");
    }
}
```

---

## Interfaces

Interfaces define a contract that implementing classes must follow.

### Example

```java
interface Payment {
    void pay();
}

class CreditCardPayment implements Payment {
    public void pay() {
        System.out.println("Paying with credit card");
    }
}
```
