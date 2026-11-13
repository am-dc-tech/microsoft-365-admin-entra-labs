# M365 User Offboarding Lab — Bob Baker

## Summary

A hands-on lab simulating the offboarding process for a departing employee in a 
Microsoft 365 environment. This lab covers blocking sign-in, removing shared mailbox 
access, and unassigning a license using the Microsoft 365 Admin Center and Entra ID.

## Environment

- Platform: Microsoft 365 Admin Center / Microsoft Entra Admin Center
- Role: Tier 1 IT Administrator
- User Being Offboarded: Bob Baker

## Scenario

Bob Baker is leaving the organization. As the IT administrator, I need to secure his 
account, remove his access to the shared mailbox, unassign his license, and confirm 
the account is in a secure offboarded state.

## Steps

1. Open Microsoft 365 Admin Center → **Users > Active Users**
2. Locate and select **Bob Baker**
3. Review his profile, assigned license, and account status
4. **Block sign-in** for Bob Baker and confirm the account is blocked

5. Go to **Teams & Groups > Active Teams & Groups**
6. Locate the shared mailbox Bob had access to
7. Open the mailbox membership settings and **remove Bob Baker**
8. Verify he is no longer listed as a member

9. Go to **Billing > Licenses**
10. Locate Bob Baker's assigned license
11. **Unassign the license** and confirm it has been removed

12. Verify offboarding from the **admin side**: confirm sign-in is blocked, 
shared mailbox access is removed, and license is unassigned

13. Verify offboarding from the **user side**: attempt to sign in at office.com 
using Bob Baker's credentials and confirm access is denied

## Expected Outcome

- Bob Baker's sign-in is blocked
- Shared mailbox access is removed
- License is unassigned and returned to the available pool
- Bob Baker can no longer access any Microsoft 365 services

## Skills Demonstrated

- User offboarding in Microsoft 365 Admin Center
- Blocking sign-in and managing account lifecycle
- Shared mailbox access removal
- License unassignment and reclamation
- Verifying offboarding from both admin and user perspectives

## Security Considerations

- Sign-in should be blocked as early as possible in the offboarding process
- Shared mailbox access must be explicitly removed — it is not automatically revoked
- License removal should follow the organization's mailbox retention requirements
- Access removal should follow the principle of least privilege

## What I Learned

- How to fully offboard a user in Microsoft 365 from sign-in blocking through 
license removal
- That shared mailbox access requires a separate removal step and is not 
automatically revoked when a user is offboarded
- How to verify offboarding from both the administrator and end-user perspective
- The importance of treating offboarding as a security task, not just an 
account cleanup
