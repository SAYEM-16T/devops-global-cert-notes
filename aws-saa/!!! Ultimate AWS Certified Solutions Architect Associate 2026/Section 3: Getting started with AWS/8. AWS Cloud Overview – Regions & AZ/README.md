

# 📘 History & Global Infrastructure of AWS Cloud

---

## 1️⃣ AWS Cloud-এর ইতিহাস (History of AWS)

### 🔹 Internal Launch (2002)

* AWS প্রথমে **2002 সালে Amazon.com-এর ভিতরে (internally)** চালু হয়
* Amazon লক্ষ্য করে:

  * তাদের **IT infrastructure খুব শক্তিশালী**
  * IT departments **externalize করা যায়**
* তখন তারা ভাবল:

  > “আমরা শুধু নিজেদের জন্য না, অন্যদের জন্যও IT service দিতে পারি”

---

### 🔹 First Public Service (2004)

* **2004 সালে** AWS প্রথম public service launch করে:

  * **Amazon SQS (Simple Queue Service)**

---

### 🔹 Major Expansion (2006)

* **2006 সালে AWS officially relaunch করে** নতুন কিছু core services নিয়ে:

  * **SQS**
  * **S3 (Simple Storage Service)**
  * **EC2 (Elastic Compute Cloud)**

👉 এই তিনটি সার্ভিস AWS-এর foundation এবং কোর্সে পরে বিস্তারিতভাবে শেখানো হবে।

---

### 🔹 Global Expansion

* AWS শুধু USA-তেই সীমাবদ্ধ থাকেনি
* তারা Europe সহ বিভিন্ন জায়গায় expand করেছে

---

### 🔹 Companies Using AWS Today

বর্তমানে অনেক বড় বড় প্রতিষ্ঠান AWS ব্যবহার করে:

* Dropbox
* Netflix
* Airbnb
* NASA

👉 অনেক application **AWS-এ run করে** অথবা **এখনো করছে**

---

## 2️⃣ AWS Today – Market Position

### 🔹 Gartner Magic Quadrant

* Gartner-এর Magic Quadrant অনুযায়ী:

  * **AWS বহু বছর ধরে market leader**
  * **13th consecutive year leader**

---

### 🔹 Revenue & Market Share

* **Revenue (2023):**

  * 💰 **$90 Billion**
* **Market Share (Q1 2024):**

  * AWS → **31%**
  * Microsoft Azure → **25%** (2nd position)

---

### 🔹 User Base

* AWS-এর আছে:

  * **1+ million active users**

👉 তাই **AWS শেখা মানে cloud career-এর জন্য strong foundation**

---

## 3️⃣ What Can You Build on AWS?

👉 **Short Answer:** Almost everything 🚀

### 🔹 AWS দিয়ে যা বানানো যায়:

* Sophisticated & scalable applications
* Enterprise IT migration
* Backup & storage solutions
* Big Data analytics
* Website hosting
* Backend for:

  * Mobile applications
  * Social applications
* Gaming servers (entire infrastructure)

---

### 🔹 Companies Using AWS

* Netflix
* McDonald’s
* 21st Century Fox
* Activision

👉 প্রায় **সব industry-তেই cloud use case আছে**

---

## 4️⃣ AWS Global Infrastructure Overview

AWS infrastructure তৈরি হয়েছে কয়েকটি core component দিয়ে:

* **Regions**
* **Availability Zones (AZ)**
* **Data Centers**
* **Edge Locations**
* **Points of Presence (PoP)**

👉 এগুলো একসাথে AWS-কে truly global বানায় 🌍

---

## 5️⃣ AWS Regions

### 🔹 What is an AWS Region?

* একটি **Region = multiple data centers-এর cluster**
* Regions পৃথিবীর বিভিন্ন জায়গায় অবস্থিত:

  * Ohio
  * Singapore
  * Sydney
  * Tokyo
  * Paris
  * Mumbai
  * Cape Town ইত্যাদি

---

### 🔹 Region Naming

* প্রতিটি Region-এর:

  * **Name** (e.g., Paris)
  * **Code** (e.g., `eu-west-3`)
