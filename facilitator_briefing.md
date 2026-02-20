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

<!--
- Welcome facilitators and thank them for volunteering their time
- This briefing should take 15-20 minutes to present
- Goal: make sure every facilitator knows exactly what to do and when, without needing to understand AI tools deeply
- Key message upfront: "Your job is simpler than you think. Dennis runs the show. You help students when they get stuck."
- Confirm logistics: venue layout, WiFi password, time the room opens, where power outlets are
- Ask: "Who has used Gemini CLI or Claude Code before?" — calibrate the room
-->

---

# Key Difference from Previous Workshops

## This is a capability showcase, not a career lecture

**Previous format:** Articles about AI and careers, then exercises to illustrate the points.

**This format:** Short demo of what the CLI can do (5 min), then students try it themselves (20 min). Repeat five times.

**Your role is simpler:** Keep time, help with CLI issues, encourage exploration. Dennis does the short intros. Students spend most of the time hands-on.

**Audience:** More general than GDG Manila. Mixed technical levels. Some may be new to the terminal. Pair them with neighbours.

<!--
- Emphasise the format change: "The GDG Manila workshop in February was lecture-heavy — articles, discussion, career framing. This workshop is hands-on from minute 15."
- The 5-15-5 pattern: "Every exercise is the same: Dennis talks for 5 minutes, students work for 15 minutes, we discuss for 5 minutes. Five exercises, same pattern every time."
- Audience calibration: "BulSU students will have mixed technical levels. Some will be comfortable in the terminal. Others may have never opened one. Your most important job is identifying the students who are stuck and pairing them with neighbours who are not."
- Role clarity: "You do not need to be an AI expert. You need to help students copy-paste a prompt, find their output file, and troubleshoot basic CLI issues. The handout has every prompt pre-written."
- Reassurance: "If a student asks you an AI question you cannot answer, say 'great question — let us ask Dennis during the discussion' and move on."
-->

---

# The Big Picture

## Three phases across the evening

| Phase | Time | Duration | What Happens |
|-------|------|----------|-------------|
| **Capability Demos** | 3:00 - 5:30 | 2.5 hrs | Dennis intros 5 capabilities, students try each one |
| **Break + Team Formation** | 5:30 - 6:00 | 30 min | Networking, snacks, teams form |
| **Hackathon + Demo** | 6:00 - 8:00 | 2 hrs | Groups build (75 min) then demo (30 min) |

<!--
- Walk through the three phases:
  - Phase 1 is structured and predictable — same 25-minute pattern repeated 5 times with a stretch break in the middle
  - Phase 2 is social — students form hackathon teams, pick a project, eat snacks. Your job is to help solo students find teams.
  - Phase 3 is creative — teams build something from scratch using what they learned. Your role shifts from "tech support" to "mentor."
- Time management note: "Phase 1 needs to stay on schedule. If an exercise runs long, Dennis will shorten the discussion, not skip the next exercise. Five exercises must happen before the break."
- Phase 3 has hard stops: "At 7:15, building stops regardless. Demos happen 7:15-7:45. The event wraps at 8:00. Do not let teams convince you they need 'five more minutes.'"
-->

---

# Schedule Detail

## Minute by minute

| Time | What | Your Job |
|------|------|----------|
| 3:00 | Welcome + setup verify | Help with `gemini --version`, pair anyone stuck |
| 3:15 | **Ex 1:** App From a Sentence | Walk around, help run prompts |
| 3:40 | **Ex 2:** Data to Dashboard | Help download CSV, open HTML output |
| 4:05 | Stretch break | Check on stuck students |
| 4:15 | **Ex 3:** Read a Real GitHub Project | Help with git clone |
| 4:40 | **Ex 4:** Build Your Own Specialist | Help create agent_prompt.md files |
| 5:05 | **Ex 5:** Research and Report | Walk around, read outputs with students |
| 5:30 | Break + team formation | Help groups form, pick hackathon option |
| 6:00 | Hackathon starts | Mentor: scope down, push testing |
| 7:15 | Demos | Help presenters share screen |
| 7:45 | Closer + QR codes | Nudge Google review scan |

