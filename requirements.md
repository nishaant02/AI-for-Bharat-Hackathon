# Suraksha-Flow
AI-Powered Fraud Detection & GST Compliance Auditor for Small Businesses

## 1. Problem Statement

Small retail businesses in India face:

1. Increasing digital payment fraud (UPI mule accounts, rapid fund cycling, synthetic identities).
2. Complex GST compliance and reconciliation.
3. Lack of affordable AI-driven financial monitoring tools.

There is no unified system that:
- Monitors transaction logs in real-time.
- Detects mule account patterns.
- Automatically generates simplified GST compliance summaries.

## 2. Objective

Build an AI Auditor that:

- Detects suspicious transaction patterns in real time.
- Flags potential mule accounts using machine learning.
- Generates GST-compliant summaries and reports automatically.
- Provides simple insights for non-technical shop owners.

## 3. Target Users

- Kirana store owners
- Small wholesalers
- Local retailers
- Micro e-commerce sellers
- Service-based SMEs

## 4. Functional Requirements

### 4.1 Transaction Monitoring
- Ingest transaction logs (CSV/API/UPI logs).
- Extract behavioral features:
  - Transaction frequency
  - Amount velocity
  - Account linkage
  - Time-based anomalies
- Generate fraud probability score.

### 4.2 Mule Account Detection
System should detect:
- Rapid in-out fund cycling
- Multiple inbound micro-transactions
- Common beneficiary endpoints
- Dormant account sudden activation

### 4.3 Real-Time Alerts
- High-risk alerts via dashboard.
- Optional WhatsApp/SMS notification.
- Risk severity classification (Low/Medium/High).

### 4.4 GST Compliance Engine
- Auto-categorize transactions into GST slabs.
- Calculate:
  - Total revenue
  - Output GST
  - Estimated Input Tax Credit
- Generate monthly compliance summary.

### 4.5 AI Report Generation
- Plain-language financial summary.
- Fraud explanation report.
- Downloadable PDF compliance document.

## 5. Non-Functional Requirements

- Scalable to 1M+ SMEs.
- Secure (AWS IAM, encryption at rest).
- Model explainability.
- Low latency (< 2 seconds inference).
- Mobile-friendly UI.

## 6. Success Metrics

- Fraud detection precision > 85%
- False positive rate < 10%
- GST reconciliation accuracy > 95%
- Report generation time < 10 seconds