* Example:

  * `us-east-1`
  * `eu-west-3`

---

### 🔹 Region Scope of Services

* বেশিরভাগ AWS service:

  * **Region-scoped**
* এক region-এ service ব্যবহার করলে:

  * অন্য region-এ সেটা **new service হিসেবে ধরা হয়**

---

## 6️⃣ How to Choose an AWS Region? (Exam Important ⭐)

নতুন application launch করার সময় region বাছার factors:

### 1️⃣ Compliance

* কিছু দেশে **data local থাকতে হয়**
* Example:

  * France → data must stay in France
  * Solution → deploy in **French region**

---

### 2️⃣ Latency

* User যেখানে বেশি → application সেখানে deploy
* Example:

  * Users in America → deploy in US
  * Australia-তে deploy করলে latency বেশি হবে

---

### 3️⃣ Service Availability

* সব region-এ সব service নেই
* Application যে service ব্যবহার করছে:

  * সেই service ওই region-এ আছে কিনা check করতে হবে

---

### 4️⃣ Pricing

* Region অনুযায়ী price ভিন্ন হয়
* AWS pricing pages দেখে compare করতে হয়

---

## 7️⃣ Availability Zones (AZ)

### 🔹 What is an Availability Zone?

* প্রতিটি Region-এ থাকে:

  * **Multiple Availability Zones**
* সাধারণত:

  * **Minimum:** 3
  * **Maximum:** 6
  * **Most common:** 3

---

### 🔹 Example: Sydney Region

* Region code: `ap-southeast-2`
* Availability Zones:

  * `ap-southeast-2A`
  * `ap-southeast-2B`
  * `ap-southeast-2C`

---

### সাধারণ Pattern (সব region-এর জন্য)

```
<location>-<direction>-<number>
```

| Part                        | মানে                 |
| --------------------------- | -------------------- |
| us / eu / ap                | Country বা Continent |
| east / west / south / north | ভৌগোলিক দিক          |
| 1 / 2 / 3                   | Region সংখ্যা        |

---

### আরো কয়েকটা Example

* `ap-south-1` → Asia Pacific + South + 1 (Mumbai)
* `eu-central-1` → Europe + Central + 1 (Frankfurt)
* `us-west-2` → USA + West + 2 (Oregon)

---


### 🔹 Inside an AZ

* Each AZ:

  * এক বা একাধিক **physical data center**
  * Has:

    * Redundant power
    * Networking
    * Connectivity

---

### 🔹 Fault Isolation

* AZ গুলো:

  * **Disaster-isolated**
* এক AZ failure হলে:

  * অন্য AZ affected হয় না

---

### 🔹 Connectivity

* AZ গুলো:

  * High bandwidth
  * Ultra-low latency network দিয়ে connected
* সব AZ মিলেই একটি **Region** তৈরি করে

---

## 8️⃣ Edge Locations & Points of Presence

### 🔹 What are they?

* AWS has:

  * **400+ Points of Presence**
  * **90 cities**
  * **40 countries**

---

---

## 🌍 Edge Locations & Points of Presence (PoP) – কী?

ভাবো তুমি **YouTube / Netflix / কোনো ওয়েবসাইট** খুলছো।
যদি সব ডাটা **একটা দূরের সার্ভার** থেকে আসে → তাহলে **লোড হতে দেরি** হবে 😖

এই সমস্যা সমাধানের জন্যই AWS ব্যবহার করে:

👉 **Edge Locations**
👉 **Points of Presence (PoP)**

---

## 🏙️ Point of Presence (PoP) মানে কী?

**PoP = একটা ফিজিক্যাল লোকেশন**, যেখানে AWS-এর:

* Cache server
* Network equipment
  থাকে।

📌 AWS-এর আছে:

* **400+ PoP**
* **90টি শহর**
* **40টি দেশ**

👉 মানে AWS প্রায় সারা পৃথিবীতেই “ছোট ছোট স্টেশন” বানিয়ে রেখেছে।

---

## ⚡ Edge Location মানে কী?

**Edge Location হলো সেই জায়গা**, যেখান থেকে:

