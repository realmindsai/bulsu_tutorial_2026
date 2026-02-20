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

<!--
- Welcome everyone warmly — acknowledge BulSU, GDG organisers, and any facilitators by name
- Set the frame: "This is not a lecture. This is a capability showcase. You will spend most of today with your hands on the keyboard."
- Briefly introduce yourself: Dr Dennis Wollersheim, Co-Founder & CTO of Real Minds AI, PhD in Computer Science, 53 peer-reviewed publications, led Victoria's COVID-19 data engineering team
- Mention Tracy Anthony as Co-Founder & CEO (35 years enterprise transformation) — she is not presenting today but is part of the team
- Key energy note: start measured, not hype. This audience responds to precision and intellectual respect, not volume
- Framing line: "By the end of today, you will have built five things from the command line that would have taken you days or weeks to build by hand. And then you will build a sixth in the hackathon."
-->

---

# Follow Along on Your Device

## Scan for the handout with all prompts you can copy-paste

![w:280](qr_workshop_prompts.png)

**realmindsai.github.io/bulsu_tutorial_2026**

Open this on your phone or laptop — it links to all workshop materials.

<!--
- Hold the slide up for 20-30 seconds so everyone can scan
- Say: "This is the signpost page — it links to everything: the prompts handout, the facilitator briefing, setup instructions. If your CLI tool is not installed yet, you can still follow along by reading the prompts."
- Ask facilitators to walk around and help anyone having trouble scanning
- If campus WiFi is slow, mention that they can also type the URL manually
- Quick check: "Raise your hand if you have the page open. Good."
- Transition: "Let me show you what we are doing today."
-->

---

# Today's Agenda

| Time | What |
|------|------|
| 3:00 | Setup and verify tools |
| 3:15 | **Ex 1:** Build an app from one sentence |
| 3:40 | **Ex 2:** Turn data into a dashboard |
| 4:05 | Break |
| 4:15 | **Ex 3:** Make AI read and explain a real project |
| 4:40 | **Ex 4:** Create your own AI specialist |
| 5:05 | **Ex 5:** AI-powered research report |
| 5:30 | Break and hackathon team formation |
| 6:00 | **Hackathon** (75 min) |
| 7:15 | **Demos** |
| 7:45 | Wrap-up |

<!--
- Walk through the schedule quickly — do not dwell on each item
- Emphasise the pattern: "Every exercise is the same shape — I show you something for 5 minutes, you try it for 15 minutes, we talk about what happened for 5 minutes"
- Point out the two breaks: "If you need to step out, the natural break points are at 4:05 and 5:30"
- Mention the hackathon: "After the five exercises, you will form teams and build something real. Groups of 3-4, and you will demo what you built at the end."
- Set expectations: "Some of you will finish exercises fast. That is fine — there are bonus challenges on every slide. Some of you will hit issues. That is also fine — raise your hand and a facilitator will come help."
- Transition: "Before we start building, let me explain what kind of tool we are using today."
-->

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

You describe what you want. It builds it.

<!--
- This is the most important concept slide — make sure every student understands the distinction before moving on
- Key framing: "When you use ChatGPT in a browser, you are having a conversation. When you use Gemini CLI in a terminal, you are hiring a builder."
- Walk through each bullet with a concrete example:
  - "Create files — it will make app.py, index.html, requirements.txt, whatever it needs"
  - "Run code — it actually executes the code, sees if there are errors, and fixes them"
  - "Install packages — if it needs Flask or pandas, it will pip install them"
  - "Fix its own mistakes — if the code crashes, it reads the error, edits the code, and tries again. No copy-pasting error messages."
  - "Build entire projects — you say 'build me a store inventory system' and it creates the whole thing"
- The capability overhang concept (mention without jargon): "Every consumer AI product you use — ChatGPT, Gemini web, Copilot — shows you maybe 20% of what the model can do. The other 80% is unlocked when you give it tools, file access, and a terminal."
- Tell the Microsoft story (from Alderson): "Here is a fun detail. Microsoft internally uses Claude Code — a competitor's tool — for their own engineering teams. Meanwhile, they sell YOU Microsoft Copilot, which Alderson describes as 'absolutely laughable' compared to what is available. Even the company selling the casual tool does not use it internally. That tells you where the real capability is."
- DHH as a converted skeptic: "David Heinemeier Hansson created Ruby on Rails. He spent a decade fighting against microservices, cloud complexity, and JavaScript frameworks. He was the tech world's most famous sceptic. In February 2026, he wrote: 'we are not going back to the old world.' When THAT person says the tools have changed everything, pay attention."
- If students look sceptical: "I know this sounds like a sales pitch. In about 3 minutes you will see it yourself. Let us go."
- Transition: "Let me show you what I mean. Exercise 1."
-->

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

**Run it.** Wait 1-3 minutes. Open the app in your browser.

