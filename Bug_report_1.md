# Bug Report #1

### Field	Value

|ID|BUG-01|
|:--:|:--:|
|Title|	Financial loss caused by allowing a transfer exceeding the account balance|
|Related| TC-02|
|Severity|	Critical|
|Priority|	High|
|Environment|	ParaBank demo - 05052026|
|Reported by|	Richard Tripodi|

### Preconditions

You must have access to two active accounts and a balance in at least one of them to make a transfer.

### Steps to reproduce
1. Log in and write down the balance of Account A. [Evidence TC_2_1](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_2_1.png)
2. Go to Transfer Funds.
3. Enter an amount 1.00 higher than the balance of Account A. [Evidence TC_2_2](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_2_2.png)
4. Select Account A as source and Account B as destination.
5. Click Transfer. [Evidence TC_2_3](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_2_3.png)

### Expected result

The transfer is rejected with a clear message about insufficient funds.
The balances of Account A and Account B do not change.
No new entries appear in the activity of either account.

### Actual result

Unsuccessful result. It was evidenced that the system allowed transfers to be made despite having insufficient funds. It processed the credits and debits without taking the balance limit into account. A possible reason is that the account may have an overdraft transfer facility (unbacked), but this needs to be verified.

### Impact

Money, balances, customers, compliance.

### Evidence

Screenshots:
1. [Evindence TC_2_1](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_2_1.png)
2. [Evindence TC_2_2](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_2_2.png)
3. [Evindence TC_2_3](https://github.com/richardtripodi15-cmyk/manual_test_case/blob/main/images/TC_2_3.png)
