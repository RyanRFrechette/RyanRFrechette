# Windows Command-Line Troubleshooting Lab

## Summary

This case study covers a Windows command-line troubleshooting lab focused on one skill: gathering clear diagnostic evidence before escalating an issue. Using common built-in tools — ipconfig, ping, tracert, nslookup, systeminfo, tasklist, and netstat — I captured real output from a Windows workstation, redacted the private details, and wrote a short note explaining what each command checks and why a support technician runs it.

## Scenario Type

Lab / support workflow demo. The commands and output are real, captured from a personal lab machine; sensitive details were removed before publishing.

## Problem

When a connectivity, DNS, performance, or system issue gets escalated, the next tier needs evidence — not a guess. This lab practices collecting that evidence in a structured way and documenting it so the issue can be escalated cleanly instead of bounced back for more information.

## User Impact

In a real workplace, a user reporting "the internet is down" could mean a lot of things. Running the right commands separates an internet outage from a DNS problem from a local config issue. Gathering that evidence up front means the user's problem reaches the right person faster, with the context already attached.

## Tools Used

- Windows Command Prompt (ipconfig, ping, tracert, nslookup, systeminfo, tasklist, netstat)
- PowerShell (for cleaning output and managing the Git workflow)
- ShareX for terminal screenshots
- Git and GitHub

## Evidence / Proof

- Nine screenshots showing each command and its terminal output
- Privacy-cleaned output files in `command-outputs/` (ipconfig, ping, tracert, nslookup, systeminfo, tasklist, netstat)
- Seven short troubleshooting notes in `troubleshooting-notes/` explaining what each command checks and when to use it
- A case study, resume bullets, and a LinkedIn post draft
- A privacy note listing exactly what was redacted (host names, usernames, MAC and IP addresses, IPv6, gateway/DHCP/DNS details, BIOS and product IDs)

## Troubleshooting or Support Workflow

1. Reviewed adapter configuration with `ipconfig /all` to check DHCP status, gateway, and DNS settings.
2. Tested raw internet connectivity with `ping 8.8.8.8`, which doesn't rely on DNS.
3. Tested name resolution with `ping google.com` — if the IP ping works but the name ping fails, that points to DNS.
4. Traced the path to a destination with `tracert google.com` to see where timeouts appear.
5. Confirmed DNS resolution directly with `nslookup google.com`.
6. Captured a safe subset of system inventory with `systeminfo` (Windows version, system type, memory, hotfix count).
7. Reviewed running processes with `tasklist` for basic performance and application triage.
8. Reviewed active connections, listening ports, and process IDs with `netstat -ano`.
9. Redacted private details from every output before saving and publishing.

## Resolution / Outcome

The lab produced a clean, screenshot-backed set of diagnostic evidence with an explanation for each command. It demonstrates a repeatable habit: gather and document evidence first, then escalate — and do it without exposing private system or network details.

## What I Learned

- Splitting the IP ping from the name ping is a fast way to tell a DNS problem apart from a connectivity problem.
- The output of these commands often contains private details, so redacting before sharing matters.
- Writing down what each command proves makes the evidence useful to whoever picks up the escalation.

## What This Proves for IT Support

It shows I know which command-line tools to reach for, can read their output in a troubleshooting context, and can document findings safely — exactly what's expected when gathering evidence before an escalation.

## Recruiter Takeaway

I can run the standard Windows diagnostic commands, interpret the results, and document clean evidence before escalating — without exposing private information.
