# Business Rules – Lead Qualification Automation

## 1. Lead Scoring

Each inquiry is evaluated using four criteria:

| Criteria | Condition | Score |
|---|---|---:|
| Urgency | Urgent | +3 |
| Budget | $1,000 or more | +3 |
| Consultation | Yes | +2 |
| Email Type | Business | +1 |

## 2. Lead Classification

- High: 7–9 points
- Medium: 4–6 points
- Low: 0–3 points

## 3. Lead Handling

- All new leads receive a confirmation email.
- High-priority leads trigger an email notification to the business owner.
- Medium- and low-priority leads follow the general tracking route.
- Medium leads requiring follow-up are marked as Pending.

## 4. Follow-Up Rules

The scheduled follow-up scenario runs daily at 9:00 AM.

A follow-up email is sent when all these conditions are met:

1. FollowUpStatus is Pending.
2. FollowUpRequired contains Yes.
3. LeadCategory contains Medium.
4. The lead was submitted more than two days ago.

After the email is sent, FollowUpStatus is updated to Sent.

## 5. Duplicate Prevention

The automation uses the follow-up status to prevent the same lead from being emailed repeatedly. Once a successful follow-up is recorded as Sent, it no longer qualifies for the Pending search.

## 6. Business Objective

The purpose of these rules is to help businesses prioritize inquiries, respond consistently, and reduce the manual effort involved in lead management.
