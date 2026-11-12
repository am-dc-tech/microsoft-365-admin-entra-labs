# Microsoft 365 Onboarding Lab

A hands-on lab for onboarding a small organization to Microsoft 365 using the Admin Center and Entra ID 

---

## Summary

This lab covers the essentials of setting up a Microsoft 365 tenant from scratch. You'll create user accounts, assign licenses, enforce MFA through Entra ID, and set up a shared mailbox — all through the browser.

**Time:** 45–60 min  
**Tools:** M365 Admin Center · Microsoft Entra ID · GitHub

---

## Scenario

Contoso Startup just purchased 10 Microsoft 365 Business Standard licenses. As the admin, you need to get three employees set up, lock down the basics before anyone logs in, and spin up a shared support mailbox the team can all use. The goal is to have everything done and pushed to this repo by end of day.

---

## Steps

### 1. Sign In to the Admin Center

Go to (https://admin.cloud.microsoft/#/homepage)

### 2. Create the Users

Go to **Users → Active users → Add a user** and create three accounts. Fill in the following for each:

| Display Name | Username | Job Title | Department |
|---|---|---|---|
| Alice Adams | alice@AMTECHLab.onmicrosoft.com | Marketing Coordinator | Marketing |
| Bob Baker | bob@AMTECHLab.onmicrosoft.com | IT Support Specialist | Information Technology |
| Carol Chen | carol@AMTECHLab.onmicrosoft.com | Financial Analyst | Finance |

During the wizard, assign each user a **Microsoft 365 Business Standard** license. Leave their role as **No admin access**.

Save the temporary passwords somewhere local — not in this repo.

<img width="891" height="132" alt="1 add-users-with-licenses" src="https://github.com/user-attachments/assets/3fedbfb8-1f4d-40ea-8892-abd5877ae231" />


### 3. Enable Security Defaults in Entra ID

Security Defaults turns on MFA for all users. Enable it before sending anyone their login.

1. Go to (entra.microsoft.com)
2. Navigate to Entra Id --> Properties  
3. Scroll down and click **Manage security defaults**
4. Toggle **Security defaults** to **Enabled** and save

<img width="215" height="815" alt="2 Entra-properties-security-defaults" src="https://github.com/user-attachments/assets/b6e226e4-a1a2-44d0-b623-7b6950790e71" />

<img width="434" height="332" alt="3 security-defaults-enabled" src="https://github.com/user-attachments/assets/13c19585-dc57-4ec9-9adf-82bed7d34c95" />


### 4. Review Users in Entra ID

While you're in Entra, take a look at how the accounts appear:

1. Go to **Identity → Users → All users**
2. Confirm Alice, Bob, and Carol are listed
3. Click into one user and review their **Properties** and **Assigned licenses** tabs

This gives you a feel for how Entra ID sits behind the M365 Admin Center.

<img width="1092" height="253" alt="4a alice-licenses" src="https://github.com/user-attachments/assets/2c76b91a-935c-4269-a066-db608812e7f1" />

<img width="1071" height="232" alt="4b-bob-licenses" src="https://github.com/user-attachments/assets/9a44e9e1-a5fe-4a8c-80c0-457e99dd6dfd" />

<img width="1072" height="233" alt="4c-carol-licenses" src="https://github.com/user-attachments/assets/2ae96979-2ae0-4b0c-b522-4d51ef040be1" />


### 5. Create the Shared Mailbox

Back in the M365 Admin Center:

1. Go to **Teams & groups → Shared mailboxes → Add a shared mailbox**
2. Set the name to `Support` and address to `support@yourdomain.onmicrosoft.com`
3. After it's created, open it and add Alice, Bob, and Carol as **Members**

They can now send and receive email from the Support mailbox.

<img width="665" height="101" alt="5a shared-mail" src="https://github.com/user-attachments/assets/66ce86a5-7ca3-42a8-9c90-505ccc35a61a" />

<img width="525" height="682" alt="5b shared-mail" src="https://github.com/user-attachments/assets/fa729004-1a0c-43f3-aad9-f9b7daa4cde7" />


### 6. Confirm Everything in the Admin Center

Do a quick pass to make sure everything looks right:

- **Users → Active users** — all three users show a license
- **Teams & groups → Shared mailboxes** — Support mailbox is listed with 3 members
- **Entra ID → Users** — all users are present and enabled

<img width="609" height="215" alt="6  confirm-account-enabled" src="https://github.com/user-attachments/assets/79935345-b9cf-4301-bf6f-ae6c92545c20" />

---

## Security Notes
- **MFA before credentials** — always enable Security Defaults before handing out logins.
- **Least privilege** — users are created with no admin roles unless explicitly needed.
- **Shared mailbox access** — revisit membership when people leave the team.

---

## What I Learned

- How to provision users and assign licenses in the M365 Admin Center
- How Entra ID sits behind Microsoft 365 and where user identities actually live
- How Security Defaults enforce MFA without needing a premium Entra license
- How shared mailboxes work in Exchange Online and how to manage member access
- Why keeping a runbook in GitHub makes IT work easier to audit and repeat

---
      