# Term 1 - Week 5: Machine Learning Basics

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
Income Predictor
**My pair partner:**
Oguzhan Bolluk (24124907)
**Tool we had to use:**
scikit-learn — the Python machine-learning library from this week's lecture. Work in Jupyter or in your editor.
**SDG we had to address:**
sdg 8 - decent work & economic growth
**What problem does it solve, and for whom?**

Many people with a low income do not get the financial support they are entitled to, often because they do not know about it or never apply. In the Netherlands, more than €1 billion of benefits (rent benefit, healthcare benefit and child budget) was not claimed in 2021 by households that had a right to it (CPB, 2025). Organisations that want to help these people have limited time and money, so they cannot contact everyone. They have to choose who to approach first.
Our user is a **social welfare organisation with a budget for 500 home visits per year**. The model predicts which people most likely have a low income (`<=50K`), so the organisation can use its limited visits for the people who need support the most. The people who benefit in the end are **low-income households** that would otherwise miss out on help.
A missed person (false negative) does not get support and may end up in debt. An unnecessary visit (false positive) costs capacity that could have helped someone else. That is why we chose balanced accuracy: the model has to find low incomes **and** avoid wasting visits.

**What did you build?**

We built a machine learning model (gradient boosting) that predicts whether a person has a low income (`<=50K`), based on details such as age, education, job, working hours and marital status. A social welfare organisation can enter a person's details and get a prediction and a probability, for example "low income, 99% chance". It can then use this to decide who to contact first with its limited budget of 500 home visits.

**Link to the live thing (if any):**

https://colab.research.google.com/drive/1YMcDwYLW7TYkk5X4bf6H9T-eSsrAcM3C?usp=sharing

**How do I run it?**

1. Open `Hackathon5.ipynb` in [Google Colab](https://colab.research.google.com).
2. Upload `adult.csv` with the folder icon on the left, so it is in the same folder as the notebook.
3. Choose **Runtime > Run all**. The notebook runs from top to bottom without extra installs. It takes about 5 to 10 minutes, mostly for the tuning in step 6.

**Python packages and versions** (all pre-installed in Google Colab):


| Package      | Version       |
| ------------ | ------------- |
| pandas       | 2.2.3         |
| scikit-learn | 1.6.1         |
| numpy        | Colab default |
| matplotlib   | Colab default |


To run it locally instead of in Colab: `pip install pandas==2.2.3 scikit-learn==1.6.1 numpy matplotlib jupyter`.

**Who did what?**
Ahmet: 
Google Collab 1-5
Readme.md
Ethical reflection
Oguzhan: 
Google Collab 5-6
Presentation
Dataset Card

**Ethical reflection - what are the risks of your tool? Who could it harm?**

- `sex` and `race` are **not** used as features. We kept them apart only to check the model's mistakes per group.
- Removing `sex` does not make the model blind to it: `relationship` and `marital.status` still carry this information.
- The census participants did not agree to this use of their data, and using tax data (`capital.gain`, `capital.loss`) would need a legal basis.
- This model should not be used for Dutch or present-day populations without retraining it on recent, local data.

The full ethical reflection is at the end of the notebook.

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
