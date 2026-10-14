# Sent Emails Tracker – Job Applications

A read-only Gmail automation that tracks job application emails, groups them by subject and recipient, counts how many times each email was sent, and exports the results to Google Sheets.
<img width="1062" height="283" alt="image" src="https://github.com/user-attachments/assets/099a9670-7eed-4768-b1d5-8c4a6033a62d" />
<img width="1453" height="533" alt="image" src="https://github.com/user-attachments/assets/8ad3d0bb-3797-459d-a3ec-f7c9a18e216e" />



## Features

- Reads sent emails from the last 60 days.
- Groups emails by subject and recipient.
- Tracks the latest send date and number of times sent.
- Calculates a suggested resend date seven days after the latest send.
- Exports results to a Google Sheet with configurable column mapping.
- Uses your own Gmail and Google Sheets credentials.

**Privacy:** The workflow is designed not to send, reply to, or modify emails. Each user must configure their own Google authorization and destination spreadsheet.

## Output Columns

| Column | Description |
|---|---|
| `date_sent` | Latest email sent date |
| `subject` | Email subject |
| `position_applied` | Job position associated with the email |
| `sent_to` | Recipient email address |
| `resend_on` | Suggested resend date |
| `times_sent` | Number of matching emails sent |

## Setup

1. Import the workflow JSON into your automation platform.
2. Configure your own Gmail credentials and authorize access.
3. Configure your own Google Sheets credentials.
4. Create a Google Sheet with the six headers listed above in the first row.
5. Select your spreadsheet and worksheet tab in the Google Sheets node.
6. Map the workflow output fields to the matching column headers.
7. Test the workflow and verify the output before activating it.

## OAuth Configuration

Use your own Google credentials when prompted. Depending on the workflow platform and OAuth setup, you may need to configure a Google Cloud project, enable the required APIs, and create an OAuth client.

Never commit client secrets, access tokens, refresh tokens, or exported credentials to the repository.

## Important Notes

- The workflow processes emails within a rolling 60-day window.
- The resend date is a suggested follow-up date, not an automatically sent email.
- Check the spreadsheet-writing and clearing behavior before running the workflow against an existing spreadsheet.
- Use a dedicated output worksheet to protect unrelated data.

## License

Add your chosen open-source license before distributing the workflow.
