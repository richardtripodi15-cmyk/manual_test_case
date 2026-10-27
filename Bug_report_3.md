# Bug Report #3

### Field	Value

|ID|BUG-03|
|:--:|:--:|
|Title|	Transfers to be made with negative values and zero amounts|
|Related| TC-04|
|Severity|	Critical|
|Priority|	Medium |
|Environment|	ParaBank demo - 05052026|
|Reported by|	Richard Tripodi|

### Preconditions

You must have access to two enabled accounts to make transfers.

### Steps to reproduce

1. Log in and go to Transfer Funds.
2. Enter the first value from the test data.
3. Select Account A as source and Account B as destination.
4. Click Transfer.
5. Repeat steps 2 to 4 for each value.

### Expected result

For each value, the system shows a validation message.
No transfer is processed and the balances do not change.

### Actual result

Unsuccessful result. The system allows transfers to be made with negative values and zero amounts.

### Impact

Money, balance, customers, compliance.

### Evidence

Screenshots:
1. [Evidence TC_4_1](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_4_1.png)
2. [Evidence TC_4_2](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_4_2.png)
