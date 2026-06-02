# Help Desk Homelab — Windows Domain Support

## Summary

This case study covers a Windows help desk homelab I built locally in VirtualBox: a Windows Server 2022 domain controller and a Windows 11 client on a lab domain called `ryanlab.local`. With the domain running, I worked through everyday help desk tasks — password resets, account disable/enable, group membership changes, shared folder access, mapped drives, and a basic Group Policy restriction — and wrote each one up as a support ticket. It's intentionally entry-level and honest, built to show practical support habits rather than advanced administration.

## Scenario Type

Lab, with simulated ticket writeups. Everything runs on local VMs with test users; there is no real company, network, or end user involved.

## Problem

A small business running a Windows domain needs routine support: reset a user's password, restore or disable an account, give someone access to a department's shared folder, map a network drive, and apply a simple policy to standard users. This lab sets up that environment and practices each task end to end.

## User Impact

In a real workplace these are the issues that stop people from working: a user who can't sign in, a salesperson who can't open the Sales share, a new mapped drive that won't connect. Handling them quickly — and documenting the fix — is most of what keeps a help desk running.

## Tools Used

- Oracle VirtualBox
- Windows Server 2022 Evaluation (domain controller)
- Windows 11 (domain-joined client)
- Active Directory Domain Services and DNS
- Active Directory Users and Computers
- Group Policy Management
- PowerShell

## Evidence / Proof

- 47 screenshots in the repo covering project setup, VM creation, Windows Server install, AD DS promotion, OU and group structure, test users, client domain join, and each support task
- Six ticket writeups: Windows 11 VM boot troubleshooting, password reset (Jane Smith), account disable/re-enable (Alex Turner), group membership change (Alex Turner), shared folder access denied (Sales share), and Control Panel restricted by Group Policy
- A documented OU structure (Users, Groups, Disabled Users, Workstations) and role-based security groups (IT-Support, HR-Shared, Sales-Shared, Remote-Users)
- `whoami` login proof for both a domain admin and a standard domain user
- A case study and resume bullets

## Troubleshooting or Support Workflow

1. Installed VirtualBox and built the Windows Server and Windows 11 VMs.
2. Installed Windows Server 2022, renamed it to `RYANLAB-DC01`, and promoted it to a domain controller for `ryanlab.local`.
3. Created an OU structure and role-based security groups, then added test users for HR, Sales, Operations, and IT.
4. Built the Windows 11 client, joined it to the domain, and confirmed both admin and standard-user logins with `whoami`.
5. Reset a standard user's password in ADUC and confirmed success.
6. Disabled and later re-enabled a user account to practice the offboarding/restore cycle.
7. Added a user to the Sales-Shared group, refreshed the session, and verified access to the Sales shared folder.
8. Mapped the Sales share to drive Z: and confirmed the user could open files.
9. Created a Group Policy Object blocking Control Panel for standard users, linked it to the user OU, forced an update, and verified the restriction applied.

## Resolution / Outcome

The lab produced a working local Windows domain and a documented set of help desk workflows, each backed by screenshots and a ticket writeup. It demonstrates the full path from "build the environment" to "resolve and document the request."

## What I Learned

- A standard user's access problems usually trace back to group membership — adding them to the right group and refreshing the session is often the whole fix.
- Group Policy changes don't apply instantly; forcing an update and then verifying on the client is part of the job.
- Clear ticket writeups make the same fix repeatable and easy to hand to someone else.

## What This Proves for IT Support

It shows hands-on comfort with the core Windows help desk tasks — password resets, account lifecycle, group-based access, shared folders, mapped drives, and basic Group Policy — plus the documentation habits a support team relies on.

## Recruiter Takeaway

I can set up and support a Windows domain at a help desk level and document each fix clearly, from account resets to shared folder access and basic Group Policy.
