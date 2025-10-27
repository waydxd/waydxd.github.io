# Project 2: Personal Diary and Reflection

**Project Title:** **Human-Robot Interaction for Disaster Management** 
Artificial Haven
**Submission:** P2.3 Personal Diary Page **Date:** October 26, 2025

This diary documents my personal journey, contributions, and critical reflections throughout the development of Project 2, focusing on the Human-Robot Interaction solution for disaster management. My aim is to convey not just the tasks completed, but the **intellectual challenges and personal ownership** I took on.

## 1. Empathize Stage: Establishing the User Need

**My Contribution & Reflection:**

My initial contribution was focused and intense: I co-led all primary research, which included securing, preparing for, and conducting all interviews and speed dating sessions with our volunteer, **Christy** (with group mate Angel). I didn't just record the answers; I focused on **synthesizing the underlying emotional and operational constraints**. Concurrently, I led the analysis of secondary research from online survivor accounts to establish a comprehensive context for conflict and disaster survival.

### A. Primary Findings (Interview with Volunteer Christy)

The interview with Christy provided the **core mandate** for the HRI agent, challenging our initial assumptions about what technology should prioritize:

1. **Conducting Informal Research:** The interview was deliberately kept **informal and conversational**, without a rigid script. My reasoning was that an informal approach would make Christy feel more relaxed, allowing her to speak her true, unfiltered thoughts without worrying about formal etiquette. This choice proved invaluable, as her most candid feedback—calling generic chatbots **"useless"**—provided a clear, high-stakes benchmark for our design.
    
2. **Crisis Priority:** Christy stressed that **getting people to shelters** is the single most urgent task. This was a critical pivot point, forcing me to recognize that many "advanced" HRI concepts (like long-term psychological support) become irrelevant if the basic safety task fails. Our focus had to be **immediate, actionable guidance**.
    
3. **HRI Rationale:** Christy’s skepticism about generic bots—calling them **"useless"**—hit hard. It was a direct rejection of low-effort AI solutions. This feedback, combined with her confirmation that **language barriers** were the massive operational challenge, transformed our HRI goal: the agent must be an **accurate, real-time, task-specific, and multilingual** communication tool. This meant the reliability of the voice interface became a design imperative, not an afterthought.
    

> **Process Documentation:** Evidence of this stage includes **screenshots of the Microsoft Teams interview with Christy**. Due to privacy concern, Christy prefers not to share the recording to others.

<img src="/courses/4461/Screenshot 2025-10-26 at 12.34.09 PM.png" alt="Interview screenshot" style="display:block;margin:0 auto;max-width:640px;width:100%;height:auto;" />

### B. Secondary Findings (Reddit Survivor Accounts)

The secondary research was personally moving and provided crucial **contextual survival constraints**. Reading firsthand accounts of civil war solidified my conviction that the HRI solution had to be simple, discreet, and reliable:

1. **Emotional Weight of Survival:** The accounts describing the shift from denial to desperation within a week and the pervasive **trauma and moral degradation** (Source 3, 6) emphasized the user's extreme cognitive load. My reflection here was that the UI couldn't be complex or visually busy; it needed a **calming color palette, clear text, and high-contrast elements** to function as an anchor during panic.
    
2. **The Imperative of Discretion:** The stress on **blending in, laying low, and avoiding drawing attention** (Source 1, 10) was a direct challenge to the idea of a flashy, conspicuous robot. This finding strongly influenced my later UI design, pushing it toward maximum clarity with minimal visual noise, treating the HRI system as a necessary tool, not a spectacle.
    

**My Synthesis and Impact:** My role ensured the **scenarios identification** was deeply grounded in empirical data and emotional reality. The final design mandate I championed was that the agent must be perceived as a **life-critical, reliable tool** that prioritizes immediate, actionable information, recognizing the profound fear and stress of the end-user.

## 2. Ideate Stage: From Needs to Concepts

