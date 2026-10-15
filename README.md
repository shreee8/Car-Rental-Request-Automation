# Car Rental Request Automation

A ServiceNow-Based Car Rental Request Management System

## Overview
Car Rental Request Automation is a ServiceNow application that streamlines how
employees request a rental car for official travel. It uses a Service Catalog
item, a custom Car Inventory table, a Flow Designer flow, and a Business Rule
to standardize request intake, route approvals, assign fulfillment work to the
Transport Team, and keep a traceable record of every request.

## Key Features
- **Standard Request Form:** A Car Rental Request catalog item in the Service
  Portal with driver name, car type, requested date, pickup location, drop
  location, duration, and reason.
- **Car Inventory Management:** A custom table that stores cars, their
  details, and availability.
- **Approval Workflow:** A Flow Designer flow that sends each request for
  approval and continues only when it is approved.
- **Task Assignment:** Approved requests automatically create a catalog task
  assigned to the Transport Team.
- **Email Notifications:** Emails for request creation, approval, rejection,
  task assignment, and completion.
- **Incident Automation:** A Business Rule creates an incident automatically,
  with the request number, when a request is closed with the defined state.
- **Request Tracking:** Requested Item (RITM) and approval records give a
  central, auditable history.
- [Optional, keep only what you built] Car dropdown filtered to available
  cars, past-date validation, mandatory reason for long rentals, and a report
  of requests by approval status.

## Technology Stack
| Component | Technology |
|---|---|
| Platform | ServiceNow |
| User Interface | Service Portal, Service Catalog |
| Data Management | Custom ServiceNow table (Car Inventory), catalog variables |
| Automation | Flow Designer, Business Rules |
| Scripting | JavaScript / ServiceNow server-side scripts |

## Workflow
1. The employee submits the Car Rental Request from the Service Portal.
2. A Request and a Requested Item (RITM) are created.
3. The flow asks for approval.
4. If approved, a catalog task is created for the Transport Team and the
   requester is emailed. If rejected, the requester receives a rejection email.
5. When the task is closed, the flow sends the completion email.
6. The Business Rule creates an incident when a request is closed with the
   defined state.

## User Roles
- **System Administrator:** Builds and administers the application, approves
  requests, and views all records.
- **Requester (Employee):** Submits requests and tracks their status.
- **Transport Team:** Receives and completes approved request tasks.

## Future Enhancements
- Check car availability automatically when a request is submitted.
- Assign a specific car from the inventory to each approved request.
- Add multi-level approval based on the requester's department or role.
- Add an SLA and dashboard to monitor turnaround time.
- Add role-based access so employees see only their own requests.
- Expand performance and security testing.

## Project Drive Link
The complete project folder with all documentation and files:
https://drive.google.com/drive/folders/1WbJpR-5OPe6tJ1g2jeZ_KOM3y1_lkFFC?usp=drive_link



## Video Demonstration
An end-to-end demonstration of the Service Portal form and the back-end
workflow automation:
https://drive.google.com/file/d/1BVlJpD3ODwvCkC2cpU-iQbelsZCp9pVb/view?usp=drive_link

## Disclaimer
This project is intended for academic and demonstration purposes only. Sample
data is fictional.