* Content (image, video, HTML, CSS, JS)
* Static files

👉 **end user-এর একদম কাছ থেকে** serve করা হয়।

📌 Edge Location = PoP-এর অংশ
সব Edge Location আসলে PoP-এর ভেতরেই থাকে।

---

## 🎯 Purpose (কেন ব্যবহার করা হয়?)

### মূল উদ্দেশ্য 👉 **Lowest Latency**

ধরো:

* Main server আছে **USA**
* User আছে **Bangladesh**

❌ Direct USA থেকে আনলে → slow
✅ Bangladesh-এর কাছের Edge Location থেকে আনলে → fast ⚡

---

## 📦 Mainly কোথায় ব্যবহার হয়?

### 🔹 Amazon CloudFront

CloudFront হলো AWS-এর **CDN (Content Delivery Network)**

CloudFront কী করে?

1. Content কে Edge Location-এ cache করে
2. User যেখান থেকে request করে
3. সবচেয়ে কাছের Edge Location থেকে content দেয়

👉 Result:

* Fast loading
* Low latency
* Better user experience 😄

---

## 🧠 খুব simple example

```
User (Dhaka)
   ↓
Nearest Edge Location (India/Singapore)
   ↓
Content delivered super fast ⚡
```

Main server (Region) সব সময় hit করতে হয় না।

---

## 📝 মনে রাখার মতো short notes (Exam friendly)

* **Edge Location** → End user-এর কাছে content দেয়
* **PoP** → AWS-এর physical location
* **Used for** → CDN, mainly CloudFront
* **Goal** → Lowest possible latency
* **Edge ≠ Region**
  (Edge Location কোনো service run করার জায়গা না)

---


### 🔹 Purpose

* End users-কে:

  * **Lowest possible latency** দিয়ে content deliver করা
* Mainly used for:

  * Content delivery (e.g., CloudFront)

👉 এই বিষয়গুলো কোর্সের later section-এ বিস্তারিত আসবে

---

## 9️⃣ AWS Services Scope

### 🌍 Global Services

* IAM
* Route 53
* CloudFront
* WAF

---

### 📍 Region-Scoped Services

* EC2
* Elastic Beanstalk
* Lambda
* Rekognition

---

## 🔟 Service Availability Check

* কোনো service কোন region-এ available কিনা জানার জন্য:

  * **AWS Region Table** check করতে হয়

---

## ✅ Final Summary (Revision Quick View)

* AWS শুরু → **2002 (internal)**
* First public service → **SQS (2004)**
* Core services → **SQS, S3, EC2 (2006)**
* Market leader → **13+ years**
* Revenue (2023) → **$90B**
* Market share (2024) → **31%**
* Regions → Multiple data centers cluster
* AZ → Disaster-isolated units
* Edge locations → Low latency content delivery

---



</br></br></br>
#
# 💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙💙
</br></br></br>



# 🌍 AWS Global Infrastructure (SAA-C03 Notes)

## 1️⃣ AWS Cloud – Exam Context (Ignore History Details)

❌ Launch year, revenue, Gartner ranking → **NOT exam relevant**
✅ Exam focuses on **Regions, AZs, Edge Locations, Scope**

---

## 2️⃣ AWS Global Infrastructure – Big Picture

AWS Global Infrastructure =
**Regions → Availability Zones (AZ) → Data Centers → Edge Locations**

Exam keywords:

* **High availability**
* **Fault tolerance**
* **Low latency**
* **Disaster isolation**

---

## 3️⃣ AWS Regions

### 🔹 What is a Region?

* A **geographical area**
* Contains **multiple Availability Zones (AZs)**
* Example:

  * `us-east-1` → N. Virginia
  * `eu-west-3` → Paris
  * `ap-southeast-2` → Sydney

👉 **Region = cluster of data centers**

---

### 🔹 Region Scope (VERY IMPORTANT 🔥)

* Most AWS services are **Region-scoped**
* Resource in one region ❌ NOT visible in another

Example:

* EC2 in `us-east-1` ≠ EC2 in `eu-west-1`

