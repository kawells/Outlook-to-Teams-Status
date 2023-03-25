# Outlook to Teams status
Use your Outlook calendar events to set your Teams statuses automatically using a Power Automate flow.

## How it works
This flow is triggered by any upcoming event in your Outlook calendar. Once triggered, it then checks to see if the event subject starts with "Status: " and declares a variable that contains the subject minus the "Status: " text. If the event subject did start with "Status: ", it then sets your Teams status using the "Send an HTTP request to SharePoint" action, but instead sends an HTTP PUT request to the Teams API. It also sends an expiration on the status equivalent to the end date/time of the event.

## How to use
From your flows, select "Import package" and select the ZIP file.
