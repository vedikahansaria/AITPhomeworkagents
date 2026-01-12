# 💎 Astra: Self-Optimizing Agentic Travel System

> **A Multi-Agent AI system that learns from user feedback to design hyper-personalized luxury travel itineraries.**

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.9%2B-blue)
![Gradio](https://img.shields.io/badge/gradio-4.0%2B-orange)
![OpenAI/OpenRouter](https://img.shields.io/badge/LLM-OpenRouter-purple)

## 🏗 Architecture

This project moves beyond simple "Chatbots" into **Agentic AI**. It uses a swarm of specialized agents that collaborate to solve the problem, and a feedback loop that permanently improves the system's performance over time.

### The Agent Swarm
1.  **🧠 The Empath (Sentiment Agent):** Analyzes the hidden emotional subtext of a user's request (e.g., detects "Burnout" vs. "Celebration") to set the strategic tone.
2.  **📝 The Architect (Planner Agent):** The core reasoning engine that designs the itinerary. It reads a **Dynamic System Prompt** that evolves based on past failures.
3.  **💰 The Broker (Pricing Agent):** A tool-use agent that scans the text for entities (hotels) and injects mock real-time pricing data.

### The Optimization Loop


1.  **User Feedback:** Users rate itineraries ("Upvote/Downvote") and provide critiques.
2.  **Memory Store:** Feedback is saved to `agent_memory.json`.
3.  **Batch Optimization:** The `batch_optimizer.py` script analyzes this data and rewrites the `prompts/strategist.txt` file, effectively "patching" the AI's behavior without changing code.

---

## 🚀 Installation & Setup

### 1. Prerequisites
- Python 3.8+
- An API Key from [OpenRouter](https://openrouter.ai/) (Access to Claude 3.5 Sonnet, GPT-4o, etc.)

### 2. Clone & Install
```bash
git clone [https://github.com/yourusername/astra-agent.git](https://github.com/yourusername/astra-agent.git)
cd astra-agent
pip install -r requirements.txt
