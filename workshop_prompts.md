---
marp: true
theme: default
paginate: true
backgroundColor: #0F1229
color: #E8E8EC
style: |
  section {
    font-family: 'Calibri', 'Segoe UI', sans-serif;
    font-size: 24px;
    line-height: 1.4;
    padding: 40px 50px;
  }
  h1 {
    color: #FFFFFF;
    font-family: 'Georgia', serif;
    font-size: 1.6em;
    border-bottom: 3px solid #E8873A;
    padding-bottom: 8px;
    margin-bottom: 12px;
  }
  h2 {
    color: #E8873A;
    font-family: 'Georgia', serif;
    font-size: 1.15em;
    margin-top: 4px;
    margin-bottom: 8px;
  }
  code {
    background: #1a1e38;
    color: #E8873A;
    padding: 2px 6px;
    border-radius: 4px;
    font-size: 0.85em;
  }
  pre {
    background: #1a1e38 !important;
    border-left: 4px solid #E76F51;
    padding: 12px 16px !important;
    border-radius: 8px;
    font-size: 0.68em;
    margin: 6px 0;
  }
  pre code {
    background: transparent;
    color: #E8E8EC !important;
  }
  pre code span {
    color: #E8E8EC !important;
  }
  table {
    background: #1a1e38 !important;
    color: #E8E8EC !important;
    border-collapse: collapse !important;
    width: 100%;
    font-size: 0.78em;
  }
  th {
    background: #E76F51 !important;
    color: white !important;
    padding: 6px 12px !important;
    text-align: left;
    border: none !important;
  }
  td {
    padding: 6px 12px !important;
    border-bottom: 1px solid #2a2e48 !important;
    border-top: none !important;
    border-left: none !important;
    border-right: none !important;
    color: #E8E8EC !important;
    background: #1a1e38 !important;
  }
  tr:nth-child(even) td {
    background: #151935 !important;
  }
  .exercise-num {
    display: inline-block;
    background: #E76F51;
    color: white;
    padding: 4px 12px;
    border-radius: 16px;
    font-weight: bold;
    font-size: 0.9em;
  }
  .concept {
    display: inline-block;
    background: #2a5298;
    color: white;
    padding: 4px 12px;
    border-radius: 16px;
    font-weight: bold;
    font-size: 0.9em;
  }
  strong {
    color: #E8873A;
  }
  a {
    color: #E8873A;
  }
  section.title-slide h1 {
    font-size: 2.2em;
    border-bottom: none;
  }
  p, ul, ol {
    margin-top: 4px;
    margin-bottom: 4px;
  }
  li {
    margin-bottom: 3px;
  }
---

<!-- _class: title-slide -->

# What Can Agentic CLI Do?

## GDG x Bulacan State University
**20 February 2026**

Copy-paste ready prompts for every exercise

---

# Setup: Package Managers

You need **one** package manager. Install whichever matches your preference.

## Python: uv

Install: **https://docs.astral.sh/uv/getting-started/installation/**

Verify: `uv --version`

## JavaScript: Bun

Install: **https://bun.sh/**

Verify: `bun --version`

---

# Setup: AI Coding Tools

Install **at least one** of these CLI tools.

| Tool | Install Page |
|------|-------------|
| **Gemini CLI** (primary) | https://github.com/google-gemini/gemini-cli |
| **Claude Code** | https://docs.anthropic.com/en/docs/claude-code |
| **Codex CLI** | https://github.com/openai/codex |

Verify your tool works:

```bash
gemini --version
```

---

# Today's Agenda

| Time | What |
|------|------|
| 3:00 | Setup and verify tools |
| 3:15 | **Ex 1:** Build an app from one sentence |
| 3:40 | **Ex 2:** Turn data into a dashboard |
| 4:05 | Break |
| 4:15 | **Ex 3:** Read code and write docs |
| 4:40 | **Ex 4:** Create your own AI specialist |
| 5:05 | **Ex 5:** AI-powered research report |
| 5:30 | Break and hackathon team formation |
| 6:00 | **Hackathon** (75 min) |
| 7:15 | **Demos** |
| 7:45 | Wrap-up |

---

# <span class="concept">Concept</span> What Is Agentic CLI?

## It is not a chatbot. It is a builder.

A **chatbot** answers questions. You type, it replies, you copy-paste.

