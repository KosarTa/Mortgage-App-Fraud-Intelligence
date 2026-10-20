## Mortgage Fraud Research
## Methods of Fraud:
# Inflated incomes
# Misrepresented employment
# Fabricated or unverifiable business activity
# Falsified or misleading documents (reportedly including false payslips and fabricated invoices)
# Offshore or third-party funds used for settlements and repayments
# Investigators also found that there were the same brokers repeatedly across multiple loan application

## Mortgage Origination lifecycle 
# 1. Enquiry & fact-find	Broker or bank gathers the borrower's goals, income, expenses and debts	-> Borrower or broker overstates income or understates expenses -> Salary, expenses
# 2. Application & documents	Application submitted with ID, payslips, bank statements, tax returns	-> Falsified documents, fake employer, identity manipulation -> Employment tenure (document checks out of scope)
# 3. Verification	Lender checks documents, employment, ID	-> Fake employers that "verify" by phone; unverifiable business income -> Employment details
# 4. Credit assessment	Lender checks serviceability, credit score, LVR, DTI	-> Numbers engineered to just pass the thresholds -> Credit score, LVR, serviceability
# 5. Valuation	Property valued to set the LVR	-> Inflated valuation (out of scope: no valuation API) -> Property value
# 6. Approval / decision	Credit decision made, sometimes conditional	-> Our system sits here: flag risk before approval -> Lending decision
# 7. Settlement	Funds paid out, property transferred	-> Third-party or offshore funds used for the deposit -> Settlement outcomes (broker data)
# 8. Post-settlement	Repayments made, arrears monitored	-> Early arrears often signal fraud (borrower could never really afford it) -> Early arrears indicators

## Broker Operating Model 
# The structure of operation is: 
# Broker(deals with the customer, compares lenders, prepares and submits the application.) 
# Aggregator(deals with the customer, compares lenders, prepares and submits the application.)
# Lender(assesses and approves the loan and pays commission via the aggregator.)

# Brokers are paid in comission, this means that a minority might be tempted to commit fraud: 
# The signs of fraud can occur from: 
# 1. Approval rate is unusually high compared to their peers
# 2. Historical Fraud referrals 
# 3. Repeated employers, income amounts or loan structures across a broker's clients

## Credit Assessment Process 
# 1. Serviceability	Can the borrower afford repayments? Income minus expenses minus existing debts, tested at a higher rate	-> Inflate income, suppress expenses, hide debts -> Salary, expenses, existing liabilities, serviceability assessment
# 2. Serviceability buffer	APRA expects banks to test repayments at 3 percentage points above the loan rate (confirmed unchanged May 2026)	-> Applications engineered to just pass -> Serviceability assessment
# 3. Living expenses	Lenders use the higher of declared expenses and a benchmark (commonly HEM, the Household Expenditure Measure)	-> Declared expenses suspiciously close to or below the benchmark -> Expenses
# 4. DTI (debt-to-income)	Total debt ÷ gross income; APRA limits banks to 20% of new lending at DTI ≥ 6 (confirmed May 2026)	-> Inflating income pushes DTI below 6 -> Salary, loan amount, existing liabilities
# 5. LVR (loan-to-value ratio)	Loan ÷ property value; above 80% usually needs Lenders Mortgage Insurance	-> Inflated property value or hidden deposit source lowers the LVR -> LVR, loan amount, property value
# 6. Credit score	Repayment history and credit behaviour	-> Identity manipulation (out of scope: no bureau integration) -> Credit score (synthetic)
# 7. Employment	Type (PAYG, self-employed), tenure, stability	-> Fake employers; short tenure with high salary -> Employment tenure