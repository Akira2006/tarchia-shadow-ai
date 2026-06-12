# 🛡️ TARCHIA: Shadow AI Guardian

Enterprise AI Security Agent powered by Google Gemini and Vertex AI Agent Builder.

## What is TARCHIA?

TARCHIA is an AI-powered security agent designed to detect Shadow AI usage inside organizations. It monitors employee interactions with AI tools, identifies sensitive data exposure risks, assigns risk scores, and recommends security actions before data leaks occur.

The system helps organizations maintain AI governance by detecting unauthorized AI usage, monitoring sensitive information transfers, and learning from manager feedback to continuously improve future risk assessments.

---

## Features

👁️ Real-time monitoring of employee-to-AI interactions

📊 Dynamic risk scoring (0–100) based on sensitivity and policy violations

🛑 Automated blocking of critical data leak attempts

🧠 Behavioral anomaly detection for suspicious usage patterns

🔄 Continuous learning from manager decisions and feedback

📋 Security recommendations including Allow, Warn, Block, and Escalate actions

---

## Built With

* Google Vertex AI Agent Builder
* Google Gemini
* Google ADK (Agent Development Kit)
* Google Cloud Logging
* Google BigQuery

---

## How It Works

TARCHIA analyzes employee AI tool activity and evaluates each interaction against enterprise security policies.

The agent:

1. Identifies whether an AI tool is approved or unauthorized.
2. Detects sensitive information such as credentials, API keys, customer records, internal documents, and database queries.
3. Calculates a risk score based on severity and context.
4. Recommends an action (Allow, Warn, Block, Escalate).
5. Generates alerts for managers when necessary.
6. Learns from manager decisions to improve future risk detection.

---

## Example Scenario

### Input

Employee: [bumblebee@company.com](mailto:bumblebee@company.com)

AI Tool: ChatGPT (Free)

Data:

```sql
SELECT * FROM customers WHERE credit_card > 0;
```

### Output

```text
Risk Score: 85/100

Action: BLOCK

Reason:
Potential PCI-DSS compliance violation involving customer payment information.
```

---

## Security Test Cases

| Scenario                       | Risk Score | Action             |
| ------------------------------ | ---------- | ------------------ |
| ChatGPT + Credit Card Data     | 85/100     | BLOCK              |
| Claude + API Keys              | 95/100     | BLOCK              |
| Approved Tool + Safe Data      | 20/100     | ALLOW              |
| Database Dumps + Unapproved AI | 98/100     | LOCK ACCOUNT       |
| Tool-Hopping Behavior          | 92/100     | FLAG               |
| Obfuscation Detection          | 91/100     | BLOCK              |
| Volume Anomalies               | 85/100     | RATE LIMIT         |
| Approved Tool + Passwords      | 88/100     | BLOCK              |
| Public Source Code + Free AI   | 15/100     | ALLOW WITH WARNING |

---

## Architecture

### Google Vertex AI Agent Builder

Core orchestration and reasoning engine.

### Google Gemini

Semantic analysis, context understanding, and risk assessment.

### Google Cloud Logging

Real-time event monitoring and audit trail generation.

### Google BigQuery

Storage and analysis of security events and behavioral patterns.

---

## Demo

TARCHIA is deployed using Google Vertex AI Agent Builder.

A complete demonstration of the system, including all workflows, security scenarios, and risk analysis examples, is available through the project submission video.

---

## Project Goal

Organizations are rapidly adopting AI tools, but many employees use unapproved AI services without security oversight. This creates significant risks involving data leakage, compliance violations, and intellectual property exposure.

TARCHIA addresses this challenge by providing automated AI governance and security monitoring while remaining adaptable through continuous learning.

---

## Future Enhancements

* SIEM integration
* Enterprise identity integration (SSO)
* Department-specific security policies
* Real-time compliance reporting
* Expanded anomaly detection capabilities

---

## License

MIT License

---

## Author

Akiranandhan Reddy Jaklapally

GitHub Repository:

https://github.com/Akira2006/tarchia-shadow-ai
