Automation Hub for n8n OAuth2 Self-Hosted Configuration
Welcome to the official support page for our self-hosted workflow automation platform. This page provides essential information regarding our application's functionality, particularly its integration with Google services via OAuth2, as required for the Google Cloud Platform verification process.

Repository Name: n8n-oauth-support (or a similar descriptive name)

What is This?
This is the designated homepage for our private, self-hosted instance of n8n.io, a powerful Fair-Code licensed workflow automation tool. n8n allows us to connect various applications and services (both internal and external) to automate repetitive tasks and create efficient, code-free workflows.

Our instance is used internally by our team to enhance productivity and streamline business processes.

Purpose: Google OAuth2 Verification
The primary purpose of this page is to fulfill the requirements for the Google OAuth2 verification process. To eliminate the 7-day expiration limit on OAuth tokens and move our application into "production" mode for internal use, Google requires a public homepage that explains how and why we use their APIs.

Our n8n instance uses Google's APIs to allow our team to build automations that interact with their own Google services, such as Google Sheets, Gmail, Google Drive, and Google Calendar. Access is only ever granted through a user-initiated OAuth2 consent flow, where the user explicitly grants permission for our application to perform actions on their behalf.

How Our n8n Instance Uses Google Scopes
When a user on our team connects their Google Account to our n8n instance, they are asked to approve certain permissions (scopes). Below is a justification for why our application requests these permissions. Our application only ever performs actions that are explicitly configured by the user within an n8n workflow.

1. Google Sheets (.../auth/spreadsheets)
Why we need it: This permission allows our team members to create workflows that can read, write, and update data in their Google Sheets.

Example Use Case: A user creates a workflow that automatically captures new customer sign-ups from a web form and adds each entry as a new row in a "New Leads" spreadsheet. This eliminates manual data entry and ensures real-time data synchronization.

2. Google Drive (.../auth/drive or .../auth/drive.file)
Why we need it: This permission enables workflows that manage files in Google Drive. This includes uploading, downloading, searching for, and organizing files.

Example Use Case: A user builds an automation that generates a monthly PDF report, then uploads that report to a specific "Monthly Reports" folder in their Google Drive for archival and team access.

3. Gmail (.../auth/gmail.readonly, .../auth/gmail.send, .../auth/gmail.modify)
Why we need it: This permission allows users to automate their email management. This can range from reading incoming emails to trigger a workflow, sending automated email responses, or organizing the inbox.

Example Use Case: A workflow is configured to monitor an inbox for emails containing invoices. When an invoice is detected, the workflow extracts the attached PDF, saves it to a specific Google Drive folder, and adds a "Processed" label to the email in Gmail.

4. Google Calendar (.../auth/calendar.events)
Why we need it: This permission allows our team to automate event scheduling and calendar management.

Example Use Case: When a client books a meeting via an online scheduling tool, a workflow automatically creates a corresponding event in the user's Google Calendar, inviting all necessary participants and including a video conference link.

Security and User Data
Our n8n instance is self-hosted and privately managed. User data and credentials are securely stored and are never shared with any third parties. All API access is performed on behalf of users only after they have given explicit consent via the Google OAuth2 screen.

For more detailed information, please review our Privacy Policy.

Contact Us
If you have any questions regarding our use of Google APIs or our n8n instance, please contact our support team at pickleballdailyarticles@gmail.com
