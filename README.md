

## 🔹 What is Datadog? (1-line answer)

**Datadog** is a **SaaS observability tool** used to monitor **infrastructure, applications, logs, and users** from one place.

🧠 **Memory trick:**
**“Datadog = SaaS + Agent + Observability”**

---

## 🔹 Why Datadog? (Why companies use it)

Because it gives:

* Metrics
* Logs
* Traces
  in **one tool**, and it’s **easy to use**

🧠 **Trick:**
**MLT = Metrics + Logs + Traces**

---

## 🔹 Is Datadog SaaS or installed?

* Datadog is **SaaS (cloud-based)**
* ❌ No Datadog server to install
* ✅ Only install **Datadog Agent** on servers

🧠 **Trick:**
**“No server, only agent”**

---

## 🔹 What is Datadog Agent?

Datadog Agent is a **lightweight software** installed on:

* EKS nodes
* EC2 instances

It collects:

* Metrics
* Logs
* Traces
  and sends them to Datadog.

🧠 **Trick:**
**“Agent = Collector + Sender”**

---

## 🔹 How data flows in Datadog

```
Server / Pod
   ↓
Datadog Agent
   ↓
Datadog SaaS
   ↓
Dashboard / Alerts
```

🧠 **Trick:**
**“Install → Collect → Send → Visualize”**

---

## 🔹 Metrics Datadog collects by default

Basic metrics:

* CPU
* Memory
* Disk
* Network

🧠 **Trick:**
**“CMDN = CPU, Memory, Disk, Network”**

---

## 🔹 What are Datadog Integrations?

Integrations tell Datadog **WHAT application you are running**.

Examples:

* AWS
* EKS
* Nginx
* MongoDB

Without integration → only basic metrics
With integration → **app-specific metrics**

🧠 **Trick:**
**“Agent = basic, Integration = smart”**

---

## 🔹 Datadog in my project (Interview GOLD)

* **Frontend**: S3 + CloudFront
* **Backend**: EKS
* **Database**: MongoDB on EC2
* **Monitoring**:

  * **Amazon CloudWatch** → EC2 native metrics
  * Datadog → Full visibility + correlation

🧠 **Trick:**
**“CloudWatch = AWS level, Datadog = Full stack”**

---

## 🔹 How Datadog integrates with AWS

1. Create **IAM Role** in AWS
2. Attach Datadog read-only permissions
3. Add AWS account in Datadog
4. Datadog pulls **CloudWatch metrics**

No access keys needed.

🧠 **Trick:**
**“IAM Role → CloudWatch → Datadog”**

---

## 🔹 What is APM? (Very important)

**APM (Application Performance Monitoring)** shows:

* Which API is slow
* Which service is slow
* Which DB call is slow

In microservices:

```
User → ALB → Service → Service → DB
```

APM shows **time spent at each step**

🧠 **Trick:**
**“APM = Where time is going?”**
🔹 APM (Application Performance Monitoring)
🔹 APM – 1-line answer

APM shows how much time each request spends inside an application, service, and database.

🧠 Memory trick:
“APM = Where time is spent”
---
🔹 Why APM is used?

Find slow APIs

Find slow services

Find slow DB queries

Fix performance issues faster

🧠 Trick:
“APM = Find slow part”
---
🔹 How APM works (VERY IMPORTANT)
User → ALB → Service → Service → Database


APM tracks time at each step (trace).

🧠 Trick:
“APM follows the request”
---
🔹 What is a Trace?

One end-to-end request

Contains multiple spans

🧠 Trick:
“Trace = One request”
---
🔹 What is a Span?

One operation inside a trace
(API call, DB call, function)

🧠 Trick:
“Span = One step”
---
🔹 How to enable APM (Easy)

Install Datadog Agent

Add Datadog APM library to app

Enable APM in agent config

Deploy application

🧠 Trick:
“Agent + Library = APM”
---
🔹 APM in estment.com (Interview GOLD)

“In estment.com, we use APM to trace backend APIs running on EKS. It helps us identify slow services and MongoDB query latency.”