📌 **Exam keyword:** *“Region-scoped service”*

---

### 🔹 How to Choose an AWS Region (EXAM FAVORITE ⭐)

| Factor                   | Meaning (Bangla + English)                                      |
| ------------------------ | --------------------------------------------------------------- |
| **Compliance**           | Data law → data must stay in country (e.g., France → eu-west-3) |
| **Latency**              | Users close → lower latency                                     |
| **Service Availability** | Not all services in all regions                                 |
| **Pricing**              | Cost varies by region                                           |

📌 **Exam Trick**:
If question mentions **data residency law** → choose **local region**

---

## 4️⃣ Availability Zones (AZ)

### 🔹 What is an Availability Zone?

* **Isolated location inside a Region**
* Each AZ = **1 or more data centers**
* Designed to **prevent cascading failures**

Example:

* Region: `ap-southeast-2` (Sydney)

  * AZs:

    * `ap-southeast-2a`
    * `ap-southeast-2b`
    * `ap-southeast-2c`

---

### 🔹 AZ Characteristics (EXAM GOLD ⭐)

* Physically **separate**
* **Independent power, cooling, networking**
* Connected with:

  * **High bandwidth**
  * **Ultra-low latency**
* Failure in one AZ ❌ does NOT affect others

📌 **Exam keywords:**

* *Fault isolation*
* *High availability*
* *Multi-AZ architecture*



---

## 🔹 Fault Isolation (ফল্ট আইসোলেশন)

### Meaning:

👉 **এক জায়গায় problem হলে, সেটা যেন অন্য জায়গায় ছড়াতে না পারে**

📌 AWS কীভাবে করে?

* System কে আলাদা আলাদা অংশে ভাগ করে
* Problem হলে শুধু ওই অংশটাই affect হয়

### Simple example:

ধরো একটা বিল্ডিংয়ে:

* এক ফ্ল্যাটে আগুন লাগলো 🔥
* কিন্তু fire wall থাকায় পুরো বিল্ডিং পুড়লো না

👉 এটাই **Fault Isolation**

### Exam line:

> Failure in one component does not affect others

---

## 🔹 High Availability (উচ্চ অ্যাভেইলেবিলিটি)

### Meaning:

👉 **System প্রায় সব সময় available থাকবে**

📌 Goal:

* Downtime কমানো
* User সব সময় service পাবে

### Simple example:

* একটা দোকান যদি ২৪/৭ খোলা থাকে → High Availability
* বারবার বন্ধ থাকলে → Low Availability

📌 AWS-এ:

* Multiple servers
* Multiple AZ
* Load Balancer

👉 সব মিলিয়ে service বন্ধ হওয়ার chance খুব কম

### Exam line:

> System remains accessible even during failures

---

## 🔹 Multi-AZ Architecture

### Meaning:

👉 **একই application একাধিক Availability Zone-এ চালানো**

📌 AZ কী?

* Same Region-এর ভেতরের আলাদা data center

### কী সুবিধা?

* এক AZ down হলে
* অন্য AZ থেকে service চলতে থাকে

### Simple example:

ধরো:

* এক স্কুল বন্ধ
* পাশের স্কুলে ক্লাস চলছেই 📚

👉 এটাই Multi-AZ concept

---

## 🔗 তিনটার relation (Exam gold ⭐)

| Keyword           | কী করে                   |
| ----------------- | ------------------------ |
| Fault Isolation   | Problem ছড়াতে দেয় না     |
| Multi-AZ          | আলাদা AZ ব্যবহার করে     |
| High Availability | Service সব সময় চালু রাখে |

👉 **Multi-AZ ব্যবহার করলে → Fault Isolation হয় → High Availability পাওয়া যায়**

---

## 🧠 One-line revision (Exam এর জন্য)

* **Fault Isolation** → Failure containment
* **High Availability** → Minimal downtime
* **Multi-AZ** → Resources in multiple AZs

---

### 🔹 AZ Count (Remember This)

* Minimum: **3 AZs**
* Maximum: **6 AZs**
* Most regions → **3 AZs**

---

## 5️⃣ Region vs Availability Zone (COMPARISON)

