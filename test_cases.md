# Test Cases – Transfer Funds (ParaBank)

### Common preconditions

The user is registered in ParaBank
The user has two accounts: Account A (source) and Account B (destination)
The balances of both accounts are known before each test

## TC-01 – Transfer between own accounts (End-to-End)

| Field	| Value |
|:--:|:--:|
| Type |	End-to-end – positive |
| Priority |	High |
| Test data	| Amount: 100.00 |

### Steps

1. Open https://parabank.parasoft.com and log in with valid credentials.
2. Go to Accounts Overview and write down the balances of Account A and Account B.
3. Go to Transfer Funds.
4. Enter amount 100.00.
5. Select Account A in "From account" and Account B in "To account".
6. Click Transfer.
7. Go to Accounts Overview.
9. Open the activity of Account A, and then the activity of Account B.

Expected result

Step 6: the message "Transfer Complete!" is displayed with the amount and both account numbers.
Step 7: the balance of Account A is 100.00 lower and the balance of Account B is 100.00 higher.
Step 8: Account A shows a debit of 100.00 and Account B shows a credit of 100.00, both with today's date.

Actual result: Completed without incident.

## TC-02 – Transfer amount greater than the available balance

| Field	| Value |
|:--:|:--:|
| Type|Functional – negative (business rule)|
|Priority|	High|
|Test data|	Amount: balance of Account A + 1.00|

Steps

Log in and write down the balance of Account A.
Go to Transfer Funds.
Enter an amount 1.00 higher than the balance of Account A.
Select Account A as source and Account B as destination.
Click Transfer.

Expected result

The transfer is rejected with a clear message about insufficient funds.
The balances of Account A and Account B do not change.
No new entries appear in the activity of either account.

Actual result: To be completed during execution Status: Not executed

TC-03 – Transfer with empty amount

| Field	| Value |
|:--:|:--:|
|Type|	Functional – negative (input validation)|
|Priority|	Medium|
|Test data|	Amount: empty|

Steps

Log in and go to Transfer Funds.
Leave the amount field empty.
Select Account A as source and Account B as destination.
Click Transfer.

Expected result

A validation message asks the user to enter an amount.
The transfer is not processed and the balances do not change.

Actual result: To be completed during execution Status: Not executed

TC-04 – Transfer with invalid amount values

| Field	| Value |
|:--:|:--:|
|Type|	Functional – negative (input validation)|
|Priority|	Medium|
|Test data|	-50, 0, abc, 10,50|

Steps

Log in and go to Transfer Funds.
Enter the first value from the test data.
Select Account A as source and Account B as destination.
Click Transfer.
Repeat steps 2 to 4 for each value.

Expected result

For each value, the system shows a validation message.
No transfer is processed and the balances do not change.

Actual result: To be completed during execution (one result per value) Status: Not executed

TC-05 – Transfer to the same account

| Field	| Value |
|:--:|:--:|
|Type|	Functional – negative (business rule)|
|Priorit|y	Medium|
|Test data|	Amount: 50.00|

Steps

Log in and write down the balance of Account A.
Go to Transfer Funds.
Enter amount 50.00.
Select Account A in both "From account" and "To account".
Click Transfer.

Expected result

The system rejects the operation with a message saying that source and destination must be different.
The balance of Account A does not change and no entries are added to its activity.

Actual result: To be completed during execution Status: Not executed

Execution summary
|ID|Title|Type|Priority|	Status|
|:--:|:--:|:--:|:--:|:--:|
|TC-01|	Transfer between own accounts|	E2E|	High|	Not executed|
|TC-02|	Amount greater than balance|	Negative|	High|	Not executed|
|TC-03|	Empty amount|	Negative|	Medium|	Not executed|
|TC-04|	Invalid amount values|	Negative|	Medium|	Not executed|
|TC-05|	Same source and destination|	Negative|	Medium|	Not executed|
