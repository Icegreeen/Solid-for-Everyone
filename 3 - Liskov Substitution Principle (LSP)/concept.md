# L — Liskov Substitution

### When a child class cannot perform the same actions as its parent class, it can cause bugs.

![39shots_so](https://github.com/Icegreeen/SOLID-for-Everyone/assets/56550632/b9d4617a-b338-47a4-8d67-dcf9d77c0c0d)

The Liskov Substitution Principle (LSP) states that objects of a superclass should be replaceable with objects of its subclass without affecting the correctness/accuracy of the program. In other words, if S is a subtype of T, then objects of type T should be replaceable with objects of type S without altering the behavior of the program in a way that violates the expected properties of T.

The child Class must be able to do everything the parent Class can do. This process is called Inheritance. When a child Class cannot perform the same actions as its parent Class, this can cause problems. According to this principle, the child Class must be able to process the same requests and provide the same result as the parent Class, or it could provide a result of the same type.

If the Child Class does not meet these requirements, it means that it has been completely changed and violates this principle.

### Another example:

If you have a base class (like "Animal") and a derived class (like "Dog"), you should be able to use an object of type "Dog" where an object of type "Animal" is expected, and the program should continue to work as expected.

This means that derived classes must be replaceable with base classes without changing the program's behavior in a way that causes problems. In other words, subclasses must follow the same behavior contract as their superclasses.


