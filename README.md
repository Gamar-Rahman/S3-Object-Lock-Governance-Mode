# S3-Object-Lock-Governance-Mode
Learn how to enable Amazon S3 Object Lock using Governance retention mode to protect objects from deletion and meet WORM compliance requirements.

# Create S3 Object Lock with Governance Retention Mode

##  Introduction
Amazon S3 Object Lock is a feature that helps prevent objects from being deleted or overwritten for a fixed amount of time or indefinitely. This immutability model is commonly used to meet **compliance and regulatory requirements** that mandate **WORM (Write Once, Read Many)** storage.

In this lab, you will learn how to enable **S3 Object Lock** and configure a **retention period using Governance mode**.

---

##  What is S3 Object Lock?
Amazon S3 Object Lock allows you to store objects using a WORM model, which prevents objects from being:
- Deleted
- Overwritten
- Modified

Objects remain immutable for the duration of a **retention period** or until a **legal hold** is removed.

This feature adds an additional layer of protection against:
- Accidental deletions
- Malicious data tampering
- Compliance violations

---

##  Object Retention Options
Amazon S3 Object Lock provides two methods to protect objects:

###  Retention Period
- Specifies a **fixed duration**
- Objects cannot be deleted or overwritten until the retention period expires

###  Legal Hold
- No expiration date
- Object remains immutable until the legal hold is explicitly removed

---

##  Retention Modes
Amazon S3 supports two retention modes:

###  Governance Mode
- Users **cannot overwrite or delete** objects by default
- Users with special IAM permissions (`s3:BypassGovernanceRetention`) **can override** the lock
- Suitable for internal compliance and governance controls

###  Compliance Mode
- **No user**, including root, can delete or modify objects
- Used for strict regulatory requirements

---

##  Lab Objective
In this lab, you will:

1. Create an S3 bucket with Object Lock enabled
2. Upload an object
3. Enable Object Lock retention
4. Configure **Governance mode**
5. Set a retention period (in days)
6. Validate that the object cannot be deleted or overwritten

---

##  Lab Details
- **Retention Mode:** Governance
- **Retention Period:** 1 day
- **Storage Model:** WORM

Object Lock ensures that objects remain immutable for the defined retention period.

---

##  Do You Know?
You can use **S3 Object Lock (Governance mode)** to protect objects against being overwritten or deleted for **up to 100 years**, while still allowing authorized users to override retention when necessary.

---

##  Prerequisites
- AWS Account
- IAM permissions for S3
- S3 bucket with Object Lock enabled (must be enabled at creation)
- AWS CLI or AWS Management Console
  
---

## Use Cases
- Compliance and regulatory data retention
- Financial records storage
- Audit logs protection
- Ransomware protection
- Backup immutability


