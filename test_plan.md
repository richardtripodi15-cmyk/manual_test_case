# Test Plan – Transfer Funds (ParaBank)
1. Objective

Verify that a registered customer can transfer money between their own accounts, and that the system applies the business rules correctly: valid amounts, available balance, and correct update of balances and account activity.

2. Scope

Transfer Funds page
Accounts Overview (to verify balances)
Account Activity (to verify debit and credit entries)

3. Test approach

Risk-based testing. Cases are prioritized by business impact:

| Priority |	Criteria |
|:--:|:--:|
|High |	A failure can cause wrong balances or loss of money |
|Medium |	A failure allows invalid data but does not move money |
|Low |	Cosmetic or usability issues |

Test types:

End-to-end: the full business flow, from login to verification of balances and activity.
Functional – positive: valid inputs produce the expected result.
Functional – negative: invalid inputs or forbidden operations are rejected.

4. Risks

| Risk |	Impact |	Mitigation |
|:--:|:--:|:--:|
| Transfer is allowed without enough balance |	High | negative balance, economic loss	TC-02 |
| Debit is applied but credit is not (or the opposite) |	High | accounting difference	 verifies both accounts TC-01 |
| Invalid amounts are accepted (empty, negative, text) |	Medium | data corruption	TC-03, TC-04 |
| Transfer to the same account creates fake movements |	Medium | wrong activity history	TC-05 |
| Demo database is reset during testing	| Low | test data lost	Create test data at the start of each session |

5. Test environment

Application: ParaBank public demo – https://parabank.parasoft.com
Browser: Google Chrome
Test data: a new user created with the Register option, with at least two accounts (the second one created with "Open New Account")

Note: the demo database can be reset at any time, so test data must be created before each execution.

6. Entry criteria
   
The application is available
A test user exists with at least two accounts with known balances

7. Exit criteria
   
100% of the test cases were executed
All High priority defects are reported with evidence
Execution results are documented in TEST_CASES.md

8. Defect severity
    
| Severity	| Description |
|:--:|:--:|
| Critical	| Wrong balances  money lost or created |
| Major	| Business rule not applied but no money moved |
| Minor	| Wrong message or validation workaround exists |
| Trivial |	Cosmetic issue |

9. Deliverables

Test plan (this document)
Test cases with execution results
Bug reports for the defects found

Author

Richard Tripodi – Manual QA | Functional Analyst – Banking and Fintech | Email: richardtripodi15@gmail.com
