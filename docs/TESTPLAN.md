# COBOL Student Accounts System Test Plan

This test plan covers the business logic implemented in the COBOL application for student account management. Use this plan to validate the system with business stakeholders and as a basis for future unit and integration tests in Node.js.

| Test Case ID | Test Case Description                | Pre-conditions                  | Test Steps                                                                 | Expected Result                                 | Actual Result | Status (Pass/Fail) | Comments |
|--------------|--------------------------------------|----------------------------------|----------------------------------------------------------------------------|--------------------------------------------------|---------------|--------------------|----------|
| TC01         | View account balance                 | Account exists                   | 1. Start app<br>2. Select 'View Balance'                                   | Current balance is displayed                     |               |                    |          |
| TC02         | Credit account with valid amount     | Account exists                   | 1. Start app<br>2. Select 'Credit Account'<br>3. Enter valid amount        | Amount is credited, new balance shown            |               |                    |          |
| TC03         | Debit account with valid amount      | Account exists, balance >= amount| 1. Start app<br>2. Select 'Debit Account'<br>3. Enter valid amount         | Amount is debited, new balance shown             |               |                    |          |
| TC04         | Debit account with excessive amount  | Account exists, balance < amount | 1. Start app<br>2. Select 'Debit Account'<br>3. Enter amount > balance     | Transaction rejected, error message shown         |               |                    |          |
| TC05         | Credit account with invalid amount   | Account exists                   | 1. Start app<br>2. Select 'Credit Account'<br>3. Enter negative/zero amount| Transaction rejected, error message shown         |               |                    |          |
| TC06         | Debit account with invalid amount    | Account exists                   | 1. Start app<br>2. Select 'Debit Account'<br>3. Enter negative/zero amount | Transaction rejected, error message shown         |               |                    |          |
| TC07         | Exit application                     | None                             | 1. Start app<br>2. Select 'Exit'                                            | Application exits gracefully                     |               |                    |          |
| TC08         | Invalid menu selection               | None                             | 1. Start app<br>2. Enter invalid menu choice                                 | Error message shown, menu re-displayed            |               |                    |          |

---
Add actual results, status, and comments after executing each test case.