# Fraud-Detection-Capital-One-
# Graph-Based Financial Fraud Detection System

## 📌 Overview

The **Graph-Based Financial Fraud Detection System** is a cybersecurity and financial technology project designed to identify potentially fraudulent activity by analyzing relationships between customers, accounts, devices, merchants, and transactions.

Instead of looking at transactions individually, this project represents financial activity as a **network of connected entities**. This makes it possible to identify unusual relationships and patterns that may not be obvious when looking at a single transaction.

This project was created to explore the intersection of **Computer Science, Cybersecurity, Artificial Intelligence, and Finance**.

---

## 🎯 Project Goals

The main goals of this project are to:

* Detect potentially fraudulent financial activity
* Analyze relationships between financial entities
* Assign risk scores to transactions and accounts
* Identify unusual patterns and suspicious connections
* Provide an easy-to-understand investigation dashboard
* Demonstrate secure software development practices
* Explore how machine learning can support fraud detection

---

## 💡 Why a Graph?

Traditional fraud detection systems may examine transactions one at a time.

This project takes a different approach by representing financial activity as a graph.

For example:

```text
Customer
   ↓
Account
   ↓
Transaction
   ↓
Merchant
   ↓
Device
```

A graph-based approach can help identify patterns such as multiple accounts being connected to the same device or unusual relationships between accounts and transactions.

The goal is not to automatically label someone as fraudulent. Instead, the system provides a **risk score and supporting information** that could help a security or fraud analyst investigate further.

---

## 🧩 Key Features

### Transaction Analysis

The system analyzes simulated financial transactions and looks for unusual activity based on factors such as:

* Transaction amount
* Transaction frequency
* Location
* Device
* Merchant
* Account activity
* Time of transaction

### 🔗 Relationship Analysis

Financial entities are represented as connected nodes.

Example:

```text
Customer A
   │
   ├── Account 1
   │      │
   │      ├── Device X
   │      └── Transaction 101
   │
   └── Account 2
          │
          ├── Device X
          └── Transaction 205
```

The system can identify relationships that may deserve additional investigation.

### 🤖 Fraud Risk Scoring

Each transaction receives a risk score based on multiple factors.

Example:

```text
Transaction ID: 10245

Risk Score: 87/100

Risk Factors:
✓ Unusual transaction amount
✓ New device
✓ Unusual location
✓ High transaction frequency
```

### 📊 Investigation Dashboard

The dashboard allows users to view:

* High-risk transactions
* Suspicious accounts
* Connected devices
* Merchant activity
* Risk scores
* Fraud patterns
* Investigation history

### 🔐 Security Features

The project incorporates security principles such as:

* User authentication
* Role-based access
* Password hashing
* Secure API endpoints
* Input validation
* Audit logging
* Protection of sensitive data

---

## 🏗️ System Architecture

```text
                ┌──────────────────┐
                │  Transaction Data │
                └────────┬─────────┘
                         ↓
                ┌──────────────────┐
                │ Data Processing  │
                └────────┬─────────┘
                         ↓
                ┌──────────────────┐
                │ Graph Construction│
                └────────┬─────────┘
                         ↓
                ┌──────────────────┐
                │ Fraud Detection  │
                │   / ML Model     │
                └────────┬─────────┘
                         ↓
                ┌──────────────────┐
                │   Risk Scoring   │
                └────────┬─────────┘
                         ↓
                ┌──────────────────┐
                │ Investigation    │
                │    Dashboard     │
                └──────────────────┘
```

---

## 🛠️ Technologies

### Programming Languages

* Python
* SQL
* JavaScript / TypeScript

### Backend

* FastAPI
* Python
* REST APIs

### Database

* PostgreSQL

### Machine Learning

* scikit-learn
* Pandas
* NumPy

### Graph Analysis

* NetworkX

### Frontend

* React
* JavaScript / TypeScript

### Development & Deployment

* Git
* GitHub
* Docker
* AWS

---

## 📂 Project Structure

```text
financial-fraud-detection/
│
├── backend/
│   ├── api/
│   ├── models/
│   ├── services/
│   └── main.py
│
├── frontend/
│   ├── components/
│   ├── pages/
│   └── App.jsx
│
├── data/
│   ├── transactions.csv
│   ├── customers.csv
│   └── accounts.csv
│
├── ml/
│   ├── preprocessing.py
│   ├── train_model.py
│   └── fraud_model.py
│
├── graph/
│   ├── build_graph.py
│   └── analyze_graph.py
│
├── tests/
│
├── requirements.txt
├── Dockerfile
└── README.md
```

---

## 📊 Dataset

This project uses **synthetic financial data** created for educational purposes.

The dataset may contain:

* Customer IDs
* Account IDs
* Transaction IDs
* Merchant IDs
* Device IDs
* Transaction amounts
* Locations
* Timestamps
* Transaction types
* Fraud labels

No real customer financial information is used.

---

## 🔍 Fraud Detection Approach

The system combines multiple signals instead of relying on one rule.

A simplified risk model could consider:

```text
Risk Score =
    Transaction Risk
  + Account Risk
  + Device Risk
  + Location Risk
  + Network Risk
```

Machine learning can then be used to identify patterns associated with previously labeled fraudulent transactions.

The graph component adds another layer by analyzing relationships between entities.

---

## 🧪 Example Scenario

Suppose three different accounts perform transactions using the same device within a short period.

The system could identify:

```text
Account A ──┐
Account B ──┼── Device X
Account C ──┘
```

Individually, each transaction may not appear highly suspicious.

However, the relationship between the accounts and device could increase the overall risk score and cause the activity to be sent for investigation.

---

## 📈 Future Improvements

Potential future versions of this project could include:

* Real-time transaction monitoring
* More advanced graph neural networks
* Real-time alerts
* AWS cloud deployment
* Explainable AI
* Automated investigation reports
* More sophisticated anomaly detection
* Model performance monitoring
* Threat intelligence integration
* Mobile dashboard
* Role-specific analyst views

---

## 🔐 Ethical Considerations

This project is intended for **educational and research purposes**.

The system should not automatically determine that a person is committing fraud based solely on an algorithmic score.

A high-risk score should be treated as a signal for additional investigation rather than proof of fraudulent behavior.

The project also uses synthetic data to avoid exposing real financial information.

---

## 🎓 Skills Demonstrated

This project demonstrates experience with:

* Computer Science
* Cybersecurity
* Financial Technology
* Machine Learning
* Data Structures
* Graph Theory
* Data Analysis
* Database Design
* API Development
* Full-Stack Development
* Secure Software Development
* Cloud Computing
* Risk Analysis

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/financial-fraud-detection.git
```

### 2. Navigate to the project

```bash
cd financial-fraud-detection
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**Mac/Linux**

```bash
source venv/bin/activate
```

**Windows**

```bash
venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Start the application

```bash
python backend/main.py
```

---

## 📌 Project Status

**Status:** 🚧 In Development

Current focus:

* [ ] Generate synthetic financial dataset
* [ ] Build transaction database
* [ ] Create financial entity graph
* [ ] Implement fraud-risk scoring
* [ ] Train machine learning model
* [ ] Build REST API
* [ ] Create investigation dashboard
* [ ] Add authentication
* [ ] Add audit logging
* [ ] Add automated testing
* [ ] Deploy application

---

## 👩🏾‍💻 About the Project

This project was created as part of my development as a **Computer Science student interested in Cybersecurity and Finance**.

My goal is to explore how software, data, and cybersecurity can be used to make financial systems more secure and intelligent.

**Built with:** Python • SQL • Machine Learning • Graph Analysis • React • PostgreSQL • Docker