An **agentic CLI tool** does work. It can:

- **Create files** on your computer
- **Run code** and check if it works
- **Install packages** it needs
- **Fix its own mistakes** and try again
- **Build entire projects** from a description

You describe what you want. It builds it. That is the difference.

---

# <span class="exercise-num">1</span> App From a Sentence

## Describe a problem. Get working software.

```bash
gemini "Build a sari-sari store POS system.
Store owners track inventory, record sales,
and see what is selling best. Simple enough
for a tindahan owner who uses Facebook but
has never touched Excel.
Web app with Python."
```

**Run it.** Wait for it to finish (1-3 minutes).

Then open the app in your browser.

---

# <span class="exercise-num">1</span> Discussion

## How close is this to real?

- Would a store owner in Malolos actually use this?
- What is missing?
- What did the AI assume that you did not ask for?

**Bonus:** Try changing one thing in your prompt and run it again. How does the output change?

---

# <span class="concept">Concept</span> Data In, Insights Out

## The CLI can analyze data, not just write code

Most people use spreadsheets. But what if you could just say:

**"Here is my data. Show me what is interesting."**

The CLI will:
- Read your data file (CSV, JSON, Excel)
- Write analysis code automatically
- Generate charts and visualizations
- Export everything as files you can open

No pandas. No matplotlib. No setup. Just **one prompt**.

---

# <span class="exercise-num">2</span> Data to Dashboard

## Step 1: Download sample data

```bash
curl -O https://raw.githubusercontent.com/realmindsai/bulsu_tutorial_2026/main/sari_sari_sales.csv
```

## Step 2: Analyze it

```bash
gemini "Analyze this sari-sari store sales data.
Create a bar chart of top selling products,
a line chart of daily revenue trend,
and a profit margin analysis by category.
Export as an HTML dashboard.
Use peso sign for currency." < sari_sari_sales.csv
```

---

# <span class="exercise-num">2</span> Discussion

## Open the HTML file in your browser

- Could you hand this dashboard to a store owner?
- What insights did the AI find that you did not ask for?
- What would you add to make it more useful?

**Bonus:** Ask the AI to add a "products to restock" alert section.

---

# <span class="concept">Concept</span> AI Can Read, Not Just Write

## Point it at existing code. It understands.

Most people think AI only **generates** code. But it can also:

- **Read** a project and explain what it does
- **Find bugs** the original developer missed
- **Generate documentation** (README, API docs, diagrams)
- **Suggest improvements** with explanations

This works with code you did not write. Code in languages you do not know. Code with zero comments.

---

# <span class="exercise-num">3</span> Read a Codebase, Write the Docs

## Step 1: Download the app

```bash
curl -O https://raw.githubusercontent.com/realmindsai/bulsu_tutorial_2026/main/broken_app.py
```

## Step 2: Generate documentation

```bash
gemini "Read this Python app and generate:
1) A README with setup instructions
2) A list of every function and what it does
3) How data flows through the app
4) Bugs or improvements you can spot
Write each to a separate file." < broken_app.py
```

---

# <span class="exercise-num">3</span> Discussion

## Read the generated README

- Is it accurate?
- Did the AI find real bugs? (Hint: there is a closure bug)
- Would this documentation help a developer understand the code?

**Bonus:** Feed the AI a project from your own coursework and generate docs for it.

---

# <span class="concept">Concept</span> System Prompts = Job Descriptions

## A few sentences turn a general AI into a specialist

Without a system prompt, the AI is a generalist. It knows everything but specializes in nothing.

With a **system prompt file**, you give it:
- A **role** ("You are a Bulacan tourism expert")
- **Rules** ("Only recommend places within Bulacan")
- **Boundaries** ("Never give medical advice")

Three sentences. That is all it takes to create a focused agent.

---

# <span class="exercise-num">4</span> Build Your Own Specialist

## Step 1: Create a system prompt file

Write 3-4 sentences in a file called `agent_prompt.md`:

- A **Bulacan tourism guide** for visitors
- A **student budget advisor** for tight allowances
- A **recipe assistant** for Filipino dishes
- A **study planner** for exam season

## Step 2: Test it

```bash
gemini --system-instruction agent_prompt.md \
  "I have 500 pesos for the week and need to
   eat 3 meals a day. Make me a plan."
```

---

