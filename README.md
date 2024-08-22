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
payment-processing-system/
│
├── main.py # Main program to execute the payment processing system
├── payment_methods.py # Contains classes for different payment methods
├── discounts.py # Contains classes for discount strategies and currency conversion
├── database.py # Contains the in-memory database logic for logging transactions
├── README.md # Project documentation
└── requirements.txt # (Optional) Python dependencies if needed

## How It Works

### 1. Payment Methods

The system supports three types of payment methods:
- **Credit Card Payment**: Requires card number, expiry date, and CVV.
- **PayPal Payment**: Requires an email address.
- **Crypto Payment**: Requires a wallet address.

Each payment method class implements the `validate_payment_details` and `process_payment` methods to handle its specific validation and payment logic.

### 2. Discount Strategies

You can apply discounts to items using:
- **Percentage-based Discount**: E.g., a 20% discount.
- **Fixed-amount Discount**: E.g., $30 off the original price.

### 3. Transaction Processing

The `PaymentProcessor` class handles:
- Validating payment details.
- Applying any discounts to the item price.
- Processing the payment and logging the transaction status.

### 4. Logging Transactions

All transactions (successful or failed) are logged and stored in a simple in-memory database. The logs include the payment amount and status.

## How to Run the Project

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/payment-processing-system.git
    cd payment-processing-system
    ```

2. Run the main script:

    ```bash
    python main.py
    ```

3. The program will simulate processing payments using different payment methods and items with varying discounts. After processing, the transaction logs will be displayed.

## Example Output

```plaintext
Validating credit card details for card ending in 5678...
Processing credit card payment of $160.0 from card ending in 5678
Validating PayPal account: user@example.com...
Processing PayPal payment of $120.0 from account user@example.com
Validating cryptocurrency wallet: 0x1234567890abcdef1234567890abcdef12345678...
Processing cryptocurrency payment of $100.0 from wallet 0x1234567890abcdef1234567890abcdef12345678

Transaction Logs:
{'amount': 160.0, 'status': 'Success'}
{'amount': 120.0, 'status': 'Success'}
{'amount': 100.0, 'status': 'Success'}
