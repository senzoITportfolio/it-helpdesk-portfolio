# 00 - Entra ID: Users, Groups and Roles

## Goal
Practise creating and managing users, groups and admin roles in
Microsoft Entra ID (Free tier) for a fictional company.

## Environment
- Azure account with Default Directory (Entra ID Free)
- Fictional company: 6 users across HR, IT and Sales

## 1. Users created
| Name | Job title | Department |
|---|---|---|
| Amy Nkosi | HR Officer | HR |
| Thabo Dlamini | HR Manager | HR |
| Sipho Mkhize | IT Support | IT |
| Lerato Naidoo | Systems Admin | IT |
| Kevin Pillay | Sales Rep | Sales |
| Zanele Cele | Sales Manager | Sales |

**Steps:** Entra ID > Users > New user > Create new user
**Screenshot:** ![users](screenshots/users-list.png)

## 2. Security groups
| Group | Members |
|---|---|
| HR-Staff | Amy, Thabo |
| IT-Admins | Sipho, Lerato |
| Sales-Staff | Kevin, Zanele |

**Steps:** Entra ID > Groups > New group (Security, Assigned)
**Screenshot:** ![groups](screenshots/groups.png)

## 3. Role assignment (least privilege)
Assigned **User Administrator** (Active, permanent) to Lerato Naidoo
instead of Global Administrator.
**Screenshot:** ![role](screenshots/role-assignment.png)

## 4. Permission testing as Lerato
| Test | Result | Why |
|---|---|---|
| View Users list | Worked | Role grants user read access |
| Reset Amy's password | Worked | Amy is a non-admin |
| Create a new user | Worked | Within User Administrator scope |
| Edit tenant Properties | Denied | Read-only, Save disabled |
| Reset my own admin account | Denied | Personal Microsoft account (#EXT#) |
| Reset a Global Admin (admin.test) | Denied | Can't manage higher-privileged accounts |

## 5. Lifecycle tasks
- Reset a user's password
- Blocked sign-in for a user
- Moved a user between groups
- Deleted and restored a user

## 6. Troubleshooting
- **P1/P2 message on the roles page:** it came from the custom-roles
  banner. Built-in roles work on Free. Role assignment succeeded
  once I clicked the role name, then Add assignments, and chose Active.
- **Wrong prediction on the admin reset test:** I expected a privilege
  denial, but the account was an external personal Microsoft account,
  so only its owner can reset it. I confirmed the privilege boundary
  with a separate Global Admin test user.

## What I learned
In this lab I created users and security groups in Microsoft Entra ID and gave one user the built-in User Administrator role instead of Global Administrator. Testing as that user showed me least privilege in practice: she could manage regular users but was blocked from tenant settings and from resetting a Global Administrator’s password. I also learned that some errors come from licensing or account type and not from permissions, such as the P1/P2 banner for custom roles and the external personal account that only its owner can reset.
