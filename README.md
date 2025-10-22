# Fraud-Detection-and-Risk-Analysis-for-Insurance-Claims

## Introduction

Verita Assurance Ltd., a mid-sized UK insurance company, faced rising fraudulent claims, with detection often happening only after payouts. This reactive process led to financial losses, higher operating costs, and risks to customer trust.

To address this, I designed a Fraud Detection and Risk Analysis framework that consolidated 7,000+ claims into one system, applied fraud scoring (0–100), and built interactive dashboards for real-time monitoring. The solution flagged 471 high-risk claims worth £8.84M, prioritized investigation by claim type, region, customer, and agent, and provided analysts with actionable intelligence.

The next steps include deploying the scoring model at claim submission, strengthening customer onboarding checks, and transitioning to machine learning models for more advanced detection.

This project demonstrates how data-driven fraud analytics can reduce losses, improve operational efficiency, and protect the reputation of an insurance company.

## Business Problem
As a mid-sized UK insurance company, Veritas Assurance Ltd has seen a **14% increase in suspicious claims over the past two years.** Fraud was often detected only after payouts had been made, leading to direct financial losses that could not be recovered.

The company’s ability to detect and respond was limited by three main issues. First, claims data was stored in separate systems for policies, payments, and investigations, which meant analysts had to manually piece together information and often missed important connections. Second, there was no real-time monitoring, so fraud checks only took place after claims were processed, allowing fraudulent payouts to slip through. Finally, analysts had no tools to prioritize the riskiest claims, so time and resources were spread thin across all cases instead of being focused where they were most needed.

These weaknesses increased costs, created compliance risks, and began to erode customer trust. To address them, Verita needed a unified system that could bring all claims data into one view, flag suspicious activity immediately, and guide analysts toward the cases most likely to involve fraud.

## My Aproach
1. The dataset used for this project contained about 7,000 insurance claims, with details on customers, policies, claim amounts, and fraud risk indicators. Before moving into analysis, the dataset had to be cleaned and structured to ensure accuracy:
   
- Duplicate claims were removed to avoid double counting.
- Formats were standardized for claim dates, amounts, and IDs to make the data consistent.
- Existing fraud flags (Duplicate, High Value, Weekend Submission) were verified to confirm they were correct.
The dataset was connected to a live source so it could refresh weekly, ensuring the dashboards always reflected the latest claims.

2.  Defining Fraud Indicators
To detect fraud, I focused on specific risk signals:

- Duplicate claims (the same event submitted more than once).
- Claims with unusually high amounts.
- Claims submitted on weekends (timing anomalies).
  
3. Fraud Risk Scoring (Credit-Style System)
Instead of viewing these indicators separately, I combined them into a Fraud Risk Score. This score works much like a credit score: the higher the score, the higher the likelihood of fraud.
- Each risk indicator was assigned points (e.g., duplicate = 30 points, high value = 25 points, weekend submission = 15 points).
- The total points gave each claim a Fraud Risk Score between 0 and 100.
- Based on this score, claims were categorized:
  a. High Risk (≥70)
  b. Medium Risk (40–69)
  c. Low Risk (<40)
- I also rolled up scores at the customer level so repeat offenders could be flagged.
This scoring framework made investigations more proactive and consistent. Analysts no longer had to guess which claim to prioritize — the system told them.

4. Dashboard Development
I built two interactive dashboards to present the findings clearly:
