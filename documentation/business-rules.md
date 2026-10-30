# Business Rules – Lead Qualification Automation

## 1. Purpose
This document explains the rules used to score, categorize, and manage incoming business leads.

## 2. Lead Scoring

Each lead receives points based on the information submitted through the Google Form.

| Criteria | Condition | Points |
|---|---|---:|
| Urgency | Urgent | +3 |
| Budget | $1,000 or more | +3 |
| Consultation | Yes | +2 |
| Email Type | Business email | +1 |

## 3. Lead Categories

| Total Score | Category |
|---|---|
| 7–9 | High |
| 4–6 | Medium |
| 0–3 | Low |

## 4. Lead Handling Rules

- All leads receive an automatic confirmation email.
- High-priority leads trigger an email notification to the business owner.
- Medium and Low leads are retained for general tracking.
- Medium leads are marked as requiring follow-up.
- Low leads do not receive the scheduled follow-up.

## 5. Follow-Up Rules

The follow-up scenario runs daily at 9:00 AM.

A lead qualifies for follow-up when:

- FollowUpStatus is Pending.
- FollowUpRequired is Yes.
- LeadCategory is Medium.
- The lead was submitted more than two days ago.

After the follow-up email is sent, the status changes from Pending to Sent.

## 6. Duplicate Prevention

The FollowUpStatus field helps prevent the same lead from receiving repeated scheduled follow-up emails.

Once the status changes to Sent, the lead no longer qualifies for the Pending search.

## 7. Tools Used

- Make.com
- Google Forms
- Google Sheets
- Gmail
