Mortgage Application & Broker Fraud Intelligence Pod 

FDM Skills Lab 

 

Project Overview 
AUSTRAC’s Fintel Alliance has uncovered coordinated mortgage fraud and systemic weaknesses across parts of Australia’s lending sector.  

Through Operation Claw, we analysed data from 10 major Australian banks and identified potentially hundreds of millions of dollars in suspected fraudulent loans. Most were linked to properties in Sydney. 

Build a proof of concept that identifies potentially fraudulent mortgage applications and high-risk broker behaviour using mortgage origination and broker performance data already held within a bank. 

The solution uses multiple AI components working together to assess application risk, detect anomalous patterns, identify emerging broker risks, and support investigators through explainable recommendations. 

The objective is not to automatically reject applications. The system provides risk indicators, investigation recommendations, and supporting evidence so lending and fraud teams can make informed decisions. 

The solution focuses exclusively on internal bank data, making it practical for rapid prototyping and realistic deployment. 

 

Business Problem 

Mortgage fraud remains one of the most costly forms of financial crime facing lenders. 

Common risks include: 

    Income inflation 

    Fictitious employment 

    Undisclosed liabilities 

    Identity manipulation 

    Application misrepresentation 

    Collusive broker behaviour 

    Organised fraud rings 

Most current controls review applications individually. 

Fraud investigations often miss patterns that emerge when applications are viewed across an entire broker portfolio. 

The result is: 

    Higher credit losses 

    Increased manual reviews 

    Poor investigator productivity 

    Regulatory exposure 

    Increased operational costs 

The proposed solution shifts detection earlier in the mortgage lifecycle. 

 

Scope 

In Scope 

Mortgage Application Data 

Synthetic datasets generated in Sprint 1 based upon: 

    Applicant demographics 

    Employment details 

    Income declarations 

    Existing liabilities 

    Property information 

    Loan characteristics 

    Serviceability assessments 

    Lending decisions 

Broker Data 

Synthetic datasets containing: 

    Broker profiles 

    Submission history 

    Approval outcomes 

    Settlement outcomes 

    Early arrears indicators 

    Historical fraud referrals 

AI Components 

    Application Risk Assessment Engine 

    Broker Risk Scoring Engine 

    Portfolio Pattern Detection Engine 

    Copilot Investigation Assistant 

User Interface 

Web application providing: 

    Broker scorecards 

    Application review queues 

    Risk explanations 

    Investigation workbench 

    Executive dashboards 

Data Platform 

    Databricks 

    Delta Tables 

    Unity Catalog 

    Power BI 

    OpenAI / Databricks Foundation Models 

 

Out of Scope 

    Credit bureau integration 

    Open Banking feeds 

    Property valuation APIs 

    Government data matching 

    Verification of Income Services 

    Real customer data 

    Automated loan approval or rejection 

    Production deployment 

 

Platform & Tools 

Data Platform 

    Databricks Community Edition or Free Edition 

    Delta Lake 

    Unity Catalog 

AI Components 

    Azure OpenAI 

    Databricks Foundation Models 

    LangChain 

    Python 

Development 

    GitHub 

    FastAPI 

    Docker 

    PyTest 

Front End 

    React 

    Power BI 

    Databricks Apps 

 

Architecture at a Glance 

Data Layer 

Mortgage Applications 

↓ 

Validation & Standardisation 

↓ 

Curated Delta Tables 

↓ 

Feature Engineering 

↓ 

Risk Scoring Models 

 

AI Layer 

Application Risk Agent 

Reviews a mortgage application. 

Outputs: 

    Risk score 

    Anomaly indicators 

    Key findings 

    Recommended actions 

 

Broker Intelligence Agent 

Reviews broker portfolio history. 

Outputs: 

    Broker risk score 

    Behavioural trends 

    Emerging risk patterns 

 

Investigation Copilot 

Provides natural language investigation capability. 

Example prompts: 

    Which brokers present the highest fraud risk? 

    Explain why Application A123 was flagged. 

    Show applications similar to this one. 

    Compare broker performance against peers. 

 

User Layer 

Fraud Operations Dashboard 

    High-risk applications 

    Broker watchlist 

    Investigation queue 

Executive Dashboard 

    Fraud risks identified 

    Portfolio exposure 

    Top-risk brokers 

    Operational savings 

 

Team Roles (6) 

Delivery Lead 

Responsibilities: 

    Sprint planning 

    Backlog management 

    Stakeholder engagement 

    Sprint reviews 

    Executive reporting 

 

Data Engineer 

Responsibilities: 

    Data ingestion 

    Data modelling 

    Feature engineering 

    Delta table management 

    Data quality controls 

 

AI Engineer 

Responsibilities: 

    Risk scoring models 

    Anomaly detection 

    Prompt engineering 

    Agent orchestration 

    Model evaluation 

 

Software Engineer 

Responsibilities: 

    API development 

    Backend services 

    Integration components 

    Authentication 

 

Front-End Engineer 

Responsibilities: 

    React dashboard 

    User experience 

    Visualisation 

    Dashboard testing 

 

Governance & Risk Engineer 

Responsibilities: 

    Explainability 

    Audit logging 

    Model governance 

    Documentation 

    Success metric reporting 

 

Sprint Plan 

Sprint 1 (Weeks 1-2) 

Discovery, Data Design & Environment Build 

Objectives 

Establish project foundations and create mortgage datasets. 

Activities 

Business Discovery 