<!--
- This is the reference slide — tell facilitators to screenshot it or keep it open on their phone
- Highlight the critical moments where facilitators are most needed:
  - 3:00 setup: "This is your busiest 15 minutes. Students who cannot get gemini running need immediate help. Pair them with neighbours if the install is failing."
  - 3:40 CSV download: "Some students will struggle with curl. Have USB backup copies of the CSV ready. Airdrop is also an option on Macs."
  - 4:15 git clone: "If git is not installed, the fallback is downloading the zip from GitHub. Help students navigate to the GitHub page and click 'Download ZIP.'"
  - 4:40 file creation: "Some students have never created a text file from the terminal. Show them nano or any text editor."
  - 5:30 team formation: "Actively help solo students find teams. Walk up and introduce them to groups that look open."
- The 4:05 stretch break: "Use this time to find students who are stuck or behind. Catch them up."
-->

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

<!--
- The 5-15-5 rhythm: "This is the heartbeat of Phase 1. Get used to it. Dennis talks, students work, everyone discusses."
- During the 5-min intro: "Stand near students who might need help. When Dennis says 'go', you should be ready to circulate immediately."
- During the 15-min work period: "Walk the room. Look for students staring at their screen with no output. Look for error messages. Look for students who are not typing anything."
- Common intervention: "Most issues are one of three things: (1) the CLI tool is not installed — pair them with a neighbour, (2) there is a typo in the prompt — help them copy-paste from the handout, (3) they cannot find the output file — help them with 'ls' to list files in their directory."
- During the 5-min discussion: "Encourage quieter students. If Dennis asks 'who wants to share?' and nobody volunteers, walk to a student who got interesting output and say 'hey, your output looked cool — want to share?'"
- Do not solve problems FOR students: "Guide them. Say 'try ls to see what files were created' rather than typing the command for them. The goal is learning, not completion."
-->

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
| git clone fails | Download the zip from GitHub instead, or pair with a neighbour |
| Student wants to use Claude Code | Totally fine. All exercises are tool-agnostic |
| Student has no CLI tool at all | They can use Gemini web (gemini.google.com) for exercises 4 and 5 |

<!--
- Walk through the table: "These are the issues we have seen in previous workshops. Most of them have simple fixes."
- The most common issue: "Installation problems. Students who cannot get the CLI running. The fix is always the same: pair them with a neighbour. Two people, one laptop. It works."
- The second most common: "Output file not found. Students run the prompt, the AI creates files, but the student cannot find them. Help them with 'ls' or 'dir' to see what is in their current directory. The AI may have created a subfolder."
- Tool-agnostic note: "If a student wants to use Claude Code instead of Gemini CLI, or Codex, or anything else — great. All exercises work with any agentic CLI tool. The prompts are the same."
- Last resort: "If a student has absolutely no CLI tool and cannot install one, they can use Gemini web at gemini.google.com. They will not get the file-creation and code-execution features, but they can still follow along for exercises 4 and 5."
- Have backup plan ready: "USB drives with the CSV file, the broken_app.py, and the GitHub project zips. If the network is down, we can still run most exercises."
-->

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

<!--
- This is the "wow" exercise — it sets the tone for the whole workshop
- Before students run: Dennis will explain outcome-based thinking — describing a problem and a user, not a technology stack
- The prompt mentions "simple enough for a tindahan owner who uses Facebook but has never touched Excel" — that is the key. It describes the USER, not the implementation.
- Expected variations in output:
  - Some students will get Flask apps, others will get Streamlit apps, some might get FastAPI or even Node.js
  - Some will have beautiful UIs, others will be basic. This variation is a feature — it shows that AI output is non-deterministic
  - Some apps will start automatically, others will need manual `python app.py`
