# manual_test_case
Manual testing project for the Transfer Funds feature of ParaBank, a public demo banking application.

## ParaBank – Manual Testing: Transfer Funds

This project shows how I plan and design tests for a banking feature, using a risk-based approach.

| File | Description |
|:--:|:--:|
|  TEST_PLAN.md	| Test plan: scope, approach, risks, environment, entry and exit criteria |
| TEST_CASES.md |	5 manual test cases: 1 end-to-end and 4 functional (positive and negative) |
| BUG_REPORT_TEMPLATE.md	| Template used to report defects found during execution |

# ¿Why this feature? 
Fund transfers move real money. A defect here can cause:

Economic loss for the customer or the bank
Wrong balances and accounting differences
Reputational damage and regulatory issues

For this reason, the test design focuses on business rules (balance, accounts, amounts) and not only on the user interface.

Approach

1 end-to-end case that covers the main business flow: login, transfer, and verification of balances and account activity.
4 functional cases that cover input validation and business rules with negative scenarios.

Author

Richard Tripodi – Manual QA | Functional Analyst – Banking and Fintech | Email: richardtripodi15@gmail.com
