# Tic Tac Toe vs AI (LLM-Assisted Timed Task)

## 📌 Overview
This project is a **Tic Tac Toe game with an AI opponent**, created as part of a **time-bound task (20 minutes)**.  
The primary goal was **not UI polish**, but to understand how **Large Language Models (LLMs)** can assist in rapid development and how developers can **analyze, validate, and explain AI-generated logic**.

At the time of this task, I was also **learning a Prompt Engineering course**, and this project was intentionally used to:
- Experiment with **how LLMs respond based on how questions are framed**
- Observe how outputs change when constraints are added
- Improve my ability to ask **clear, structured technical prompts**

---

## ⏱️ Task Context
- **Time limit:** 20 minutes  
- **Objective:**
  - Build a playable Tic Tac Toe game
  - Add an AI opponent
  - Ask an LLM to explain the AI logic
  - Refine prompts to improve both the game and the explanations

This simulates a real-world scenario where developers must:
- Deliver functionality quickly
- Use AI tools effectively
- Still fully understand and justify the generated output

---

## 🧪 Prompt Engineering Process (Iteration Matters)

Since I’m learning Prompt Engineering, I treated this task as an experiment in **how AI output changes depending on how we ask**.

### Step 1 — Initial Prompt (Too broad)
I first asked:
> “Create a Tic Tac Toe game with an AI opponent.”

**What I got:**
- A basic instant-play game
- No start/stop flow
- No difficulty levels
- No score tracking
- AI behavior that felt either random or unbeatable
- Limited control over user experience

**Learning:**  
Broad prompts usually give fast but minimal results.

---

### Step 2 — Ask for Rules & Strategies
Next, I asked the LLM:
- “What are the rules of Tic Tac Toe?”
- “What strategies does an AI use and why?”

**What I got:**
- A structured list of rules
- Clear strategic concepts (center control, blocking wins, forks, optimal play)

**Learning:**  
Understanding rules and constraints first helps guide better prompts and better code.

---

### Step 3 — Refined Prompt (Constraints + Features)
Then I asked the LLM to **use those rules and strategies** and build a better version:

> “Based on the rules and strategies you listed, create a Tic Tac Toe game with:
> - score tracking,
> - selectable player symbol,
> - difficulty levels,
> - proper game flow,
> - and clearly explained AI logic.”

**Result:**
- A more structured game loop
- Difficulty-based AI behavior
- Clearer explanations that were easier to verify
- A better learning experience overall

---

## 🎮 Game Behavior
- Player symbol: **X**
- AI symbol: **O**
- If the **AI wins or the game draws**, the board automatically resets
- The game **stops only when the human player wins**

This design encourages repeated play to observe and test AI decision-making.

---

## 🧠 AI Opponent — What I Understood

### 1️⃣ Win Detection Logic
- Checks the **8 possible winning combinations**
- Declares a win when all symbols in a line match
- Declares a draw when the board is full and no winner exists
- Used both for:
  - Ending rounds
  - Evaluating simulated future moves

---

### 2️⃣ Simulation Engine — Minimax Algorithm
- Recursively simulates all possible future game states
- Assumes both players play optimally

**Scoring:**
- AI win → `+10`
- Human win → `-10`
- Draw → `0`

**Decision logic:**
- AI maximizes its score
- Human is assumed to minimize it
- Depth scoring (`10 - depth`) prioritizes faster wins and delayed losses

---

### 3️⃣ Difficulty Control
- **Easy:** random moves
- **Medium:** mix of optimal and random moves
- **Hard:** full Minimax evaluation (unbeatable with perfect play)

This shows how the same algorithm can be adapted for different experiences.

---

### 4️⃣ Emergent Strategy
Without hard-coding rules, the AI naturally:
- Prefers the center
- Blocks winning moves
- Creates forks
- Forces draws when necessary

These behaviors emerge from outcome evaluation, not fixed rules.

---

## 📚 Key Learnings
- How prompt phrasing impacts AI responses
- How to validate AI-generated logic
- Practical understanding of Minimax
- Using LLMs as a **learning aid**, not a shortcut

---

## 🤖 Meta Note (Yes, This README Too)
This README was also **AI-assisted**.

Why?
Because while learning Prompt Engineering, I wanted to:
- See how AI structures documentation
- Experiment with tone (professional vs casual)
- Refine explanations iteratively
- I'm more than imopressed after the way this LLM is explaining things.

In short:
> I used AI to explain how I used AI to learn how AI explains things.

Very on brand for 2026.

---

## 🛠️ Tech Stack
- HTML
- CSS
- Vanilla JavaScript
- Deployed using **Replit**

---

## 🌐 Live Demo
👉 https://tic-tac-toe-ai--harshinichowda4.replit.app

---

## 👩‍💻 Author
**Harshini Chowdary Kilari**