- If a student's app crashes on startup: "Check if it needs dependencies. The AI usually prints install instructions. Try 'pip install flask' or 'uv pip install flask'."
- The discussion should focus on: "Would a real sari-sari store owner use this? What is missing?" Push for specifics: utang/listahan tracking, Tagalog interface, phone-friendly design.
- Filipino context: There are over 1 million sari-sari stores in the Philippines. This is not a toy example — it is a real market with real pain points.
-->

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

<!--
- The two-step process: (1) download the CSV, (2) pipe it into the AI
- The CSV contains 3,200+ rows of synthetic sari-sari store sales — Filipino products (Lucky Me, Bear Brand, Mang Tomas, etc.), peso prices, Bulacan barangay names
- The < symbol in the command pipes the file into the AI. Some students may not know this. Explain: "The less-than sign means 'feed this file as input.'"
- If curl is not available: "Use the backup copies on USB. Or try: 'Invoke-WebRequest -OutFile bulacan_sari_sari_sales_6months.csv [URL]' on Windows PowerShell."
- Opening HTML output: "The AI will create an HTML file. Students need to open it in a browser. On Mac: 'open dashboard.html'. On Windows: 'start dashboard.html'. Or just drag the file into Chrome."
- Expected charts: top products by revenue, daily/weekly revenue trend, profit by category, busiest barangays. The AI usually uses plotly or matplotlib.
- Discussion focus: "Could you hand this to a real store owner? What would you add?" Push for: restock alerts, month-over-month comparison, mobile-friendly layout.
-->

---

# Exercise-Specific Notes

## <span class="phase">Exercise 3</span> Read a Real GitHub Project

**What happens:** Students clone a real open-source Python project and ask the AI to read and document it.

**Three options:** heartrate (execution visualizer), simpleeval (math evaluator), or a snake game.

**Expected output:** README, file-by-file breakdown, code walkthrough, and bug/improvement list.

**Watch for:**
- Students need `git` installed to clone repos. If git is missing, they can download the zip from GitHub
- The AI needs to run inside the cloned folder (`cd heartrate` first)
- Some repos are bigger than others - heartrate has more files to analyze

**Discussion prompt:** "Did the AI understand what the project does? Could a developer use this documentation?"

<!--
- The three options are graded by complexity:
  - Snake game: under 50 lines, single file, fast analysis. Good for students who are new to Python or want quick results.
  - simpleeval: a focused library with clear purpose, 570+ stars, used in production. Mid-complexity.
  - heartrate: the most complex — multiple files, sophisticated Python, 1,800+ stars. Best for advanced students.
- The cd step is critical: "The AI needs to be running inside the project folder. If a student runs 'gemini' from their home directory, it will not see the project files. Make sure they 'cd heartrate' (or whichever project) first."
- Git fallback: "If git is not installed, they can go to the GitHub page in a browser, click the green 'Code' button, and 'Download ZIP'. Then unzip it."
- The bug-finding aspect is the most interesting: "Did the AI find real bugs or just style issues? Sometimes the AI catches genuine problems the original developer missed. Sometimes it confidently reports non-issues."
- Verification is the lesson: "Can the student verify whether the AI's analysis is correct? That requires actually understanding the code. This is Pike's power saw — the AI amplifies skill, it does not replace it."
-->

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

<!--
- File creation is the biggest hurdle: "Many students have never created a file from the command line. Options: 'nano agent_prompt.md' (type, Ctrl+O to save, Ctrl+X to exit), or open any text editor (VS Code, Notepad, TextEdit) and save the file in their current directory."
- What a good system prompt looks like:
  - "You are a student budget advisor for Filipino college students. Help plan meals and expenses on a tight weekly allowance. All prices should be in Philippine pesos. Reference local food options — carinderia, sari-sari store, palengke. Never recommend spending more than the stated budget."
- The --system-instruction flag: "This tells Gemini CLI to read the file and adopt that role. The flag is --system-instruction, not --system-prompt."
- The "break it" step is where learning happens: "Ask students to test their agent with an out-of-scope question. A tourism guide should not give medical advice. A budget advisor should not write code. When the agent breaks character, that is the lesson — boundaries matter."
- Real-world connection: "Companies spend months building and testing system prompts for their AI products. Students just did it in 5 minutes. The quality testing (boundary testing) is what separates a toy from a product."
-->

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