🧠 Trick:
“APM = API + DB latency”
---
🔹 APM vs Synthetic vs RUM (SUPER IMPORTANT)
Type	Who hits	Purpose
Synthetic	Robot	Check uptime
APM	Real request	Find bottleneck
RUM	Real user	User experience

🧠 Trick:
“Robot → App → Human”
---
🔹 What problems APM solves?

High response time

Microservice latency

Database slowness

Error spikes

🧠 Trick:
“APM solves slowness”
---
🔹 ONE-LINE MASTER FORMULA (REMEMBER THIS 🔥)
APM = Trace → Spans → Bottleneck


If you remember this, you can answer ANY APM question confidently.

---

## 🔹 Synthetic Monitoring

* Robot (not real user)
* Hits API / URL 24×7
* Checks:

  * Uptime
  * Response time
  * SSL expiry

🧠 **Trick:**
**“Synthetic = Robot testing”**
---
🔹 Synthetic Monitoring (1-line answer)

Synthetic Monitoring proactively checks website/API availability using robots from global locations.

🧠 Memory trick:
“Synthetic = Robot checking, not humans”
---
🔹 Why Synthetic Monitoring?

Runs 24×7

Detects issues before users

Checks uptime, latency, SSL, correctness

🧠 Trick:
“Before user complains”
---
🔹 Types of Synthetic Tests (VERY IMPORTANT)
1️⃣ API Test

Tests single endpoint

Checks:

Status code (200)

Response time

Response body

🧠 Trick:
“API = One URL, one check”
---
2️⃣ Browser Test

Simulates real user journey

Multiple steps:

Open page

Click

Fill form

Submit

🧠 Trick:
“Browser = Click, Type, Submit”
---
🔹 How to set up Synthetic Test (Easy steps)

Go to Digital Experience → New Test

Choose API or Browser

Enter URL

Add assertions

Status = 200

Response < 1 sec

Select locations

Add alert recipients

🧠 Trick:
“Type → URL → Rule → Location → Alert”
---
🔹 Example (Interview GOLD)

“We use Synthetic Monitoring estment.com to check backend APIs behind ALB. API tests verify status codes and response time from multiple regions before users face issues.”

🧠 Trick:
“Synthetic = API health before user”
---
🔹 ONE-LINE MASTER FORMULA (REMEMBER THIS)
Synthetic = Robot + URL + Global + Alert


If you say this confidently, interviewer will be satisfied ✅

---

## 🔹 Real User Monitoring (RUM)

* Tracks **real users**
* Browser-based
* Shows user experience

🧠 **Trick:**
**“RUM = Real Humans”**

---

## 🔹 Logs in Datadog

* Central place for:

  * App logs
  * System logs
* Logs are:

  * Collected
  * Parsed
  * Filtered

🧠 **Trick:**
**“Logs = What happened?”**

---

## 🔹 Dashboards in Datadog

Dashboards show:

* Metrics
* Logs
* Traces
  using graphs and charts

🧠 **Trick:**
**“Dashboard = Single screen truth”**

---

## 🔹 Alerts in Datadog

Alerts trigger when:

* CPU > threshold
* Error rate increases
* Service is down

🧠 **Trick:**
**“Alert = Act fast”**

---

## 🔹 Datadog vs CloudWatch (1-liner)

> CloudWatch monitors AWS resources, Datadog connects infrastructure, applications, and users together.

🧠 **Trick:**
**“CloudWatch sees parts, Datadog sees whole”**

---

## 🔹 ONE MASTER MEMORY FORMULA (USE THIS 🔥)

### **Datadog =**

```
Agent
+ Integrations
+ Metrics
+ Logs
+ Traces
+ Dashboards
+ Alerts
```



🔑 FINAL 10-SECOND INTERVIEW SUMMARY (MEMORIZE THIS)

“Datadog is a SaaS-based observability platform. We install Datadog Agents on servers and Kubernetes nodes to collect metrics, logs, and traces. Using integrations, Datadog monitors AWS, EKS, and MongoDB. We use APM for performance tracing, Synthetic monitoring for uptime checks, RUM for user experience, dashboards for visibility, and alerts for proactive issue detection. CloudWatch is used alongside Datadog for AWS-native metrics.”
