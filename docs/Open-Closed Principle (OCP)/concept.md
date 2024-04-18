# O - Open-Closed Principle (OCP)

### Classes should be open for extension, but closed for modification

![136shots_so](https://github.com/Icegreeen/SOLID-for-Everyone/assets/56550632/13493153-733b-4413-93f7-17d5c1181f8c)

The Open-Closed Principle (OCP) states that a class should be open for extension but closed for modification. This means that the behavior of a class must be extended without modifying it, that is, assigning new behaviors.

In technical terms, this is achieved through the use of abstractions and polymorphism. Instead of modifying the code of an existing Class to add new behavior, new functionality is introduced by creating subclasses or implementing interfaces. This allows the class's behavior to be extended without changing it.

The ultimate goal of the Open-Closed Principle (OCP) is to make it easier to extend the behavior of a class without modifying its existing code. This allows the software to be easily adapted and extended to meet new requirements or functionality without introducing changes that could compromise the relationships it makes or break existing functionality.