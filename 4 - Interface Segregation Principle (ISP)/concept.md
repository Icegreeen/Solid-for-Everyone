# Interface Segregation Principle (ISP)

### Clients should not be forced to depend on methods that they do not use.

![846shots_so](https://github.com/Icegreeen/SOLID-for-Everyone/assets/56550632/e8feb790-307a-4cfe-acf3-1ccd347542fa)

The Interface Segregation Principle (ISP) states that clients should not be forced to rely on methods they do not use. In other words, a class should not be forced to implement interfaces that contain methods that are not relevant to it.

For example, imagine a scenario where we have an interface called Animal with methods like walk(), fly() and swim(). If we have a Dog class, it wouldn't make sense to force this class to implement the fly() method, as dogs don't fly.

Instead, we should divide the Animal interface into smaller, more specific interfaces, such as Walker, Swimmer, and Flyer. This way, classes can implement only the interfaces relevant to them, without relying on unnecessary functionality.

By following the ISP, you keep your interfaces cohesive and focused, avoiding creating "fat" interfaces with methods that are not relevant to all the classes that implement them, dividing a set of actions into smaller sets so that a Class performs ONLY the set of actions required.