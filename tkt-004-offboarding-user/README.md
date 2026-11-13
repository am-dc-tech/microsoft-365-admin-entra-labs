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

<img width="878" height="293" alt="1 block-sign-in" src="https://github.com/user-attachments/assets/e0cbe227-93c6-4979-9751-f19a5b07836c" />


3. Open **Microsoft Entra Admin Center** → **Users** → select Bob Baker


4. Go to **Revoke sessions** and confirm all active sessions are terminated

<img width="906" height="128" alt="2 revoke-session" src="https://github.com/user-attachments/assets/eca11a74-31b5-4da0-aa86-4385c32cd686" />


5. Confirm under **Properties** that **Account enabled = No**

<img width="262" height="81" alt="3 account-enabled-no" src="https://github.com/user-attachments/assets/ffa8b092-7305-4960-9f6c-b79f100c82a9" />


6. Back in Microsoft 365 Admin Center → **Teams & Groups**


7. Locate the shared mailbox → remove **Bob Baker** from membership

<img width="496" height="713" alt="4 remove-user-from-shared-mailbox" src="https://github.com/user-attachments/assets/4fadee1e-10e5-403c-b21e-781d75194538" />


8. Verify he is no longer listed

<img width="676" height="288" alt="5 remove-from-group" src="https://github.com/user-attachments/assets/453ec8a8-971f-41ce-b360-d05e82429e81" />



9. Go to **Billing > Licenses** → locate Bob's license → **unassign it**

<img width="1102" height="428" alt="6 remove-license" src="https://github.com/user-attachments/assets/56a76657-29e5-4f7a-adb2-1108f77e681e" />


10. Confirm the license has been removed

<img width="1080" height="257" alt="7 bob-removed-from-licenses" src="https://github.com/user-attachments/assets/7b936dda-f32c-4581-bfe4-e51a456ace30" />


11. Verify from the **user side**: attempt to sign in at office.com with Bob's 
credentials and confirm access is denied

<img width="1570" height="342" alt="login-issue-no-outlook" src="https://github.com/user-attachments/assets/a56ea3f1-7b17-4c40-a574-3d2299d5ee87" />


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
