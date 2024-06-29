# AuditAndCompliance
The Audit and Compliance project leverages generative AI to revolutionize audit and compliance processes within financial institutions. By automating traditionally manual tasks, the project aims to enhance accuracy, efficiency, and adaptability in managing regulatory standards and financial transactions. Through seamless integration of technologies like Microsoft Azure and OpenAI, the project ensures robust compliance frameworks that can adapt to evolving regulations, thereby optimizing organizational compliance efforts while minimizing operational overhead. Key components include: 

A. Data Integration and Preprocessing
File: data_integration_preprocessing.py

Overview
In this module, we aggregate financial transaction data from various sources into a centralized data repository. This is a crucial step for ensuring that all relevant data is available for subsequent analysis by AI models.

Steps
i. Fetching Data:
We use an API to fetch transaction data from an ERP (Enterprise Resource Planning) system.
The API call is authenticated using a mock API key.

ii. Data Conversion:
The fetched data, typically in JSON format, is converted into a Pandas DataFrame for easier manipulation and analysis.

iii. Data Storage:
The processed DataFrame is uploaded to Azure Blob Storage, a scalable object storage service provided by Microsoft Azure. This ensures that the data is securely stored and easily accessible for downstream processing.

Mock Placeholders
ERP_API_URL: Mock URL for the ERP system's transaction data API.
ERP_API_KEY: Mock API key for authentication.
AZURE_STORAGE_CONNECTION_STRING: Mock connection string for Azure Blob Storage.

B. Anomaly Detection
File: anomaly_detection.py

Overview
This module detects anomalies in financial transactions using AI-driven algorithms. It helps in identifying potential non-compliance or fraudulent activities.

Steps
i. Data Loading:
Transaction data stored in Azure Blob Storage is loaded into a Pandas DataFrame for analysis.
2. Anomaly Detection:
OpenAI's GPT is used to analyze transaction data and identify anomalies. The model prompts with transaction data and returns any detected anomalies.

Mock Placeholders
AZURE_OPENAI_API_KEY: Mock API key for accessing OpenAI services.
AZURE_OPENAI_ENDPOINT: Mock endpoint for OpenAI services.

C. Report Generation
File: report_generation.py

Overview
This module generates comprehensive audit reports based on analyzed transaction data. It provides detailed insights and documentation of the auditing process.

Steps
i. Data Loading:
Load transaction data from centralized storage.

ii. Report Generation:
OpenAI's GPT is used to generate detailed audit reports, including analysis of transaction data and detected anomalies.

iii. Report Storage:
Generated reports are uploaded to SharePoint for easy access and collaboration.

Mock Placeholders
AZURE_OPENAI_API_KEY: Mock API key for accessing OpenAI services.
SHAREPOINT_SITE_URL: Mock URL for the SharePoint site.
SHAREPOINT_ACCESS_TOKEN: Mock access token for SharePoint.

D. Regulatory Monitoring
File: regulatory_monitoring.py

Overview
This module continuously monitors regulatory updates and notifies stakeholders about changes in compliance requirements.

Steps
i. Fetching Regulatory Updates:
Periodically fetch updates from a regulatory updates API.

ii. Analysis and Notification:
Analyze updates to identify relevant changes and send notifications to Microsoft Teams for proactive compliance management.

Mock Placeholders
REGULATORY_UPDATES_URL: Mock URL for regulatory updates.
TEAMS_WEBHOOK_URL: Mock webhook URL for Microsoft Teams notifications.