Research: 

    Mortgage fraud schemes 

    Broker operating models 

    Mortgage origination lifecycle 

    Credit assessment process 

 

Data Model Design 

Design datasets for: 

Applications 

Fields: 

    Application ID 

    Customer ID 

    Broker ID 

    Salary 

    Expenses 

    Employment tenure 

    Loan amount 

    Property value 

    LVR 

    Credit score 

Broker Dataset 

Fields: 

    Broker ID 

    Region 

    Aggregator 

    Applications submitted 

    Approval rate 

    Fraud referrals 

    Early arrears rate 

 

Synthetic Data Creation 

Generate: 

    100,000 applications 

    2,000 brokers 

    500 fraud-labelled applications 

Fraud scenarios: 

    Income inflation 

    Expense suppression 

    Employment anomalies 

    Broker collusion 

 

Environment Setup 

Build: 

    Databricks workspace 

    GitHub repository 

    CI/CD pipeline 

    Data lake structure 

Deliverables 

    Data dictionary 

    Solution architecture 

    Synthetic datasets 

    Curated Delta tables 

Sprint Review 

Demonstrate: 

    Data structure 

    Fraud scenarios 

    Initial dashboards 

 

Sprint 2 (Weeks 3-4) 

Application Fraud Detection 

Objectives 

Identify suspicious mortgage applications. 

Activities 

Feature Engineering 

Build risk indicators: 

    Income-to-occupation variance 

    Expense anomalies 

    LVR anomalies 

    DTI ratio outliers 

    Employment inconsistencies 

 

Anomaly Detection 

Implement: 

    Isolation Forest 

    Statistical outlier detection 

    Cluster analysis 

 

Application Risk Scoring 

Generate scores: 

    Low Risk 

    Medium Risk 

    High Risk 

 

Investigation Explanations 

Provide reasons such as: 

"Declared income is 3.4x higher than comparable applicants." 

"Living expenses are significantly below peer averages." 

 

Deliverables 

    Application scoring engine 

    Risk explanation engine 

    Fraud dashboard 

Sprint Review 

Demonstrate: 

    Fraud detection capability 

    Top flagged applications 

    Explainable AI outputs 

 

Sprint 3 (Weeks 5-6) 

Broker Intelligence & Portfolio Risk 

Objectives 

Assess broker behaviour and portfolio quality. 

Activities 

Broker Risk Framework 

Calculate: 

    Application quality 

    Approval trends 

    Arrears trends 

    Fraud referral trends 

 

Portfolio Analysis 

Identify: 

    Similar borrower patterns 

    Geographic concentration 

    Repeated employers 

    Repeated income structures 

 

Broker Ranking 

Generate: 

    Low-risk brokers 

    Medium-risk brokers 

    High-risk brokers 

 

Network Analysis 

Detect: 

    Broker clusters 

    Related fraud patterns 

    Emerging behaviours 

 

Deliverables 

    Broker scorecards 

    Broker ranking engine 

    Portfolio risk dashboard 

Sprint Review 

Demonstrate: 

    High-risk brokers 

    Broker comparison views 

    Historical trends 

 

Sprint 4 (Weeks 7-8) 

Copilot Investigation Assistant & Executive Demo 

Objectives 

Create investigator experience using natural language interaction. 

Activities 

Copilot Assistant 

Enable queries: 

"Show all High Risk applications this week." 

"Why is Broker BR109 classified as High Risk?" 

"Compare this application to similar approved applications." 

 

Investigation Workspace 

Provide: 

    Case summaries 

    Risk factors 

    Supporting evidence 

    Audit history 

 

Executive Dashboard 

Metrics: 

    Fraud cases detected 

    Estimated losses avoided 

    High-risk broker count 

    Investigation productivity gains 

 

Evaluation Framework 

Measure: 

    Detection accuracy 

    Precision 

    False positive rate 

    User acceptance 

 

Deliverables 

    Copilot Assistant 

    Investigation Dashboard 

    Executive Dashboard 

    Final Presentation 

Sprint Review 

Live demonstration of: 

Application Submission → Risk Assessment → Broker Review → Investigation Copilot → Executive Reporting 

 

Evaluation Metrics 

Fraud Detection 

    Precision > 75% 

    Recall > 80% 

    Explainability coverage 100% 

Operational Efficiency 

    30% reduction in manual review effort 

    50% faster investigation completion 

User Experience 

    Investigator satisfaction score 

    Fraud team acceptance rate 

Business Value 

    Fraud losses identified 

    Estimated cost avoidance 

    Potential productivity savings 

 

Governance & Risk Requirements 

    No real customer data 

    Full auditability of all model outputs 

    Explainable risk decisions 

    Role-based access controls 

    Synthetic data only 

    Human approval required for all lending decisions 

 

Stretch Goals 

If the pod progresses ahead of schedule: 

Document Intelligence 

Analyse payslips and employment letters. 

Multi-Agent Workflow 

Specialised agents for: 

    Income analysis 

    Broker assessment 

    Portfolio analysis 

GenAI Investigation Reports 

Automatically generate case summaries for fraud analysts. 

Executive Copilot 

Natural language portfolio analytics: 

"Which brokers represent the greatest risk exposure to the bank this quarter?" 

 

Final Deliverables 

    Working fraud detection platform 

    Synthetic mortgage dataset 

    Application risk scoring engine 

    Broker intelligence engine 

    Copilot investigation assistant 

    Power BI executive dashboard 

    Evaluation report 

    GitHub repository 

    Architecture documentation 

    Executive presentation 