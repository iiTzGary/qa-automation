# Abstract Classes in Java – Interview Questions & Answers (QA Automation Focus)

This document contains the **most common interview questions about abstract classes**, with **clear, role-appropriate answers** for a **QA Automation Engineer (Java)**.

---

## 1️⃣ What is an abstract class?

**Answer:**  
An abstract class is a class that cannot be instantiated and is used to define common behavior that subclasses must implement or can reuse.

It can contain both abstract methods and concrete (implemented) methods.

---

## 2️⃣ Why do we use abstract classes?

**Answer:**  
Abstract classes are used to share common logic while forcing subclasses to implement specific behavior.

**QA Automation example:**  
They are often used for `BasePage` or `BaseTest` classes to centralize setup logic.

---

## 3️⃣ Can an abstract class have implemented methods?

**Answer:**  
Yes. An abstract class can have both abstract methods and fully implemented methods.

**Example use case:**  
Common setup or utility methods can be implemented, while browser- or page-specific logic is abstract.

---

## 4️⃣ Can an abstract class have constructors?

**Answer:**  
Yes. Abstract classes can have constructors, and they are executed when a subclass is instantiated.

**Why it matters:**  
Useful for initializing shared objects like WebDriver or configuration.

---

## 5️⃣ Can an abstract class have variables?

**Answer:**  
Yes. Abstract classes can have instance variables, static variables, and constants.

---

## 6️⃣ Can we create an object of an abstract class?

**Answer:**  
No. Abstract classes cannot be instantiated directly.

However, they can be referenced using a parent type.

```java
Vehicle v = new Car(); // valid
```

---

## 7️⃣ Abstract class vs Interface (VERY COMMON)

**Answer:**  
An abstract class is used when classes share common state and behavior, while an interface is used to define a contract.

### Quick comparison

| Abstract Class | Interface |
|--------------|-----------|
| Can have state | No state (mostly) |
| Can have constructors | No constructors |
| Single inheritance | Multiple inheritance |
| Can have implemented methods | Default methods only |

---

## 8️⃣ When would you choose an abstract class over an interface?

**Answer:**  
When shared code or state is required between related classes.

**QA example:**  
A `BasePage` that contains common wait logic and driver initialization.

---

## 9️⃣ Can an abstract class implement an interface?

**Answer:**  
Yes. An abstract class can implement an interface and choose not to implement all of its methods.

---

## 🔟 Can an abstract class extend another abstract class?

**Answer:**  
Yes. Abstract classes can extend other abstract classes.

---

## 1️⃣1️⃣ Can abstract methods be private?

**Answer:**  
No. Abstract methods cannot be private because they must be implemented by subclasses.

---

## 1️⃣2️⃣ Can abstract methods be static or final?

**Answer:**  
No.

- `static` methods cannot be overridden  
- `final` methods cannot be overridden  

Abstract methods must be overridable.

---

## 1️⃣3️⃣ Real QA Automation Use Case

**Question:** How do you use abstract classes in automation frameworks?

**Answer:**  
Abstract classes are used for base layers such as `BaseTest` or `BasePage`, where common logic like driver setup, waits, and utilities are implemented, while page-specific actions are left abstract.

---

## 🧠 30-Second Interview Summary

Abstract classes are used to share common behavior and state while enforcing specific implementations. They support code reuse, improve maintainability, and are widely used in automation frameworks for base test and page layers.