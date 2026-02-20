---
marp: true
theme: default
paginate: true
backgroundColor: #0F1229
color: #E8E8EC
style: |
  section {
    font-family: 'Calibri', 'Segoe UI', sans-serif;
    font-size: 22px;
    line-height: 1.4;
    padding: 40px 50px;
  }
  h1 {
    color: #FFFFFF;
    font-family: 'Georgia', serif;
    font-size: 1.6em;
    border-bottom: 3px solid #E8873A;
    padding-bottom: 8px;
    margin-bottom: 8px;
  }
  h2 {
    color: #E8873A;
    font-family: 'Georgia', serif;
    font-size: 1.1em;
    margin-top: 4px;
    margin-bottom: 8px;
  }
  h3 {
    color: #FFFFFF;
    font-size: 1.0em;
    margin-top: 4px;
    margin-bottom: 4px;
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
    padding: 8px 12px !important;
    border-radius: 8px;
    font-size: 0.7em;
    margin: 4px 0;
  }
  pre code {
    background: transparent;
    color: #E8E8EC !important;
  }
  strong {
    color: #E8873A;
  }
  a {
    color: #E8873A;
  }
  p, ul, ol {
    margin-top: 4px;
    margin-bottom: 4px;
  }
  li {
    margin-bottom: 2px;
  }
  table {
    background: #1a1e38 !important;
    color: #E8E8EC !important;
    border-collapse: collapse !important;
    width: 100%;
    font-size: 0.8em;
  }
  th {
    background: #E76F51 !important;
    color: white !important;
    padding: 4px 10px !important;
    text-align: left;
    border: none !important;
  }
  td {
    padding: 4px 10px !important;
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
  section.title-slide h1 {
    font-size: 1.8em;
    border-bottom: none;
  }
  .phase {
    display: inline-block;
    background: #E76F51;
    color: white;
    padding: 4px 14px;
    border-radius: 16px;
    font-weight: bold;
    font-size: 0.85em;
  }
---

<!-- _class: title-slide -->

# Facilitator Briefing
## What Can Agentic CLI Do? Workshop
**GDG x Bulacan State University** | 20 Feb 2026

For facilitators and mentors

---

# Key Difference from Previous Workshops

## This is a capability showcase, not a career lecture

**Previous format:** Articles about AI and careers, then exercises to illustrate the points.

**This format:** Short demo of what the CLI can do (5 min), then students try it themselves (20 min). Repeat five times.

**Your role is simpler:** Keep time, help with CLI issues, encourage exploration. Dennis does the short intros. Students spend most of the time hands-on.

**Audience:** More general than GDG Manila. Mixed technical levels. Some may be new to the terminal. Pair them with neighbours.

---

# The Big Picture

## Three phases across the evening

| Phase | Time | Duration | What Happens |
|-------|------|----------|-------------|
| **Capability Demos** | 3:00 - 5:30 | 2.5 hrs | Dennis intros 5 capabilities, students try each one |
| **Break + Team Formation** | 5:30 - 6:00 | 30 min | Networking, snacks, teams form |
| **Hackathon + Demo** | 6:00 - 8:00 | 2 hrs | Groups build (75 min) then demo (30 min) |

---

# Schedule Detail

## Minute by minute

| Time | What | Your Job |
|------|------|----------|
| 3:00 | Welcome + setup verify | Help with `gemini --version`, pair anyone stuck |
| 3:15 | **Ex 1:** App From a Sentence | Walk around, help run prompts |
| 3:40 | **Ex 2:** Data to Dashboard | Help download CSV, open HTML output |
| 4:05 | Stretch break | Check on stuck students |
| 4:15 | **Ex 3:** Read Codebase, Write Docs | Help download broken_app.py |
| 4:40 | **Ex 4:** Build Your Own Specialist | Help create agent_prompt.md files |
| 5:05 | **Ex 5:** Research and Report | Walk around, read outputs with students |
| 5:30 | Break + team formation | Help groups form, pick hackathon option |
| 6:00 | Hackathon starts | Mentor: scope down, push testing |
| 7:15 | Demos | Help presenters share screen |
| 7:45 | Closer + QR codes | Nudge Google review scan |

---

# What You Do During Exercises

## Every exercise follows the same pattern (25 min each)

**Dennis intro** (5 min):
- Shows what the capability is
- Maybe runs it live or shows expected output
- Says "Open your handout to Exercise N, run the prompt"

**Students work** (15 min):
- Everyone runs the same prompt
- Your job: walk around, help anyone stuck
- Common issues: CLI not installed, typos in prompt, output file not found

**Discussion** (5 min):
- Dennis asks "What did you get? Is it useful?"
- Students share screens or describe output
- No pressure to present - just conversation

---

# Common Issues and Fixes

## What will go wrong and how to handle it

| Problem | Fix |
|---------|-----|
| Student cannot install Gemini CLI | Pair them with a neighbour. Two people, one laptop works fine |
| `gemini` command not found | Check PATH. Try restarting terminal. Worst case, use `npx @anthropic-ai/claude-code` or web UI |
| Prompt takes very long | Normal for app generation (Ex 1). Let it run. Can take 2-5 min |
| Output file not found | Check current directory with `ls`. AI may have created a subfolder |
| CSV download fails | Share the file via USB or airdrop. Have backup copies ready |
| Student wants to use Claude Code | Totally fine. All exercises are tool-agnostic |
| Student has no CLI tool at all | They can use Gemini web (gemini.google.com) for exercises 4 and 5 |

---

# Exercise-Specific Notes

## <span class="phase">Exercise 1</span> App From a Sentence

**What happens:** Students ask the CLI to build an entire sari-sari store POS system.

**Expected output:** A Flask or Streamlit web app with inventory tracking and sales recording.

**Watch for:**
- Students who do not know how to run a Python app - help them with `python app.py` or `uv run app.py`
- The app may need dependencies installed - the AI usually tells you how
- Some students will get a different tech stack (Node, etc.) - that is fine

**Discussion prompt:** "How close is this to something a real store owner could use? What would you change?"

---

# Exercise-Specific Notes

## <span class="phase">Exercise 2</span> Data to Dashboard

**What happens:** Students feed a CSV of sari-sari store sales data into the CLI and get charts and analysis back.

**Expected output:** An HTML file with bar charts, line charts, and a profit analysis.

**Watch for:**
- Students need to download the CSV first (`curl` command in the handout)
- If `curl` is not available, share the file directly
- The HTML output needs to be opened in a browser - help students find the file
- Charts should show Filipino products and peso formatting

**Discussion prompt:** "Could you hand this dashboard to a store owner? What is missing?"

---

# Exercise-Specific Notes

## <span class="phase">Exercise 3</span> Read a Codebase, Write the Docs

**What happens:** Students feed a 190-line Python app to the CLI and ask it to generate documentation.

**Expected output:** A README.md, function list, data flow description, and bug list.

**Watch for:**
- Students need to download broken_app.py first
- The AI should identify the closure bug in `build_stat_collectors` (all departments show Product stats)
- Some students may try to fix the bugs - encourage that! But the exercise is about documentation

**Discussion prompt:** "Did the AI find real issues? Is the README accurate enough to use?"

---

# Exercise-Specific Notes

## <span class="phase">Exercise 4</span> Build Your Own Specialist

**What happens:** Students write a short system prompt, save it to a file, and test a custom agent.

**Expected output:** An agent that stays in character and gives domain-specific advice.

**Watch for:**
- Students may struggle to create a text file from the terminal - help with `nano agent_prompt.md` or have them use any text editor
- Some agents will break character immediately - that is the learning moment
- The "break it" step is important: ask them to give it an out-of-scope question

**Discussion prompt:** "Did your agent stay in role? What rule would you add to make it better?"

---

# Exercise-Specific Notes

## <span class="phase">Exercise 5</span> Research and Report

**What happens:** Students ask the CLI to research a Bulacan industry and produce a professional report.

**Expected output:** A structured report with sections, data, and an executive summary in Markdown and HTML.

**Watch for:**
- This exercise uses web search, which may be slower or blocked on campus networks
- If web search is not available, the AI will generate from its training data - still useful
- Output quality varies a lot with this one - good discussion topic

**Discussion prompt:** "Is this something you could present to a professor? What would you fact-check?"

---

# <span class="phase">Phase 2</span> Hackathon (6:00 - 7:15 PM)

## Groups pick a project and assign roles

### Step 1: Choose (2 min)
Groups pick from Options A, B, C, or D (on the handout)

### Step 2: Assign roles (1 min)

| Role | Does What |
|------|-----------|
| **PM** | Writes and refines the prompt, adds local context |
| **Engineer** | Runs the AI, iterates on output |
| **Tester** | Tries to break it, feeds failures back |
| **Presenter** | Prepares the demo |

### Step 3: Build (70 min)

---

# What You Do During the Hackathon

## Your role shifts to mentor

- Help groups **scope down** ("You have 75 minutes. Get the core working first")
- If the PM and Engineer are arguing, that is **good** - they are learning to spec
- If the Tester says "it works fine" after 2 minutes, push them ("What about edge cases? Filipino characters in names? Zero stock?")
- Remind the Presenter: "Prepare your demo! You need something to show"

**30 min warning:** "Half time. What do you have so far?"

**15 min warning:** "Whatever you have now IS your demo. Polish, do not build."

**5 min warning:** "Stop building. Presenter: is your demo ready?"

---

# <span class="phase">Phase 3</span> Demos (7:15 - 7:45 PM)

## Show and tell

- **2-3 min per group:** Presenter shares their screen or walks through their project
- Audience votes (hand raise) for:
  - **Most useful** - would someone actually use this?
  - **Best failure** - which group learned the most from things going wrong?

**No prizes needed.** The learning is the artifact.

"We tried X, it failed, we pivoted to Y, and here is what Y does" is more impressive than a rehearsed pitch.

---

# Your Cheat Sheet

## Keep this open on your phone

| Time | What is Happening | Your Job |
|------|-------------------|----------|
| 3:00 | Setup + verify | Help with CLI installs, pair stuck students |
| 3:15 | Ex 1: App From a Sentence | Help run prompts, find output files |
| 3:40 | Ex 2: Data to Dashboard | Help download CSV, open HTML |
| 4:05 | Break | Check on stuck students |
| 4:15 | Ex 3: Codebase to Docs | Help download broken_app.py |
| 4:40 | Ex 4: Custom Agent | Help create text files |
| 5:05 | Ex 5: Research Report | Walk around, read outputs |
| 5:30 | Break + teams | Help groups form |
| 6:00 | Hackathon | Mentor: scope down, push testing |
| 7:15 | Demos | Help presenters share screen |
| 7:45 | Closer | Nudge Google review QR scan |

---

# FAQ

## Common questions facilitators ask

**"Do I need to be an AI expert?"**
No. You need to help students copy-paste a prompt and run it. The handout has every prompt pre-written.

**"What if a student's output looks completely different from everyone else's?"**
That is expected. AI output varies. It is a feature, not a bug - good discussion topic.

**"What if someone finishes early?"**
Give them a stretch goal: "Now modify the prompt to add a feature" or "Try the same exercise with a different AI tool and compare."

**"What if the campus network is slow?"**
Exercises 1, 3, and 4 work offline. Exercise 2 needs the CSV (share via USB). Exercise 5 needs web access but can fall back to training data.

---

<!-- _class: title-slide -->

# Questions?

## The key message for facilitators:

Your job is to keep students **running prompts, reading output, and discussing results.**

The AI does the heavy lifting. You manage the humans.
