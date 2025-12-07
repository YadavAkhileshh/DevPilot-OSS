# DevPilot OSS

![VS Code](https://img.shields.io/badge/VS%20Code-Extension-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)
![AWS-Bedrock](https://img.shields.io/badge/AWS-Bedrock-orange)
![Status](https://img.shields.io/badge/status-MVP%20Ready-brightgreen)

DevPilot OSS is an AI-powered VS Code extension that helps first-time open-source contributors get started with clear, step-by-step, context-aware guidance.

Many students want to join open source (GSSoC, Hacktoberfest, classroom projects), but they often struggle because:
- Issues are vague  
- Large codebases feel overwhelming  
- Reviews and contributor expectations feel intimidating  

DevPilot does not write code for you. It helps you understand the project, learn existing patterns, and submit your first PR with confidence.

---

## How It Works

1. Install the extension. It is free and open source.  
2. Run **DevPilot: Find My First Issue**.  
3. Enter any public GitHub repository (for example `github.com/xyz/project`).  
4. DevPilot opens a guided panel inside VS Code with:
   - **Context**  
     *This project uses React and Firebase, similar to your past work.*
   - **Step-by-step guidance**  
     ```js
     // Step 1: Add theme state (follows the pattern in utils/auth.js)
     const [theme, setTheme] = useState('light');
     ```
   - **Testing instructions**  
     *Open DevTools, toggle theme, and check class update.*
5. Click **Clone Repo**, work locally, and submit your PR.

No login required. No extra setup. Works on any public GitHub repository.

---

## Installation

1. Open VS Code.  
2. Go to the Extensions panel.  
3. Search for **DevPilot OSS**.  
4. Click **Install**.  
5. Open the Command Palette (`Ctrl + Shift + P` or `Cmd + Shift + P`).  
6. Run **DevPilot: Find My First Issue**.  
7. Enter a public GitHub repository link and follow the guided steps.

---

## Why GenAI Matters

Traditional tutorials cannot provide the context developers need.  
DevPilot offers guidance that is:

- Personalized to your work  
- Aware of the project structure  
- Focused on explaining why, not only what  
- Helpful to maintainers with clear PR descriptions  

This type of support is not possible with static templates.

---

## Tech Stack

- **Extension**: TypeScript with VS Code Webview  
- **Backend**: Node.js running on AWS Lambda  
- **GenAI**: AWS Bedrock using Claude 3 Haiku  
- **Orchestration**: LangChain  
- **Data Source**: GitHub REST API (public repositories only)

The MVP focuses on one simple workflow:  
Find an issue, understand the context, implement the change, and submit a PR.

---

**DevPilot OSS**  
Helping new contributors take their first step into open source, one PR at a time.
