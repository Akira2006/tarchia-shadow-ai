# 🛡️ TARCHIA: Shadow AI Guardian

Enterprise AI Security Agent powered by Google Gemini and Vertex AI Agent Builder.

## What is TARCHIA?
TARCHIA is an autonomous security agent, that catches unauthorized AI tool usage, blocks data leaks in real time, and kinda learns from manager decisions so corporate data breaches don’t slip through . It watches patterns , then tweaks its own detection over time.

## Features
- 👁️ Real-time monitoring of employee-to-AI interactions, kind of like a quiet bouncer
- 📊 Risk scoring (0-100) based on data sensitivity, more or less
- 🛑 Instant blocking of critical data leaks, no waiting around
- 🧠 Behavioral anomaly detection, spotting weird stuff not expected
- 🔄 Learning from manager feedback, because humans still steer

## Built With
- Google Vertex AI Agent Builder
- Google Gemini Enterprise
- Google Cloud Logging
- Google BigQuery

## How It Works
TARCHIA intercepts AI tool usage, analyzes the payloads for sensitive data (API keys, databases, credentials) , then it figures out risk scores, and decides whether to block or allow transfers using security policies. Afterwards it keeps learning from manager decisions, so the signal gets cleaner as time goes.

## How to Run

TARCHIA is deployed as a Google Cloud Agent Builder application. To access and test:

### Prerequisites
- Google Cloud Account (free tier available)
- Access to Vertex AI Agent Builder

### Steps
1. Go to `console.cloud.google.com`
2. Navigate to **Agent Platform** → **Studio**
3. Open the **tarchia_shadow_ai** agent
4. Click **"Preview"** to test the agent
5. Add test cases (employee data, tool usage, sensitive information)
6. See TARCHIA analyze, then generate security alerts

### Example Test Case
Employee: bumblebee@company.com
AI Tool: ChatGPT (Free)
Data: SELECT * FROM customers WHERE credit_card > 0

TARCHIA will respond with:
- Risk Score: 85/100
- Action: BLOCK
- Reason: PCI-DSS compliance violation

### Live Demo
You can see the agent doing its thing on the Google Cloud Agent Builder Console, live.

## Test Cases (9 Scenarios)
✅ ChatGPT + Credit Cards (85/100 risk) → BLOCK  
✅ Claude + API Keys (95/100 risk) → BLOCK  
✅ Approved Tools + Safe Data (20/100 risk) → ALLOW  
✅ Dark Web AI + Database Dumps (98/100 risk) → LOCK ACCOUNT  
✅ Tool Hopping Patterns (92/100 risk) → FLAG ESPIONAGE  
✅ Obfuscation Detection (91/100 risk) → BLOCK  
✅ Volume Anomalies (85/100 risk) → RATE LIMIT  
✅ Approved Tool + Passwords (88/100 risk) → BLOCK  
✅ Public Code + Free AI (15/100 risk) → ALLOW WITH WARNING  

## Architecture
- **Agent Builder:** the core multi-step reasoning engine, the brain part
- **Gemini Enterprise:** deep semantic analysis, payload decoding too
- **Cloud Logging:** real-time event tracking, stream vibes
- **BigQuery:** data warehousing for pattern detection, later analysis

## Why TARCHIA Wins
- 🥇 A first mover in the AI-policing-AI category, kind of early and loud
- 🎯 Solves $60B+ unsolved enterprise crisis energy
- 🔐 Deals well with edge cases (obfuscation, tool-hopping, volume anomalies)
- 📈 Gets better by learning from manager decisions
- ☁️ Built on enterprise-grade Google Cloud, not a toy stack

## License
MIT License

## Contact
If you want more information, head to the GitHub repository.
