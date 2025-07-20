# 🗂️ Amazon S3 Configuration – Portfolio Documentation

This project documents my hands-on setup of key S3 features: **Versioning**, **Object Lock**, and **Cross-Region Replication**. The screenshots and steps demonstrate how I created and configured these features using the AWS Console.

---

## 1️⃣ Creating the Source Bucket (`meline-bucket`)

The first step involved creating a new S3 bucket named `meline-bucket`.

![01 Create Bucket](screenshots/01-meline-bucket.png)

---

## 2️⃣ Uploading an Object

An object (file) was uploaded to `meline-bucket` to prepare for testing versioning and replication.

![02 Upload File](screenshots/02-upload-melinebucket.png)

---

## 3️⃣ Enabling Versioning

Versioning was enabled on the source bucket. This allows multiple versions of the same object to be preserved.

📌 **Why it matters:** Versioning protects against accidental deletions and allows recovery of previous object states.

![03 Enable Versioning](screenshots/03-enabled-version-melinebucket.png)

---

## 4️⃣ Creating Destination Bucket & Enabling Object Keys

Created a destination bucket `meline2bucket` and enabled key settings for replication.

![04 Destination Bucket](screenshots/04-meline2bucket-objectkeyenabled.png)

---

## 5️⃣ Enabling Object Lock

Object Lock was enabled on the source bucket to prevent object deletions/modifications for a set period.

📌 **Use case:** Ensures compliance and protection against accidental or malicious changes.

![05 Object Lock Enabled](screenshots/05-enabled-objectlock.png)

---

## 6️⃣ Confirmed Lock on Destination Bucket

Confirmed that the destination bucket was configured to support Object Lock as well.

![06 Lock Confirmed](screenshots/06-meline2bucket-locked.png)

---

## 7️⃣ Creating Replication Rule

A replication rule was created to replicate objects from `meline-bucket` to `meline2bucket`.

📌 **Key Details:**
- Status: Enabled
- Rule applies to all objects
- Replicates delete markers and existing objects (optional)

![07 Replication Rule](screenshots/07-creation-replicationrule.png)

---

## 8️⃣ Replication Configuration Complete

Final configuration screen showing the replication successfully set up.

![08 Replication Complete](screenshots/08-replication-configured.png)

---

## ✅ Summary

This S3 configuration demonstrates:
- How to enable **versioning** for object-level recovery
- How to use **Object Lock** for compliance and protection
- How to set up **replication** to another bucket (cross-region supported)

> 📂 All screenshots are stored inside the `screenshots/` folder.

---
