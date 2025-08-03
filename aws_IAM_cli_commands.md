# 🔐 AWS IAM CLI Commands  
*Organized and Easy to Understand Format*

---

## 👤 User Management

| Purpose                  | Command                                                                 |
|--------------------------|--------------------------------------------------------------------------|
| Create a user            | `aws iam create-user --user-name <user-name>`                           |
| List users               | `aws iam list-users`                                                    |
| Get user info            | `aws iam get-user --user-name <user-name>`                              |
| Delete a user            | `aws iam delete-user --user-name <user-name>`                           |

---

## 🔐 Access Key Management

| Purpose                          | Command                                                                             |
|----------------------------------|--------------------------------------------------------------------------------------|
| Create access key                | `aws iam create-access-key --user-name <user-name>`                                 |
| List access keys                 | `aws iam list-access-keys --user-name <user-name>`                                  |
| Delete an access key             | `aws iam delete-access-key --access-key-id <key-id> --user-name <user-name>`        |
| Update access key status         | `aws iam update-access-key --access-key-id <key-id> --status Active|Inactive --user-name <user-name>` |

---

## 👥 Group Management

| Purpose              | Command                                                             |
|----------------------|----------------------------------------------------------------------|
| Create a group       | `aws iam create-group --group-name <group-name>`                    |
| List groups          | `aws iam list-groups`                                               |
| Add user to group    | `aws iam add-user-to-group --user-name <user-name> --group-name <group-name>` |
| Remove user from group | `aws iam remove-user-from-group --user-name <user-name> --group-name <group-name>` |
| Delete group         | `aws iam delete-group --group-name <group-name>`                    |

---

## 🔖 Policy Management

| Purpose                      | Command                                                                 |
|------------------------------|--------------------------------------------------------------------------|
| Attach policy to user        | `aws iam attach-user-policy --user-name <user-name> --policy-arn <arn>` |
| Detach policy from user      | `aws iam detach-user-policy --user-name <user-name> --policy-arn <arn>` |
| List attached user policies  | `aws iam list-attached-user-policies --user-name <user-name>`           |
| List all policies            | `aws iam list-policies`                                                 |
| Create a policy              | `aws iam create-policy --policy-name <policy-name> --policy-document file://<policy-file>.json` |
| Delete a policy              | `aws iam delete-policy --policy-arn <arn>`                              |

---

## 🧑‍💼 Role Management

| Purpose                     | Command                                                                 |
|-----------------------------|--------------------------------------------------------------------------|
| Create a role               | `aws iam create-role --role-name <role-name> --assume-role-policy-document file://<trust-policy>.json` |
| List roles                  | `aws iam list-roles`                                                   |
| Attach policy to role       | `aws iam attach-role-policy --role-name <role-name> --policy-arn <arn>` |
| Detach policy from role     | `aws iam detach-role-policy --role-name <role-name> --policy-arn <arn>` |
| Delete a role               | `aws iam delete-role --role-name <role-name>`                           |

---

## ✅ Login Profile (Console Access)

| Purpose                       | Command                                                                 |
|-------------------------------|--------------------------------------------------------------------------|
| Create login profile          | `aws iam create-login-profile --user-name <user-name> --password <password>` |
| Update login profile password | `aws iam update-login-profile --user-name <user-name> --password <password>` |
| Delete login profile          | `aws iam delete-login-profile --user-name <user-name>`                   |

---

## 📋 Miscellaneous

| Purpose                  | Command                                        |
|--------------------------|------------------------------------------------|
| Get current user         | `aws iam get-user`                             |
| Get user policies (inline)| `aws iam list-user-policies --user-name <user-name>` |
| Get group users          | `aws iam get-group --group-name <group-name>` |

---