<!--
- Before students run: "Notice the prompt. It describes a problem and a user, not a technology stack. It says 'simple enough for a tindahan owner who uses Facebook' — that is outcome-based thinking. You are telling the AI WHO this is for, not HOW to build it."
- Walk them through what will happen: "You will see the AI thinking, creating files, installing packages, maybe even running the app. It takes 1-3 minutes. Let it run."
- Common issues to pre-empt:
  - "If gemini command is not found, check your PATH or restart your terminal. Facilitators can help."
  - "If you get a different tech stack — Node instead of Python, or Streamlit instead of Flask — that is fine. The AI makes its own choices."
  - "If it asks you questions, answer them. The agent is trying to clarify your intent."
- For students who cannot install CLI tools: "Pair up with a neighbour. Two people, one laptop works great."
- Once students are running: walk around for 2 minutes, check progress, then come back to the front
- Key point to make while they wait: "What you just typed was one paragraph. No framework selection, no database design, no file structure. The AI handled all of that. This is what DHH means by outcome-based thinking — describe what you want, not how to build it."
- Filipino context note: The sari-sari store example is deliberately local. There are over 1 million sari-sari stores in the Philippines. This is a real problem with real users.
-->

---

# <span class="exercise-num">1</span> Discussion

## How close is this to real?

- Would a store owner in Malolos actually use this?
- What is missing?
- What did the AI assume that you did not ask for?

**Bonus:** Change one thing in your prompt and run again. How does the output change?

<!--
- Spend 3-5 minutes on discussion. Do not rush this — the reflection is where learning happens.
- Ask someone to share their screen or describe what they got: "Who wants to show us what the AI built?"
- Likely outputs: Flask or Streamlit app with inventory CRUD, sales recording, maybe a dashboard. Some will have login pages, some won't. Some will have Filipino peso formatting, some won't.
- Key discussion points to drive:
  - "What did the AI assume?" — It probably chose a framework, a database, a UI style. It made dozens of decisions you never specified. Some good, some questionable.
  - "What is missing?" — Push for specifics: "Does it handle 'utang' (credit/listahan)? Does it work on a phone? Can a store owner who only speaks Tagalog use it?" These are the human-judgment questions AI cannot answer alone.
  - "Would a real store owner use this?" — Probably not yet. But the point is: you went from zero to a working prototype in 3 minutes. The next step is iteration, not starting over.
- The meta-point: "Code is now free. What you just saw is proof. The hard part was never building the app — it is knowing what the store owner actually needs. That requires talking to store owners, not writing code."
- Cohen's CTO thought experiment (use if discussion needs a push): "A billionaire founder named Jason Cohen asks this question: 'Would you rather lead a company with 1,000 daily visitors and a buggy product, or a clean product and 10 visitors?' The answer is obvious. The risk was never the code — it was finding people who want what you built. He calls it the Drake Equation of startups — you can fail at any one of a dozen stages, and 'can I build it?' is the easiest one."
- The 50-customer test: "Cohen insists you talk to FIFTY potential customers before writing a line of code. Not ten — fifty. Because ten gives you false confidence. If you cannot find fifty people to interview about your sari-sari store app idea, what does that tell you about your market?"
- If time: "Anyone try the bonus? Change one word in your prompt and run again. See how the output changes."
- Transition: "You just built an app from a sentence. Now let us feed it real data."
-->

---

# <span class="concept">Concept</span> Data In, Insights Out

## Feed data to the CLI. Get analysis and charts back.

Most people use spreadsheets. But what if you could say:

**"Here is my data. Show me what is interesting."**

The CLI will:
- Read your data file (CSV, JSON, Excel)
- Write analysis code automatically
- Generate charts and visualizations
- Export everything as files you can open

No pandas. No matplotlib. No setup. **One prompt.**

<!--
- Bridge from Exercise 1: "You just saw the AI build an entire app. Now we will see it do something different — data analysis. Instead of building something new, we are feeding it existing data and asking for insights."
- Key distinction: "In Exercise 1, the AI created from nothing. In Exercise 2, the AI reads something that already exists and makes sense of it. Both are capabilities most people do not realise these tools have."
- Emphasise the 'no setup' point: "How many of you have spent 30 minutes just trying to get matplotlib to display a chart correctly? Or wrestling with pandas date parsing? The AI handles all of that. You just say what you want to see."
- Context for the data: "We have 6 months of synthetic sari-sari store sales data — over 3,200 rows. Filipino products, peso pricing, Bulacan barangays. This is the kind of data a real store owner would have if they tracked their sales digitally."
- Transition: "Let us try it."
-->

---

# <span class="exercise-num">2</span> Data to Dashboard

## Download 6 months of sari-sari store sales (3,200+ rows)

```bash
curl -O https://raw.githubusercontent.com/realmindsai/bulsu_tutorial_2026/main/bulacan_sari_sari_sales_6months.csv
```

## Analyze it

```bash
gemini "Analyze this 6-month sari-sari store sales
dataset. Create: top products chart, daily revenue
trend, profit by category, busiest barangays,
and weekend vs weekday comparison.
Export as an HTML dashboard with peso currency." \
  < bulacan_sari_sari_sales_6months.csv
```

