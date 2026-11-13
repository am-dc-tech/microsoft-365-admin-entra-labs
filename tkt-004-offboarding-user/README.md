# M365 User Offboarding Lab — Bob Baker

## Summary

A hands-on lab simulating the offboarding of a departing employee using Microsoft 365 
Admin Center and Microsoft Entra Admin Center. This lab covers blocking sign-in, 
revoking active sessions, removing shared mailbox access, and unassigning a license.

## Environment

- Platform: Microsoft 365 Admin Center · Microsoft Entra Admin Center
- Role: Tier 1 IT Administrator
- User Being Offboarded: Bob Baker

## Scenario

Bob Baker is leaving the organization. As the IT administrator, I need to secure his 
account, revoke his active sessions, remove his shared mailbox access, and unassign 
his license to complete a secure offboarding.

## Steps

1. Open Microsoft 365 Admin Center → **Users > Active Users**
2. Select **Bob Baker** and **block sign-in** — confirm the account is blocked

3. Open **Microsoft Entra Admin Center** → **Users** → select Bob Baker
4. Go to **Revoke sessions** and confirm all active sessions are terminated
5. Confirm under **Properties** that **Account enabled = No**

6. Back in Microsoft 365 Admin Center → **Teams & Groups**
7. Locate the shared mailbox → remove **Bob Baker** from membership
8. Verify he is no longer listed

9. Go to **Billing > Licenses** → locate Bob's license → **unassign it**
10. Confirm the license has been removed

11. Verify from the **user side**: attempt to sign in at office.com with Bob's 
credentials and confirm access is denied

## Expected Outcome

- Sign-in is blocked and confirmed in both Admin Center and Entra
- All active sessions are revoked
- Shared mailbox access is removed
- License is unassigned
- Bob Baker cannot access any Microsoft 365 services

## Skills Demonstrated

- User offboarding across Microsoft 365 Admin Center and Entra Admin Center
- Session revocation via Entra ID
- Shared mailbox access removal
- License unassignment and reclamation
- Cross-platform verification of offboarding status

## Security Considerations

- Block sign-in first — before any other offboarding step
- Revoking sessions in Entra ensures active tokens are invalidated immediately
- Shared mailbox access is not automatically removed when sign-in is blocked
- License removal should follow the organization's mailbox retention policy

## What I Learned

- How to offboard a user across both Microsoft 365 Admin Center and Entra Admin Center
- That blocking sign-in alone is not enough — active sessions must also be revoked in Entra
- That shared mailbox access requires a separate explicit removal step
- How to verify offboarding from both the administrator and end-user perspective
