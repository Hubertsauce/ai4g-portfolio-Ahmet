# Term 1 - Week 2: Loops & Functions

---

## 1. Homework & workshop assignments -> [`homework/`](homework/)

**What was the assignment?**

**What did I hand in?**
_List the files, or link to them. Notebook exports, screenshots, scripts._

**What did I find difficult, and how did I solve it?**

### Checklist
- [ ] My workshop / homework files are in `homework/`
- [ ] Everything runs without errors, or I explained what does not and why

---


## 2. Hackathon prototype -> [`hackathon/`](hackathon/)

> Your tool and your SDG for this hackathon are announced at the **start of Friday's class**.
> Write them down here once you know them.

**Project title:**
Burnout Guard
**My pair partner:**
Allan Hassan (24097292)
**Tool we had to use:**
n8n.io
**SDG we had to address:**
SDG 3 - Good health & well-being
**What problem does it solve, and for whom?**
It helps high-stakes professionals, such as healthcare workers, emergency responders, and executive leaders who operate in "constant pressure" environments and often ignore early physiological and psychological signs of burnout (sleep problems, meeting density, extreme workload) until they reach a breaking point. This isn't just a personal wellbeing issue, burnout in these roles can lead to critical errors in high-stakes professional responsibilities since their decisions might have serious consequences and affect others' life.

**What did you build?**
An automated N8N workflow that acts as a proactive mental health assistant for high-stakes professionals. The system evaluates real-world calendar density across the work week. A Google Gemini AI node calculates a dynamic Burnout Risk Score and generates tailored Micro-Recovery Actions, such as a 5-minute walk or breathing break scheduled into open calendar gaps. These suggestions are delivered straight to the user's inbox via an automated Gmail briefing.

**Link to the live thing (if any):**
[Link naar Demo](https://drive.google.com/file/d/1R4wCZZu2-mUqCMFPTc8vj9ZhfTT3zVgw/view?usp=drive_link)

**How do I run it?**
1.	Import the workflow into n8n and connect Google Calendar, google sheets, Gmail and prepare a Gemini API key.
2.	The flow is setup to run automatically on the daily Schedule Trigger (default 8:00 AM) no manual action by the user is required.
3.	Each run fetches the user data including name, role, stress tolerance, preferred method for stress relief and their email address. Next, it reads the week's calendar, processes the day appointments and sends this data to the google gemini agent. The agent scores the Burnout Risk, and based on this evaluation, the right email is being generated and sent to the user via gmail.
4.	To test manually, use n8n's "Execute Workflow" button on the Trigger node.


**Who did what?**
•	Ahmet: Did research about burnout in health sectors, wrote the README and made the PowerPoint
•	Allan: 
o	Thought about what we are going to build, and came up with idea’s which are been discussed. Set up google cloud console, set up gemini API key and then created the workflow in n8n.
o	Recorded a short demo about how the flow works.
•	Both: 
o	Brainstormed about what we could potentially build to that aligns with SDG3.
o	Refined the presentation.
o	Filled the README file

**Ethical reflection - what are the risks of your tool? Who could it harm?**
•	Data Privacy: Burnout Guard uses Google Calendar for information every day. Meeting titles, attendee lists, and meeting times may show private details about the user.
To protect user privacy, all data processing must happen only within the n8n workflow in order to avoid any data leaks.
•	The World Health Organization (WHO) defines burnout as a work-related problem, not a medical condition. Suggestions made by AI in our tool are small, research-based and not medical treatments. 
A major risk is giving a “Low Risk” score when someone is actually experiencing burnout. The AI only looks at how busy a person’s calendar is. It cannot detect personal stress, emotional exhaustion, or work done outside the calendar.
•	Technical Failures and Protections:
o	External services may stop working, or the AI may produce incorrect results. This could cause important alerts to be missed.
o	We added a try-catch fallback in the Code Node. If the Gemini API stops working or returns information in the wrong format, the system catches the error. It then sends a general wellness checklist through Gmail instead of stopping completely.
o	Required disclaimer: Every email includes a clear message at the bottom:
“This automated briefing is an organizational nudge tool, not medical advice.”


### Checklist
- [ ] Prototype code (or export / workflow file) is in `hackathon/`
- [ ] This week's slides are in `hackathon/`
- [ ] The prototype actually runs, and I wrote down how to run it
- [ ] Ethical reflection written above

---

## 3. Presentation -> [`presentation/`](presentation/)

*Only fill this in for the week your group was selected to present. You need at least **one** of these across the whole term.*

- [ ] My group presented in this week
- [ ] Slides are in `presentation/`
- [ ] Proof of the live demo is in `presentation/` (recording, screenshots, or link)

**How did it go? What would I do differently next time?**

---

## 4. Reflection

**What is the most important thing I learned this week?**

**Where does this connect to "AI for Good"?**
_One concrete link to ethics, sustainability or social impact._
