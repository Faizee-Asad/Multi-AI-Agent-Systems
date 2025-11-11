# 🚀 CrewAI BlogForge
> An AI-powered multi-agent content generation system that plans, writes, and edits SEO-optimized blog posts using OpenRouter API.

---

## 🧩 Overview

**CrewAI BlogForge** is a multi-agent workflow built using [CrewAI](https://github.com/joaomdmoura/crewAI) where three intelligent agents — **Planner**, **Writer**, and **Editor** — collaborate to produce a polished, publication-ready blog article.

Each agent performs a specific task:
1. **🧭 Planner:** Researches the topic, identifies key trends, outlines structure, and suggests SEO keywords.
2. **✍️ Writer:** Expands the plan into a full-length, engaging article with logical flow and tone.
3. **🧹 Editor:** Refines the content for style, grammar, tone, and brand consistency.

The system uses **OpenRouter API** for LLM access, enabling you to run it with multiple AI models such as GPT-4, Claude, or Mistral.

---

## ⚙️ Features

- 🧠 Multi-agent coordination with role-based workflows  
- 🌐 Uses OpenRouter API (cheaper and flexible than OpenAI)  
- ✍️ Auto-generates SEO-friendly, well-structured blog posts  
- 🪶 Outputs Markdown format ready for blog publication  
- 💡 Extensible design – add more agents or modify tasks easily  

---

## 🧠 Architecture

+-------------------+
| Content Planner |
+-------------------+
↓
+-------------------+
| Content Writer |
+-------------------+
↓
+-------------------+
| Editor |
+-------------------+


Each agent runs through a `Crew` pipeline, performing its task in sequence.

---

## 🧰 Installation (Google Colab or Local)

### 1️⃣ Clone the repository
```bash
git clone https://github.com/Faizee-Asad/Multi-AI-Agent-Systems.git
cd Multi-AI-Agent-Systems/CrewAI-BlogForge