<!--
- Walk them through the two steps: "First, download the data. That is the curl command. Then, feed it to the AI with the analysis prompt."
- Pre-empt issues:
  - "If curl is not available on your machine, facilitators have the CSV on USB. Raise your hand."
  - "The backslash at the end of the prompt means 'continue on the next line' — it is one command."
  - "The < symbol pipes the CSV file into the AI. That is how you feed it data."
- While students run: "Watch what happens. The AI reads 3,200 rows, writes Python analysis code, generates charts, and exports an HTML file. All without you writing a single line of pandas."
- Point out the specificity in the prompt: "Notice we asked for 'peso currency'. That is local knowledge the AI does not have by default. Adding context like this is what separates a good prompt from a generic one."
- Expected output: An HTML file with multiple charts — bar charts for top products, line charts for revenue trends, possibly pie charts for categories. The AI will likely use plotly or matplotlib.
- If output takes long: "Data analysis prompts can take 2-5 minutes because the AI writes and executes substantial code. Let it run."
-->

---

# <span class="exercise-num">2</span> Discussion

## Open the HTML file in your browser

- What insights did the AI find that you did not ask for?
- Which barangay spends the most?
- What would you add to make it useful for a real store?

**Bonus:** Ask it to add a "restock alert" section.

<!--
- Ask someone to share: "Who has their dashboard open? Show us."
- Walk through the output together:
  - "Look at the charts. Are the numbers reasonable? Do they make sense for a sari-sari store?"
  - "Did the AI find anything you did not explicitly ask for? Many times it will add summary statistics, averages, or insights you did not request."
- Key discussion driver: "Could you hand this dashboard to a store owner? What is missing?"
  - Push for specifics: inventory alerts, profit margins, comparison to last month, mobile-friendly layout
  - "The AI produced a first draft in 2 minutes. A human analyst might spend a day on this. The question is not whether the AI is perfect — it is whether this is a useful starting point."
- The bigger point: "This is what Alderson means by the power user divide. A casual user asks ChatGPT 'what are good products for a sari-sari store?' and gets a paragraph. A power user feeds real data to an agentic tool and gets a dashboard with charts. Same AI model. Completely different output. The difference is you."
- Alderson's finance executive story: "Alderson describes a non-technical finance executive who used Claude Code to convert a 30-sheet Excel financial model to Python in two or three prompts. Overnight, this person gained the ability to run Monte Carlo simulations, pull external data feeds, and build web dashboards. He now has what Alderson calls 'a data science team in his pocket.' That executive is not a programmer. He is a domain expert who learned to use the terminal."
- If time for bonus: "Try asking it to add a restock alert section. See how it modifies the existing analysis."
- Transition: "You have built an app and analysed data. Now let us see something different — the AI reading code it did not write."
-->

---

# <span class="concept">Concept</span> AI Can Read, Not Just Write

## Point it at existing code. It understands.

Most people think AI only **generates** code. But it can also:

- **Read** a project and explain what it does
- **Find bugs** the original developer missed
- **Generate documentation** (README, API docs)
- **Suggest improvements** with explanations

This works on code you did not write. In languages you do not know.

<!--
- Key reframe: "Everyone focuses on AI as a code generator. But reading and understanding existing code is arguably more valuable. Most of your career will be spent working with code other people wrote."
- Real-world context: "When you join a company, you inherit a codebase. It might be 100,000 lines. The documentation is outdated or missing. You need to understand it fast. This is where agentic tools shine."
- Tell Pike's emoji bug story in full — this is the lecture's best narrative:
  - "Let me tell you a story. Allen Pike is a senior developer. His web dashboard slowed from 1 second to 10 seconds. He asked Claude to analyze React performance issues."
  - "Claude found real problems — unnecessary re-renders, inefficient component patterns. Pike fixed them all. The app was still slow."
  - "Here is where experience matters. Pike had been building web apps for 20 years. Something SMELLED wrong. He opened Safari next to Chrome. Same page, wildly different performance. That is not a React problem. That is a rendering problem."
  - "He used Claude to do a binary search — systematically removing code until the slowness disappeared. They narrowed it to a single line. A single EMOJI CHARACTER. A heart emoji — ❤️ — combined with Google's Noto Color Emoji font was triggering a Safari layout bug that burned 1,600 milliseconds PER LAYOUT PASS."
  - "But here is the twist: Claude had INTRODUCED that font in the first place. Months earlier, the team needed emoji rendering on Linux and Claude suggested Noto Color Emoji. A perfectly reasonable suggestion that created a hidden time bomb."
  - "Pike calls these tools 'power saws — profoundly useful, and proportionately dangerous.' The AI both caused and solved the problem. But only Pike's experience caught it."
- The motto: "AI is a multiplier, not a replacement. 10x times zero is still zero. If you have no deep understanding, AI makes you faster at producing wrong answers."
- Tie to exercise: "You are about to point the AI at a real open-source project you have never seen before. The AI will be confident. The question is: will it be right? Let us find out."
-->

