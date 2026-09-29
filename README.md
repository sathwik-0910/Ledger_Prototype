````markdown
# 🧠 Ledger — AI-Powered Code Review with Organizational Memory

## 🚀 Live Demo

👉 https://ledgerprototype.vercel.app/

## 📌 Overview

Ledger is an AI-powered code review system that brings **organizational memory** into the Pull Request review process.

Instead of reviewing every Pull Request only based on the current code, Ledger remembers:

- 🏢 Global team coding rules
- 👨‍💻 Developer-specific recurring patterns
- 📚 Previous engineering decisions
- 🔍 Historical review feedback

This helps generate more **context-aware and explainable code reviews**.

## 🎯 Problem

Development teams often face repeated issues:

- Important coding rules are forgotten.
- Previous PR decisions are difficult to find.
- Developers may repeat similar mistakes.
- New team members may not know historical engineering decisions.
- Traditional code analysis does not understand team-specific context.

## 💡 Solution

Ledger acts as a **memory layer for code reviews**.

```text
GitHub Pull Request
        ↓
Code Analysis
        ↓
Ledger Memory
        ↓
┌─────────────────────────┐
│ Tier 1: Team Rules      │
│ Tier 2: Developer Habits│
│ Tier 3: Past Decisions   │
└─────────────────────────┘
        ↓
Memory Convergence
        ↓
Review Findings
        ↓
Actionable Feedback
````

## 🧠 Three-Tier Memory

### Tier 1 — Global Team Rules

Stores rules that apply across the development team.

Example:

```text
Payment catch blocks must use
Telemetry.captureException().
```

Ledger can detect when a Pull Request violates an established team rule.

### Tier 2 — Developer Habits

Ledger identifies recurring patterns associated with individual developers.

Example:

```text
Developer: @alex-chen

Recurring patterns:
• console.error inside catch blocks
• HTTP requests without explicit timeouts
```

### Tier 3 — Past Engineering Decisions

Ledger remembers decisions made during previous Pull Requests.

Example:

```text
Third-party integrations should use
a maximum 3000ms timeout.
```

When a new Pull Request introduces a similar issue, Ledger can compare it with the previous decision.

## 🔍 Diff Test Sandbox

Ledger includes a sandbox where developers can test code against stored organizational memory.

Example:

```javascript
try {
    const res = await fetch(
        "https://api.internal.billing/v1/charge"
    );

    const data = await res.json();

    return data;

} catch (e) {
    console.error("Failed charge:", e);
    return null;
}
```

Ledger can identify issues such as:

```text
❌ Team Rule Match
console.error used inside a catch block

❌ Developer Pattern Match
HTTP request without an explicit timeout
```

## 🔄 GitHub Workflow

```text
Developer creates Pull Request
            ↓
       GitHub Actions
            ↓
     Ledger Review Engine
            ↓
       Analyze Changes
            ↓
      Check Ledger Memory
            ↓
      Generate Findings
            ↓
     Actionable Feedback
```

## ✨ Key Features

* 🧠 Organizational memory for code reviews
* 🏢 Global team rules
* 👨‍💻 Developer habit tracking
* 📚 Historical engineering decisions
* 🔍 Context-aware PR analysis
* ⚡ Diff Test Sandbox
* 🔗 GitHub workflow integration
* 📊 Confidence-based findings
* 💬 Explainable review feedback

## 🛠️ Tech Stack

* HTML
* CSS
* JavaScript
* Git
* GitHub
* GitHub Actions
* Vercel

## 🌐 Live Demo

**Ledger:**
[https://ledgerprototype.vercel.app/](https://ledgerprototype.vercel.app/)

## 📂 Project Structure

```text
Ledger_Prototype/
│
├── index.html
└── README.md
```

## 🚀 Getting Started

Clone the repository:

```bash
git clone https://github.com/sathwik-0910/Ledger_Prototype.git
```

Navigate to the project:

```bash
cd Ledger_Prototype
```

Open `index.html` in your browser or use VS Code Live Server.

## 🔮 Future Scope

* Real GitHub App integration
* Automated PR comments
* Vector database for long-term memory
* LLM-powered code explanations
* Support for more programming languages
* Team-level analytics
* Learning from reviewer feedback
* Slack and Microsoft Teams integration
* Advanced developer pattern detection

## 👥 Team

Built as a prototype demonstrating **AI-powered code review with persistent organizational memory**.

## 📜 License

This project is intended for educational, demonstration, and hackathon purposes.

```
```
