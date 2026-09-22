# Salesforce Employee Onboarding & Access Management System

## Project Overview

This Salesforce Admin portfolio project demonstrates an employee onboarding and access management solution built using declarative Salesforce tools.

The system tracks employee onboarding information, automates access approval status based on access level, enforces business rules, applies permission-based security, and provides reporting and dashboard visibility.

## Key Features

- Custom Employee Onboarding object
- Record-Triggered Flow automation
- Access-level based approval status
- Validation rules for data quality
- Permission Set security
- Reports and dashboard
- Automated handling of Standard, Elevated, and Privileged access

## Employee Onboarding Data

The solution tracks:

- Employee Name
- Employee Email
- Start Date
- Department
- Job Title
- Employment Type
- Onboarding Status
- Access Level
- Laptop Required
- Software Access Required
- Access Approval Status
- Manager Approval Date
- Onboarding Completion Date

## Flow Automation

Created a Record-Triggered Flow named **Employee Onboarding Access Automation**.

When a new Employee Onboarding record is created:

- **Elevated Access** → Access Approval Status is automatically set to **Pending**
- **Privileged Access** → Access Approval Status is automatically set to **Pending**
- **Standard Access** → follows the default path and remains **Not Submitted**

The Flow uses a Decision element and Assignment elements and is optimized for Fast Field Updates.

## Validation Rule

A validation rule prevents an employee onboarding record from being marked **Completed** until access has been approved.

Error message:

> Access must be approved before onboarding can be completed.

## Security

Created an **Employee Onboarding Specialist** Permission Set to provide appropriate access to the Employee Onboarding object and fields while supporting least-privilege security.

## Reports

Created reports to analyze onboarding records by:

- Onboarding Status
- Access Level
- Department
- New Onboardings
- Completed Onboardings
- Pending Employee Onboardings

## Dashboard

Created an **Employee Onboarding Dashboard** displaying:

- Total Onboarding
- New Onboardings
- Completed Onboardings
- Pending Employee Onboardings
- Employee Onboardings by Status
- Employee Onboardings by Access Level
- Employee Onboardings by Department

## Testing

Tested multiple business scenarios including:

- Standard access remains Not Submitted
- Elevated access automatically becomes Pending
- Privileged access automatically becomes Pending
- Onboarding cannot be completed before access approval
- Reports and dashboard update as new records are created

## Salesforce Skills Demonstrated

- Salesforce Administration
- Custom Objects and Fields
- Record-Triggered Flow
- Decision Logic
- Assignment Elements
- Validation Rules
- Permission Sets
- Salesforce Security
- Reports and Dashboards
- Business Process Automation
- Testing and Troubleshooting

## Purpose

This project was created as part of my Salesforce portfolio to demonstrate the design and implementation of a realistic employee onboarding and access management process using Salesforce declarative tools.

## Screenshots

### Employee Onboarding Dashboard

![Employee Onboarding Dashboard](screenshots/Screenshot%202026-09-22%20095719.png)

### Employee Onboarding Access Automation Flow

![Employee Onboarding Access Automation Flow](screenshots/Screenshot%202026-09-21%20113615.png)

### Validation Rule – Approval Required for Completion

![Validation Rule](screenshots/Screenshot%202026-09-21%20113837.png)

### Permission Set Security

![Permission Set Security](screenshots/Screenshot%202026-09-21%20114308.png)

### Validation Rule Test

![Validation Rule Test](screenshots/Screenshot%202026-09-21%20114719.png)

### Privileged Access Automation Test

![Privileged Access Automation Test](screenshots/Screenshot%202026-09-21%20114927.png)