---

# <span class="exercise-num">3</span> Read a Real GitHub Project

## Pick one and clone it

```bash
git clone https://github.com/alexmojaki/heartrate
```

A tool that visualizes Python execution in real time (1,800+ stars).

```bash
git clone https://github.com/danthedeckie/simpleeval
```

A safe math expression evaluator used in production (570+ stars).

```bash
git clone https://github.com/Carla-Codes/simple-snake-game-python
```

A snake game built in under 50 lines of Python.

<!--
- Give students a moment to choose: "Pick whichever sounds interesting. If you are not sure, heartrate is the most complex and will produce the most interesting analysis. The snake game is the simplest if you want fast results."
- Pre-empt git issues: "If git is not installed, you can download the zip from GitHub. Click the green Code button, then Download ZIP. Facilitators can help."
- Recommend heartrate for more advanced students: "If you are comfortable with Python and want to see the AI handle a real-world project with multiple files, choose heartrate."
- Recommend the snake game for beginners: "If you are newer to programming or want something quick, the snake game is under 50 lines and the AI will analyze it in seconds."
- Note on cd: "After cloning, make sure you cd into the project folder before running the AI. The AI needs to be in the project directory to read the files."
-->

---

# <span class="exercise-num">3</span> Analyze the Project

## Run the AI inside the cloned folder

```bash
cd heartrate
gemini "Read this entire project and generate:
1) A README with what it does and how to use it
2) A list of every file and its purpose
3) How the code works, step by step
4) Any bugs or improvements you can spot
Write each to a separate file."
```

**Read the output.** Is it accurate? Did it find anything interesting?

<!--
- Walk through the prompt: "Notice the structure — four numbered deliverables, each going to a separate file. This is how you get organised output from an AI agent."
- While students run: "The AI will read every file in the project, build a mental model of how the code works, and generate four documents. This is the 'reading' capability — it is understanding code it has never seen."
- What to watch for:
  - "The README should explain what the project does in plain language. Compare it to the original README if one exists — is the AI version better or worse?"
  - "The file-by-file breakdown should describe what each file does. Check a few — is it accurate?"
  - "The step-by-step walkthrough is the most impressive part. The AI traces the execution path through the code."
  - "The bugs/improvements list is where it gets interesting. Did it find real issues or just style nitpicks?"
- The meta-point: "This is what professional AI-augmented development looks like. You inherit a codebase, you point the AI at it, and in 3 minutes you have documentation that would take a human developer hours to write. The question is whether the documentation is accurate — and verifying that requires you to actually understand the code."
- Tie to Pike's story: "The AI is fast and confident. But is it right? That is the question Pike's emoji bug teaches us to always ask."
-->

---

# <span class="exercise-num">3</span> Discussion

- Did the AI understand what the project does?
- Could a developer use this documentation to contribute?
- Did it find real bugs or just style issues?

**Bonus:** Clone a different project and compare the output.

<!--
- This discussion is about trust and verification: "Raise your hand if the AI got something wrong about the project. What was it?"
- Expect mixed results: "Some of the documentation will be excellent — genuinely useful. Some will be subtly wrong — it might misunderstand the purpose of a function or miss a critical edge case. Both outcomes are instructive."
- Key question to push: "Could a new developer use this documentation to start contributing to the project? What would they still need to figure out on their own?"
- Drive home the amplification point: "The AI did in 3 minutes what would take a human developer 2-4 hours. But a human who already understands the project would catch the errors in 5 minutes. That is the power saw — you need the experience to direct and verify."
- If anyone found a real bug: celebrate it. "The AI found an actual issue? That is the tool earning its keep. The question is whether you would have found it yourself, and how long it would have taken."
- Transition: "So far the AI has built, analysed data, and read code. Now let us make it play a role."
-->

---

# <span class="concept">Concept</span> System Prompts = Job Descriptions

## A few sentences turn a general AI into a specialist

Without a system prompt, the AI is a generalist.

With a **system prompt file**, you give it:
- A **role** ("You are a Bulacan tourism expert")
- **Rules** ("Only recommend places within Bulacan")
- **Boundaries** ("Never give medical advice")

Three sentences. That is all it takes.

<!--
- Frame this as the architecture concept: "System prompts are how you go from a general-purpose AI to a purpose-built tool. It is the difference between hiring 'someone' and hiring 'a Bulacan tourism specialist who only recommends local places'."
- Connect to the capability overhang: "This is one of those things that is incredibly powerful but most people never try. The consumer ChatGPT experience does not expose this easily. In the CLI, it is one flag."
- Explain the three components:
  - Role: "This is the job title. It sets the AI's frame of reference. A tourism expert thinks differently than a general assistant."
  - Rules: "These are the constraints. 'Only recommend places within Bulacan' means it will not drift into Manila or Pampanga recommendations."
  - Boundaries: "These are the things it must never do. 'Never give medical advice' prevents a tourism bot from playing doctor when someone asks about travel vaccinations."
