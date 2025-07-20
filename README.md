# 🛡️ Amazon S3 Data Protection Walkthrough

This project documents a hands-on walkthrough of how to **protect data on Amazon S3** from accidental deletion or corruption using:

- ✅ S3 Versioning
- 🔐 S3 Object Lock
- 🔁 S3 Cross-Region Replication

The steps include screenshots and explanations, designed as part of my AWS learning journey and portfolio.

---

## 📁 1. Creating an S3 Bucket

- Navigate to **Amazon S3 > Create bucket**
- Assign a unique name and select your preferred AWS Region
- Enable the following options:
  - ✅ Block all public access
  - ✅ Enable bucket versioning
  - *(Optional)*: Enable Object Lock (requires versioning to be enabled)

🖼️  
![Create Bucket](screenshots/1-create-bucket.jpg)

---

## 🔄 2. Enabling Versioning

Versioning helps retain, retrieve, and restore every version of every object stored in your bucket.

- Go to your bucket > Properties
- Scroll to **Bucket Versioning**
- Click **Edit** > Enable > Save changes

🖼️  
![Enable Versioning](screenshots/2-versioning.jpg)

---

## 🔐 3. Enabling Object Lock

Object Lock prevents object versions from being overwritten or deleted for a fixed amount of time or indefinitely.

- Enable **Object Lock** at bucket creation (required)
- After creation:  
  - Go to **Management > Object Lock**
  - Create a **retention policy** (Governance or Compliance mode)

🖼️  
![Enable Object Lock](screenshots/3-object-lock.jpg)

---

## 🌍 4. Setting Up S3 Replication (Cross-Region)

S3 Replication (CRR) allows you to copy objects automatically to a destination bucket in a different region for added resilience.

### Steps:
- Create a destination bucket in a **different region**
- On the **source bucket**:  
  - Go to **Management > Replication rules**
  - Create a rule and choose:
    - ✅ Entire bucket or specific prefix
    - ✅ Destination bucket and region
    - ✅ IAM role for replication
    - ✅ Option to replicate existing objects

🖼️  
![S3 Replication Rule](screenshots/4-replication-rule.jpg)

---

## 🧠 Summary Table

| Feature | Purpose |
|----------------|------------------------------------------------------|
| S3 Versioning | Recover from accidental deletion or overwrite |
| Object Lock | Prevent deletion/modification based on policies |
| S3 Replication | Cross-region backup for availability and durability |

---

## 🙋 About Me

I’m **Cameline Nasambu**, a finance professional transitioning into the tech space with a keen interest in **Cloud Computing** and **Digital Transformation**. Working on documenting hands-on projects to deepen my learning and hoping for a successful transition to bridge the gap between finance and tech.

---

## 📬 Contact

- 📧 Email: [nasambucamelinen@gmail.com](mailto:nasambucamelinen@gmail.com)  
- 💼 LinkedIn: [linkedin.com/in/camelinenyongesa-879b8320b](https://www.linkedin.com/in/camelinenyongesa-879b8320b)  
- 🌐 Portfolio: [EC2 Portfolio Site](http://54.155.86.225)

---

> **Note**: This is a static documentation-only repository. For the full portfolio, visit my main GitHub or hosted EC2 site.
