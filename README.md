java c
Bank Management System Database Design Document
1. Introduction
This document describes the database design for a Bank
Management System, which aims to provide comprehensive data
management solutions for banking operations, including customer and account management, transaction processing, loan servicing, and
mobile banking capabilities.
2. Business Problems Addressed
The database is designed to tackle key business challenges:
•     Quick and Informed Decision-making: Need for real-time insights into banking activities for faster and more accurate
decisions.
• ATM Network Efficiency: Challenges in maintaining an
efficient ATM network, including issues with cash shortages and maintenance, impacting user experience.
•     Operational Efficiency in Banking Services: Difficulty in ensuring operational efficiency with real-time transaction
monitoring and cash flow management.
3. Entities Description
3.1 Customer
•    Attributes: CustomerID, Name, Address, ContactInfo
•     Relationships: Has Accounts, Has Loans, Uses Mobile Banking, Receives Alerts, Performs Transactions, Belong to a Branch
3.2 Account
•    Attributes: AccountNumber, Type, Balance, CustomerID, BranchID
•     Relationships: Owned by Customer, Handled by Branch, Involved in Transactions, Has Beneficiaries, Accessible via Mobile Banking
3.3 Transaction
• Attributes: TransactionID, Date, Time, Type, Amount, AccountNumber
•     Relationships: Involves Account, Processed by Branch or ATM, Initiated via Mobile Banking, Triggers Alerts
3.4 Loan
•    Attributes: LoanID, Amount, Type, InterestRate, CustomerID
•     Relationships: Taken by Customer, Includes Payments 3.5 Loan Payment
• Attributes: PaymentID, Date, Amount, LoanID
•     Relationships: Applied to Loan 3.6 Employee
• Attributes: EmployeeID, Name, Position, BranchID
•     Relationships: Works at Branch 3.7 Branch
• Attributes: BranchID, Name, Location, ManagerID
•     Relationships: Houses Employees, Manages Accounts and Transactions, Consists of Customers
3.8 ATM
• Attributes: ATMID, Location, ManagedByBranchID
•     Relationships: Processes Transactions 3.9 Account Beneficiary
•    Attributes: BeneficiaryID, Name, Relationship, AccountNumber
•     Relationships: Assigned to Account 3.10 Alerts
• Attributes: AlertID, Type, Message, CustomerID
•     Relationships: Sent to Customer, Can be Triggered by Transactions, Managed via Mobile Banking
3.11 Mobile Banking
• Attributes: MobileBankingID, CustomerID, DeviceID, RegistrationDate, LastAccessDate
•     Relationships: Provides Banking Services to Customer, Initiates Transactions, Manages Alerts, Linked to Accounts
4. Entity Relationships
4.1 Customer<代 写Bank Management System Database Design DocumentC/C++
代做程序编程语言br>• Accounts: One-to-Many (A customer can hold multiple accounts).
•     Loans: One-to-Many (A customer can have several loans).
•     Mobile Banking: One-to-One (Each customer can register a single mobile banking profile for their use).
•     Branch: Many-to-One ( A Customer must belong to a branch )
• Alerts: One-to-Many (Multiple customers are linked to a single branch ).
•    Transactions: One-to-Many (A customer can perform. numerous transactions).
4.2 Account
•     Customer: Many-to-One (Multiple accounts can be held by a single customer).
•    Transactions: One-to-Many (Multiple transactions can occur on a single account).
•     Branch: Many-to-One (Multiple accounts can be managed by a single branch).
•     Beneficiaries: One-to-One (An account can have one beneficiary).
•     Mobile Banking: Many-to-One (Multiple accounts can be accessed via a single mobile banking application).
4.3 Transaction
•    Account: Many-to-One (Multiple transactions are associated with a single account).
•    ATM/Branch: Many-to-One (Multiple transactions can be processed by a single ATM or branch).
•     Mobile Banking: Many-to-One (Multiple transactions can be initiated through mobile banking).
4.4 Loan
• Customer: Many-to-One (A customer can have multiple loans).
•     Payment: One-to-Many (A loan can have multiple associated payments).
4.5 Loan Payment
•     Loan: Many-to-One (Multiple payments can be applied to a single loan).
4.6 Employee
•     Branch: Many-to-One (Several employees can work at a single branch).
4.7 Branch
•     Employee: One-to-Many (A branch can employ multiple employees).
• Customer: One-to-Many(A branch contains multiple customers).
• Accounts: One-to-Many (A branch can manage multiple accounts).
• Transactions: One-to-Many (A branch can process numerous transactions).
4.8 ATM
• Transactions: One-to-Many (An ATM can handle numerous transactions).
4.9 Account Beneficiary
•    Account: One-to-One (A beneficiary must be linked to a single account).
4.10 Alerts
•     Customer: Many-to-One (Multiple alerts can be sent to a single customer).
•     Mobile Banking: Many-to-One (Multiple alerts can be managed via a single mobile banking application).
4.11 Mobile Banking
•     Customer: One-to-One (A single mobile banking profile is associated with one customer).
• Transactions: One-to-Many (A mobile banking profile can initiate multiple transactions).
•    Alerts: One-to-Many (A mobile banking profile can receive and manage multiple alerts).
•    Accounts: One-to-Many (A mobile banking profile can access multiple accounts owned by the customer).
5. ER Diagram






         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