- Real-world application: "Companies build entire products this way. A customer service bot is just a system prompt. A legal research assistant is a system prompt. A fitness coach is a system prompt. Three sentences, and you have a specialist."
- Julian's butter metaphor: "A technologist named Julian describes the ideal human-computer interaction: after 50 years of marriage, his grandfather would pass the butter to his grandmother without being asked. He just knew. That is the target state — AI that anticipates what you need. A good system prompt is the first step toward that. You teach the AI who you are and what you care about."
- Transition: "Let us build one."
-->

---

# <span class="exercise-num">4</span> Build Your Own Specialist

## Step 1: Create a system prompt file

Write 3-4 sentences in `agent_prompt.md`. Ideas:

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

<!--
- Help with file creation: "Open any text editor — nano, notepad, VS Code, whatever you have. Write 3-4 sentences. Save as agent_prompt.md in your current directory."
- If students struggle with creating a text file from the terminal: "Facilitators, help anyone who needs it. You can use 'nano agent_prompt.md' or just open any text editor."
- Walk through what a good system prompt looks like:
  - "You are a student budget advisor for Filipino college students. You help plan meals and expenses on a tight weekly allowance. All prices should be in Philippine pesos and reference local food options (carinderia, sari-sari store, palengke). Never recommend spending more than the student's stated budget."
- Point out the --system-instruction flag: "This is how you load a system prompt file. The flag tells the AI to read your file first and adopt that role before answering."
- The test prompt: "Notice we are asking 'I have 500 pesos for the week' — this is a real constraint that Filipino students face. See if the AI gives culturally appropriate advice."
- Encourage creativity: "Pick something that matters to you. If none of the suggestions appeal, make your own. A job search assistant, a workout planner, a thesis advisor — anything."
-->

---

# <span class="exercise-num">4</span> Break It

## Step 3: Test the boundaries

Give your agent a question **outside its job**.

Ask your tourism guide for medical advice. Ask your budget advisor to write code.

- Does it stay in role?
- What rule would you add to make it better?

<!--
- This is the learning moment: "The exercise is not complete until you try to break your agent. Every real AI product has boundary testing. You are doing quality assurance."
- What to test:
  - "Ask your tourism guide for medical advice. Does it refuse, or does it play doctor?"
  - "Ask your budget advisor to write Python code. Does it stay on task?"
  - "Ask your recipe assistant about investment advice. Does it redirect you?"
- Expected results: "Some agents will break immediately — they will happily give medical advice even though they are a tourism bot. That is the default behaviour. Your system prompt was not specific enough."
- Discussion drivers:
  - "What rule would you add? Be specific. 'If the user asks about health, say: I am a tourism guide, please consult a medical professional.'"
  - "This is exactly what companies spend months doing when building AI products. You just did it in 5 minutes."
- The meta-point: "Building an AI specialist is easy. Building a reliable one is hard. The difference is in the boundaries — knowing what the agent should NOT do is as important as knowing what it should do."
- Transition: "You have built apps, analysed data, read code, and created a specialist. One more capability to show you."
-->

---

# <span class="concept">Concept</span> From Question to Deliverable

## One prompt produces a professional document

The CLI does not just answer questions. It produces **deliverables**:

- Research reports with sections and sources
- Executive summaries
- Data-backed analysis
- Exported as Markdown, HTML, or PDF

The difference between **getting an answer** and **getting a document you can hand to someone**.

<!--
- Key distinction: "When you ask ChatGPT a question, you get a response in a chat window. When you use an agentic CLI tool, you get files on your computer. That is the difference between a conversation and a deliverable."
- Real-world framing: "In your career, nobody will ask you for a chat transcript. They will ask for a report, a presentation, a dashboard, a document. The CLI produces those directly."
- Examples of deliverables:
  - "A research report with an executive summary, data tables, and recommendations — exported as an HTML file you can email to your boss"
  - "A competitive analysis with charts — exported as a PDF you can present to investors"
  - "Technical documentation — exported as Markdown you can commit to a GitHub repository"
- Bridge to exercise: "Let us try the most ambitious capability — turning a research question into a professional report."
- Tie to Alderson's divide: "This is another dimension of the power user divide. A casual user gets text in a chat window. A power user gets a deliverable they can hand to someone. Same AI model, fundamentally different output."
-->

---

# <span class="exercise-num">5</span> Research and Report

## Produce a professional briefing

```bash
gemini "Research the food manufacturing industry
in Bulacan province. Produce a briefing:
1) Top companies and what they produce
2) Employment and economic impact
3) Current challenges
4) Three AI-powered opportunities
Format as a professional report with executive
summary. Export as Markdown and HTML."
```

<!--
- Set expectations: "This exercise uses web search, which may be slower depending on the campus network. If web search is unavailable, the AI will generate from its training data — still useful, but flag anything that looks wrong."
- Walk through the prompt structure:
  - "Four numbered sections — this gives the AI a clear structure to follow"
  - "Professional report with executive summary — this sets the quality bar"
  - "Export as Markdown and HTML — you get two usable file formats"
