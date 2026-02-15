# Suraksha-Flow System Design

## 1. High-Level Architecture

[POS / UPI Logs]
        ↓
[Data Ingestion Layer]
        ↓
[Feature Engineering Pipeline]
        ↓
[Fraud Detection Model - Amazon SageMaker]
        ↓
[Risk Scoring Engine]
        ↓
[GST Classification Engine]
        ↓
[AI Compliance Generator - Amazon Q]
        ↓
[Dashboard + Alerts]

---

## 2. Technology Stack

### Backend
- Python (FastAPI)
- AWS Lambda
- Amazon S3
- Amazon DynamoDB

### Machine Learning
- Amazon SageMaker
- XGBoost / Isolation Forest
- Feature store for transaction behavior

### Generative AI
- Amazon Q for:
  - Compliance summary
  - Fraud explanation
  - Report drafting

### Frontend
- React / Flutter (Mobile-first)
- Real-time risk dashboard

---

## 3. Fraud Detection Design

### 3.1 Feature Engineering

Features extracted:
- tx_count_last_10min
- avg_tx_amount
- inbound_outbound_ratio
- beneficiary_frequency
- time_gap_between_tx
- device_id_reuse_score

### 3.2 Model Strategy

Phase 1:
- Supervised learning using labeled fraud data.

Phase 2:
- Semi-supervised anomaly detection.

Model Output:
- Fraud Probability (0-1)
- Risk Tier (Low, Medium, High)

---

## 4. Mule Pattern Detection Logic

Graph-based detection:
- Build transaction network.
- Detect:
  - High centrality nodes
  - Funnel patterns
  - Circular flows

Optional: Integration with Amazon Neptune for graph analytics.

---

## 5. GST Engine Design

Step 1: Categorize transaction
Step 2: Assign GST slab (5%, 12%, 18%, 28%)
Step 3: Compute:
  - Output GST
  - Input GST
  - Net payable
Step 4: Generate monthly report

---

## 6. AI Compliance Generator

Input:
- Structured financial summary
- Flagged suspicious transactions

Amazon Q generates:
- Human-readable explanation
- Compliance summary
- Risk insights

---

## 7. Security & Privacy

- AWS IAM roles
- Encrypted storage (S3 + KMS)
- No PII stored beyond business scope
- Audit logging enabled
