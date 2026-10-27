# Bug Report #2

### Field	Value

|ID|BUG-02|
|:--:|:--:|
|Title|	Incorrect message|
|Related| TC-02|
|Severity|	Trivial|
|Priority|	Medium |
|Environment|	ParaBank demo - 05052026|
|Reported by|	Richard Tripodi|

### Preconditions

You must have access to two enabled accounts to make transfers.

### Steps to reproduce
1. Log in and go to Transfer Funds.
2. Leave the amount field empty.[Evindence TC_3_1](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_3_1.png)
3. Select Account A as source and Account B as destination.
4. Click Transfer.[Evindence TC_3_2](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_3_2.png)

### Expected result

A validation message asks the user to enter an amount.
The transfer is not processed and the balances do not change.

### Actual result

Unsuccessful result. The system response is not as expected, although it functionally prevents monetary losses.

### Impact

Customers, compliance.

### Evidence

Screenshots:
1. [Evindence TC_3_1](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_3_1.png)
2. [Evindence TC_3_2](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_3_2.png)