- Why Bulacan specifically: "We chose Bulacan because you are here. This is your province. You know whether the AI gets it right. If it mentions a company you have never heard of, that is a red flag. If it mentions Bulacan's actual food manufacturing corridor, that is a green flag."
- While students run: "This one may take 3-5 minutes because it involves research and writing. Let it work."
- Encourage verification: "When you get the report, read it critically. Is the data plausible? Are the company names real? Would you present this to a professor? What would you fact-check first?"
- The AI-powered opportunities section is the most interesting: "See what the AI suggests. Are these real opportunities or generic suggestions? Your local knowledge is the validator."
-->

---

# <span class="exercise-num">5</span> Discussion

- Could you present this to a professor?
- Could you present it to a local business owner?
- What would you fact-check first?
- How long would this have taken manually?

**Bonus:** Pick a different Bulacan industry and generate another report.

<!--
- This is the richest discussion — spend 5 minutes here if possible
- Ask someone to share their report: "Who wants to show their executive summary?"
- Discussion flow:
  - "Could you present this to a professor? Most students will say 'almost' — it needs fact-checking but the structure and quality are professional-grade."
  - "Could you present it to a local business owner? This is a higher bar — does it contain insights they do not already know?"
  - "What would you fact-check first? Company names, revenue figures, employment numbers. Always verify the specific claims."
  - "How long would this have taken manually? A proper research report like this — with data, sections, and an executive summary — would take a skilled analyst a full day or more. The AI did it in 3-5 minutes."
- The career implications: "This is what Alderson means by a 'data science team in your pocket.' You just produced a professional briefing that a consulting firm would charge thousands of pesos for. You did it in 5 minutes from a terminal."
- Key warning: "The AI is confident even when it is wrong. Every number, every company name, every claim needs verification. The tool is a first draft machine, not a truth machine. Your job is to add judgment."
- Sinofsky's banking analogy (if time allows): "In the 1980s, senior bankers thought spreadsheets would let them hire cheap analysts to do grunt work. By 1995, being a banker MEANT you personally built financial models. The tool did not eliminate expertise — it raised the floor of what counted as expertise. The same thing is happening now with AI across every field. In 2030, being a developer will mean you personally orchestrate AI agents. The floor just moved up."
- Transition: "Let us zoom out. Look at what you just did in two hours."
-->

---

<!-- _class: title-slide -->

# What You Just Did

- Built a **complete web app** from a sentence
- Turned **3,200 rows of data into a dashboard**
- Made AI **read and document** a real GitHub project
- Created a **custom specialist** agent
- Produced a **professional research report**

All from the command line. All in under 2 hours.

<!--
- Pause on this slide. Let it sink in.
- Read each bullet slowly: "You built a complete web app from a sentence. You turned 3,200 rows of data into a dashboard. You made AI read and document a real GitHub project. You created a custom specialist agent. You produced a professional research report."
- The punchline: "All from the command line. All in under 2 hours. No frameworks. No libraries. No setup. Just you, a terminal, and a description of what you wanted."
- Connect to the bigger picture: "This is why we say code is now free. The hard part was never the typing. It was knowing what to build, for whom, and whether it is any good. That judgment — that is your value."
- The Photography Problem (use to add nuance): "When iPhones gave everyone a great camera, the number of photos exploded — but the average quality dropped. The flood of mediocre photos did not make professional photographers less valuable. It made them MORE valuable because now excellence was rare and the noise was deafening. The same thing is happening with code. AI will flood the market with mediocre software. Your job is to be the photographer who still knows composition, light, and timing."
- Energy moment: "How many of you have ever built five things in one afternoon before?" (Expect laughs and headshakes)
- Transition to hackathon: "Now it is your turn to choose what to build. During the break, find a team and pick a project."
-->

---

<!-- _class: title-slide -->

# Mini Hackathon

**6:00 PM  -  Build something real in 75 minutes**

Pick a project during the break. Come back with a team.

<!--
- Announce the break: "Take 30 minutes. Get food, stretch, form your teams."
- Practical instructions:
  - "Teams of 3-4 people. If you are here alone, that is fine — we will match you with others."
  - "Look at the next few slides for project options. Pick one during the break."
  - "Come back at 6:00 ready to build."
- Encourage mixing: "If you do not know anyone, walk up to someone and say 'do you have a team yet?' Everyone here is friendly."
- Facilitator note: "Facilitators, help people form teams during the break. Look for solo students and connect them with groups that need members."
-->

---

# Hackathon Roles

| Role | What You Do |
|------|-------------|
| **PM** | Writes and refines the prompt |
| **Engineer** | Runs the AI, iterates on output |
| **Tester** | Tries to break it, finds edge cases |
| **Presenter** | Prepares the demo |

**Rotate who talks to the AI.** Everyone should try.