**My Contribution & Reflection:**

While the Ideate stage was a comprehensive **group effort**, my personal experience was defined by a struggle with **communication and advocacy**. I found myself hesitant to present my best ideas, partly because I'm not good at explaining abstract concepts, and partly due to a deep aversion to defending my proposals against what I perceived as "stupid questions" or unnecessary suspicion from teammates.

The **"speed dating"** session, which Angel and I co-led, was the inflection point. We presented three distinct concepts, but Christy’s immediate reaction—that the ideas should be **"merged"** to prioritize getting people to safety—was a powerful validation of our Empathize work. I strongly advocated for the final concept that integrated the multilingual AI's strength with the core task of **shelter routing and queue management**.

My reflection on collaboration here is mixed: I disliked the friction of working with people who didn't immediately grasp the vision, but I also struggled to communicate effectively, realizing the fault wasn't purely external. The real lesson learned is the necessity of **finding a balance** in collaboration—not just with people's skill levels, but in developing the resilience to advocate for good ideas clearly, even when facing internal resistance or doubt. The outcome, **responsible convergence**, was ultimately successful because the user's voice broke the deadlock.

## 3. Prototyping & Implementation: From Concept to System

**My Contribution & Thinking (Primary Focus):**

This phase was my technical and execution battlefield, where the constraints of collaboration and tooling became most acute. Working closely with Harry, I owned the deployment pipeline and the front-end user experience, tackling several critical implementation hurdles.

### A. Prototyping Strategy & Tooling Dilemma

I was the main driver in defining and executing the **mixed Vertical + Horizontal prototyping strategy**. This was a deliberate choice to de-risk the project by guaranteeing the functionality of the **Vertical Path** (Voice Intake → Queue Handoff), which was the **core HRI demonstration**. My personal belief was that a fully functional core, even with simulated ancillary features, was infinitely more valuable than a fragile, fully "Wizard-of-Oz'd" system.

However, this stage introduced a significant **tooling constraint**: we were locked into **Streamlit** (an earlier group choice). Streamlit is poor for custom UI/UX, which made achieving a truly **mobile-responsive and clean disaster-relief UI** exceptionally difficult. Although I knew a different framework (like a modern JS framework) would have offered greater extensibility, I reluctantly agreed to stick with Streamlit to **avoid wasting the existing work** of my groupmates, which felt like a necessary collaborative compromise at the time.

### B. Core Technical Contributions & The "Wasted Work" Reflection

- **UI Design and Horizontal Prototype:** My greatest time investment was in the **UI/UX design**. I led the creation of the **horizontal prototype**, meticulously mapping out the operator dashboard and the user-facing screens. The difficulty in customizing Streamlit forced me to invest far more time than anticipated simply to achieve a minimally acceptable mobile-responsive layout.
    
- **Vertical Chatbot Prototype (Offline Solution):** I took ownership of structuring the **offline solution** for the vertical chatbot. This was technically challenging because it required hard-coding the complex conversational decision tree and state management without relying on external API calls. This ensured the core HRI dialogue—the very thing Christy asked for—was **robust and instantly responsive**, even in a simulated disconnected environment.
    
- **Deployment for Usability Testing:** I handled the complete **deployment to the public server**. This involved navigating various hosting constraints and ensuring cross-browser compatibility, a non-trivial task that guaranteed our group could collect real-world usability data without technical failure.
    
- **The Protracted Planning Dilemma:** My greatest frustration came when some of my work—work that adhered to the initially defined scope—was later deemed peripheral, replaced, or not demonstrated directly in the final video. This felt like a profound **waste of effort**. This experience left me confused: should we have **"frozen" the requirements** with proper early planning to prevent wasted effort, or must we simply accept that the **prototype process requires rapid, evolutionary changes** that inevitably lead to discarded work? I learned that balancing these two philosophies—the **structured plan** versus the **agile pivot**—is perhaps the hardest part of any collaborative engineering project.
    
