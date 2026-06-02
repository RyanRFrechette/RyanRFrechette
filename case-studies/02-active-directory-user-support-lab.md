# Active Directory User Support Lab

## Summary

This case study covers an Active Directory lab I built on Azure virtual machines: a Windows Server domain controller and a Windows client joined to the domain. With that environment running, I practiced the account support tasks that fill a help desk queue — password resets, account unlocks, disabling and enabling accounts, and provisioning new users — and documented each as a simulated ticket.

## Scenario Type

Lab, with simulated support tickets. The domain, users, and tickets are all built for practice; none are real production systems or real people.

## Problem

A small organization running a Windows domain needs someone who can keep user accounts working: get a new employee set up in the right place, reset a forgotten password, unlock an account after too many failed logins, and disable access when needed. This lab builds that environment from scratch and then walks through those tasks.

## User Impact

If these go unhandled in a real workplace, people can't log into their computers. A locked-out account stops someone's whole day. A domain join that fails because of DNS means a workstation can't reach company resources at all. These are the first-line issues a help desk is expected to clear quickly.

## Tools Used

- Microsoft Azure virtual machines
- Windows Server 2022 (domain controller)
- Windows 10 (domain-joined client)
- Active Directory Domain Services (AD DS)
- Active Directory Users and Computers (ADUC)
- DNS Manager
- Remote Desktop Protocol (RDP)
- PowerShell / PowerShell ISE

## Evidence / Proof

- Screenshot evidence embedded in the repo README covering domain controller prep, the AD structure and admin user, client domain join and RDP, PowerShell user creation, and account administration
- Five simulated support tickets (user cannot log in, password reset, account locked, new employee setup, domain/RDP access issue)
- An architecture diagram and authentication flow in `diagrams/architecture.md`
- A case study and resume bullets, with a written note that the tickets are simulated scenarios, not production incidents

## Troubleshooting or Support Workflow

1. Deployed Windows Server and Windows 10 VMs in Azure on a shared virtual network.
2. Confirmed connectivity between the VMs before configuring the domain.
3. Promoted the server to a domain controller with AD DS and DNS, creating a new forest and domain.
4. Created organizational units for employees and administrators.
5. Created a domain admin account and assigned the right permissions.
6. Pointed the Windows client's DNS at the domain controller and joined it to the domain.
7. Configured Remote Desktop access for domain users.
8. Practiced account support: password resets, unlocks, disabling, and enabling, using both ADUC and PowerShell.

## Resolution / Outcome

The lab produced a working two-machine domain and a documented set of account support workflows. Along the way it reinforced one of the most useful AD troubleshooting lessons: when a domain join or login fails, DNS is almost always the first thing to check.

## What I Learned

- Active Directory depends heavily on correct DNS — the client must point at the domain controller, not a public resolver.
- Account access issues follow a logical order: account status, then password, then group membership, then machine domain status, then network.
- Azure VMs are an affordable way to practice Windows administration without physical hardware.

## What This Proves for IT Support

It shows the core Active Directory account support a desktop or help desk role expects: provisioning users, resetting passwords, unlocking and enabling/disabling accounts, and troubleshooting domain join and login problems in a structured way.

## Recruiter Takeaway

I can work inside an Active Directory environment to handle everyday account support and follow a sensible troubleshooting path when logins or domain joins fail.
