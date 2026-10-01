# Term 1 - Week 4: Strings, Text & Files

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
Support your club. Not every new kit.

**My pair partner:**
Nina Borutyńska (25044923)

**Tool we had to use:**
ComyUI

**SDG we had to address:**
 SDG 13: Climate Action*

**What problem does it solve, and for whom?**
Every season, football clubs bring out a new kit. Many fans buy the new shirt every year, while the old ones pile up in the wardrobe. Football shirts are usually made of polyester, which is basically plastic made from oil.. One polyester shirt is responsible for about 20 kg of CO₂ over its lifetime. That is about the same as driving 140 km by car. And every time the shirt is washed, tiny bits of plastic end up in the water. 
The film is for **football fans in the Netherlands, around 15 to 25 years old, who buy the new club shirt every season.** For them, buying the new kit feels like part of supporting their club. And one shirt feels small and harmless. Where they will see the film: on TikTok and Instagram Reels, in the week a club launches its new kit. 
- People who already avoid fast fashion.
- People who don't follow football, because the story would not work for them. 

Sources:
- One polyester T-shirt ≈ 20.56 kg of CO₂ over its lifetime, about the same as driving 140 km. RMIT University study (2018), reported by ABC News (29 August 2023). https://www.abc.net.au/news/2023-08-29/researchers-find-one-polyester-shirt-creates20/102788106 *Note: this number is for a regular polyester T-shirt, not a football shirt specifically, so for our film it is an estimate.*
- Synthetic clothes (mainly polyester) cause up to 35% of the tiny plastic pieces (microplastics) found in the ocean. Environmental Science & Technology (2026), PMC12825150.
- One 6 kg load of laundry can release around 700,000 plastic microfibres. Scientific Reports (2025), PMC12859020.
- Recycled polyester is not the answer: it sheds about 55% more microfibres than new polyester. Changing Markets Foundation, "Spinning Greenwash" (2025). https://changingmarkets.org/report/spinning-greenwash/
- Football shirts are usually made of polyester. For example, the Ajax home shirt 2025/26 is 100% recycled polyester. Voetbalshop.nl: https://www.voetbalshop.nl/en/adidas-ajaxhome-shirt-2025-2026.html

**What did you build?**
We built a 33-second AI-generated short film, "Support your club. Not every new kit.", about the climate impact of buying a new football shirt every season. The film follows a young fan who keeps buying new kits until his wardrobe overflows, then zooms out to the factory where the polyester shirts are mass-produced and to the smoke rising from its chimneys, which drifts over a full stadium. It ends with a fact card and a call to action: wear your shirt for another season.

**Link to the live thing (if any):**
[_Deployed URL, workflow export, video demo - whatever proves it works._
](https://youtu.be/e02sWHgL7ko)

**How do I run it?**
We made the film in ComfyUI. Our laptop doesn't have a strong enough graphics card, and the free version of Comfy Cloud would not run our workflows. So we used RunningHub (runninghub.ai), a website that runs real ComfyUI in the browser. **Video clips** (`MiniMax H3 T2VA text to video.json`): 1. Open RunningHub, or any ComfyUI with the MiniMax H3 nodes. 2. Drag the JSON file into the ComfyUI window. 3. Paste the prompt of the shot you want into the **T2VA Text Encode** box. 4. Set the duration, width and height in the **T2VA Target** box. 5. Type the seed into the **Dual Sigma Sampler** box. 6. Give the file a name in the **Save Video** box and click **Run**. You can find the prompt, duration and seed of every shot in our shot list. **Text screens** (`Y-Z-Image-turbo-workflow.json`): 1. Drag the JSON file into the ComfyUI window. 2. Paste the text of the screen into the **CLIP Text Encode** box. 3. Type the seed into the **KSampler** box and click **Run**. RunningHub puts a small "RunningHub AI" logo in the corner of every video. We removed it only by cropping the image, not with any other AI tool, so everything in the film still comes from ComfyUI. ## Made with AI Everything in this film was made with AI. The fan, the factory and the stadium are not real, and nothing shown is a real place or event. 

**Who did what?**
Ahmet:
The video's using Comfyui
Storyboard
workflow's

Nina:
Presentation
Readme
uploaded on Youtube

Together:
We made the script together.

**Ethical reflection - what are the risks of your tool? Who could it harm?**
Our facts come from real sources. But the 20 kg CO₂ number is for a normal polyester Tshirt, not a football shirt, so it is only an estimate. The smoke over the stadium can look like a real fire, but it is not real. The factory, the chimneys and the stadium are all made up. We did not use real club names, logos or sponsors on purpose. Still, the AI sometimes added marks that looked like real sports brand logos. So we added "no badges" to our prompts, tried other seeds, but one logo that looks like Adidas is still visible in the film. The fan is not a real person, so we did not need anyone's permission. But the AI chose how he looks by itself. In our first version, the AI kept making East Asian faces for "a young man", and once it even made a young woman. So we changed the prompt to "a young Dutch man". This showed us that AI can be biased. Viewers know the film is made with AI because every shot has a "Generated by AI" label in the corner. The YouTube description and our README also say this. To get our 8 shots and 2 text screens, we made 39 generations in total. We think this is okay for a short film for fans who buy a new shirt every year. We also tried to use less energy: we tested at low quality first, used fewer steps (20 instead of 50) and used some clips again instead of making new ones. 


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