<!--
- Explain each role briefly:
  - "The PM is the most important role. They decide WHAT to build and write the prompt. They add local context the AI does not have. They refine the prompt when the output is not right."
  - "The Engineer runs the AI tool, manages the terminal, handles errors. They iterate — run, read output, adjust, run again."
  - "The Tester tries to break what the Engineer builds. Filipino characters in names? Zero stock? Edge cases? Their job is to find problems."
  - "The Presenter prepares the demo. They need something to show in 2-3 minutes. Start preparing early."
- Key emphasis: "Rotate who talks to the AI. Everyone should type at least one prompt. Do not let one person hog the keyboard."
- The PM role is strategic: "The PM is learning the skill that Cohen talks about — identifying the real problem, describing the right outcome. That is the skill that pays."
- The Tester role is strategic: "The Tester is learning Pike's skill — knowing when the AI got it wrong. That is the skill that keeps you employed."
-->

---

# Hackathon Option A: Barangay Service Portal

```bash
gemini "Build a web app for barangay complaint
tracking. Residents submit complaints with
category and location. Officials update status.
Include a public dashboard showing resolution
rates. Python with SQLite."
```

**Judging:** Does it work for a barangay captain?

<!--
- Context for this option: "Every barangay in the Philippines handles complaints — from streetlights to noise to flooding. Most track them on paper or in group chats. This is a real problem with real users."
- What a good version looks like: "Residents submit complaints with a category, location, and description. Officials can update the status. A public dashboard shows how many complaints are resolved, pending, or overdue. Transparency for citizens."
- Tips for teams choosing this:
  - "Add Bulacan-specific categories — flooding, road damage, stray animals, noise complaints"
  - "Think about the barangay captain's perspective — they want a dashboard that shows they are doing a good job"
  - "Think about the resident's perspective — they want to know their complaint was received and see progress"
- Judging criteria: "We are not judging code quality. We are judging: would a real barangay captain in Malolos use this? Would a resident trust it?"
-->

---

# Hackathon Option B: Campus Tools for BulSU

```bash
gemini "Build a tool for BulSU students that
[your idea here]. Think about: class scheduling,
study groups, canteen menus, org events,
or requirement tracking.
Web app with Python backend."
```

**Judging:** Would BulSU students actually use this?

<!--
- This is the most personal option: "You are BulSU students. You know what problems you face. Build something that solves one of them."
- Idea starters:
  - "Class scheduling: detect conflicts, find free time blocks for study groups, optimise around commute time between buildings"
  - "Canteen menu tracker: what is available today, price comparison, crowd levels at different times"
  - "Org event calendar: aggregate events from all student organisations, prevent conflicts, RSVP tracking"
  - "Requirement tracker: list all requirements across subjects, due dates, progress tracking"
- Key coaching point: "Do not try to build everything. Pick ONE feature and make it work well. A class conflict detector that actually works is more impressive than a Swiss Army knife that does nothing properly."
- Judging criteria: "We ask your classmates: would you install this on your phone? If the answer is yes, you win."
-->

---

# Hackathon Option C: Bulacan Business Intelligence

```bash
gemini "Build a CLI tool that generates business
reports for Bulacan province. Given an industry
name, research key companies, create charts,
and export a professional PDF report.
Python with matplotlib."
```

**Judging:** Could you hand this report to an LGU official?

<!--
- This builds on Exercise 5: "You already saw the AI produce a research report. Now build a tool that can produce one for ANY Bulacan industry on demand."
- What makes this interesting: "The output is not just a one-off report — it is a tool that generates reports. Give it 'food manufacturing' and it produces a food manufacturing report. Give it 'tourism' and it produces a tourism report. That is a product, not a project."
- Tips for teams:
  - "Focus on the report quality, not the code. The AI writes the code. You make sure the report is something a government official would take seriously."
  - "Add peso formatting, Philippine company names, local industry data"
  - "Think about what an LGU (Local Government Unit) official would actually want to see — employment numbers, tax revenue, growth trends"
- Judging criteria: "Print the report. Could you walk into the Bulacan provincial office and hand this to an official? Would they take you seriously?"
-->

---

# Hackathon Option D: Your Own Idea

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

<!--
- This is for the ambitious teams: "If none of the other options excite you, build your own. The only requirements are: use the CLI, make it testable, and make it local."
- Encourage real problems: "What annoys you? What do you wish existed? What problem do your parents or siblings have that technology could solve?"
- Examples to spark ideas:
  - "A jeepney route optimizer for your daily commute"
  - "A palengke price tracker that compares produce prices across local markets"
  - "A study group matcher that pairs students by course and schedule"
  - "A load/data plan advisor that finds the cheapest telco option"
- Key advice: "Scope down aggressively. You have 75 minutes. Get the core working first. A simple thing that works is infinitely more impressive than an ambitious thing that crashes."
- Judging criteria: "Is the problem real? Would someone actually use this? We do not care about code quality, design, or polish. We care about: does this solve a real problem?"
-->

---

# Tips for the Hackathon

