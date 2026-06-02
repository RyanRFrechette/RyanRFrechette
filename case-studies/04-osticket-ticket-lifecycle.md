# osTicket Help Desk — Ticket Lifecycle

## Summary

This case study covers a help desk ticketing lab built with osTicket running locally in Docker. I configured the system the way a small support desk would — departments and help topics — and then created, worked, and closed six realistic support tickets. Each one moves through the full lifecycle: intake, categorization, an internal triage note, a customer-facing reply, and resolution. It shows what it looks like to actually work inside a ticketing queue, not just describe one.

## Scenario Type

Support workflow demo with simulated tickets. The ticketing system is real (osTicket), but the user and all six tickets are created for practice.

## Problem

Almost every help desk runs on a ticketing system. The skill being practiced here is the workflow itself: take in a request, categorize it correctly, document troubleshooting in internal notes, communicate clearly with the user, and close the ticket with a useful resolution. This lab demonstrates that loop across the most common Tier 1 scenarios.

## User Impact

In a real workplace, a ticket is how a user's problem gets tracked and resolved. Good ticket handling means the user gets clear communication and a documented outcome; poor handling means dropped requests and repeat questions. The internal notes also let another technician pick up where the last one left off.

## Tools Used

- osTicket
- Docker Desktop and Docker Compose
- MySQL container
- Windows PowerShell
- ShareX for screenshot evidence
- Git and GitHub

## Evidence / Proof

- 37 screenshots covering osTicket setup, the agent dashboard, admin settings, department and help topic configuration, a test user, and each ticket from creation to closed
- Six ticket writeups in the repo: user cannot log in, password reset, shared folder access, slow computer, software install request, and new user onboarding
- A `docker-compose.yml` showing the local environment setup
- A case study, resume bullets, and a screenshot checklist confirming each proof type was captured

## Troubleshooting or Support Workflow

1. Stood up osTicket locally with Docker and confirmed the agent login and dashboard loaded.
2. Configured departments (IT Support, Hardware/Software, Account Support, Maintenance) and realistic help topics.
3. Created a test user to submit tickets against.
4. For each of the six scenarios: created the ticket, opened it in the staff panel, posted an internal triage note, replied to the user, and resolved it.
5. Confirmed each closed ticket appeared in the closed queue with the correct subject, user, and closing agent.

## Resolution / Outcome

Six tickets were taken from intake through resolution, each documented with internal notes and a user-facing reply, and each verified in the closed queue. The lab demonstrates a complete, repeatable ticket-handling workflow in a real ticketing platform.

## What I Learned

- Internal notes and customer replies serve different audiences — one records the troubleshooting, the other communicates clearly with the user.
- Good help topic and department setup makes routing and tracking much easier later.
- A consistent lifecycle (intake, triage, note, reply, close) keeps a queue organized and nothing gets lost.

## What This Proves for IT Support

It shows I can work inside a ticketing system the way a help desk expects: categorize requests, document troubleshooting, communicate with users professionally, and track tickets through to resolution.

## Recruiter Takeaway

I'm comfortable working a ticket queue end to end in a real ticketing system, with clear internal documentation and professional user communication.
