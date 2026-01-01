# Bank-System-Management_JAVA

##Overview
A comprehensive Java-based banking application that simulates real-world banking operations for Savings Bank (SB) and Fixed Deposit (FD) accounts. This console application demonstrates core banking functionalities including account management, transactions, interest calculations, and customer relationship management with proper validation and error handling.

Account (Base Class)
├── accnumber: int
├── balance: double
├── Account() - Default constructor
└── Account(int, double) - Parameterized constructor

├── SBAccount (Savings Bank Account)
│   ├── deposit(double amount) - Add funds to account
│   ├── withdraw(double amount) - Withdraw with min balance check
│   └── calc_interest() - Calculate 4% quarterly interest

└── FDAccount (Fixed Deposit Account)
    ├── period: int - Deposit tenure
    ├── calc_interest() - Calculate 8.25% FD interest
    └── close() - Close FD and calculate maturity amount

Customer (Customer Management)
├── cust_id: int
├── name: String
├── address: String
├── sbacc: SBAccount
├── fdacc: FDAccount
├── static sbno, fdno - Auto-generated account numbers
├── createAccount(int type) - Create SB/FD account
└── transaction(int type) - Perform account operations

BankDemo (Main Driver)
└── Main menu-driven interface for banking operations

Core Technologies
1.Java SE: Core Java programming
2.Object-Oriented Programming: Inheritance, encapsulation, polymorphism
3.Exception Handling: Try-catch blocks for robust error management
4.I/O Streams: BufferedReader for console input
5.Static Members: Class variables for account number generation

Design Patterns
1.Inheritance: Account → SBAccount, FDAccount
2.Encapsulation: Protected data members with public methods
3.Singleton Pattern: Single instance of bank operations
4.Factory Pattern: Account creation based on type