<!--
- Network dependency: "This is the exercise most likely to be affected by slow campus WiFi. The AI uses web search to research the topic. If the network is slow, the output takes longer but still works."
- Fallback if web search is blocked: "The AI will generate from its training data instead of live research. The report will still be structured and professional, but the data may be less current. Mention this to students — it is a good discussion point about AI limitations."
- Quality variation: "This exercise produces the most variable output. Some reports will be excellent. Others will have plausible-sounding but incorrect data. That variation is the discussion topic."
- Verification is key: "When students get their report, ask them to fact-check one claim. Is that company real? Is that revenue figure plausible? Does that employment number make sense? Bulacan students should know enough local context to catch obvious errors."
- The career implication: "A consulting firm would charge thousands of pesos for this kind of report. The AI produced a first draft in 5 minutes. The question is whether the student can verify and improve it — that is where their value lies."
-->

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

<!--
- Team formation should happen during the 5:30-6:00 break. By 6:00, every student should be in a team with a project picked.
- If teams are not formed by 6:00: "Help stragglers join existing teams. A team of 5 is fine. A team of 2 is fine. Nobody works alone."
- Role assignment: "Make sure every team has a PM and a Presenter at minimum. The PM decides what to build and writes the prompt. The Presenter needs to start preparing their demo early."
- Options recap:
  - A: Barangay Service Portal — complaint tracking for local government
  - B: Campus Tools for BulSU — solve a real student problem
  - C: Bulacan Business Intelligence — automated report generation
  - D: Your Own Idea — anything local and testable
- If a team cannot decide: "Pick Option B. You are BulSU students, you know your own problems. Build something that solves one."
-->

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

<!--
- Your most important job during the hackathon: scope management
  - Teams will try to build too much. Help them focus: "What is the ONE thing this app must do? Build that first. Everything else is a bonus."
  - If a team is stuck on their prompt after 10 minutes: "Just run something. See what happens. You can iterate."
- Healthy conflict: "If the PM says 'build a complaint system' and the Engineer says 'that is too complex', that is a good conversation. They are learning to spec. Do not intervene unless they are truly stuck."
- Push the Tester role: "If the Tester says 'it works' after 2 minutes, they are not doing their job. Push them: 'What happens with Filipino characters in names? What about zero stock? What if someone enters a negative number?'"
- Time warnings are critical:
  - 30-min mark: Walk to every team and ask "What do you have so far?" This forces a checkpoint.
  - 15-min mark: "Whatever you have now IS your demo. Stop adding features. Polish what exists."
  - 5-min mark: "Stop building. Presenter, show me your demo plan." If the Presenter has not prepared, help them right now.
- If a team has nothing working at the 15-min mark: "Help them get the simplest possible version running. Even a single-page app that does one thing is better than nothing."
-->

---

# <span class="phase">Phase 3</span> Demos (7:15 - 7:45 PM)

## Show and tell

- **2-3 min per group:** Presenter shares their screen or walks through their project
- Audience votes (hand raise) for:
  - **Most useful** - would someone actually use this?
  - **Best failure** - which group learned the most from things going wrong?

**No prizes needed.** The learning is the artifact.

"We tried X, it failed, we pivoted to Y, and here is what Y does" is more impressive than a rehearsed pitch.

<!--
- Demo logistics:
  - "Each group gets 2-3 minutes. With 8-10 groups, this takes about 30 minutes."
  - "Presenter shares their screen on the projector. If screen sharing is not possible, walk to their laptop."
  - "Help presenters connect to the projector. Test this during the hackathon if possible."
- Framing the demos: "Dennis will MC. He will introduce each group and keep time. Your job is to help with screen sharing and keep the audience engaged."
- The two awards:
  - "Most useful: would someone actually use this? This rewards practical thinking."
  - "Best failure: which group learned the most from things going wrong? This rewards honesty and resilience. It is often more impressive than the 'most useful' winner."
