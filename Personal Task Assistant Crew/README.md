# 🧩 Personal Task Assistant Crew (Gemini + Serper)

A **minimal working example** of a **CrewAI-based Personal Task Assistant** that plans and executes structured learning or work goals.  
It combines **Google Gemini 2.5 Flash** for reasoning and **Serper** for real-time web search — all orchestrated using the `crewai` framework.

---

## 🚀 Overview

This notebook demonstrates how to create a two-agent CrewAI workflow for personalized planning:

- **🧠 Planner Agent:**  
  Breaks a goal into ordered, actionable subtasks.
  
- **🧑‍💻 Executor Agent:**  
  Turns those subtasks into a concrete day-by-day schedule with time estimates, study tips, and useful links (via Serper web search).

Example goal:  
> “Plan a study schedule for RHCSA in 10 days.”

---

## ⚙️ Architecture

```
Goal → Planner → Plan → Executor → Final Schedule
```

### Agents
| Agent | Role | Description |
|-------|------|--------------|
| 🧠 **Planner** | Strategic breakdown | Splits a user goal into 6–10 logical subtasks |
| 🧑‍💻 **Executor** | Schedule builder | Converts the plan into a daily schedule using real-time web data |

### Tools Used
- **LLM:** [Google Gemini 2.5 Flash](https://ai.google.dev)
- **Web Search:** [Serper.dev](https://serper.dev)
- **Framework:** [CrewAI](https://pypi.org/project/crewai/)
- **Utilities:** `crewai-tools`, `datetime`, `re`

---

## 🧰 Installation

Run in Google Colab **or locally** with Python 3.10+.

```bash
pip install -qU crewai crewai-tools google-generativeai
```

🔑 API Keys

Set your API keys before running:

import os

os.environ["GOOGLE_API_KEY"] = "YOUR_GOOGLE_API_KEY"  # from https://ai.google.dev
os.environ["SERPER_API_KEY"] = "YOUR_SERPER_API_KEY"  # from https://serper.dev


(Optional) Remove redundant Gemini key warnings:
os.environ.pop("GEMINI_API_KEY", None)

🧠 How It Works

Define your goal
e.g. "Plan a study schedule for RHCSA in 10 days"

Planner Agent
Breaks the goal into subtasks in logical order.

Executor Agent
Uses real-time web search to build a detailed schedule:

One subtask per day

Time estimates

Actionable tips

Helpful resource links

CrewAI Orchestration
The two agents run sequentially to produce the final structured plan.

▶️ Example Usage

result = run_crew("Plan a study schedule for RHCSA in 10 days")

The output is printed as structured Markdown with daily breakdowns, including:

Day and Date

Topics to Cover

Estimated Time

Tip

Useful Links

📂 Project Structure

📁 Personal-Task-Assistant-Crew/
│
├── Personal Task Assistant Crew Agents.ipynb   # Main notebook
├── README.md                                   # Project documentation
└── requirements.txt                            # Optional dependency list

💡 Customization

You can easily adapt the assistant for other goals:

Project planning ("Plan my 5-day sprint for web app MVP")

Skill learning ("Learn Python for data analysis in 7 days")

Certification prep ("AWS Cloud Practitioner in 14 days")

Just modify the goal text — the CrewAI agents handle the rest.

🧾 License

MIT License © 2025 — Open for use, modification, and learning.

🌟 Acknowledgments

CrewAI
 — Multi-agent orchestration framework

Google Gemini
 — Advanced LLM for reasoning

Serper.dev
 — Search API for real-time data

Inspired by practical AI task automation workflows.

Author: [Your Name]
Created: November 2025
Purpose: Demonstrate a minimal, working AI-powered task planning crew.