# <span class="exercise-num">4</span> Break It

## Step 3: Test the boundaries

Give your agent a question **outside its job**.

Ask your tourism guide for medical advice. Ask your budget advisor to write code.

- Does it stay in role?
- What rule would you add to make it better?
- How is this different from just asking the AI directly?

---

# <span class="concept">Concept</span> From Question to Deliverable

## One prompt can produce a professional document

The CLI does not just answer questions. It can produce **formatted deliverables**:

- Research reports with sections and sources
- Executive summaries
- Data-backed analysis
- Exported as Markdown, HTML, or PDF

This is the difference between **getting an answer** and **getting a document you can hand to someone**.

---

# <span class="exercise-num">5</span> Research and Report

## Produce a professional briefing document

```bash
gemini "Research the food manufacturing industry
in Bulacan province. Produce a briefing document:
1) Top companies and what they produce
2) Employment and economic impact
3) Current challenges the industry faces
4) Three opportunities where AI tools could help
Format as a professional report with an
executive summary. Export as Markdown and HTML."
```

---

# <span class="exercise-num">5</span> Discussion

## Read the report

- Could you present this to a professor?
- Could you present it to a local business owner?
- What would you fact-check first?
- How long would this have taken you to write manually?

**Bonus:** Pick a different Bulacan industry and generate another report.

---

<!-- _class: title-slide -->

# What You Just Did

- Built a **complete web app** from a sentence
- Turned **raw data into a dashboard** with charts
- Made AI **read and document** existing code
- Created a **custom specialist** agent
- Produced a **professional research report**

All from the command line. All in under 2 hours.

---

<!-- _class: title-slide -->

# Mini Hackathon

**6:00 PM  -  Build something real in 75 minutes**

Pick a project during the break. Come back with a team.

---

# Hackathon Roles

## Assign these within your team

| Role | What You Do |
|------|-------------|
| **PM** | Writes and refines the prompt |
| **Engineer** | Runs the AI, iterates on output |
| **Tester** | Tries to break it, finds edge cases |
| **Presenter** | Prepares the demo |

**Rotate who talks to the AI.** Everyone should try.

---

# Hackathon Option A

## Barangay Service Portal

```bash
gemini "Build a web app for barangay complaint
tracking. Residents submit complaints with
category and location. Officials update status
and add notes. Include a public dashboard
showing resolution rates.
Python with SQLite."
```

**Judging:** Does it work for a barangay captain?

---

# Hackathon Option B

## Campus Tools for BSU

```bash
gemini "Build a tool for BSU students that
[your idea here]. Think about: class scheduling,
study groups, canteen menus, org events,
or requirement tracking.
Web app with Python backend."
```

**Judging:** Would BSU students actually use this?

---

# Hackathon Option C

## Bulacan Business Intelligence

```bash
gemini "Build a CLI tool that generates
business reports for Bulacan province.
Given an industry name, research key companies,
create comparison charts, and export a
professional PDF report.
Python with matplotlib."
```

**Judging:** Could you hand this to an LGU official?

---

# Hackathon Option D

## Your Own Idea

**Requirements:**
- Use an agentic CLI tool to build it
- Must be testable in the demo
- Must address a local context

```bash
gemini "Build [your idea]. [describe users].
[describe core workflow]. Simple enough
to demo in 5 minutes."
```

**Judging:** Is it real? Would someone use it?

---

# Tips for the Hackathon

- **Start small.** Get the core working before adding features
- **Iterate.** Your first prompt will not be perfect. Refine it
- **Test outcomes, not code.** Does it do what a user needs?
- **Add local knowledge** the AI does not have
- **Prepare your demo early.** Whatever you have IS your demo

**Help:** Raise your hand. Mentors are circulating.

---

<!-- _class: title-slide -->

# The CLI is not just for coders.

## It is for anyone who can describe what they want.

20 February 2026

---

# Connect With Us

**Dr Dennis Wollersheim** - Co-Founder and CTO
linkedin.com/in/dennis-wollersheim

**Tracy Anthony** - Co-Founder and CEO
linkedin.com/in/tracyanthony

**Real Minds AI** | wisdom, amplified
realmindsai.au

---

# Enjoyed Today?

## Leave us a Google review

![w:300](qr_google_review.png)

Scan to review - it helps us bring workshops like this to more communities.

---
