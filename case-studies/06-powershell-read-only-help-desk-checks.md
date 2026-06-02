# PowerShell Read-Only Help Desk Checks

## Summary

This case study covers a small PowerShell toolkit I built for first-level Windows support checks. It's six scripts that gather the information a technician usually collects at the start of a ticket — system info, disk space, network connectivity, local users, and recent event log errors — and can roll them into a single timestamped support report. Every script is **read-only**: it reads and reports, but makes no changes to the system.

## Scenario Type

Personal portfolio project / support workflow demo. The scripts run against a personal lab machine; output was reviewed before being added to the repo.

## Problem

At the start of a ticket, a help desk technician often needs the same baseline facts: what machine is this, how much disk is free, is the network reachable, what local accounts exist, and what recently errored. Doing that by hand every time is slow and inconsistent. This toolkit makes those checks fast, repeatable, and safe to run.

## User Impact

In a real workplace, faster and more consistent first-level checks mean a user's issue gets triaged sooner and escalations arrive with the right information already attached. Because the scripts are read-only, running them carries no risk of changing or breaking the user's machine.

## Tools Used

- PowerShell
- Windows System and Application event logs (read-only)
- Git and GitHub

## Evidence / Proof

- Six scripts, each mapped to a short command: `sysinfo`, `diskreport`, `netcheck`, `usersummary`, `supportreport`, and `eventerrors`
- 13 screenshots showing each command, its terminal output, and the saved report path
- Saved output files written only inside the repo's `outputs/` folder
- A case study, resume bullets, and a LinkedIn post draft
- Stated safety notes: scripts are read-only, avoid destructive commands, and omit event log message bodies to reduce private data exposure

## Troubleshooting or Support Workflow

1. `sysinfo` — collects hostname, OS version, uptime, RAM, and CPU, the basics gathered at the start of a ticket.
2. `diskreport` — reviews drive size, free space, percent free, and low-space status for storage and performance issues.
3. `netcheck` — checks the gateway, DNS server, internet IP connectivity, and DNS resolution.
4. `usersummary` — lists local accounts, enabled status, last logon, and password requirement.
5. `eventerrors` — reviews recent System and Application errors while omitting the message bodies.
6. `supportreport` — combines the core checks into one timestamped report that can be attached to a ticket or handed to a higher tier.

## Resolution / Outcome

The toolkit produces consistent, read-only support output for common first-level scenarios — a slow computer, a connectivity complaint, an account review, or a post-crash check — and can package it all into a single escalation-ready report. Each workflow is backed by a screenshot showing the command and its real output.

## What I Learned

- Keeping the scripts strictly read-only makes them safe to run on any machine without worrying about side effects.
- Small details matter for privacy — omitting event log message bodies keeps potentially sensitive text out of the report.
- A combined report saves time and gives an escalation a consistent, complete starting point.

## What This Proves for IT Support

It shows I can write practical, safe PowerShell for everyday help desk checks, understand read-only safety discipline, and turn endpoint data into a clear report a support team can use.

## Recruiter Takeaway

I can build and explain simple, read-only PowerShell that speeds up first-level Windows checks and produces clean, escalation-ready reports.
