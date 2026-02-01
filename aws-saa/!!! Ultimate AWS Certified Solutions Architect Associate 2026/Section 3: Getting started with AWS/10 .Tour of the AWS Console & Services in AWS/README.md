# AWS Console Tour & Services (SAA-C03 Exam Notes)

## 1️⃣ AWS Management Console – Basics

### What is AWS Console?

* AWS resources manage করার **web-based UI**
* Browser দিয়ে access করা যায়

### Why important for exam?

* Exam এ **region**, **global service**, **service availability** নিয়ে indirect questions আসে

---

## 2️⃣ AWS Regions (VERY IMPORTANT 🔥)

### What is a Region?

* AWS data center এর **geographical location**
* Example:

  * `us-east-1` → N. Virginia
  * `eu-west-1` → Ireland
  * `af-south-1` → Cape Town

### Key Points (Exam Focus):

* Region select করা হয় **top-right corner** থেকে
* Physically ওই region এ থাকা বাধ্যতামূলক না
* **Closest region = lower latency**

### Exam Keywords:

* *Latency*
* *Geographical proximity*
* *Region-specific resources*

### Common Trap ❌

* ❌ Assume করা যে সব service সব region এ available
* ✅ Reality: **Not all AWS services are available in all regions**

---

## 3️⃣ Global Services vs Regional Services (VERY HIGH YIELD 🔥🔥)

### Global Services

* Region selection লাগে না
* Same view everywhere

**Examples (Must Remember):**

* Route 53
* IAM
* CloudFront
* AWS WAF (mostly)

### Regional Services

* Region-specific
* Resource only visible in selected region

**Examples:**

* EC2
* RDS
* Lambda
* S3 (bucket is global namespace, but data is regional)

---

### 🔁 Comparison Table (Exam Favorite)

| Feature             | Global Service         | Regional Service        |
| ------------------- | ---------------------- | ----------------------- |
| Region selector     | ❌ Not needed           | ✅ Required              |
| Example             | Route 53               | EC2                     |
| Resource visibility | Same globally          | Region-specific         |
| Exam trap           | Forgetting it's global | Looking in wrong region |

---

## 4️⃣ AWS Route 53 (Mentioned in Video)

### What is Route 53?

* AWS DNS (Domain Name System) service

### Exam-Relevant Point:

* Route 53 is a **GLOBAL SERVICE**
* Console shows **“Global”** instead of region name

### Exam Trap ❌

* ❌ Thinking Route 53 is region-based
* ✅ Route 53 is **global**

---

## 5️⃣ EC2 Console & Region Dependency

### EC2 Key Exam Points:

* EC2 is **region-specific**
* If you change region → EC2 instances disappear (not deleted, just not visible)

### Exam Scenario Example:

> “You cannot see your EC2 instance”

✅ Correct thinking:

* Check **correct region**
* Not IAM issue (most common mistake)

---

## 6️⃣ AWS Services Navigation (Low but Useful)

### Ways to find services:

* **Services menu** (category / alphabetical)
* **Search bar** (fastest & recommended)

### Exam Tip 💡

* Not directly tested, but helps understanding AWS structure

---

## 7️⃣ AWS Global Infrastructure & Service Availability

### What is AWS Global Infrastructure page?

* Shows:

  * Regions
  * Availability Zones
  * Services per region

### Why Important for Exam?

* Some services are **not available in all regions**
* Exam question example:

  > “Service X not available in region Y – what should you do?”

✅ Answer logic:

* Switch to another region
* Check regional availability

---

## 8️⃣ Important Exam Traps & Mistakes ❌

* ❌ Forgetting to check region
* ❌ Assuming all services are global
* ❌ Assuming all services exist in every region
* ❌ Thinking region = availability zone

---

## 9️⃣ Exam Keywords to Remember 🧠

* Region
* Global service
* Regional service
* Latency
* Service availability
* AWS Global Infrastructure
* Region selector
* Resource visibility

---

## 🔁 Quick Revision (Last 30 Seconds)

* AWS Console → web UI to manage services
* **Region matters** for most services
* Closest region → lowest latency
* **Route 53 = Global service**
* **EC2 = Regional service**
* Resources missing? → Check region first
* Not all services available in all regions

---
