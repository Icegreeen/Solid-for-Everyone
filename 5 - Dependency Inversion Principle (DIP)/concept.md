# Dependency Inversion Principle (DIP)

### Clients should not be forced to depend on methods that they do not use.

![156shots_so](https://github.com/Icegreeen/blog-graphQL/assets/56550632/5d0ffa74-7d0c-4f20-abb8-8b4387b17554)

Let's consider a practical example to illustrate the Dependency Inversion Principle (DIP) in action, using a payment management system in an online store:

Suppose we have two classes: PaymentProcessor and PaymentGateway.

- PaymentProcessor: This is the high-level class that performs the action of processing a payment.
- PaymentGateway: This is the low-level class that provides the specific details of how to carry out the payment, such as communicating with payment providers, making HTTP requests, etc.

According to the DIP:

1 - Separation of Concerns: Instead of PaymentProcessor directly depending on PaymentGateway, both should depend on an abstraction. Let's call it PaymentService, representing an interface defining methods like processPayment().

2 - Focus on Abstractions: The PaymentService interface does not need to know how each specific payment gateway works. Instead, implementation details, such as integrating with PayPal, Stripe, etc., should be handled in the concrete classes that implement this interface.

3 - Flexibility and Maintenance: If at any point we decide to switch payment providers (e.g., transitioning from PayPal to Stripe), we don't need to modify the PaymentProcessor. We just need to create a new PayPalPaymentService or StripePaymentService class that implements the PaymentService interface. This keeps our code modular, flexible, and easy to maintain.


This approach following the DIP allows us to create a payment processing system that is less dependent on specific implementations of payment gateways, making maintenance and evolution of the system easier over time.

