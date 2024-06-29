# Audit and Compliance Project Overview

The **Audit and Compliance** project leverages generative AI to transform audit and compliance processes within financial institutions. By automating traditionally manual tasks, the project aims to enhance accuracy, efficiency, and adaptability in managing regulatory standards and financial transactions. Through seamless integration of technologies like Microsoft Azure and OpenAI, the project ensures robust compliance frameworks that can adapt to evolving regulations, thereby optimizing organizational compliance efforts while minimizing operational overhead.

## A. Data Integration and Preprocessing

**File**: `data_integration_preprocessing.py`

### Overview

This module aggregates financial transaction data from various sources into a centralized data repository. This step ensures that all relevant data is available for subsequent analysis by AI models.

### Steps

1. **Fetching Data**:
   - Utilizes an API to fetch transaction data from an ERP (Enterprise Resource Planning) system. The API call is authenticated using a mock API key.

2. **Data Conversion**:
   - Converts fetched data, usually in JSON format, into a Pandas DataFrame for easier manipulation and analysis.

3. **Data Storage**:
   - Uploads the processed DataFrame to Azure Blob Storage, a scalable object storage service provided by Microsoft Azure. This ensures secure storage and accessibility for downstream processing.

### Mock Placeholders

- `ERP_API_URL`: Mock URL for the ERP system's transaction data API.
- `ERP_API_KEY`: Mock API key for authentication.
- `AZURE_STORAGE_CONNECTION_STRING`: Mock connection string for Azure Blob Storage.

## B. Anomaly Detection

**File**: `anomaly_detection.py`

### Overview

This module identifies anomalies in financial transactions using AI-driven algorithms, aiding in detecting potential non-compliance or fraudulent activities.

### Steps

1. **Data Loading**:
   - Loads transaction data stored in Azure Blob Storage into a Pandas DataFrame for analysis.

2. **Anomaly Detection**:
   - Utilizes OpenAI's GPT to analyze transaction data and identify anomalies. The model prompts with transaction data and returns any detected anomalies.

### Mock Placeholders

- `AZURE_OPENAI_API_KEY`: Mock API key for accessing OpenAI services.
- `AZURE_OPENAI_ENDPOINT`: Mock endpoint for OpenAI services.

## C. Report Generation

**File**: `report_generation.py`

### Overview

This module generates comprehensive audit reports based on analyzed transaction data, providing detailed insights and documentation of the auditing process.

### Steps

1. **Data Loading**:
   - Loads transaction data from centralized storage.

2. **Report Generation**:
   - Utilizes OpenAI's GPT to generate detailed audit reports, including analysis of transaction data and detected anomalies.

3. **Report Storage**:
   - Uploads generated reports to SharePoint for easy access and collaboration.

### Mock Placeholders

- `AZURE_OPENAI_API_KEY`: Mock API key for accessing OpenAI services.
- `SHAREPOINT_SITE_URL`: Mock URL for the SharePoint site.
- `SHAREPOINT_ACCESS_TOKEN`: Mock access token for SharePoint.

## D. Regulatory Monitoring

**File**: `regulatory_monitoring.py`

### Overview

This module continuously monitors regulatory updates and notifies stakeholders about changes in compliance requirements.

### Steps

1. **Fetching Regulatory Updates**:
   - Periodically fetches updates from a regulatory updates API.

2. **Analysis and Notification**:
   - Analyzes updates to identify relevant changes and sends notifications to Microsoft Teams for proactive compliance management.

### Mock Placeholders

- `REGULATORY_UPDATES_URL`: Mock URL for regulatory updates.
- `TEAMS_WEBHOOK_URL`: Mock webhook URL for Microsoft Teams notifications.
