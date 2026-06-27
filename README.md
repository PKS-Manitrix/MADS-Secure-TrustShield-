# MADS-Secure-TrustShield
A Privacy-First Adaptive Identity Trust Framework for Digital Banking

# Overview
MADS-Secure-TrustShield is a privacy-first, adaptive identity trust framework designed to enhance security across digital banking channels.
Traditional banking systems primarily rely on passwords and frequent OTP verification. However, passwords can be stolen, phishing attacks are increasing, and excessive OTP requests create a poor user experience.
Our solution introduces an intelligent **Identity Trust Engine** that continuously evaluates the trustworthiness of users and dynamically adapts authentication based on risk.

Instead of asking:
> "Did the user enter the correct password?"
our system asks:
> "How confident are we that this person is genuinely the account owner?"

# Problem Statement

Digital banking faces several major security challenges:

* Account Takeover (ATO)
* KYC Fraud
* Identity Theft
* Suspicious Account Recovery
* Insider Threats
* Privileged Access Misuse
* Fraudulent Onboarding
* Device and Location Spoofing

Current systems often use static authentication mechanisms that either:

1. Provide insufficient security or
2. Create excessive friction by requesting OTP verification for every login.

A smarter and more adaptive approach is required.


# Our Solution

MADS-Secure-TrustShield acts as an intelligent security layer that can be integrated into any banking application.

The framework continuously analyzes contextual signals and calculates a dynamic risk score for every login and sensitive action.

Based on the calculated risk, the system decides whether to:

* Allow Access
* Request Additional Verification
* Block the Activity
* Alert the User or Administrator

---

# Key Features

### Adaptive Risk-Based Authentication

Authentication requirements change depending on the calculated risk.

### Low Risk

Direct login.

### Medium Risk

OTP verification.

### High Risk

Biometric verification or security questions.

### Critical Risk

Account blocked and security alert generated.

---

## Device Trust Analysis

The system identifies trusted and untrusted devices.

Factors:

* New Device
* Browser Change
* Operating System Change
* Device Fingerprinting

---

## Location and IP Analysis

The system evaluates:

* New City
* New Country
* Impossible Travel Patterns
* Suspicious IP Addresses

---

## Account Takeover Prevention

Even if an attacker knows the correct password, access is denied if contextual signals indicate suspicious behavior.

---

## Suspicious Account Recovery Detection

The system monitors:

* Excessive password reset requests
* Recovery attempts from new devices
* Recovery attempts from unusual locations

---

## KYC and Onboarding Protection

The system simulates:

* Document verification
* Identity verification
* Duplicate account detection
* Suspicious onboarding detection

---

## Insider Threat Detection

The framework monitors employees and administrators to detect:

* Abnormal account access patterns
* Unusual activity volume
* Privileged access misuse

---

## Role-Based Access Control (RBAC)

The system supports three user roles:

### Customer

* View account
* Perform transactions
* Manage profile

### Employee

* View customer accounts
* Process service requests

### Administrator

* System management
* Security monitoring
* User management

Every role can access only the resources they are authorized to use.

---

# AI-Assisted Risk Analysis

In addition to predefined risk rules, MADS-Secure-TrustShield incorporates Artificial Intelligence to improve fraud detection and continuously learn from user behavior.

The AI module analyzes patterns such as:

* Frequently used devices
* Typical login locations
* Login timings
* Transaction patterns
* Account recovery behavior
* Employee access patterns

Over time, the model learns what constitutes "normal" behavior for each user and detects anomalies that may indicate fraud or account compromise.

### Example

A customer usually:

* Logs in from Salem using an Android device between 8 PM and 10 PM.

Suddenly:

* A login attempt occurs from another country at 3 AM using an unknown laptop.

Although the password is correct, the AI model identifies this as abnormal behavior, increases the risk score, and triggers additional verification or blocks the login attempt.

The AI component therefore acts as an intelligent assistant to the risk engine, enabling more accurate fraud detection and adaptive authentication while reducing unnecessary verification for genuine users.

--- 

# System Architecture

```text
Customer / Employee / Admin
            │
            ▼
       Login Portal
            │
            ▼
   Identity Trust Engine
            │
 ┌──────────┼──────────┐
 │          │          │
 ▼          ▼          ▼
Device   Location   Behaviour
Analysis Analysis   Analysis
 │          │          │
 └──────────┼──────────┘
            │
            ▼
      Risk Scoring Engine
            │
            ▼
      Decision Engine
            │
 ┌──────────┼──────────┐
 │          │          │
 ▼          ▼          ▼
Allow      OTP       Block
```

---

# Risk Scoring Engine

Every suspicious activity contributes to the overall risk score.

| Event                             | Risk Score |
| --------------------------------- | ---------- |
| New Device                        | +30        |
| Different City                    | +20        |
| Different Country                 | +50        |
| Multiple Failed Password Attempts | +20        |
| Suspicious Recovery Attempt       | +40        |
| Unusual Login Time                | +15        |
| Excessive Employee Access         | +60        |

---

# Authentication Decisions

| Risk Score | Decision                |
| ---------- | ----------------------- |
| 0 - 30     | Allow Login             |
| 31 - 60    | OTP Verification        |
| 61 - 80    | Additional Verification |
| 81 - 100   | Block Access            |

---

# Example Scenarios

---

## Scenario 1 – Genuine Customer Login

```text
Device: Samsung S24
Location: Salem
Browser: Chrome
Password: Correct
```

Risk Score: 10

Decision:

✅ Allow Login

---

## Scenario 2 – New Device Login

```text
Device: New Laptop
Location: Salem
Password: Correct
```

Risk Score: 40

Decision:

📱 OTP Verification Required

---

## Scenario 3 – Possible Account Takeover

```text
Device: Unknown
Location: Russia
Password: Correct
```

Risk Score: 90

Decision:

🚨 Block Login and Generate Alert

---

## Scenario 4 – Suspicious Account Recovery

```text
Forgot Password Requests: 5
Device: New
Location: Different Country
```

Risk Score: 85

Decision:

🚨 Lock Recovery Process and Alert User

---

## Scenario 5 – Insider Threat

```text
Employee accesses 500 accounts in one day.
```

Risk Score: 95

Decision:

🚨 Generate Insider Threat Alert

---

# Privacy-First Design

Our framework follows privacy-first principles:

* Collect only essential metadata.
* Encrypt sensitive information.
* Avoid storing unnecessary personal data.
* Trigger additional verification only when risk is elevated.

---

# Technology Stack

## Frontend

* HTML
* CSS
* JavaScript

## Backend

* Python (Flask)

## Database

* SQLite

## Dashboard

* Chart.js

---

# Future Enhancements

* Machine Learning-Based Risk Prediction
* Behavioral Biometrics
* Face Verification
* Device Reputation System
* Continuous Session Monitoring
* Advanced Fraud Analytics
* Real Banking API Integration

---

# Why MADS-Secure-TrustShield?

✅ Prevents Account Takeover

✅ Reduces Fraud

✅ Improves User Experience

✅ Enables Adaptive Authentication

✅ Supports Customers, Employees, and Administrators

✅ Provides Secure and Friction-Optimized Digital Banking 

##
