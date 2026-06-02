# Microsoft 365 / Entra ID User Support Lab

## Summary

This case study covers a Microsoft 365 and Entra ID lab where I practiced the full life of a cloud user account — creating it, giving it access, supporting it, and eventually offboarding it. I did the work two ways: through the Microsoft 365 and Entra admin centers, and through Microsoft Graph PowerShell, then verified every change in both places. It shows the kind of cloud account support a Tier 1 help desk technician handles every day.

## Scenario Type

Lab, using a Microsoft 365 Business Premium trial tenant with a test user. All accounts are test accounts; there are no real employees or company data.

## Problem

A small organization would need someone to handle routine Microsoft 365 account work: onboard a new hire, assign a license, grant group access, reset a password, suspend access when something looks wrong, and cleanly offboard a departing user. This lab practices each of those tasks against a trial tenant so the workflow is documented and repeatable.

## User Impact

In a real workplace, these are the requests that block people from working. A new hire can't start without an account and license. A locked-out user can't reach email. A departing employee who isn't properly offboarded leaves an access risk behind. Getting these handled quickly and correctly is most of what keeps a help desk queue moving.

## Tools Used

- Microsoft 365 admin center
- Microsoft Entra admin center
- Microsoft Graph PowerShell
- PowerShell 5.1 on Windows
- ShareX for screenshot evidence
- Git and GitHub for documentation

## Evidence / Proof

- 32 screenshots in the repo covering setup, Graph PowerShell connection, user creation, group membership, licensing, password reset, authentication methods review, sign-in block/restore, and offboarding
- Six ticket-style writeups (onboarding, password reset/sign-in, group access, license and app access, MFA/authentication review, offboarding)
- Exported CSV reports: `reports/baseline-users.csv`, `reports/license-inventory.csv`, `reports/final-users.csv`
- A full screenshot walkthrough in the repo README
- A scope note in the case study stating what was *not* done (no Conditional Access, no session revocation, no Intune)

## Troubleshooting or Support Workflow

1. Confirmed admin access to both the Microsoft 365 and Entra admin centers.
2. Installed Microsoft Graph PowerShell and connected with delegated admin scopes.
3. Exported a baseline user report as a starting record.
4. Created a test user (Alex Morgan) and verified it in PowerShell and the admin center.
5. Created an "IT Support Team" security group and added the user, then confirmed membership in Entra.
6. Reviewed tenant license inventory, assigned a Business Premium license, and verified it.
7. Reset the user's password with a forced change at next sign-in.
8. Reviewed the Entra authentication methods area to understand the available sign-in and MFA settings.
9. Blocked the user's sign-in, confirmed the account was disabled, then restored it.
10. Offboarded the user: removed group membership, removed the license, blocked sign-in, and exported a final audit report.

## Resolution / Outcome

Every step was completed and verified in two places — PowerShell and the admin center — and the before/after state was captured in screenshots and CSV reports. The lab documents a clean, repeatable user lifecycle from onboarding to offboarding.

## What I Learned

- Microsoft 365 and Entra split responsibilities between productivity, identity, licensing, and security settings, and it helps to know which console handles what.
- Microsoft Graph PowerShell makes routine account work faster and repeatable, but it's worth confirming the result in the admin center.
- Documenting exactly what was done — and being clear about what was out of scope — keeps the work honest.

## What This Proves for IT Support

It shows comfort with the everyday Microsoft 365 support queue: account creation, licensing, group access, password resets, suspending and restoring access, and offboarding — plus the habit of verifying changes and writing them up.

## Recruiter Takeaway

I can handle common Microsoft 365 and Entra ID account support tasks end to end, using both the admin centers and PowerShell, and document the work clearly for a support team.
