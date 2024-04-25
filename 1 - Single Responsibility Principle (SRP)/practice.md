
Let's compare the two approaches: one without following the SRP principle and the other applying the SRP principle in the context of the payments system.

Without SRP:

```ts
class PaymentProcessor {
    public processPayment(): void {
        // Simulating transaction reading
        const transaction = this.readTransaction();

        // Simulating fee calculation
        const fee = this.calculateFee(transaction);

        // Simulating transaction and fee logging to a log file
        this.logTransaction(transaction, fee);
    }

    private readTransaction(): Transaction {
        // Simulating transaction reading
        return {
            id: "1",
            amount: 100.00,
            date: new Date(),
            payer: "John",
            payee: "Mary"
        };
    }

    private calculateFee(transaction: Transaction): number {
        // Simulating fee calculation
        return transaction.amount * 0.02; // For example, 2% fee
    }

    private logTransaction(transaction: Transaction, fee: number): void {
        // Simulating transaction and fee logging to a log file
        console.log(`Transaction logged - ID: ${transaction.id}, Amount: ${transaction.amount}, Fee: ${fee}`);
    }
}

const paymentProcessor = new PaymentProcessor();
paymentProcessor.processPayment();
```

Applying the SRP:

```ts
class PaymentTransactionReader {
    public readTransaction(): Transaction {
        // Here we would perform the transaction reading, e.g., from a database
        return {
            id: "1",
            amount: 100.00,
            date: new Date(),
            payer: "John",
            payee: "Mary"
        };
    }
}

class PaymentFeeCalculator {
    public calculateFee(transaction: Transaction): number {
        // Here we would calculate the transaction fee based on some criteria
        return transaction.amount * 0.02; // For example, 2% fee
    }
}

class PaymentTransactionLogger {
    public logTransaction(transaction: Transaction, fee: number): void {
        // Here we would log the transaction and fee to a log file, database, etc.
        console.log(`Transaction logged - ID: ${transaction.id}, Amount: ${transaction.amount}, Fee: ${fee}`);
    }
}

const transactionReader = new PaymentTransactionReader();
const feeCalculator = new PaymentFeeCalculator();
const transactionLogger = new PaymentTransactionLogger();

const transaction = transactionReader.readTransaction();
const fee = feeCalculator.calculateFee(transaction);
transactionLogger.logTransaction(transaction, fee);
```

Comparison:

### Without SRP:

- The PaymentProcessor class is responsible for reading the transaction, calculating the fee, and logging the transaction to a log file.
- This violates the SRP because the class is dealing with multiple responsibilities.

### With SRP:

We have three distinct classes, each with a single responsibility:

-   PaymentTransactionReader is responsible only for reading payment transactions.
-   PaymentFeeCalculator is responsible only for calculating the fee for a payment transaction.   
-   PaymentTransactionLogger is responsible only for logging payment transactions to a log file.

Each class has a single reason to change and is easier to understand and maintain.

Following the SRP makes the code more modular, cohesive, and easier to understand, facilitating maintenance and evolution of the system over time.