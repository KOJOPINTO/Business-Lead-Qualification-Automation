# Workflow Overview – Business Lead Qualification & Follow-Up Automation

## Introduction

This project consists of two connected automation scenarios built with Make.com. Together, they manage incoming business inquiries, qualify leads, prioritize opportunities, and automate follow-up communication.

## Scenario 1: Lead Qualification and Routing

**Trigger:** A new response is submitted through Google Forms.

### Process

1. **Capture Lead:** Google Sheets detects a newly submitted form response.
2. **Calculate Lead Score:** Make.com evaluates the lead using predefined business rules.
3. **Assign Lead Category:** The lead is classified as High, Medium, or Low.
4. **Send Confirmation:** Gmail sends an automatic confirmation email to the customer.
5. **Update Lead Record:** Google Sheets stores the calculated score and category.
6. **Route Lead:** A Make.com router directs the lead based on its category.
7. **Notify Business Owner:** High-priority leads trigger an internal email notification.
8. **Flag Medium Leads:** Medium leads requiring follow-up are marked as Yes and Pending in Google Sheets.

## Scenario 2: Scheduled Follow-Up

**Schedule:** Daily at 9:00 AM.

### Process

1. **Search Records:** Google Sheets searches for leads with a Pending follow-up status.
2. **Check Eligibility:** Make.com checks whether the lead:
   - Requires follow-up.
   - Is classified as Medium.
   - Was submitted more than two days ago.
3. **Send Follow-Up:** Gmail sends a follow-up email to eligible customers.
4. **Update Status:** Google Sheets changes the follow-up status from Pending to Sent.

## Data Tracking

Google Sheets acts as the central record for lead information and follow-up progress.

Important tracking fields include:

- LeadScore
- LeadCategory
- FollowUpRequired
- FollowUpStatus

## Expected Outcome

The combined workflows provide a more organized approach to managing customer inquiries. They reduce repetitive administrative tasks, help businesses identify priority leads, and ensure eligible leads receive timely follow-up communication.

## Automation Platform

The workflows are implemented using Make.com integrations with Google Forms, Google Sheets, and Gmail.
