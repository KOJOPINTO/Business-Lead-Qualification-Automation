# Workflow Overview – Business Lead Qualification Automation

## Project Overview

This project automates the process of capturing, qualifying, categorizing, and following up with business leads.

It uses two Make.com scenarios to reduce manual work and help businesses respond to potential customers more efficiently.

## Scenario 1: Lead Qualification and Routing

1. A customer submits a Google Form.
2. Google Sheets stores the submitted information.
3. Make.com calculates a lead score based on the qualification rules.
4. The lead is categorized as High, Medium, or Low.
5. The customer receives an automatic confirmation email.
6. The lead score and category are saved in Google Sheets.
7. A router directs the lead based on its category.
8. High-priority leads trigger an email notification to the business owner.
9. Medium and Low leads remain available for general tracking.
10. Medium leads are marked for scheduled follow-up.

## Scenario 2: Automated Follow-Up

1. The scenario runs daily at 9:00 AM.
2. Google Sheets searches for leads with a Pending follow-up status.
3. Make.com checks whether the lead is Medium priority, requires follow-up, and is more than two days old.
4. Eligible customers receive a follow-up email through Gmail.
5. Google Sheets updates the follow-up status from Pending to Sent.

## Business Benefits

- Reduces manual lead qualification.
- Helps businesses identify high-priority prospects.
- Improves response consistency.
- Automates follow-up reminders and emails.
- Maintains a record of lead and follow-up status.
- Reduces the risk of sending duplicate scheduled follow-ups.

## Technology Stack

- Make.com – Workflow automation
- Google Forms – Lead collection
- Google Sheets – Lead database and tracking
- Gmail – Customer and business-owner notifications
