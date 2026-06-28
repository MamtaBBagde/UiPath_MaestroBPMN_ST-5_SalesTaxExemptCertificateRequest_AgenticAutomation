# UiPath_MaestroBPMN_ST-5_SalesTaxExemptCertificateRequest_AgenticAutomation
ST-5 Sales Tax Exemption Certificate Agentic Automation is an end-to-end intelligent automation built on UiPath Maestro BPMN that handles the entire ST-5 certificate request lifecycle from incoming email to delivered certificate with minimal human intervention.

ST5 Sales Tax Exempt Certificate Request Agentic Use Case created using UiPath Maestro Flow. 
- Use of one Autonomous Agent
- One coded agent to get communication data and extract required fields
- Use of Human in the loop to validate vendor if vendor is not found in the database
- Use of context grounding storage bucket
- Use of RPA process to fill the ST-5 form
- Use of Outlook Microsoft 365 integration service

ST-5 Sales Tax Exempt Certificate Agentic Automation

Problem:
Today, processing ST-5 Sales Tax Exemption Certificate requests - issued to exempt organizations such as nonprofits and government entities to enable tax-exempt purchases from vendors is a largely manual, email-driven workflow that places significant burden on Accounts Payable teams. When a vendor submits a request, staff must manually review the email for complete information, validate the vendor, review the request, find missing information, identify and retrieve the ST-5 exemption certificate, populate the ST-5 form, and send it to the vendor, all while maintaining audit records and managing exceptions along the way. The process is repetitive, time-consuming, and dependent on human coordination, resulting in delays, inconsistent experiences, and administrative overhead.

What is ST-5?
The ST-5 Sales Tax Exemption Certificate is used in New Jersey. It is issued to exempt organizations (nonprofits, government entities, etc.) to make tax-exempt purchases from vendors. When an exempt organization (like a nonprofit or government agency) buys goods or services, they do not pay sales tax on those purchases. Normally, when anyone buys something, the seller charges sales tax. But if the buyer shows the vendor their ST-5 certificate, the vendor is legally allowed to skip charging sales tax on that transaction.
Example: A nonprofit buys office/medical supplies worth $10,000. Normally they did pay $10,662.50 (with NJ's 6.625% sales tax). With the ST-5, they just pay $10,000. 

Agentic Solution:
We have built an agentic ST-5 fulfillment automation powered by UiPath Agent, Communication Mining, Integration Services and Maestro that autonomously manages the end-to-end ST-5 request lifecycle.
The solution uses UiPath's agentic technology stack - Coding Agent, Action Center, Autonomous Agent, Context Grounding, Integration Services, Maestro BPMN to automate the end-to-end ST-5 request lifecycle with minimal human intervention.
Step 1 - Read & Extract Emails - Coded Agent
The process begins when a vendor submits an ST-5 request via email. UiPath coded agent automatically reads incoming vendor emails, intelligently extracts key fields using Communication Mining required to populate the ST-5 form including full vendor/supplier name, type of products or services provided, delivery location, and date of transaction and routes the request downstream for processing.
Step 2 - Validate Vendor (Action Center)
If the vendor is not found in the database, then human confirms the vendor's identity and eligibility. If the vendor is unrecognized or data is incomplete, the agent escalates to a human reviewer via Action Center keeping humans in the loop only for exceptions, not routine cases. Unresolvable cases are logged as business exceptions and the process terminates gracefully.
Step 3 - Populate Sales Tax Form (RPA)
Once all required data is validated, Maestro workflow autonomously populates the ST-5 exemption certificate using the extracted information eliminating manual form-filling by the Accounts Payable team entirely.
Step 4 - Audit Transactions
The completed ST-5 form is saved to a shared location, and an automated audit log is generated, verifying the tax-exempt status of the transaction and maintaining a complete, compliance-ready record for every request processed.
Step 5 - Send ST-5 certificate to Vendor
The filled ST-5 certificate is automatically emailed to the requesting vendor. Results are simultaneously shared with internal stakeholders and stored securely for audit defense ensuring full traceability from request to resolution. 
