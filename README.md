# Outlook to Teams status
Use your Outlook calendar events to set your Teams status text automatically using a Power Automate flow.

## How it works
Yes, Outlook already sets your *availability* automatically. However, you know how you can set that little status message with an expiration date/time, kind of like back in the AIM days? Don't you wish you could automate that to show people when you're working remotely or show off some dreadful emo lyrics? Sure you do. Here's how it does it.

This flow is triggered by any upcoming event in your Outlook calendar. Once triggered, it then checks to see if the event subject starts with "Status: " and declares a variable that contains the subject minus the "Status: " text. If the event subject did start with "Status: ", it then sets your Teams status to that variable using the "Send an HTTP request to SharePoint" action, but instead sends an HTTP PUT request to the Teams API. It also sends an expiration on the status equivalent to the end date/time of the event.

## How to use
From your flows, select "Import package" and select the ZIP file. Update the connections for your account.

Create a calendar event with a subject like "Status: Working from home". When the event is about to start, your Teams status will automatically become "Working from home" and will clear itself when the event ends.