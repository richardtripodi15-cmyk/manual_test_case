# Bug Report #4

### Field	Value

|ID|BUG-04|
|:--:|:--:|
|Title|	Incorrect transfer|
|Related| TC-05|
|Severity|	Major |
|Priority|	Low |
|Environment|	ParaBank demo - 05052026|
|Reported by|	Richard Tripodi|

### Preconditions

You must have access to two enabled accounts to make transfers.

### Steps to reproduce

1. Log in and write down the balance of Account A.
2. Go to Transfer Funds.
3. Enter amount 100.00.
4. Select Account A in both "From account" and "To account". [Evindence TC_5_1](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_5_1.png)
5. Click Transfer.

### Expected result

The system rejects the operation with a message saying that source and destination must be different.
The balance of Account A does not change and no entries are added to its activity.

### Actual result

Unexpected outcome. The system allowed a transfer where the source and destination accounts were the same.

### Impact

Customers, compliance.

### Evidence

Screenshots:
1. [Evindence TC_5_1](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_5_1.png