- Encourage failure stories: "The best demo is not 'look, it works perfectly.' The best demo is 'we tried X, it failed because of Y, we pivoted to Z, and here is what Z does.' That narrative shows real learning."
- No prizes: "The learning is the artifact. Do not promise prizes. Applause and recognition from peers is enough."
-->

---

# Your Cheat Sheet

## Keep this open on your phone

| Time | What is Happening | Your Job |
|------|-------------------|----------|
| 3:00 | Setup + verify | Help with CLI installs, pair stuck students |
| 3:15 | Ex 1: App From a Sentence | Help run prompts, find output files |
| 3:40 | Ex 2: Data to Dashboard | Help download CSV, open HTML |
| 4:05 | Break | Check on stuck students |
| 4:15 | Ex 3: Real GitHub Project | Help with git clone |
| 4:40 | Ex 4: Custom Agent | Help create text files |
| 5:05 | Ex 5: Research Report | Walk around, read outputs |
| 5:30 | Break + teams | Help groups form |
| 6:00 | Hackathon | Mentor: scope down, push testing |
| 7:15 | Demos | Help presenters share screen |
| 7:45 | Closer | Nudge Google review QR scan |

<!--
- Tell facilitators: "Screenshot this slide or keep it open on your phone. This is your reference for the entire evening."
- The three columns tell you everything: what time, what is happening, what you do
- Colour-coded priorities:
  - RED moments (most facilitator help needed): 3:00 setup, 3:40 CSV download, 4:15 git clone, 5:30 team formation
  - YELLOW moments (moderate help): 3:15 and 4:40 exercises, 6:00 hackathon start
  - GREEN moments (low help): 5:05 research exercise, 7:15 demos, 7:45 closer
- If you have a quiet moment during an exercise, use it to check on students at the back of the room. The ones who need help most are the ones least likely to raise their hand.
-->

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

<!--
- Walk through each FAQ:
  - "Do I need to be an AI expert?" — "No. Seriously. Your job is people management and troubleshooting, not AI expertise. If a student asks a deep AI question, redirect it to Dennis."
  - "Different output?" — "Every student will get different output from the same prompt. That is how AI works — non-deterministic. Embrace it. It makes great discussion material."
  - "Finishes early?" — "Stretch goals: modify the prompt, add a feature, try a different AI tool, help a neighbour. Never let a fast student sit idle."
  - "Slow network?" — "Exercises 1, 3, and 4 do not need network once the CLI tool is installed. Exercise 2 needs the CSV file — have USB backups. Exercise 5 uses web search but falls back to training data if search is blocked."
- Additional FAQ not on the slide:
  - "What if a student wants to use a different tool?" — All exercises are tool-agnostic. Claude Code, Codex, even web-based Gemini work for most exercises.
  - "What if the event runs long?" — Demos can be shortened. Cut to 1-2 minutes per group. The closer (QR codes + thank you) takes 5 minutes max.
-->

---

<!-- _class: title-slide -->

# Questions?

## The key message for facilitators:

Your job is to keep students **running prompts, reading output, and discussing results.**

The AI does the heavy lifting. You manage the humans.

<!--
- Open the floor for facilitator questions: "What are you worried about? What do you need from me?"
- Common concerns to address:
  - "What if I cannot answer a student's question?" — "Say 'great question, let us ask Dennis during the discussion.' Then flag it to me."
  - "How do I know if a student's output is correct?" — "You do not need to. The exercises are about exploration, not correctness. If their app runs, it is a success."
  - "What if half the students cannot install the tool?" — "That is what the first 15 minutes are for. Pair stuck students with neighbours. The workshop works with shared laptops."
- Final reminder: "Your job is not to teach AI. Your job is to keep the room moving. Students typing, outputs appearing, discussions happening. That is a successful workshop."
- Thank the facilitators: "You are volunteering your time to help students learn. That matters. Thank you."
- Confirm logistics: start time, where to meet, what to bring, WiFi details, contact number for day-of issues
-->

---