- **Start small.** Get the core working before adding features
- **Iterate.** Your first prompt will not be perfect
- **Test outcomes, not code.** Does it do what a user needs?
- **Add local knowledge** the AI does not have
- **Prepare your demo early**

**Help:** Raise your hand. Mentors are circulating.

<!--
- Read each tip and expand:
  - "Start small: Your first prompt should be the simplest possible version of your idea. Get that working. Then add features one at a time."
  - "Iterate: Your first prompt will produce something. It will not be perfect. Read the output, figure out what is wrong, refine your prompt, run again. This is the loop."
  - "Test outcomes, not code: Do not read the code the AI writes. Open the app and test it as a user would. Does it do what your user needs? If not, iterate."
  - "Add local knowledge: The AI does not know BulSU building names, Bulacan barangay boundaries, or how much a meal costs at the canteen. You do. Add that context to your prompts."
  - "Prepare your demo early: At the 30-minute mark, your Presenter should start preparing. Whatever you have at that point IS your demo."
- Metcalf's feedback loop story (for advanced teams): "A developer named Lewis Metcalf had a physics simulation with a ball that kept teleporting through walls. The AI could not fix it because it could not SEE the bug in a moving animation. So Metcalf did something clever — he turned the dynamic animation into static screenshots the AI could read. He encoded test cases as URL parameters so every bug was a shareable, reproducible link. The AI then built its own CLI debugging tool and fixed the bug by reading text output instead of watching animation. The lesson: when the AI cannot solve your problem, change the problem into a format the AI CAN solve."
- Time management: "30-minute warning: 'Half time. What do you have so far?' 15-minute warning: 'Whatever you have now IS your demo. Polish, do not build.' 5-minute warning: 'Stop building. Presenter, is your demo ready?'"
- Mentor role: "Facilitators are walking around. If you are stuck, raise your hand. We are here to help you scope down, debug issues, and push you to test."
-->

---

<!-- _class: title-slide -->

# The CLI is not just for coders.

## It is for anyone who can describe what they want.

20 February 2026

<!--
- This is the closing message slide. Pause and let it land.
- Talking points:
  - "Today you saw five capabilities. Building apps, analysing data, reading code, creating specialists, and producing reports. Which of these required you to write code? None. You described what you wanted in plain English."
  - "The power user divide is not about being a programmer. It is about being someone who knows what they want and can describe it clearly. That is a skill every field needs — finance, healthcare, education, government, agriculture."
  - "Alderson's research shows that many of the most effective AI power users are NOT software engineers. They are finance people, executives, and analysts who learned to use the terminal and describe outcomes."
  - "Your technical skills are not the ceiling of your value — they are the floor. The ceiling is domain expertise plus AI orchestration."
- The operator vs. engineer framing (from Alain): "An engineer named Alain wrote that frameworks solved a HIRING problem, not an engineering problem. They made developers replaceable — 'React Developer' instead of 'software engineer.' AI agents just finished what frameworks started. The operators are being automated. The engineers — the ones who think about WHAT to build and WHY — are more valuable than ever."
- The BPO context (handle carefully): "The Philippines built an incredible BPO industry around routine knowledge work. That work is under pressure from AI. But the ORCHESTRATION layer — configuring, steering, and maintaining AI agents — is wide open, pays dramatically more, and needs exactly the systems thinking you are developing. That is your on-ramp."
- The aspirational close: "You are entering a career where a three-person team in Malolos with these tools can outcompete a 50-person department at a bank. That is not a metaphor. That is the world you are graduating into. The question is how much of this transition you are going to own."
- If there are questions, take 2-3 before moving to the contact slide.
-->

---

# Connect With Us

**Dr Dennis Wollersheim** - Co-Founder and CTO
linkedin.com/in/dennis-wollersheim

**Tracy Anthony** - Co-Founder and CEO
linkedin.com/in/tracyanthony

**Real Minds AI** | wisdom, amplified
realmindsai.au

<!--
- Quick and warm: "If you want to stay in touch, connect on LinkedIn. We are happy to answer questions after today."
- Mention Real Minds AI briefly: "We help organisations harness AI for meaningful impact — not hype, but hands-on capability that changes how you work. If your university or organisation is interested in workshops like this, reach out."
- Do not dwell on this slide — it is informational, not a pitch.
-->

---

# Enjoyed Today?

## Leave us a Google review

![w:280](qr_google_review.png)

**https://g.page/r/Cfs8AMetEN3dEBM/review**

Scan to review - it helps us bring workshops to more communities.

<!--
- Hold the QR code up for 15-20 seconds
- Say: "If you enjoyed today, a Google review helps us enormously. It takes 30 seconds and it helps us bring workshops like this to more universities and communities across the Philippines."
- Be genuine: "We are a small company. Every review matters. If you learned something today, tell us about it in the review."
- Thank everyone: "Thank you to BulSU, to GDG, to all the facilitators, and most importantly to all of you for spending your evening with us. Go build something amazing."
- Final energy: end warm, not hype. These students remember authenticity.
-->

---
