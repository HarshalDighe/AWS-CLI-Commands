# ☁️ AWS S3 CLI Commands  

---

## 📦 S3 Bucket Commands

| Purpose                     | Command                                                   |
|-----------------------------|------------------------------------------------------------|
| Create a bucket             | `aws s3 mb s3://<bucket-name>`                             |
| List all buckets            | `aws s3 ls`                                               |
| List contents of a bucket   | `aws s3 ls s3://<bucket-name>/`                            |
| Delete a bucket             | `aws s3 rb s3://<bucket-name>`                             |
| Delete bucket (force)       | `aws s3 rb s3://<bucket-name> --force`                     |

---

## 📁 S3 Object (File) Commands

| Purpose                         | Command                                                                 |
|----------------------------------|--------------------------------------------------------------------------|
| Upload a file                   | `aws s3 cp <local-path> s3://<bucket-name>/<key>`                        |
| Download a file                 | `aws s3 cp s3://<bucket-name>/<key> <local-path>`                        |
| Copy object between buckets     | `aws s3 cp s3://<source-bucket>/<key> s3://<dest-bucket>/<key>`          |
| Delete an object                | `aws s3 rm s3://<bucket-name>/<key>`                                     |

---

## 🔄 Sync Commands

| Purpose                 | Command                                                           |
|--------------------------|--------------------------------------------------------------------|
| Sync folder to bucket   | `aws s3 sync <local-folder> s3://<bucket-name>`                    |
| Sync bucket to folder   | `aws s3 sync s3://<bucket-name> <local-folder>`                    |

---

## 🔐 Permissions & Access

| Purpose                        | Command                                                                 |
|----------------------------------|--------------------------------------------------------------------------|
| Set public read on object      | `aws s3api put-object-acl --bucket <bucket-name> --key <key> --acl public-read` |
| Get object ACL                 | `aws s3api get-object-acl --bucket <bucket-name> --key <key>`            |

---

## ⚙️ Advanced / API-level (s3api)

| Purpose                          | Command                                                                 |
|----------------------------------|--------------------------------------------------------------------------|
| Enable bucket versioning        | `aws s3api put-bucket-versioning --bucket <bucket-name> --versioning-configuration Status=Enabled` |
| Get bucket versioning status    | `aws s3api get-bucket-versioning --bucket <bucket-name>`                |
| List object versions            | `aws s3api list-object-versions --bucket <bucket-name>`                 |
| List bucket policy              | `aws s3api get-bucket-policy --bucket <bucket-name>`                    |
| Set bucket policy               | `aws s3api put-bucket-policy --bucket <bucket-name> --policy file://policy.json` |
|Get bucket policy             | `aws s3api get-bucket-policy --bucket <bucket-name>`

## 😊Other

| Purpose                        | Command                                                                 |
|----------------------------------|--------------------------------------------------------------------------|
| Check Object Metadata  | `aws s3api head-object --bucket <bucket-name --key <key>`

---
