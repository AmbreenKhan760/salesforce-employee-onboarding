# Salesforce Employee Onboarding & Access Management System

## Project Overview

This project demonstrates a Salesforce-based Employee Onboarding and Access Management solution built using declarative Salesforce tools.

The solution manages employee onboarding information, automates access approval status, enforces business rules, applies permission-based security, and provides reporting and dashboard visibility.

## Business Requirements

The organization needs a centralized Salesforce solution to:

- Track new employee onboarding
- Capture employee, department, and employment information
- Track required laptop and software access
- Automatically manage access approval status
- Prevent onboarding completion before required access approval
- Apply appropriate security permissions
- Provide management visibility through reports and dashboards

## Salesforce Configuration

A custom **Employee Onboarding** object was created to store onboarding information.

Key fields include:

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
- User

## Flow Automation

A Record-Triggered Flow named **Employee Onboarding Access Automation** was created.

The Flow evaluates the employee's Access Level when an onboarding record is created.

Automation logic:

- Standard Access → remains Not Submitted
- Elevated Access → Access Approval Status becomes Pending
- Privileged Access → Access Approval Status becomes Pending

The Flow uses a Decision element and Assignment elements and is optimized for Fast Field Updates.

## Validation Rule

A validation rule named **Require_Approval_For_Completion** prevents an onboarding record from being marked Completed unless the Access Approval Status is Approved.

This helps maintain process integrity and prevents onboarding from being completed prematurely.

## Security

A Permission Set named **Employee Onboarding Specialist** was configured using the principle of least privilege.

Users with this permission set can:

- Read Employee Onboarding records
- Create Employee Onboarding records
- Edit Employee Onboarding records

Delete, View All Records, and Modify All Records permissions are not granted.

Field-level permissions were also configured to control access to onboarding information.

## Reports and Dashboard

Reports were created to analyze:

- Employee Onboardings by Status
- Employee Onboardings by Access Level
- Employee Onboardings by Department
- New Onboardings
- Completed Onboardings
- Pending Employee Onboardings

An **Employee Onboarding Dashboard** provides management with a visual overview of onboarding activity, access levels, departments, and onboarding progress.

## Testing

The solution was tested using multiple business scenarios:

- Standard access remains Not Submitted
- Elevated access automatically becomes Pending
- Privileged access automatically becomes Pending
- Onboarding cannot be completed before access approval
- Reports and dashboard update as new records are created

## Salesforce Skills Demonstrated

- Salesforce Administration
- Custom Objects and Fields
- Record-Triggered Flows
- Decision Logic
- Assignment Elements
- Validation Rules
- Permission Sets
- Field-Level Security
- Reports and Dashboards
- Data Quality
- Business Process Automation
- Testing and Troubleshooting

## Project Outcome

This project demonstrates how Salesforce declarative tools can be used to build a secure and scalable employee onboarding process without custom Apex or Lightning Web Components.
