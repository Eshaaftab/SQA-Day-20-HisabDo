# SQA-Day-20-HisabDo
# HisabDo Mobile User Flow Testing

## 📱 Project Overview

This repository contains the **Manual Mobile User Flow Testing Report** for the **HisabDo Mobile Application**.

The purpose of this testing activity was to validate complete end-to-end user journeys and verify that users can move between different application modules without unnecessary interruption, incorrect navigation, data loss, or blocked functionality.

**Project:** HisabDo Mobile Application
**Testing Type:** Manual Mobile User Flow Testing
**Tester:** Esha Tur Razia – SQA Intern
**Testing Date:** 29 August 2026

---

## 🎯 Testing Objectives

The main objectives of this testing activity were:

* Validate complete user journeys from entry point to final outcome.
* Verify navigation between dependent screens.
* Verify that data entered in one step is correctly reflected in subsequent steps.
* Identify broken or interrupted user journeys.
* Validate authentication and account-related flows.
* Verify transaction, customer, reporting, PDF and analytics journeys.
* Verify offline data handling and data persistence.
* Provide clear Pass/Fail results for further development and regression testing.

---

## 🔍 Testing Scope

The following areas were covered:

* Application Launch
* Guest Mode
* Account Registration
* Login
* Forgot Password
* Logout
* Re-login
* Income Transactions
* Expense Transactions
* Receivable Transactions
* Payable Transactions
* Customer Management
* Reports
* Invoice PDF
* Analytics
* Settings
* Offline Usage
* Data Persistence
* Cross-Module Navigation

---

## 📊 Test Execution Summary

| Metric           |    Result |
| ---------------- | --------: |
| Total Test Cases |        20 |
| Passed           |        18 |
| Failed           |         2 |
| Pass Rate        |       90% |
| Testing Status   | Completed |

---

## 🧪 Testing Results

### Passed Flows

18 out of 20 user-flow test cases passed successfully.

The following major journeys were successfully validated:

* New User Registration
* Login
* Guest Mode
* Income Transaction
* Expense Transaction
* Receivable
* Payable
* Customer Management
* Reports
* Invoice PDF
* Analytics
* Logout
* Re-login
* Settings Persistence
* Offline Transaction
* Data Persistence
* Cross-Module Navigation
* Transaction-to-PDF Journey

---

## 🐞 Failed User Flows

### UF-004 – Guest → Create Account

**Issue:** Create Account shortcut from Guest Mode does not open the Create Account screen directly.

**Steps to Reproduce:**

1. Open the application.
2. Select Guest Mode.
3. Select Create Account.

**Expected Result:**
Create Account page should open directly.

**Actual Result:**
Welcome/Main screen opens first.

**Priority:** Medium
**Status:** Open

---

### UF-013 – Forgot Password

**Issue:** Password recovery journey does not complete.

**Steps to Reproduce:**

1. Open Login screen.
2. Select Forgot Password.
3. Enter email.
4. Select Reset.

**Expected Result:**
Password recovery should complete successfully.

**Actual Result:**
Recovery flow did not proceed.

**Priority:** High
**Status:** Open

---

## ⚠️ Risk & Impact

### UF-004 – Guest → Create Account

The unexpected intermediate screen creates navigation friction and may confuse users by adding an unnecessary step to the registration journey.

### UF-013 – Forgot Password

The failed password recovery flow can prevent users from regaining access to their accounts, making this a higher-impact issue.

---

## 💡 Recommendations

* Route **Guest Mode → Create Account** directly to the registration screen if this is the intended user journey.
* Review the Forgot Password endpoint, redirect and mobile implementation.
* Retest both failed flows after fixes.
* Perform regression testing on Login, Registration, Logout and account recovery.
* Verify that transaction data remains consistent across Dashboard, Reports, Analytics and PDF.
* Perform final closure verification after successful retesting.

---

## 🔄 Regression User Flows

The following flows are recommended for regression testing:

```text
New User → Registration → Account Created → Login → Dashboard

Guest User → Guest Mode → Create Account → Registration

Login → Dashboard → Add Income → Dashboard/Reports/Analytics

Login → Dashboard → Add Expense → Dashboard/Reports/Analytics

Customer → Add → Search → Edit → Delete

Transaction → Invoice PDF → Verify Customer and Amount

Login → Forgot Password → Reset → Login Again

Login → Logout → Re-login

Change Settings → Close App → Reopen → Verify Persistence

Offline → Add Transaction → Reopen → Verify Saved Data
```

---

## 📈 Overall Assessment

The testing achieved an overall **90% pass rate**, with **18 of 20 end-to-end user journeys passing successfully**.

Most core application journeys are functioning correctly. However, two flows require attention:

1. Guest Mode → Create Account
2. Forgot Password

The recommended next step is:

**Fix → Retest → Regression Testing → Closure Verification**

---

## 📁 Repository Contents

```text
HisabDo-Mobile-User-Flow-Testing/
│
├── README.md
│
└── HisabDo_Mobile_User_Flow_Testing_Report.docx
```

---

## 👩‍💻 Tester

**Esha Tur Razia**
SQA Intern

**Project:** HisabDo Mobile Application
**Testing:** Manual Mobile User Flow Testing
**Date:** 29 August 2026