- **Video Demo Footage:** I personally recorded and edited the screen captures for the final video demonstration.
    

> **Process Documentation:** The **video footage of the app usage** demonstrates the fully functional vertical paths: Voice Intake, Queue Handoff, and Multilingual Announcement Playback.

<video controls preload="metadata" style="display:block;margin:0 auto;max-width:640px;width:100%;height:auto;">
  <source src="/courses/4461/Diary.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<video controls preload="metadata" style="display:block;margin:0 auto;max-width:640px;width:100%;height:auto;">
  <source src="/courses/4461/music_80OhDr6r.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<video controls preload="metadata" style="display:block;margin:0 auto;max-width:640px;width:100%;height:auto;">
  <source src="/courses/4461/sidebar_BCrJaUlT.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<video controls preload="metadata" style="display:block;margin:0 auto;max-width:640px;width:100%;height:auto;">
  <source src="/courses/4461/sidebar_BCrJaUlT copy.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

**Reflection on AI Usage ("Vibe Coding"):**

I utilized AI tools in the prototyping phase for what I call "**vibe coding**" and aesthetic scaffolding. Specifically, I leveraged the AI to quickly generate the initial CSS structure for the Streamlit UI, especially for responsive layouts and card designs. This wasn't lazy coding; it was **strategic acceleration**. It allowed me to bypass tedious styling tasks and dedicate my focus to the complex, hand-written core logic—the conversational flow, state handling, and the offline solution—which I **meticulously examined and engineered myself**. My final code, while AI-assisted in form, was entirely my responsibility in function and integrity.

## 4. Presentation & Finalization: Documentation and Results

**My Contribution & Reflection:**

In the final documentation phase, my focus shifted to **translating technical effort into measurable results**.

- **Presentation and Report Writing:** I was primarily responsible for writing the **Usability Testing results** section. This involved the tedious but crucial task of synthesizing raw quantitative Likert scale data and qualitative open-ended comments into clear, defensible conclusions. My goal was to prove, using the data, that our vertical path had successfully reduced cognitive load and increased user confidence, thus directly addressing the concerns raised in the Empathize stage.
    

> **Results Documentation:** The **questionnaire report charts** summarize the user satisfaction, confidence, and cognitive load metrics gathered during the usability test runs, demonstrating the success of the HRI design.

[Download the questionnaire report (PDF)](/courses/4461/4461.pdf)

<details>
<summary>View embedded PDF (may not display in all browsers)</summary>

<embed src="/courses/4461/4461.pdf" type="application/pdf" width="100%" height="480px" />

</details>

- **Documentation:** I authored the detailed descriptions of the **horizontal prototype** and created the **"System at a Glance" diagram**. My design philosophy here was to provide a visual aid that instantly communicated the system’s complexity to a non-technical audience. I was passionate about this diagram because it showed the full scope of our design thinking, even if some parts were simulated.
    

My reflection here is that the final stage is about **advocacy for your work**. Writing the results section forced me to prove that the late nights spent engineering the vertical path actually paid off in tangible, measurable user benefits, providing a final justification for the challenging process.

## Overall AI Usage Summary

AI tools were a significant aid but not a replacement for critical thinking or implementation:

1. **Vibe Coding (Prototype):** Used for front-end styling and boilerplate code generation.
    
2. **Personal Reflection Drafting:** Used to structure initial thoughts and ensure all required points for this diary were covered.
    
3. **Presentation Slides:** Used for initial layout and drafting of clear, concise talking points.
    

In all instances, the AI output was treated as a powerful first draft, requiring my review, verification, and finalization to meet the academic standard and ensure the quality and integrity of the project artifact.

## Appendix

<details>
<summary>View embedded PDF (may not display in all browsers)</summary>

<embed src="/courses/4461/COMP4461-Google-doc.pdf" type="application/pdf" width="100%" height="480px" />

</details>