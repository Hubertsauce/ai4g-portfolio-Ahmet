# Term 1 - Week 6: Language Models

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
Road Pulse

**My pair partner:**
Amien el Azzouzi (26159430)

**Tool we had to use:**
A pre-trained sentiment model from Hugging Face (https://huggingface.co/models), run with the transformers library, as in this week's lecture. 

**SDG we had to address:**
9 — Industry, Innovation and Infrastructure

**What problem does it solve, and for whom?**
_Name a real, specific user. "Everyone" is not a user._

User: the Highways team at Surrey County Council, the council with the most road reports in our data (19% of 4,188 reports). 

Problem: local roads in England and Wales face a repair backlog of £18.62 billion, and 49% of local roads have less than 15 years of structural life left (ALARM survey 2026). Residents report potholes and broken pavements on FixMyStreet every few minutes. The council handles each report as a separate job: a category, a location and a size. Nobody tracks how residents feel. Signals like “reported 3 times already” or “they said it was fixed, it hasn’t been” only become visible once frustration reaches the local news.

What Road Pulse does: it reads every new road and pavement report and scores its sentiment with a pre-trained transformer. It shows the Highways team, per hour or per day, when frustration rises above normal. With one click they can read the reports behind that dip and act before it escalates.

What it does not do: it does not measure road condition. A quiet area can still have bad roads, because not everyone reports online.

**What did you build?**
_Two or three sentences. What can a user actually do with it?_
Road Pulse collects new reports from FixMyStreet and uses a pre-trained Hugging Face transformer to classify the sentiment in each report as negative, neutral or positive. The results are shown on a dashboard, where users can look at changes by hour or day.

**Link to the live thing (if any):**
_Deployed URL, workflow export, video demo - whatever proves it works._
https://road-pulse-csahn7rlvryu8wmhxjjvyb.streamlit.app/

https://github.com/Hubertsauce/road-pulse.git

**How do I run it?**
_Short instructions so someone else can start it._
Open the live dashboard at https://road-pulse-csahn7rlvryu8wmhxjjvyb.streamlit.app/. Choose hour or day, filter by council or category, and click Lowest point (dip) or Highest point (peak) to read the reports behind it.

**Who did what?**
_Be honest about the split of work between you and your partner._
Ahmet: chose live dataset, wrote code for pull, streamlit, readme.
Anmien: both trabsformers, code for testing and testig it self, Powerpoint, 

**Ethical reflection - what are the risks of your tool? Who could it harm?**
_Every hackathon requires this. One honest paragraph beats three vague ones._

## Who is represented in the data?
FixMyStreet only includes people who choose to report problems online in English. This leaves out people who report by phone, people with limited access to digital services, and people who have stopped reporting. This means the data may represent some neighbourhoods better than others. We added a warning to the dashboard and explain in the README that a quiet area does not automatically have good roads.
 
## Mistakes made by the model
The model can classify a factual report as negative because it contains words about damage. It can also miss frustration that is implied or  misunderstand polite complaints. A council with many reports, or one very active reporter, can also affect the trend. The dashboard shows the number of reports next to each score, marks periods with fewer than five reports as unreliable, and allows users to read the reports behind a high or low point.
 
## Privacy
FixMyStreet reports are public. Its privacy policy says that names are shown only if a reporter chooses to provide them, and that the site provides RSS/JSON feeds for public reports. We chose not to store names, coordinates or photos because this information could help identify a person's home. However, around 8% of report texts include a house number, street name or postcode. A next step would be to remove these automatically before storing the text.
 
## Risk of relying on the score too much
A council might focus on the areas with the most complaints instead of the roads in the worst condition. It might also assume that a calm trend means there are no road problems, or use the score to judge individual staff. Road Pulse does not measure road condition and should not be used for those purposes.

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
