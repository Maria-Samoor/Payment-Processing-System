# Payment Processing System

This project implements a payment processing system that supports multiple payment methods (Credit Card, PayPal, Cryptocurrency) and discount strategies (Percentage-based, Fixed-amount). The system is designed with flexibility, allowing easy integration of additional payment methods and discounts. The project also includes a transaction logging mechanism for tracking payment outcomes.

## Features

- **Payment Methods:**
  - **Credit Card Payment**: Validates card number, expiry date, and CVV before processing.
  - **PayPal Payment**: Validates email format and processes the payment.
  - **Cryptocurrency Payment**: Validates a wallet address before processing the payment.

- **Discount Strategies:**
  - **Percentage Discount**: Applies a discount based on a percentage of the item price.
  - **Fixed-Amount Discount**: Subtracts a fixed amount from the item price.

- **Currency Conversion**: Supports converting between different currencies (USD, EUR, GBP).

- **Transaction Logging**: Logs each transaction's amount and status (Success or Failure).

## Technologies Used

- Python 3.x
- Object-Oriented Design Principles
- Strategy Pattern for discount strategies
- Abstract Base Classes for payment methods
- In-memory storage for transaction logs

## Project Structure

