# Java List – Explanation & Interview Questions (QA Automation Focus)

This document explains what a **List** is in Java and covers the **most common interview questions** for a **QA Automation Engineer** role.

---

## What is a List in Java?

**Interview-ready definition:**  
A `List` in Java is an ordered collection that allows duplicate elements and provides index-based access.

### Key characteristics
- Part of the **Java Collections Framework**
- Maintains **insertion order**
- Allows **duplicate elements**
- Supports **index-based access**

### Example

```java
List<String> names = new ArrayList<>();
names.add("Alice");
names.add("Bob");
names.add("Alice"); // duplicates allowed
```

---

## Common List Implementations

| Implementation | When to use |
|---------------|------------|
| ArrayList | Fast read operations, dynamic size |
| LinkedList | Fast insertions and deletions |
| Vector | Thread-safe (legacy) |
| CopyOnWriteArrayList | Modern thread-safe alternative |

---

## Common Interview Questions & Answers

---

## 1️⃣ Difference between List and Set

**Question:** What is the difference between `List` and `Set`?

**Answer:**  
A `List` allows duplicate elements and preserves insertion order, while a `Set` does not allow duplicates and does not guarantee order.

---

## 2️⃣ ArrayList vs LinkedList (VERY COMMON)

**Question:** What is the difference between `ArrayList` and `LinkedList`?

**Answer:**  
`ArrayList` is backed by a dynamic array and is faster for read operations, while `LinkedList` is backed by a doubly linked list and is faster for insertions and deletions.

**QA Tip:**  
In automation frameworks, `ArrayList` is used more often because test logic usually reads data more than it modifies it.

---

## 3️⃣ Why is List an interface and not a class?

**Question:** Why is `List` an interface?

**Answer:**  
`List` is an interface to provide a common contract for multiple implementations such as `ArrayList` and `LinkedList`.

---

## 4️⃣ How does ArrayList work internally?

**Question:** How does `ArrayList` work internally?

**Answer:**  
`ArrayList` uses a dynamic array. When the array exceeds its capacity, a new larger array is created and existing elements are copied into it.

---

## 5️⃣ How do you iterate over a List?

**Question:** How can you iterate over a `List`?

**Answer:**  
Using:
- Traditional `for` loop  
- Enhanced `for-each` loop  
- `Iterator`  
- Java Streams

```java
for (String name : names) {
    System.out.println(name);
}
```

---

## 6️⃣ Difference between Array and List

**Question:** What is the difference between an array and a List?

**Answer:**  
An array has a fixed size and can store primitive values, while a `List` has a dynamic size and stores objects only.

---

## 7️⃣ How do you remove duplicates from a List?

**Question:** How do you remove duplicates from a List?

**Answer:**  
By converting the `List` into a `Set` and then back to a `List`.

```java
List<String> unique = new ArrayList<>(new HashSet<>(names));
```

---

## 8️⃣ How do you sort a List?

**Question:** How do you sort a List?

**Answer:**  
Using `Collections.sort()` or `List.sort()`.

```java
Collections.sort(names);
```

---

## 9️⃣ What happens if you modify a List while iterating?

**Question:** What happens if you modify a List while iterating?

**Answer:**  
It can throw a `ConcurrentModificationException` unless the modification is done using the iterator’s `remove()` method.

---

## 🔟 How do you make a List thread-safe?

**Question:** How do you make a List thread-safe?

**Answer:**  
- `Collections.synchronizedList()`  
- `CopyOnWriteArrayList`

---

## 1️⃣1️⃣ List vs Collection vs Iterable

**Question:** What is the difference between `Iterable`, `Collection`, and `List`?

**Answer:**  
`Iterable` is the root interface, `Collection` extends it, and `List` extends `Collection` by adding ordered and index-based behavior.

---

## 1️⃣2️⃣ Can a List store null values?

**Question:** Can a List store null values?

**Answer:**  
Yes. Most `List` implementations allow multiple `null` values, except some concurrent implementations.

---

## 1️⃣3️⃣ Real QA Automation Use Case

**Question:** How are Lists used in QA automation?

**Answer:**  
Lists are used to store:
- Web elements  
- API responses  
- Test data  
- Dynamic UI data (tables, dropdowns)

```java
List<WebElement> rows = driver.findElements(By.tagName("tr"));
```

---

## 🧠 30-Second Interview Summary

A `List` in Java is