| Topic    | Region                | Availability Zone     |
| -------- | --------------------- | --------------------- |
| Scope    | Large geographic area | Inside a region       |
| Contains | Multiple AZs          | 1+ data centers       |
| Failure  | Regional outage = big | AZ failure = isolated |
| Exam Use | Compliance, pricing   | High availability     |

---

## 6️⃣ Edge Locations & Points of Presence (PoP)

### 🔹 What are Edge Locations?

* Used for **content delivery**
* Part of **CloudFront**
* Closer to end users

📌 Stats (memorize concept, not numbers):

* 400+ Points of Presence
* 90+ cities
* 40+ countries

---

### 🔹 Why Edge Locations?

* **Lowest latency**
* Faster content delivery (images, videos, static files)

📌 **Exam keywords:**

* *CloudFront*
* *Edge location*
* *Low latency*
* *Global content delivery*

---

## 7️⃣ Global vs Regional Services (VERY IMPORTANT 🔥)

### 🌍 Global Services

Same across all regions:

* IAM
* Route 53
* CloudFront
* WAF

📌 **Exam Tip:**
If service works **across regions automatically** → Global

### মানে কী?

👉 যদি কোনো AWS service এমন হয় যে:

* তোমাকে **region select করতে হয় না**
* Service নিজে থেকেই **সব region জুড়ে কাজ করে**
* Data / functionality **automatically worldwide available**

➡️ তাহলে ওই service কে বলা হয় **Global Service**

---

## 🌍 Global Service মানে

* Region-bound না
* Single region-এর ভিতরে আটকে থাকে না
* User যেখান থেকেই আসুক → service কাজ করে

---

## 🧠 Simple example

ধরো:

* তুমি **Gmail** ব্যবহার করছো
* তুমি India, USA, Bangladesh — যেখান থেকেই login করো
  👉 Gmail কাজ করেই

➡️ এটা **Global concept**

AWS-এও same idea 👇

---

## ✅ AWS Global Services (Exam এ আসে)

| Service        | কেন Global                    |
| -------------- | ----------------------------- |
| **IAM**        | User/role সব region-এ কাজ করে |
| **Route 53**   | Global DNS                    |
| **CloudFront** | Edge Locations worldwide      |
| **WAF**        | Global protection             |

📌 এগুলোতে:

* Region choose করতে হয় না
* Automatically all regions cover করে

---

## ❌ Regional Service (contrast বুঝার জন্য)

| Service | কেন Regional          |
| ------- | --------------------- |
| EC2     | Region select করতে হয় |
| RDS     | Region specific       |
| VPC     | Region specific       |

---

## 📝 Exam short rule (মাথায় রাখো)

> **No region selection + works worldwide = Global**

আর

> **Region select করতে হয় = Regional**


---

### 📍 Regional Services

Exist per region:

* EC2
* Lambda
* Elastic Beanstalk
* Rekognition
* RDS
* S3 (bucket is regional!)

📌 **Exam Trap ⚠️**

* S3 is **regional**, but **globally accessible via URL**

---

## 8️⃣ Common Exam Traps & Mistakes ⚠️

❌ Thinking AZ = Region
❌ Assuming resources auto-replicate across regions
❌ Ignoring compliance requirement
❌ Deploying single-AZ architecture for HA
❌ Thinking all services available in all regions

---

## 9️⃣ How AWS Exam Questions Are Framed 🧠

Typical question style:

> “A company needs **high availability** and **fault tolerance** for an application in Sydney…”

✅ Correct answer:

* **Deploy across multiple AZs in ap-southeast-2**

---

## 🔟 Quick Revision 🚀

### ✅ Remember This:

* **Region** = geographic area
* **AZ** = isolated data center group
* **Multi-AZ** = high availability
* **Edge Location** = CloudFront, low latency
* **IAM / Route 53 / CloudFront** = Global
* **EC2 / Lambda / RDS / S3** = Regional

### 🧠 Exam Keywords:

`Region-scoped` | `Multi-AZ` | `Fault isolation` | `Low latency` | `Compliance`



























