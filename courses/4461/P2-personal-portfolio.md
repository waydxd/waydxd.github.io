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


# Appendix
<!-- markdownlint-disable MD033 -->
<details>
  <summary><strong>Show / hide appendix & notes</strong></summary>

  You can hide or reveal the appendix and extra notes using this toggle. This uses the HTML5 <code>&lt;details&gt;</code> / <code>&lt;summary&gt;</code> element supported by modern browsers and GitHub Pages.

  <!-- Paste long notes, TODOs, or the COMP4461 text below -->
TODO List

# **TODO**

| **Task** | **Timeline** | **Notes** |
| --- | --- | --- |
| User Observation & Scenario Identification -> Narrow down direction | Before Weekend Meeting<br><br>(Oct 4-5) | <https://www.when2meet.com/?32688269-8GMQu><br><br><https://www.figma.com/board/Hkx3jacKqrfwbS9ssjs77e/COMP4461?node-id=0-1&t=9thcFDks0q9P6Mma-0> |
| --- | --- | --- |
| Story Board | By Oct 8 11:59 | Idea 1: Harry  <br>Idea 2: Angel<br><br>Idea 3: Voiresa |
| --- | --- | --- |
| Interview | Oct 9 - 12 |     |
| --- | --- | --- |
| Finalize Idea | Oct 12 - 13 |     |
| --- | --- | --- |
| Build Prototype | Oct 13 - 16 |     |
| --- | --- | --- |
| Video Demo | Oct 17 - 18 |     |
| --- | --- | --- |
|     |     |     |
| --- | --- | --- |
|     |     |     |
| --- | --- | --- |
|     |     |     |
| --- | --- | --- |


# **Project 2 Description**

**COMP4461 Project 2 Human-Robot Interaction for Disaster Management**

**Deadline:**

- Thu Sep 25: P2.0 Project 2 announcement
- Wed Oct 8 Lab: HRI programming session 1
- Wed Oct 15 Lab: HRI programming session
- Wed Oct 22: P2.1 Submit video of working demo and slides to Canvas
- Thu Oct 23: P2.2 In-class presentation & evaluation
- Mon Oct 27: P2.3 Submit P2 personal diary page to Canvas (11:59pm)

**Project Description**

- ~~If staying in the same group as in Project 1 (switching groups is also allowed)~~
  - ~~Swap task assignments among members~~
- Empathize
  - Observe and/or interview users
  - Identify in what scenario(s) a **voice agent/chatbot/physical robot** can facilitate **disaster management** (e.g., shelters, hospitals, response center, volunteers, impacted communities, etc.)
  - **Note that it can be any types of disaster happening anywhere in the world -- but ensure that you empathize with real users (not on hypothetical situations)**
- Ideate:
  - Construct POV
  - Brainstorming ideas
  - Storyboarding of various alternatives
  - Speed dating for verification to help narrow down the design
- Build a prototype of your final proposed HRI solution
  - The conversation part needs to be a working prototype
  - Other features can be prototyped through other tools
- Compile a video demo and conduct usability testing
  - Document the live demonstration and testing - invite someone who is not from your team as the user
  - Actually **implement the core interactions**
    - Apply vertical prototyping to your key features, which, in the video, should be recorded live demos (no wizard-of-the-oz)
    - The other less critical features can apply horizontal prototying and be demonstrated through other means such as wizard-of-the-oz
    - For example, if you propose a physical robot that can comfort victims, the dialogue part needs to be functional, while the appearance of the robot can be illustrated through sketches or 3D models, and its movement can be manually manipulated.
  - Submit the video link and the presentation slides to Canvas
- Present your group project in class
  - Describe your empathy + ideation + prototyping process
  - Video showcase
  - Feedback from the user testing and reflection
  - Q&A
  - Peer + TA evaluation
- Write your personal diary of Project 2
  - Document the process and results with text, pictures, videos, etc.
  - Stress your own contribution and thinking
  - Reflect on the usage of AI tools, if any
  - Submit the page link

**Flow of P2.2 Presentation (8 min presentation + 1 min Q&A per team)**

- Brief introduction
  - Group
  - Topic
  - …
- Present your design process and outcomes with evidence
  - Justify your design decisions
  - Submit and test your slides and video beforehand
  - The presentation should be self-explanatory
- Summary
  - In case you have anything to add or clarify
- Q&A
  - Every member needs to answer at least one question from the audience

**Criteria used in P2.2 Peer + TA Evaluation (group-based)**

- Overall
  - Human centricity
  - Appropriateness of usage scenario identified
  - Practicality of the proposed HRI solution
  - Appropriateness of the design process
  - Presentation and Q&A quality
- User experience with the robot/agent/chatbot system, as shown in the video
  - Usefulness
  - Engagement
  - Interactivity
  - Reliability
  - Satisfactory

**Requirement for P2.3 Personal Diary**

- Project 2 page with a complete personal diary of the project
- Highlight your own contributions and thoughts (reflection) on the project
- Acknowledge your AI usage, if any

**Note**

- Your final score (total 20 pts) = group performance (15 pts: based on in-class peer + TA evaluation & participation) + individual performance (5 pts: diary)
- Chatbot dialogue flow

Meeting Minutes

## 2025年9月30日 | COMP 4461 Project 2 Meeting 1

Participants: Everyone

Empathize

- Disaster Management
  - Earthquake?
  - Command center in natural disaster?
- Jenson
  - Agentic AI - use a group of AIs?

## 2025年10月4日 | COMP 4461 Project 2 Meeting 2

Participants: Everyone

Project direction

- Emotional support?
  - In situations without internet -> starlink (see: Russia - Ukraine war)

## 2025年10月8日 | COMP 4461 Project 2 Meeting 3

Participants: Everyone

- Interview
  - Several different groups
    - People who have experienced war
    - People who have not experienced war (imagine)
- Storyboard
  - Three ideas
- Questionaire

##

Empathize


**Scenario**

- War Area
  - Bomb attacks -> escape to bomb (air raid) shelters
  - Hearing bombs -> trauma, petrified / paralyzed, desensitised
  - Discovering a trap / stepping on a trap

**POV Users Needs Insights**

- Users near potential bomb attack areas need a way to help them avoid danger, especially because they might be paralyzed from fear
- Users in war areas need a way to reconnect with family members they were separated from
- Users escaping from attacks in war zones need guidance to shelters
- Users who discovered / stepped on a trap need to remain calm and deactivate the trap safely

### **Point of View Statement**

In war zones, civilians facing trauma, displacement, and fragmented services need a resilient, offline AI voice agent that can guide them through shelters and clinics, provide empathetic psychological support, and securely help reconnect families. This agent should operate locally-first with multilingual voice interaction, structured intake and wayfinding, simple triage and announcements, and privacy-by-default missing-person matching, while prioritizing safety, consent, and human-in-the-loop verification to reduce harm, prevent misuse, and maintain trust in hostile, low-connectivity environments.

**Solutions**

- Using voices to snap them out of petrified state
- Offline / pre-downloaded maps to direct users to shelters
  - Internet -> update map based on situation

**Idea 1: Voice Agent for Psychological Support**

- Hardware
  - Starlink (Satellite Internet)
    - We assume that this is provided everywhere :D
    - Offline mode: Core functions must operate without any internet connection
    - Data compression: Optimize for low-bandwidth scenarios (< 100 kbps)
  - Built for hostile conditions
    - Waterproof/dustproof rating: IP67 or higher
    - Shock-resistant design: Military-grade drop test standards (MIL-STD-810G)
    - Extended battery life: Minimum 72-hour operation, solar charging capability
    - Bone conduction microphone: Captures voice in extreme noise environments
    - Multi-microphone array: Beamforming technology to isolate voice from explosions/sirens
    - Temperature tolerance: -20°C to 60°C operating range
  - Voice (speakers)
    - High-volume output: Clear audio in noisy environments (90+ dB)
    - Directional speakers: Privacy protection, prevents others from overhearing sensitive conversations
    - Haptic feedback: Vibration alerts when audio isn't feasible
- App or specific device?
  - App -> for people wPyith phones
    - More features
  - Specific device for people without access
    - Only contains LLM and other simple features such as alerts and GPS?
    - Basic survival tool integration: Flashlight, SOS signal light, FM/AM radio
    - Physical emergency button: One-touch connection to human responders
    - Simplified interface: Large buttons, high-contrast display, operable under stress
    - Ruggedized e-ink display option: Power-efficient, readable in direct sunlight
    - Distributed to disaster areas if necessary
- Features
  - Emergency Alert System
    - Automatically activates when there's an emergency
    - Emergency mode? (Built-in feature in modern phones)
    - Geofencing triggers: Automatic detection when user enters dangerous zones
    - Sound pattern recognition: Detects explosions, gunfire, sirens and auto-activates
    - Mass alert broadcasting: Sends threat warnings to all users in the area
    - Safe route recommendations: Plans evacuation routes based on real-time conflict data
    - Shelter locator: Identifies nearest safe spaces, hospitals, aid stations
    - Silent mode: Visual-only alerts when sound would compromise safety
  - LLM Features
    - Provide directions
      - Multimodal navigation: Voice + simple arrow indicators (low cognitive load)
      - Landmark-based navigation: Uses local buildings rather than street names (street signs often destroyed in war zones)
      - Danger zone marking: Integrates real-time conflict data to avoid active combat areas
      - Offline maps: Pre-cached regional maps with last-known safe routes
      - Crowd-sourced updates: Users can report blocked/unsafe routes
    - Psychological support
      - Trauma-informed dialogue: Questioning approaches that avoid re-traumatization
      - Cultural adaptation: Adjusts support style based on user's cultural background
      - Tiered support levels:
        - Immediate calming (breathing exercises, grounding techniques)
        - Short-term coping strategies
        - Long-term psychological resilience building
      - Special population modes: Customized support for children, elderly, pregnant women
      - Collective trauma response: Addresses community-level distress, not just individual
      - Grief support: Specific protocols for loss and bereavement
      - De-escalation techniques: For panic attacks, acute stress responses, dissociation
      - Psychoeducation: Normalizes trauma responses ("What you're feeling is a normal reaction to abnormal circumstances")
    - Detect whether a user requires special attention, and alerts management personnel
      - **Multi-dimensional crisis detection:**
        - Language patterns (suicidal ideation, extreme hopelessness, dissociation symptoms)
        - Voice characteristics (trembling, rapid speech, abnormal calmness)
        - Behavioral patterns (sudden usage frequency changes, midnight distress calls)
        - Physiological data (if sensors available: abnormal heart rate, rapid breathing)
        - Contextual factors (location in high-risk area, time since last traumatic event)
      - **Tiered response system:**
        - Level 1: Enhanced AI support (more empathetic, frequent check-ins)
        - Level 2: Connect to trained peer volunteer
        - Level 3: Professional mental health worker
        - Level 4: Emergency medical/security intervention
      - False positive management: Avoids excessive alerts causing alarm fatigue
      - Human-in-the-loop verification: Critical alerts reviewed by trained staff before escalation
      - Privacy-preserving flagging: Alerts responders without exposing full conversation content

\- Offline Content Library

- **Pre-loaded resources:**
  - Grounding techniques (5-4-3-2-1 sensory exercise, etc.)
  - Guided breathing and meditation
  - Culturally-specific prayers/meditation content
  - Basic first aid guide
  - Water purification, shelter building, survival skills
  - Common trauma responses and coping strategies
- **Children's section:**
  - Calming stories, simple games
  - Guidance for parents to comfort children
  - Age-appropriate explanations of war/disaster
  - Agent Requirements
    - ASR should tolerate heavy noise and strong accents (discussion only)
    - Stress speech recognition: Speech patterns change under traumatic stress
    - Multi-language dialect support: Including minority languages and mixed languages
    - Code-switching handling: War zone residents often mix multiple languages in sentences
    - Low-resource languages: Develop solutions for languages lacking training data
    - Child speech recognition: Specialized models for younger users
    - Whispered speech detection: For situations where speaking loudly is dangerous
- Technical Implementation
  - LLM
    - Search for LLMs built for this purpose

**\- Base model selection:**

- Online: Med-PaLM derivatives, Mental-LLaMA, specialized trauma-care models
- Offline: Llama 3.2 (1B/3B), Phi-3-mini (quantized to 2-4 bit), Mistral 7B (quantized)

**\- Model architecture requirements:**

- Fast inference (< 500ms response time)
- Small memory footprint (< 4GB RAM)
- Multilingual capability
  - - Reinforcement learning w/ database (ideally)
      - Prompt Engineering
  - Hardware (for people without phones)
    - Purpose-built device, with a screen, microphone, speakers
      - Screen specs: E-ink (power-efficient) or high-brightness LCD (readable in sunlight)
      - Processor: Capable of running quantized LLM (e.g., Qualcomm Snapdragon 8 Gen series or equivalent edge AI chip)
      - Storage: Minimum 8GB for offline models and content library
      - RAM: 4-6GB for smooth LLM inference
      - Sensors (optional): Heart rate, accelerometer (detects falls/immobility), GPS
      - Connectivity: 4G/5G, WiFi, Bluetooth, satellite (Starlink/Iridium)
      - Form factor: Pocket-sized (< 200g), wearable clip option
    - Connect to our backend / go to our webpage
      - Progressive enhancement: Works better with connectivity but functional offline
      - Secure communication protocols: TLS 1.3, certificate pinning
- Consent
  - Obtain when download app // before disaster occurs
  - Layered Consent Framework
    - Basic usage consent:
      - Clearly explains AI nature and limitations
      - Data collection scope (anonymized telemetry vs. conversation content)
      - Right to withdraw at any time
      - Plain language + visual explanations (for literacy barriers)

### **Idea 2: Voice Agent for Practical Guidance**

Scope/Safety

- Operational guidance at shelters/clinics/aid points.  

- No medical advice or diagnosis; only routing/triage questions.  

Hardware/Connectivity

- App first; works offline; syncs when online.  

- Simple staff console (phone/tablet) to set queues/announcements.  

Features

- Spoken intake → structured card (household, meds/allergies, special needs) → QR/short code.  

- Wayfinding + estimated wait; voice call-up.  

- Multilingual announcements from local phrase packs (offline OK).  

- Simple symptom triage Q&A → directs to correct line.  

Agent Requirements

- ASR with hotwords (names/places/meds).  

- Multilingual TTS; interruptible prompts.  

Technical Implementation

- Local form cache; conflict-free sync.  

- Operator inputs crowd level; basic counter integration (manual or sensor).  

Consent

- Intake card shows what's stored/shared; opt-in for data share to orgs.  

MVP Demo

- 3 flows: intake→card, queue handoff/call-up, multilingual announcement.  

Metrics

- Avg registration time; data completeness; misrouting rate; comprehension score.

### **Idea 3: Family Searching**

Scope/Safety

- Missing-person registration, matching, and safe contact.
- Privacy by default; protect at-risk groups (children, women, etc.).

Hardware/Connectivity

- App + volunteer web/terminal; low-bandwidth text broadcast.
- Works local-first; relays when online.

Features

- Voice registration → structured record (name/nickname, relation, last-seen time/place, features, safe callback).
- Local/nearby broadcast to boards/volunteer consoles.
- Optional on-device embeddings for photo/voice; no raw biometrics sent by default.
- Double-consent contact; sensitive location delayed disclosure.

Agent Requirements

- Agent should be able to report fraud and abuse (e.g. impersonation)
- Tiered privacy defaults (stricter for minors).

Technical Implementation

- Edge-preferred matching; hash/ID only sharing.
- Human-in-the-loop verification for uncertain matches.

Consent

- Explicit opt-ins for any public/posting; per-match consent before reveal.

MVP Demo

- Register → broadcast → match → contact across two volunteer terminals + one survivor app; offline→online handoff.

Metrics

- True-match rate; time to confirmation; false positives; perceived safety.

## **Additional Ideas for Disaster Management HRI**

### **Idea 4: Adaptive Crowd Coordination Agent**

**Problem**: In mass evacuations or shelter arrivals, panic spreads quickly and bottlenecks form when people don't know where to go or what to do next.

**Solution**: A distributed voice agent system that manages crowd flow dynamically:

- **Features**:
- Real-time crowd density monitoring (via phone signals, simple sensors, or volunteer reports)
- Dynamic route adjustment: "Gate A is full, please proceed to Gate C"
- Staggered departure instructions to prevent stampedes
- Group-aware guidance: "Families with children under 5, proceed first"
- Panic detection through aggregate voice analysis → switches to calming, slower speech
- **Hardware**: Wall-mounted speakers + mobile app + simple volunteer terminals
- **Offline capability**: Pre-cached priority rules and basic routing logic
- **Trust building**: Shows real-time numbers ("47 people ahead of you") and transparent reasoning

### **Idea 5: Skills-Matching Volunteer Hub**

**Problem**: Volunteers arrive with diverse skills but often get assigned randomly or wait idly while critical gaps exist elsewhere.

**Solution**: Voice-first volunteer intake and dynamic task matching:

- **Features**:
- Rapid skill assessment: "Do you speak Mandarin? Can you lift 20kg? Have medical training?"
- Real-time task board: "We need 3 Arabic translators at Shelter B, 2 drivers with trucks at Supply Point D"
- Shift scheduling with fatigue tracking: "You've worked 8 hours, take a 2-hour break"
- Training-on-demand: Voice-guided micro-lessons (basic first aid, food distribution protocols)
- Credentialing verification through voice + simple photo upload
- **Integration**: Connects to your Idea 2 (Practical Guidance) to route volunteers where help is needed
- **Safety**: Tracks volunteer locations for their safety; alerts if someone hasn't checked in

### **Idea 6: Multi-Sensory Accessibility Companion**

**Problem**: Visually impaired, deaf, cognitively disabled, or non-literate survivors face extreme barriers in chaotic disaster environments.

**Solution**: Adaptive multimodal agent that switches interaction modes based on user needs:

- **Features**:
- **For blind users**: Spatial audio navigation ("water station 3 meters ahead on your right"), haptic feedback patterns (vibration codes for alerts)
- **For deaf users**: Visual symbol language + sign language avatar on screen, flash alerts
- **For cognitive disabilities**: Ultra-simplified language, pictogram interfaces, repetition without frustration
- **For illiterate users**: Icon-based menus, voice-only interaction with no text requirements
- Device pairing with assistive tech (screen readers, hearing aids, wheelchairs with sensors)
- **Proactive assistance**: "I notice you've been in the same location for 20 minutes. Do you need help?"
- **Buddy system**: Allows pairing with another user or volunteer for guided support

### **Idea 7: Resource Inventory & Distribution Optimizer**

**Problem**: Aid supplies arrive chaotically; shelters don't know what they have, what's coming, or how to distribute fairly.

**Solution**: Voice-based inventory management for non-technical staff:

- **Features**:
- Quick logging: "50 blankets arrived from Red Cross"
- Smart distribution: "12 families need blankets, we have 8, request 4 more"
- Expiration tracking for food/medicine
- Fair allocation algorithms: Tracks who received what to prevent duplicate requests or hoarding
- Supply chain visibility: "Water truck is 30 minutes away"
- **Hardware**: Works with basic barcode scanners or voice-only input
- **Offline-first**: Syncs inventory when connection available
- **Multi-shelter coordination**: Nearby shelters can see each other's surplus/shortages

### **Idea 8: Cultural & Religious Sensitivity Navigator**

**Problem**: Disasters affect diverse populations with different cultural, religious, and dietary needs that responders may not understand.

**Solution**: Context-aware agent that helps both survivors and responders navigate cultural differences:

- **Features**:
- **For survivors**: "Halal food is available at Station 3"; "Prayer space is in Building B, Qibla direction marked"
- **For responders**: Quick cultural guidance: "This family observes Ramadan, provide food for evening"; "Remove shoes before entering this shelter area"
- Gender-segregated space navigation (important in some cultures)
- Religious calendar awareness for timing of aid/events
- Traditional medicine integration: "This group prefers traditional healing alongside modern medicine"
- **Privacy**: Opt-in cultural profile that survivors can share or hide
- **Multilingual**: Deeply integrated with cultural context, not just translation

### **Idea 9: Post-Trauma Memory & Documentation Helper**

**Problem**: Survivors need to document damage for insurance/aid claims but are traumatized, overwhelmed, and documentation is the last thing they can focus on.

**Solution**: Voice-guided documentation assistant that works over days/weeks:

- **Features**:
- Guided photo documentation: "Take a photo of each damaged room. Now tell me what was lost."
- Loss inventory building: "Describe what you remember, I'll help organize it later"
- Timeline reconstruction: Helps survivors piece together what happened for legal/aid purposes
- Evidence preservation: Timestamps, GPS tags, secure storage
- Aid application assistance: "For this relief program, you need these 4 documents. You have 2. Let's work on the others."
- **Emotional awareness**: Detects distress during documentation, offers breaks: "This is hard. Would you like to continue tomorrow?"
- **Multi-day sessions**: Picks up where user left off, gentle reminders without pressure

### **Idea 10: Adversary-Aware Secure Communication Network**

**Problem**: In conflict zones or politically sensitive disasters, survivors need to communicate but face surveillance, internet shutdowns, or malicious actors.

**Solution**: Privacy-first, mesh-network communication system with voice interface:

- **Features**:
- Peer-to-peer encrypted voice messages (no central server required)
- Dead-drop information exchange: Leave voice messages at locations for specific people
- Duress codes: Special phrases that trigger silent alerts or data wipes
- Fake "normal" mode: If forced to unlock, shows innocent content
- Network resilience: Routes through trusted nodes, automatically finds alternate paths
- Identity verification: Voice recognition or shared secrets prevent impersonation
- **Hardware**: Works on basic smartphones with Bluetooth mesh networking
- **Ethical design**: Built with human rights organizations, informed by refugee/activist experience
- **Non-technical interface**: "Send a secure message to Maria" just works

### **Idea 11: Child-Specific Calming & Reunification Agent**

**Problem**: Children separated from parents are terrified, may not be able to articulate needs, and need specialized emotional support.

**Solution**: Child-friendly voice companion with reunification focus:

- **Features**:
- Age-appropriate calming: Games, songs, stories while waiting for help
- Simple information gathering: "What's your name? What does your mom look like? What's your favorite color?" (makes info gathering feel like play)
- Safety education through stories: "Let me tell you about Super Safe Sam who talks to helpers with badges"
- Non-threatening check-ins: "Are you hungry? Do you need the bathroom?"
- Automatic integration with Idea 3 (Family Searching) - child's info feeds into matching system
- Guardian verification: Won't release child to anyone without proper verification
- **Voice design**: Warm, patient, never rushed
- **Safeguarding**: Every interaction logged, volunteer oversight required

### **Idea 12: Disaster Simulation & Preparedness Trainer**

**Problem**: People don't prepare for disasters because they seem abstract or they don't know how.

**Solution**: Voice-guided disaster preparedness in everyday life:

- **Features**:
- Personalized risk assessment: "Your area faces earthquakes and floods. Let's prepare."
- Progressive preparation: "This week, let's build a go-bag. Tell me when you've added water bottles."
- Household drill simulator: Voice-guided practice evacuations at home
- Scenario training: "Your building is shaking. What do you do?" with feedback
- Family plan builder: Coordinates plans among family members
- Maintenance reminders: "Your emergency water expires in 30 days"
- **Gamification**: Badges, preparedness scores, neighborhood challenges
- **Crisis switch**: The same agent that trained you guides you during real emergency (familiar voice = trust)


Initial ideas

Idea 3: Family Searching

Here's a draft of a **formal report** you can use / adapt for the "Family Searching / Missing Person Matching" idea. You can fill in details specific to your implementation as you build. If you like, I can produce a polished PDF version or adjust for your institution's style.

# **Report: Family Searching - Missing-Person Registration & Matching Agentic System**

## **Abstract**

This report describes a voice- and text-based system for registering missing-person reports, broadcasting candidate records locally, and supporting matches with mutual consent while preserving privacy. The project emphasizes privacy by default, works offline/local-first, and implements core HRI flows: registration, broadcast to volunteers, match request with consent, and safe contact. We built a vertical prototype for these critical interactions, and simulated ancillary features. Usability and safety metrics (match accuracy, time to confirmation, false positives, perceived safety) were evaluated in small scale tests. Our findings indicate that voice registration and local candidate broadcasts can reduce time to report entry, mutual consent flows improve trust, though matching remains sensitive to record detail and handling of ambiguity. Implications for deployment include better privacy policy design, volunteer supervision of matches, and careful handling of sensitive cases (e.g. minors, impersonation risk).

## **1\. Introduction**

- **Motivation and Context**
  - Disasters / crises often lead to missing persons; families and volunteer groups struggle to register and match missing person reports when resources are limited.
  - Privacy, consent, safety are critical especially for vulnerable people (children, women, etc.).
  - Low connectivity, chaotic environments, and mistrust make simple, privacy-aware tools valuable.  

- **Problem Statement**
  - How can we design a missing-person registration & matching system that:
    - Supports low-resource / low-connectivity conditions (offline, local broadcasts)
    - Maintains strong privacy by default and per-match consent
    - Provides trust and safety (fraud checks, verification)
    - Enables volunteer support without exposing sensitive data  

- **Scope & Constraints**
  - Voice/text registration; no raw biometrics by default.
  - Local device processing where feasible; limited bandwidth.
  - Human-in-the-loop for uncertain matches.
  - Sensitive location / identity delayed until consented.

## **2\. Related Work & Design Principles**

- Brief survey of existing missing-persons / family locating systems (government / NGO / apps), especially in disasters.
- Privacy-by-design standards, consent mechanisms, low-bandwidth / offline systems in humanitarian settings.  

- Design principles drawn from HCI / Human-Robot Interaction: transparency, mutual consent, fallback for ambiguous input, usability under stress.  

## **3\. System Design & Requirements**

### **3.1 Functional Requirements**

- Registration of missing-person reports: fields (name / nickname, relation, last seen place/time, distinguishing features, safe callback info).
- Consent dialogues: broadcast consent, contact consent.
- Local broadcast of new reports to volunteer consoles.
- Match request flow: volunteer propose match → reporter consents → safe contact exchanged.
- Offline operation + sync when online.  

### **3.2 Non-Functional Requirements**

- Privacy & safety: default privacy settings, special protection for minors, fraud reporting.
- Usability: voice + text, fallback when voice fails.
- Multilingual if needed.
- Performance under constrained resources: minimal latency; responsive in offline or intermittent connectivity.  

## **4\. Interaction Design**

- Personas (e.g. family member reporting, volunteer).
- User flows (Mermaid diagrams) for registration → broadcast → match.
- Wireframes / UI mockups for Reporter app and Volunteer console.
- Error handling and edge-cases (ambiguous matches, lack of consent, impersonation).  

## **5\. Prototype Implementation**

### **5.1 Vertical vs Horizontal Prototyping**

| **Feature** | **Vertical (Fully implemented)** | **Simulated / Wizard-of-Oz or Mocked** |
| --- | --- | --- |
| Registration dialogue (voice/text), record creation, consent | ✔️  | -   |
| --- | --- | --- |
| Broadcast to volunteer consoles and display candidate entries | ✔️  | -   |
| --- | --- | --- |
| Mutual consent flow for sharing safe callback/contact | ✔️  | -   |
| --- | --- | --- |
| Offline-first + sync when online | ✔️  | (complex conflict resolution mocked) |
| --- | --- | --- |
| Embedding-based matching (photo / voice) | -   | Simulated via dummy data |
| --- | --- | --- |
| Fraud/abuse detection, impersonation checks | -   | Mock logic or flags for test cases |
| --- | --- | --- |
| Sensitive location disclosure delay | -   | UI representation only |
| --- | --- | --- |

### **5.2 Technical Architecture**

- Frontend frameworks (Reporter App, Volunteer Console)
- Agent or logic layer for dialogue management
- Local storage (browser local, or mobile device)
- Backend or sync server (minimal) for broadcast, matches, contact mediation
- Data schema: hashed/pseudonymized IDs, minimal fields, privacy tiers  

### **5.3 Implementation Details**

- Voice input via Web Speech API or fallback to text
- Consent dialogues clearly shown; default privacy settings depending on age or relation
- Broadcast via WebSocket or polling
- Safe callback sharing only after reporter consents  

## **6\. Evaluation**

### **6.1 Metrics**

- True match rate: fraction of matches that are correct
- Time to confirmation: time from report to mutual consent/contact
- False positives / false negatives rate
- Perceived safety: via user survey (reporters & volunteers)
- Usability metrics: time to complete registration; errors / corrections needed  

### **6.2 Study Design**

- Recruit small number of participants (reporters & volunteers) in lab / simulated field setting
- Use test/dummy missing-person entries to test matching flow
- Include cases of ambiguous data, missing fields, minors, etc.
- Record how participants feel about privacy, trust, safety  

### **6.3 Results**

-  

## **7\. Discussion**

- What the prototype demonstrates: viability of local broadcasting, voice registration, consent flows, offline sync.
- Limitations: matching quality depends on record detail; false match risk; handling of fraud/abuse is shallow in prototype.
- Ethical considerations: privacy, consent, possible misuse, safety of reporters / matched persons.

## **8\. Future Work**

- Improve embedding-based matching (photo / voice) with privacy guarantees
- More robust fraud / impersonation detection
- Richer privacy policies, legal compliance (GDPR, local laws)
- Scaling to many users / many volunteer nodes / real network environments
- Enhancing UI / UX for more languages, low literacy, audio clarity  

## **9\. Conclusion**

- Restate what was done, what was found, why it matters.
- Emphasize how privacy by default and mutual consent are central.
- Suggest how this could be deployed or tested in realistic disaster scenarios.  

## **10\. References**

- List academic or technical sources about privacy, missing-persons systems, HCI design practices.  

- Include HCI & privacy design guides, any related deployment case studies.  

## **Appendices**

- Mermaid diagrams & flowcharts
- Screenshots / wireframes
- Survey instruments (if used)
- Data schemas, consent forms  

If you like, I can generate a **filled-in example** for your prototype (with mock results) or format this in IEEE / ACM style. Do you want me to prepare that?

Nice shift of direction - the "Family Searching / Missing Person Matching" idea is compelling and high impact. Below are:

- Key flows expressed as **Mermaid diagrams** (flowcharts + sequence)  

- Suggestions for vertical vs horizontal prototyping  

- A sketch of the prototype plan with core interactions  

- Some possible edge cases to handle  

You can embed these diagrams into your report.

## **1\. Key Interaction Flows in Mermaid**

### **1.1. Registration → Intake card (Flowchart)**


This captures the full lifecycle from registration through broadcasting to matching and consented contact.

### **1.2. Sequence Diagram: Registration to Match Interaction**

This shows the messages exchanged over time between the reporter app, agent logic, volunteer console, and backend.

## **2\. Vertical vs Horizontal Prototyping for This Idea**

### **Vertical (must-build) interactions**

- **Registration dialogue / agent**: voice/text capture, structured record, confirmations, consent prompt
- **Broadcast & receipt**: volunteer console receiving a broadcast and viewing candidate entries
- **Match & consent exchange**: mutual consent interaction, share minimal safe contact
- **Local-first logic / offline → online sync**: local caching and later relay when connectivity returns  

These must be fully working for the demo (no Wizard-of-Oz).

### **Horizontal / Wizard-of-Oz simulations**

- **On-device embedding / similarity matching (photo / voice embeddings)**: you can simulate match suggestions by curated dummy data  

- **Automated fraud/abuse detection (impersonation checks)**: stub logic, or flag known test cases  

- **Delayed sensitive location disclosure**: this can be post-hoc in UI or via overlay (not real geolocation logic)  

- **Extensive privacy-tier defaults and policy engine**: you can mock strict defaults for minors and have UI toggles rather than full rule engine  

## **3\. Prototype Plan & Core Implementation**

### **3.1 Architecture & Modules**

- **Frontend (Reporter App, Volunteer Console)  
    **
  - Use a web framework (React, Vue, Svelte)  

  - Reporter side: voice + text input UI, record review, consent dialogues  

  - Volunteer side: list of candidate records, match-request UI  

- **Agent Logic  
    **
  - Dialogue management (ask fields, confirm)  

  - Local storage of reports  

  - Broadcast logic to volunteer consoles (via WebSocket or periodic polling)  

  - Consent management (per‐match opt-ins)  

- **Backend / Sync Server (minimal)  
    **
  - Receive broadcast submissions  

  - Serve candidate lists to console clients  

  - Handle "match consent" requests and safe callback mediation  

  - Simple in-memory store or JSON store  

- **Data & Privacy Schemas  
    **
  - Use hashed IDs or pseudonyms  

  - Only share limited info unless both sides consent  

  - Tiered privacy defaults (for minors, location delayed)  

### **3.2 Interaction Design & Error Handling**

- **Clarification prompts**: if user's response is ambiguous, ask again ("Did you say \___?")  

- **Fallback input**: always allow text correction  

- **Consent confirmation**: show before broadcasting or sharing any detail  

- **Match ambiguity cases**: if match is uncertain, escalate to human review (volunteer)  

- **Opt-out / deletion**: allow reporter to revoke or delete their record  

### **3.3 Milestones & Timeline**

| **Stage** | **Tasks** | **Deliverable** |
| --- | --- | --- |
| Stage 0 | Bootstrap project, layout UI shells | Basic UI scaffolding |
| --- | --- | --- |
| Stage 1 | Build registration dialogue + record capture + consent | Reporter side vertical path |
| --- | --- | --- |
| Stage 2 | Implement volunteer console to receive broadcast and show entries | Volunteer interface vertical |
| --- | --- | --- |
| Stage 3 | Implement match-request / mutual consent flow | Full match vertical path |
| --- | --- | --- |
| Stage 4 | Simulate embedding/matching with dummy dataset (horizontal) | Demo matches for test cases |
| --- | --- | --- |
| Stage 5 | Offline caching and sync logic (local-first, delayed relay) | Demo offline→online handoff |
| --- | --- | --- |
| Stage 6 | Testing, video capture, user trials | Demo video + prototype ready |
| --- | --- | --- |

Record a live demo of:

- A reporter registering a missing-person entry (voice → structured record)  

- The volunteer console receiving and listing that entry  

- A volunteer selecting a candidate, triggering a match request  

- Mutual consent prompt on reporter side, then safe callback exchange  

## **4\. Edge Cases & Design Considerations**

- **False positives / wrong matches  
    **
  - Mitigate with thresholding, human review, and mutual confirmation  

- **Privacy of sensitive groups (children, victims of violence, women in danger)  
    **
  - Default disable broadcast or share only minimal info until extra consent  

- **Impersonation / fraud  
    **
  - Use challenge questions, verification questions, or cross-check fields  

- **Connectivity loss / conflicts  
    **
  - Use CRDT-like structures or last-write-wins for sync, backup local  

- **Multiple matches / ambiguity  
    **
  - Allow multiple candidate suggestions, let user pick, or escalate to volunteer  

- **Unresponsive reporters or volunteers  
    **
  - Timeouts and fallback paths (alert moderator)  

If you like, I can now produce **wireframes**, **state diagrams**, or even **pseudocode for the agent logic** for this new "Family Searching" idea. Which one do you want next?

Idea 2: Guidance Voice Agent

## **1\. Objectives & Rationale**

**Purpose of this prototype stage**

- Validate the _interaction core_ - the conversational voice agent handling intake, routing, and announcements - in a realistic setting (no wizard-of-oz for that part).  

- Demonstrate feasibility of synchronization, multilingual TTS, and queue handoff in a constrained environment.  

- Use simulated or partial versions of ancillary features to show the broader vision without overengineering in the prototype phase.  

**Why vertical + horizontal prototyping**

- Vertical prototyping of the conversational core ensures that the critical HRI path is fully functional and testable.  

- Horizontal or Wizard-of-Oz treatment of secondary features (e.g. crowd counting, physical robot motion, advanced offline sync) lets you show system breadth without investing in every component upfront.  

- This mixed approach is standard: vertical = deep in one path; horizontal = broad coverage of features superficially. ([simonwhatley.co.uk](https://www.simonwhatley.co.uk/writing/horizontal-vs-vertical-prototyping-in-service-design/?utm_source=chatgpt.com))  

## **2\. Scope & Feature Prioritization**

### **2.1. Core "Vertical" Features (Must be fully functional)**


- **Voice Intake → Digital Card Flow  
    **
  - Microphone capture using Web Speech API or similar  

  - Conversational agent logic to ask questions, parse responses, fill structured fields  

  - Visual "Intake Card" display (on screen) summarizing captured data  

  - QR / short-code generation for that card


- **Queue Handoff & Call-Up Flow  
    **
  - Simple operator dashboard to mark "next" in queue  

  - Agent TTS announcement to call up next (by name or card ID)  

  - Agent voice prompt confirming that the person should proceed


- **Multilingual Announcement Playback  
    **
  - Preloaded phrase packs in a few target languages  

  - UI to pick announcement + language  

  - TTS engine to speak the announcement  

  - Display of textual announcement for fallback  

### **2.2. Secondary / Simulated (Horizontal or Wizard-of-Oz) Features**

These can be represented or stubbed, without full backend logic, so long as they help illustrate the full concept.

- **Crowd-level / sensor input  
    **
  - Use manual slider or numeric input in operator UI (simulate sensor)  

  - (Wizard-of-Oz) simulate automated crowd count reports  

- **Conflict-free data sync (offline ↔ server)  
    **
  - Leave as a "Sync" button that pushes local data to remote (no real conflict resolution logic)  

  - Mock remote server with simple JSON store  

- **Physical robot embodiment / movement  
    **
  - Use static images, sketches, or CAD mockups to show how a robot may look  

  - Robot movement may be storyboarded or manually puppeteered (Wizard-of-Oz)  

- **ASR hotword tuning, robust error correction  
    **
  - Have fallback to manual text input if speech is unclear  

  - Use "Did you say …?" confirmation steps  

## **3\. Architecture & Technologies**

### **3.1. Agent + Conversation Logic**

- Use a lightweight agent framework (e.g. **LangChain.js**, **OpenAI function-calling**, or a simplified decision-tree agent)  

- Dialogue component handles:  
  - Field list and status (what still needs to be asked)  

  - Mapping user input to structured fields (name, meds, allergies, needs)  

  - Handling interruptions, corrections, clarifications  

  - Decision logic for routing / queue assignment  

### **3.2. Frontend & UI**

- Web stack: React / Vue / Svelte (whichever you prefer)  

- Pages / Views:  
  - **Intake view**: big microphone button, speech transcript, next question, "correction" button  

  - **Card view**: summary of fields + QR / code  

  - **Operator dashboard**: queue list, "Next" button, announcement controls, crowd-level input  

  - **Announcement screen**: configure + play announcements  

- TTS: browser native SpeechSynthesis for offline use; fallback to cloud TTS in online mode  

- ASR: browser Web Speech API (if available) or fallback to text input  

### **3.3. Data Storage**

- Use browser local storage or IndexedDB for intake cards and conversation states  

- JSON schema for intake card records  

- For "server," a minimal Node.js / Express backend or mock via local JSON file / memory store  

## **4\. Interaction Design & Flow Diagrams**

You should prepare **interaction flow diagrams** and **state charts** for:

- **Intake dialogue flow**: question → response → confirm → next question → final summary  

- **Queue flow**: card enters queue → operator "next" → agent prompts call-up → user responds  

- **Announcement flow**: operator selects announcement → agent speaks in selected language  

Additionally, prepare **wireframes / mockups** of screens to accompany flow diagrams.

## **5\. Prototype Implementation Plan & Timeline**

| **Stage** | **Tasks** | **Delivery / Milestone** |
| --- | --- | --- |
| **Stage 0: Setup & skeleton** | Set up project repo, UI framework, basic pages, agent stub | Blank pages + dummy routing |
| --- | --- | --- |
| **Stage 1: Intake vertical path** | Build mic input, agent logic, field capture, card display, QR code | Fully working intake → card flow |
| --- | --- | --- |
| **Stage 2: Queue & call-up path** | Build operator UI, interface to agent, TTS call-up voice | Live demo: intake → queue → call-up |
| --- | --- | --- |
| **Stage 3: Announcement module** | Load phrase packs, play announcements in multiple languages | Demo announcements in e.g. English, Japanese, Chinese |
| --- | --- | --- |
| **Stage 4: Stub / simulate secondary features** | Manual crowd input, sync button, robot mockups | Show full UI map |
| --- | --- | --- |
| **Stage 5: Testing & recording live demo** | Conduct test runs, record video of flows, user test with sample users | Video clips for submission |
| --- | --- | --- |

You can schedule this in e.g. 4-6 weeks depending on your time budget.

## **6\. Demonstration & Deliverables**

For your **video demonstration**, record _live use_ (no wizard-of-oz) of the vertical paths:

- A user speaks answers for intake; the agent queries, user clarifies, card is generated.  

- Operator triggers "Next"; the agent calls up next user by voice.  

- Operator selects an announcement, and the agent voices it in different languages.  

For horizontal parts, you can show UI mockups or simulate via slide overlays or "fake" buttons (e.g., "simulate sensor count").

Your **deliverables package** should include:

- The interactive web prototype (hosted or runnable locally)  

- Source code (frontend + minimal backend)  

- Flow diagrams, wireframes, state charts  

- Video recording of live demonstration  

- A written description of which parts are fully functional vs simulated (i.e. Wizard-of-Oz)  

- A plan for next steps / extension  

## **7\. Risks, Mitigations & Trade-offs**

| **Risk / Challenge** | **Mitigation / Strategy** |
| --- | --- |
| ASR error / misrecognition | Provide fallback by showing transcript and "correct" option; ask confirmation prompts |
| --- | --- |
| TTS not natural / pronunciation errors | For MVP, accept synthetic voice; choose high-quality TTS voices or phrase-pack tuning |
| --- | --- |
| Latency / offline constraints | Cache agent logic locally; keep dialogue logic lightweight |
| --- | --- |
| Unexpected user utterances | Predefine limited domain; for out-of-domain, respond "Can you rephrase?" |
| --- | --- |
| Integration complexity | Keep data sync and backend minimal; defer robust conflict resolution to future work |
| --- | --- |

In your report, explicitly note which features are left simulated and why (time constraints, lower priority).

## **8\. Evaluation Plan (Usability + Interaction Metrics)**

Once prototype is built, run a small usability test (5-10 participants) focusing on the vertical paths.

Measures and observations:

- **Completion time** of intake  

- **Error / clarification count** (how many times user had to re-answer)  

- **User satisfaction / cognitive load** (post-task questionnaire)  

- **Comprehension test**: user repeats back what they heard in multilingual announcement  

- **Observer notes**: hesitation, confusion, mismatch  

Use these to refine dialogue pacing, question phrasing, error recovery strategies.

## **9\. Report Structure (for formal submission)**

- **Introduction & Motivation  
    **
- **Related Work / Design Patterns** (e.g. use of interaction blocks in HRI) ([UW Computer Sciences](https://pages.cs.wisc.edu/~bilge/pubs/2014/CHI14-Sauppe.pdf?utm_source=chatgpt.com))  

- **Design Goals & Constraints  
    **
- **Feature Prioritization & Prototyping Strategy (vertical vs horizontal)  
    **
- **Interaction Design** (flow diagrams, wireframes)  

- **Technical Architecture & Implementation Details  
    **
- **Prototype Demonstration Plan  
    **
- **Evaluation Plan & Metrics  
    **
- **Limitations & Future Work  
    **
- **Conclusion**

**Appendix:**

**1\. Intake → Card Flow (Conversation + UI) Flow:  

**2\. Queue Handoff & Call-Up Flow**



Idea 1: Voice Agent for Psychological Support

**Idea 1: Voice Agent for Psychological Support**

- Hardware
  - Starlink (Satellite Internet)
    - We assume that this is provided everywhere :D
    - Offline mode: Core functions must operate without any internet connection
    - Data compression: Optimize for low-bandwidth scenarios (< 100 kbps)
  - Built for hostile conditions
    - Waterproof/dustproof rating: IP67 or higher
    - Shock-resistant design: Military-grade drop test standards (MIL-STD-810G)
    - Extended battery life: Minimum 72-hour operation, solar charging capability
    - Bone conduction microphone: Captures voice in extreme noise environments
    - Multi-microphone array: Beamforming technology to isolate voice from explosions/sirens
    - Temperature tolerance: -20°C to 60°C operating range
  - Voice (speakers)
    - High-volume output: Clear audio in noisy environments (90+ dB)
    - Directional speakers: Privacy protection, prevents others from overhearing sensitive conversations
    - Haptic feedback: Vibration alerts when audio isn't feasible
- App or specific device?
  - App -> for people with phones
    - More features
  - Specific device for people without access
    - Only contains LLM and other simple features such as alerts and GPS?
    - Basic survival tool integration: Flashlight, SOS signal light, FM/AM radio
    - Physical emergency button: One-touch connection to human responders
    - Simplified interface: Large buttons, high-contrast display, operable under stress
    - Ruggedized e-ink display option: Power-efficient, readable in direct sunlight
    - Distributed to disaster areas if necessary
- Features
  - Emergency Alert System
    - Automatically activates when there's an emergency
    - Emergency mode? (Built-in feature in modern phones)
    - Geofencing triggers: Automatic detection when user enters dangerous zones
    - Sound pattern recognition: Detects explosions, gunfire, sirens and auto-activates
    - Mass alert broadcasting: Sends threat warnings to all users in the area
    - Safe route recommendations: Plans evacuation routes based on real-time conflict data
    - Shelter locator: Identifies nearest safe spaces, hospitals, aid stations
    - Silent mode: Visual-only alerts when sound would compromise safety
  - LLM Features
    - Provide directions
      - Multimodal navigation: Voice + simple arrow indicators (low cognitive load)
      - Landmark-based navigation: Uses local buildings rather than street names (street signs often destroyed in war zones)
      - Danger zone marking: Integrates real-time conflict data to avoid active combat areas
      - Offline maps: Pre-cached regional maps with last-known safe routes
      - Crowd-sourced updates: Users can report blocked/unsafe routes
    - Psychological support
      - Trauma-informed dialogue: Questioning approaches that avoid re-traumatization
      - Cultural adaptation: Adjusts support style based on user's cultural background
      - Tiered support levels:
        - Immediate calming (breathing exercises, grounding techniques)
        - Short-term coping strategies
        - Long-term psychological resilience building
      - Special population modes: Customized support for children, elderly, pregnant women
      - Collective trauma response: Addresses community-level distress, not just individual
      - Grief support: Specific protocols for loss and bereavement
      - De-escalation techniques: For panic attacks, acute stress responses, dissociation
      - Psychoeducation: Normalizes trauma responses ("What you're feeling is a normal reaction to abnormal circumstances")
    - Detect whether a user requires special attention, and alerts management personnel
      - **Multi-dimensional crisis detection:**
        - Language patterns (suicidal ideation, extreme hopelessness, dissociation symptoms)
        - Voice characteristics (trembling, rapid speech, abnormal calmness)
        - Behavioral patterns (sudden usage frequency changes, midnight distress calls)
        - Physiological data (if sensors available: abnormal heart rate, rapid breathing)
        - Contextual factors (location in high-risk area, time since last traumatic event)
      - **Tiered response system:**
        - Level 1: Enhanced AI support (more empathetic, frequent check-ins)
        - Level 2: Connect to trained peer volunteer
        - Level 3: Professional mental health worker
        - Level 4: Emergency medical/security intervention
      - False positive management: Avoids excessive alerts causing alarm fatigue
      - Human-in-the-loop verification: Critical alerts reviewed by trained staff before escalation
      - Privacy-preserving flagging: Alerts responders without exposing full conversation content

\- Offline Content Library

- **Pre-loaded resources:**
  - Grounding techniques (5-4-3-2-1 sensory exercise, etc.)
  - Guided breathing and meditation
  - Culturally-specific prayers/meditation content
  - Basic first aid guide
  - Water purification, shelter building, survival skills
  - Common trauma responses and coping strategies
- **Children's section:**
  - Calming stories, simple games
  - Guidance for parents to comfort children
  - Age-appropriate explanations of war/disaster
  - Agent Requirements
    - ASR should tolerate heavy noise and strong accents (discussion only)
    - Stress speech recognition: Speech patterns change under traumatic stress
    - Multi-language dialect support: Including minority languages and mixed languages
    - Code-switching handling: War zone residents often mix multiple languages in sentences
    - Low-resource languages: Develop solutions for languages lacking training data
    - Child speech recognition: Specialized models for younger users
    - Whispered speech detection: For situations where speaking loudly is dangerous
- Technical Implementation
  - LLM
    - Search for LLMs built for this purpose

**\- Base model selection:**

- Online: Med-PaLM derivatives, Mental-LLaMA, specialized trauma-care models
- Offline: Llama 3.2 (1B/3B), Phi-3-mini (quantized to 2-4 bit), Mistral 7B (quantized)

**\- Model architecture requirements:**

- Fast inference (< 500ms response time)
- Small memory footprint (< 4GB RAM)
- Multilingual capability
  - - Reinforcement learning w/ database (ideally)
      - Prompt Engineering
  - Hardware (for people without phones)
    - Purpose-built device, with a screen, microphone, speakers
      - Screen specs: E-ink (power-efficient) or high-brightness LCD (readable in sunlight)
      - Processor: Capable of running quantized LLM (e.g., Qualcomm Snapdragon 8 Gen series or equivalent edge AI chip)
      - Storage: Minimum 8GB for offline models and content library
      - RAM: 4-6GB for smooth LLM inference
      - Sensors (optional): Heart rate, accelerometer (detects falls/immobility), GPS
      - Connectivity: 4G/5G, WiFi, Bluetooth, satellite (Starlink/Iridium)
      - Form factor: Pocket-sized (< 200g), wearable clip option
    - Connect to our backend / go to our webpage
      - Progressive enhancement: Works better with connectivity but functional offline
      - Secure communication protocols: TLS 1.3, certificate pinning
- Consent
  - Obtain when download app // before disaster occurs
  - Layered Consent Framework
    - Basic usage consent:
      - Clearly explains AI nature and limitations
      - Data collection scope (anonymized telemetry vs. conversation content)
      - Right to withdraw at any time
      - Plain language + visual explanations (for literacy barriers)

Interview Questions

| **#** | **Interviewee** | **Date** | **PIC** |
| --- | --- | --- | --- |
| 1   | Girl from Syria<br><br>And Possible Friends |     |     |
| --- | --- | --- | --- |
| 2   | Girl from Ukraine |     |     |
| --- | --- | --- | --- |
|     | German Lady from Kosovo |     |     |
| --- | --- | --- | --- |
| 3   | Domestic Helper |     | Angel |
| --- | --- | --- | --- |
| 4   | Executive Officer |     | Harry |
| --- | --- | --- | --- |
| 5   | Volunteer (Christy) | 11 Oct | Angel and Jenson |
| --- | --- | --- | --- |
| 6   | Volunteer from HKU |     |     |
| --- | --- | --- | --- |
| 7   |     |     |     |
| --- | --- | --- | --- |
| 8   |     |     |     |
| --- | --- | --- | --- |
| 9   |     |     |     |
| --- | --- | --- | --- |
| 10  |     |     |     |
| --- | --- | --- | --- |
|     |     |     |     |
| --- | --- | --- | --- |

**Needfinding Interview Flow**

- Briefing
  - Ask how to call the interviewee
  - Get consent for note taking / recording
  - Introduce background & purpose of project
- Needfinding
  - Generic
    - Situation
      - Your Basic information(nationality, age, social role)
      - What happened to you or your family, friends before?
      - What challenges do you face?
    - Thoughts/Experience on Technology
      - Have you used any chatbot or digital assistant before? What was your experience?
      - What language and communication methods do you prefer/are typically used? (e.g., text, voice calls)
    - Safety/Privacy
      - Would you be comfortable sharing personal information with a chatbot? What concerns do you have?
      - What can be done to make you trust and feel safe using this technology?
    - Others
      - Is there anything else you would like to tell us?
      - What type of chatbot functions would be the most helpful to \*the\* situation?
      - Any other doubt or hesitation do you hold for this chatbot?
  - War
    - What are your immediate needs during this conflict? (e.g., shelter, food, medical aid)
    - How do you receive information about safety, aid, and evacuation options?
    - Are you currently safe in your location? If not, what are the main threats?
    - Do you have access to a phone or internet regularly / during special events?
  - Natural Disaster
    - What kind of natural disasters have affected you recently?
    - What are the biggest challenges you face in responding to or recovering from disasters?
    - How do you usually get information about disaster warnings or relief services?
    - What mobile or digital tools do you use during natural disaster events?
    - Disaster management:
      - In case of evacuation, etc, who are involved? How is information / instructions delivered?
  - Disaster Relief (Executive Officer, Volunteers)
    - Operational Bottlenecks
      - When handling high volumes (e.g., triage, volunteer registration), what are the main communication bottlenecks or manual tasks you face?
      - How does information flow informally between you and other volunteers or departments?
    - Cognitive Load & Decision-Making
      - In crisis situations, when making real-time decisions (e.g., task allocation, rapid triage), what are your biggest cognitive demands?
    - Volunteer Management
      - What challenges do you face in quickly coordinating large numbers of new volunteers (in hk: 關愛隊)? How do you ensure they receive immediate training or task assignments?
    - Emotional Labor
      - What kinds of emotional labor are involved in your work? Are there system supports that could help with emotional self-checks or burnout prevention?
    - Existing Tools
      - How would you assess the usability of any digital tools you currently use to support shelter operations or crisis coordination?
    - What are some common needs / issues of the people you are helping?

**Speed Dating Interview Flow**

- Speed Dating
  - Present storyboards to them
  - Questions
    - Core Needs & Practicality
      - Which option best meets your most urgent need?
      - If only 2-3 features, which are essential?
      - Which is most practical in your context (hospital, shelter, volunteer mgmt)?
    - Do you think this would be helpful?
    - What problems can this solve / will not be solved?
    - Is it practical?
    - Would you use this?
    - Is it easy for you to use(user-friendly)

Jane-Ukrane

### 1\. Personal Background

My name is Jane (Ukrainian name: Genya Uhenia). I am 25 years old and originally from Ukraine. I currently live in Brussels, where I work as a Communication and Events Assistant at a company while also pursuing my graduate studies. I hold a bachelor's degree from Ukraine and an international master's degree from Europe.

When the war began on February 24, 2022, I was in Kyiv. I stayed in Ukraine for the first seven to ten days, then moved to Poland for about seven months. Afterward, I returned to Ukraine for three months before moving again to work elsewhere in Europe. I have now been back in Ukraine for about a month and a half.

### 2\. Experiences During the War

I have lived through power outages and bombings, especially during the autumn of 2022, when the blackouts were at their worst. There were days without electricity or internet connection. The situation has improved since then, but just yesterday there was another ten-hour outage after a power station was bombed.

Like many others, I relied on Telegram and similar channels to receive real-time information about air raids and bomb locations, which helped me decide whether to take shelter. These updates were extremely useful, even though the sources were often unclear.

Personally, I was not physically harmed, but I witnessed explosions, windows shattering, and other life-threatening events. In my community, some people were injured or killed, and many men were conscripted into the army.

### 3\. Use and Perception of Chatbots

I use ChatGPT and other AI assistants for a variety of purposes, including emotional support, although I have never discussed the war through these platforms.

I am not overly concerned about privacy, as the topics I discuss usually don't involve sensitive information, but I still maintain a degree of caution. I typically communicate with chatbots in Ukrainian.

### 4\. Feedback on the Three Project Ideas

First idea (psychological support voice assistant): I find this concept very helpful, especially for individuals who need mental or emotional support. I would suggest adding a children's mode and considering the market competition in this area.

Second idea (voice assistant for guiding people to shelters): I think such an application may be unnecessary at this stage, as most Ukrainians are already familiar with the locations of nearby shelters.

Third idea (finding missing family members): This would be particularly valuable in extreme situations, such as during the siege of Mariupol, but at present, Ukrainian cities are relatively organized, and the demand for such a tool may be limited.

### 5\. Suggestions on Product Form

I recommend developing a mobile application first, as it would be easier to distribute and promote compared to a standalone hardware device. Depending on future needs, dedicated hardware could be developed later.

Pici's Mom-Kosovo-Albanian

i.)

1\. Misrete Haziri, Kosovo-Albanian, 46 years old, housewife.

2\. The schools were closed because several students had been murdered, including some of my friends. My brother fled abroad because he was about to be drafted into the army. Many Serbs from our village were drafted to other towns so they could commit crimes there without being recognized, since we were all neighbors. My sisters and brother and I hid with our aunt outside the danger zone because the situation threatened to escalate. Only my father and uncle stayed at home to look after the animals and the dog. Many fled abroad, but I stayed close because my father and uncle stayed at home.

3\. Back then, we were supposed to report to the local government every day, where we reported who lived where. But that was just an excuse to see where Albanians lived so they could be systematically killed. Leaving the house was impossible because you were subject to checks and even kidnappings. A normal daily routine, like going to school or shopping, was impossible.

II)

- No I never used such technology.
- Personally, I can only use my cell phone (calls and texting); I find it difficult to use things like computers, etc.

III)

- I would have no problem exchanging information, but I would be afraid that it would end up with the enemy, such as where I live.
- International laws that prohibit the use of this information to prevent persecution.

iv)

- People in war zones have problems trusting others and technology.
- The function where you can keep a diary to document events. It would help document the war and it helps the soul.
- Whether people can access it when all technology is blocked

i)

Needs would be: safe space, food, medical care, education for the children and contact with international needs.

ii)

News through TV and NATO troops

iii)

The war ended 26 years ago so I'm safe

iv)

Yes, I do have access.

Volunteer Christy

# **Needfinding Interview: Christy (Volunteer)**

### **Briefing**

- **Interviewee name preference:** Christy
- **Consent for note-taking/recording:** Granted
- **Background & purpose of project:** Introduced

## **Part 1: General Background**

- **Basic Information:  
    **
  - Nationality: HKSAR
  - Age: 21
  - Role: Undergraduate student
- **Family/Friends' Situation:** Nothing significant reported.
- **Personal Challenges:** None mentioned.

## **Part 2: Technology Use & Communication**

- **Experience with Chatbots/Digital Assistants:  
    **
  - Found them "useless" because they only provide generic answers.
- **Preferred Communication Methods:  
    **
  - **Text:** Anytime, convenient, casual.
  - **Voice calls:** Only for urgent matters, since they require stopping other tasks.
- **Safety & Privacy Concerns:  
    **
  - Might share personal information if relevant, but avoids unnecessary disclosure.
  - Believes legislation could help build trust, but doubts companies can be trusted fully.

## **Part 3: Disaster Relief & Volunteer Work**

### **Cognitive Load & Decision-Making**

- Did not specify major cognitive challenges in real-time crisis decisions.

### **Volunteer Management**

- **Key Challenge:** Language barriers and cultural differences.
- Example: Teaching with coworkers who lacked expected English proficiency, leading to miscommunication.

### **Emotional Labor**

- Believes emotional support systems are necessary.
- Notes that even when such systems exist, people often don't use them due to laziness or lack of effort.

### **Existing Tools**

- Current digital tools are somewhat useful but not efficient enough due to accuracy issues and user competence.
- **Positive Example:** Believes accurate real-time transcription (e.g., AirPods audio-to-text) could greatly improve efficiency in disaster or war zones.

### **Needs & Issues of Beneficiaries**

- **Volunteers:** Often lack competence or initiative; not qualified enough.
- **Local Communities (Indonesia, Vietnam):**
  - Education and farming support needed.
  - Language barriers prevent effective communication and awareness-building.

### **Information Flow**

- Typically obtained from the **event** person-in-charge via text or face-to-face.
- Information is not always clear or consistent, depending on the person's ability to communicate effectively.

### **Overwhelm**

- Did not feel overwhelmed by instructions or demands.

## **Part 4: Key Observations & Interviewer Notes**

- **Recurring Theme:** Language barriers and inconsistent communication styles are the biggest obstacles.
- **Cultural differences and translation errors** also contribute to misunderstandings.
- **Real-time transcription** could significantly improve efficiency in disaster relief, provided accuracy is high.

## **Part 5: Speed Dating Interview (Concept Testing)**

- **Core Needs & Practicality:  
    **
  - Christy believes that ideas could be merged.
  - Getting people to shelters is the most urgent priority; many other problems (e.g., finding parents, psychological help) can be addressed there.
- **Usefulness & Adoption:  
    **
  - Would use the solution if in urgent need ("if she is dying for help then of course").
  - User-friendliness depends on the actual product design.
- **Critical Question:  
    **
  - Asked whether a **Guidance Voice Agent** could provide **real-time updates** (e.g., avoiding enemies or bombs). Without this, she doubts its usefulness.

✅ **Summary of Christy's Perspective:**

- Biggest challenge: **Language and communication barriers** in volunteer work.
- Believes **real-time transcription and translation tools** could transform disaster relief efficiency.
- Skeptical about trust in companies but sees potential if technology is accurate and practical.
- Prioritizes **getting people to shelters** as the most critical step in disaster response.

Draft

**Needfinding Interview**

- Briefing
  - Ask how to call the interviewee - Christy
  - Get consent for note taking / recording - Consent
  - Introduce background & purpose of project - Introduced
- Needfinding
  - Generic
    - Situation
      - Your Basic information(nationality, age, social role)
        - HKSAR, 21, UG Student
      - What happened to you or your family, friends before?  
                Nothing
      - What challenges do you face?
        - None
    - Thoughts/Experience on Technology
      - Have you used any chatbot or digital assistant before? What was your experience?
        - Useless, bcuz the chatbot she uses only give Generic Answer
      - What language and communication methods do you prefer/are typically used? (e.g., text, voice calls)
        - text, anytime, convenience, casual. Voice only for urgent, bcuz need to stop to do phone calling.
    - Safety/Privacy
      - Would you be comfortable sharing personal information with a chatbot? What concerns do you have?
        - Maybe, if not needed (Like the info is not related to the stuff she asks) then wont.
      - What can be done to make you trust and feel safe using this technology?
        - Legislation, but not possible for companies cuz no one will trust them.
    - Others
      - Is there anything else you would like to tell us?
        - no
  - Disaster Relief (Executive Officer, Volunteers)
    - Operational Bottlenecks
      - When handling high volumes (e.g., triage, volunteer registration), what are the main communication bottlenecks or manual tasks you face?
      - How does information flow informally between you and other volunteers or departments?
    - Cognitive Load & Decision-Making
      - In crisis situations, when making real-time decisions (e.g., task allocation, rapid triage), what are your biggest cognitive demands?
    - Volunteer Management
      - What challenges do you face in quickly coordinating large numbers of new volunteers (in hk: 關愛隊)? How do you ensure they receive immediate training or task assignments?
        - Communication problems like bad English, like she assumes they have some level of ability, but bcuz of lang barriers, cultural diff, not meeting the expectation of Christy. Example Scenario: Teaching with coworkers.
    - Emotional Labor
      - What kinds of emotional labor are involved in your work? Are there system supports that could help with emotional self-checks or burnout prevention?
        - She says it must have, but didnt specify the type. It must have,but she thinks people dun know how to use or didn't try to use it (Like being lazy or not putting effort)
    - Existing Tools
      - How would you assess the usability of any digital tools you currently use to support shelter operations or crisis coordination?
        - She thinks It must have some use, but the efficiency is not high enough bcuz of both the accuracy and the people who uses it.
        - Respond to existing tech: New Airpods audio transcribe, if accurate then must benefit many ppl, especially in war and disasters, highly increase the efficiency.
    - What are some common needs / issues of the people you are helping?
      - Christy thinks her volunteer coworkers are not competent enough and didn't know how to solve stuff, and even didn't try to do that. Not qualified enough.
      - She Have some issues tho,like educating people in Indonesia, and helping people to farm. (She teach some younger people, and teach topics which needed to be spread awareness)Lang barrier exists so cannot communicate effectively with the target of volunteering.
    - When you needed information (like where to go, who to help, or what supplies to bring), how did you usually get it? A: Ask the 負責人, text + f2f
    - Was the information always clear and consistent? Not really, since they have a certain level, but except for coworkers and the people needed to be helped.
    - Did you ever feel overwhelmed by too many instructions or too many people needing help at once? No

Other feedbacks:  
She keeps emphasizing language barriers or communication style inconsistent(?. ANd she thinks this is very hard to mitigate in a short time.  
Some other notes from interviewer:  
\[10/11/25, 6:47:09 PM\] 問號姐 ❔❓❔: -> language is a big issue to overcome

\[10/11/25, 6:47:37 PM\] 問號姐 ❔❓❔: i think this is also true in war areas - volunteers may not speak the local language, etc

\[10/11/25, 6:50:21 PM\] 問號姐 ❔❓❔: understanding mismatch due to culture differences, translation errors, etc

\[10/11/25, 6:55:15 PM\] 問號姐 ❔❓❔: real time transcription would largely increase efficiency in disaster situations - mainly because it removes barrier and facilitates effective communication with locals

\[10/11/25, 6:56:06 PM\] 問號姐 ❔❓❔: assuming that it is accurate ^

\[10/11/25, 7:10:07 PM\] 問號姐 ❔❓❔: idea 2 (prob most useful). if its human attack how often does it update?

**Speed Dating Interview Flow**

- Speed Dating
  - Present storyboards to them
  - Questions
    - Core Needs & Practicality
      - Which option best meets your most urgent need?
      - If only 2-3 features, which are essential?
        - She thinks idea 3 is actually everything (can integrate idea 2 and 1)
      - Which is most practical in your context (hospital, shelter, volunteer mgmt)?
    - Do you think this would be helpful?
    - What problems can this solve / will not be solved?
    - Is it practical?
    - Would you use this? If she is dying for help then ofc.
    - Is it easy for you to use(user-friendly) Unanswerable, cuz it depends on the actual product.

Christy thinks the ideas can be merged:  
Just get to the shelters and then most stuff can be solved there with volunteers (like the problems other ideas are trying to solve like finding parents, psychological help).  
She thinks getting to shelters is much more important.  
Christy asks about if the Guidance voice agent could be real time updated, like if u can really avoid enemies or bombs at that moment etc. Otherwise not very useful?

Mary-Syria

i. Situation

1.Your basic information (nationality, age, social role)

Hiya, I'm Mariam Jamous (Mary). I'm Syrian, twenty years old and currently in my junior year studying English Literature.

2\. What happened to you or your family, friends before?

I was only a child when the Syrian Revolution began, but its images are etched into my memory as if they happened yesterday. I remember the chants rising from the streets, the crowds marching for freedom and how my school would abruptly send us home as protests grew closer. The air would tremble with the sound of gunfire, echoing between buildings that once felt safe.

I left my childhood home fleeing from war. Those days were filled with terror -- I saw flames devour houses, lifeless bodies lying where people once lived and I walked the streets with just my parents and my sister under the shadow of a military plane circling above. A soldier's gun was pointed at us as we passed. Somehow, we survived.

We fled that burning city for what we hoped was safety, still within Syria. About a year later, we dared to return to our old home to collect what we could. I can still picture it -- the door hanging loose, every belonging tossed across the floor, the air thick with dust and the faint, bitter smell of smoke. My parents wouldn't let us go inside. They gathered what little remained: a few clothes, some carpets that still carried the scent of burning, and small things they could hide and smuggle past checkpoints -- a microwave, a hoover, anything the fallen regime's men might have stolen.

We were lucky, in a grim way. Our home was looted and shattered, but it still stood. Many others weren't so fortunate. My parents did everything they could to shield us from fear. When missiles fell nearby, they'd close the windows and make us sit in the centre of the house. When gunfire echoed through our building, they stayed calm, pretending it was all just another passing storm.

I can't compare my story to those who endured even worse. I was spared the horrors of chemical attacks, of starvation, of being detained or disappeared. Friends of mine weren't so lucky -- some had family members taken to prisons like Saydnaya, vanishing into the darkness for daring to speak against the regime, or even just for being born Sunni. Everyone knew what went on in those prisons, even if no one dared to say it aloud.

When I finally left that dangerous place behind, we found refuge in another part of Syria - safer, perhaps, but still haunted by the echoes of war and the country's heartbeat was still trembling. Even then, safety was an illusion. And yet, another trauma awaited -- Israel. I remember waking in the dead of night, my heart racing at every sound, expecting the next explosion. Bombings would come without warning - at dawn, in the middle of the night, during school hours - it made no difference. They struck without care for the lives beneath. To this day, I can say it without hesitation: Israel traumatised me. The sound of bombing is something that never leaves you.

3\. What challenges do you face?

The biggest challenges I face today are the mental scars left by the war. Even years later, I still feel its effects - moments of anxiety, sudden fear and signs of PTSD that surface without warning. Loud noises, crowded spaces, or even the smell of smoke can trigger memories I'd rather forget. Sometimes it feels like my mind is caught between the past and the present and the simple act of feeling safe can be difficult. Even ordinary sounds -- the rumble of a car, something falling at a neighbour's house, music, or the hiss of a gas tank -- can make my heart race, and for a fleeting moment, I find myself thinking: "They are bombing."

ii. Thoughts/Experience on Technology

1\. Have you used any chatbot or digital assistant before? What was your experience?

I've used a school Telegram bot to get course summaries and materials, but I've never really used a chatbot as such. I'd say AI tools are the closest thing I've tried and I think they're pretty interesting

2\. What language and communication methods do you prefer/are typically used? (e.g, text, voice calls)

I personally prefer English and I usually communicate through text. I'd use voice calls too, especially if I'm in my room studying and want to ask questions, or when I need to talk directly and get something done quickly.

iii. 1. Would you be comfortable sharing personal information with a chatbot? What concerns do you have?

think I'd still be a bit cautious about sharing personal information with a chatbot - it really depends on what kind of information it is and how secure the system feels. I'd be fine sharing general things, but I'd avoid anything too private or sensitive. My main concern would be privacy and who actually has access to the data. But honestly, I'm also a bit of an open book, haha - so I'd probably end up sharing more than I plan to anyway.

2\. What can be done to make you trust and feel safe using this technology?

I guess I'd feel safer using this kind of technology if it was controlled or supervised by trustworthy people - like certified therapists or professionals who actually care about users' wellbeing. I'd also want it to be independent, not connected to big platforms like Meta, so I know my information isn't being tracked or shared. Transparency about privacy and how it works would make me trust it much more. If I knew it was in safe hands, I'd definitely feel more comfortable using it.

Ahmad Al-Madani-Syria

Generic:

1) situation

A) Name: Ahmad Al-Madani

Age: 20

Social role: student+doing sale

Nationality: Syrian#

B)

\- i lost my Grandma... She got killed with a sniper bullet.

\- my family and I got displaced four times because of the war. We also went to constant instability when it comes to work and residence.

\- I hardly managed to keep going with my school education because I was living in conflict zones.

\- I lost friends in that conflect... There are also friends of mine who went through financial and residential harships because of the war and its consequences.

\- my parents got humiliated so many times by randome militarized forces during the war.

\- the people who had strong relationships with war leaders always used their power, weapons and authority against others whether at school, hospitals, work... Etc.

\- my parents lost all of their net worth (more than a million dollar) during the war.

2)

A)

\- chatbots are tools that make it easier to do and finish daily tasks.

\- they make my life easier and helps me strengthen my productivity and efficiency.

\- The use of chatbots might turn from being useful to being harmful if it does not get used the right way.

\- I've never used any chatbots related to psychological support.

B) English/arabic

Voice calls.

3)

A) I Would be comfortable sharing personal information with a chatbot. I have to concerns as long as it's a well-trusted chatbot.

B)

\- applying extreme Encrypting on conversarions.

\- using a chatbot that is not affiliated to any political group and has bo strong relation with any politicians.

E) chatbots that include texting, voice messaging and voicecalls.

F) no.

War:

1) medical aid.

underground shelters to keep us from bombs

food.

fuel for escaping the conflict zone when there is a chance.

masks that are used to keeps lungs safe from the pollution coming out of the bombs, exploisions and destroyed concret.

2) from the locals.

3) Im safe now.

4) yes! 4.Emotional Labor

What kinds of emotional labor are involved in your work?

\-Comforring people and letting them know that whatever war-related disasters hapening to them ar simply not their fault.

What are some common needs / issues of the people you are helping?

\-Longing the ones they lost in war.

\-going through finantial hardships.

\-seeking safety

\-the extreme need for mental health support; especially for those who got injured or lost loved ones at war.

Pastebin

According to **Human-Centric Design** principles, during the **Empathize** stage, **semi-structured interviews** should explore **predefined themes** while also allowing for spontaneous follow-up questions.

These questions should aim to uncover users' **real needs, behaviors, cognitive challenges, and system gaps** in disaster scenarios, in order to identify where voice agents/chatbots could provide support.

Below are the interview themes and example questions, organized by stakeholder groups, based on source materials:

### **Category 1: Operations, Logistics, and Workflows (for frontline responders, volunteers, and staff)**

These questions aim to understand procedures, workflows, and human resource needs in crisis situations.

| **Thematic Focus** | **Example Questions** | **Source Support** |
| --- | --- | --- |
| **Operational Processes & Bottlenecks** | What does your **current operational workflow** look like? When handling high volumes (e.g., triage or registration), what are the main **communication bottlenecks** you encounter? |     |
| --- | --- | --- |
| **Real-Time Decision-Making & Cognitive Demands** | In crisis situations, when making **real-time decisions** (e.g., rapid triage, volunteer management), what are your biggest **cognitive demands** or pressure points? |     |
| --- | --- | --- |
| **Emotional Labor** | In such high-pressure environments, what kinds of **emotional labor** are involved in carrying out your duties? Are there system supports that could help ease this burden? |     |
| --- | --- | --- |
| **Usability of Digital Tools** | How would you assess the **usability** of the **digital tools** (if any) you currently use to support shelter operations or crisis coordination? |     |
| --- | --- | --- |

### **Category 2: Information Access, Trust, and Cognitive Barriers (for affected community members and vulnerable groups)**

These questions aim to explore users' ability to process information, their level of trust in systems, and the challenges they face in accessing information.

| **Thematic Focus** | **Example Questions** | **Source Support** |
| --- | --- | --- |
| **Information Processing & Stress** | When you receive complex or conflicting emergency information, how is your **cognitive ability to process and understand** that information affected? What factors increase your **frustration**? |     |
| --- | --- | --- |
| **Trust & Compliance** | In a crisis, what is your level of **trust** in official government statements or information? What reasons might cause you to **resist following** protective instructions (e.g., shelter-in-place)? |     |
| --- | --- | --- |
| **Access Challenges for Vulnerable Groups** | During evacuation or sheltering, what challenges have you faced in **accessing or acting** on information? What needs do you have for **multilingual or sensory-friendly** information? |     |
| --- | --- | --- |
| **Information Sources** | When formal communication structures break down, do you rely on **informal social networks** to obtain critical information? |     |
| --- | --- | --- |
| **Psychological Needs** | Beyond information and resources, what are your most important **emotional needs** or forms of **support** during isolation, stress, or grief? |     |
| --- | --- | --- |

### **Category 3: HRI Potential & Scenario Identification (for all stakeholders)**

These questions aim to directly explore the practical applications of voice agents or chatbots in disaster management.

| **Thematic Focus** | **Example Questions** | **Source Support** |
| --- | --- | --- |
| **Potential Use Cases** | In what specific **contexts** (e.g., hospitals, shelters, response centers, volunteer management) do you think **voice agents or chatbots** could provide **convenience or support**? |     |
| --- | --- | --- |
| **Emergency Information Needs** | In the early stages of a crisis, what types of **location-based information** (e.g., shelter availability, medical aid) do you most often request from systems or personnel? |     |
| --- | --- | --- |
| **Hands-Free/Offline Needs** | In what situations would you need to access information or perform tasks **hands-free** or **without internet connectivity**? |     |
| --- | --- | --- |
| **Support Role** | If you had a virtual assistant, would you prefer it to act as an **authoritative guide** or as an **empathetic supporter** during emergencies? |     |
| --- | --- | --- |

These questions integrate insights from **Contextual Inquiry** and other **ethnographic methods**, ensuring that HRI solutions are designed to genuinely enhance user experience rather than add extra cognitive burden.

To build a chatbot for war disaster management by interviewing war zone citizens to find their needs, it is important to ask questions that reveal their experiences, challenges, priorities, and the type of support they require.

Key question types to ask include:

- Their immediate needs and priorities during and after conflict (e.g., shelter, food, medical aid, safety).
- How they currently receive information and communicate during war emergencies.
- Challenges they face in accessing aid, services, or safe locations.
- Their perceptions of the conflict actors and any safety concerns related to aid providers.
- What types of assistance or information a chatbot could provide to be most helpful.
- Preferred communication channels (e.g., text, voice) and language preferences.
- Their experience with technology and comfort in using digital tools.
- Suggestions on how to make the chatbot culturally sensitive and trustworthy.
- Any concerns about privacy, security, or stigma in using a chatbot.
- Timing and frequency of updates or alerts that would be useful during conflict cycles.

Such questions gather insights to design a responsive, safe, and context-aware chatbot for war disaster management by focusing directly on the affected people's needs, communication habits, and the conflict environment.

Opening and context

- Could you briefly share your experience living/working in a conflict or crisis situation? What are the biggest challenges your community faces during emergencies?
- In your most recent emergency, what help or information did you need immediately? How did you get it?
- What devices and channels do you typically use to get information? (Phone, radio, notice boards, volunteers, relatives)

Information access and barriers

- During crises, what makes it hardest to get reliable information? (Language, noise, unstable connectivity, crowding/queues, distrust, overload, delays)
- In these situations, do you prefer voice, text, or human support? When would your preference change?

Psychological support (Idea 1)

- When under stress or panic, how do you usually calm yourself? What works for you?
- Would you accept emotional support and guidance from a voice-based AI (e.g., breathing, grounding, coping strategies)? What tone or style feels safest (calm, firm, empathetic, concise)?
- Are there topics you don't want an AI to touch? (Religious content, trauma details, personal privacy, etc.)
- If the AI detects high emotional risk (panic, overwhelm), how should it respond? (Stay with me, connect me to a human/volunteer/professional, share resources)

Practical guidance and triage (Idea 2)

- At shelters/clinics/aid points, what problems do you face most? (Unclear routes, unknown wait times, language barriers, outdated announcements)
- Would you use a short voice Q&A to create an "info card" (household members, allergies/meds, special needs) to speed up triage? What concerns do you have?
- What are your expectations for call-up announcements and wait-time estimates? Which languages/dialects do you need? Are you comfortable with public name calls?
- If the AI gives wayfinding and announcements, how should it present them to avoid confusion or risk?

Family reconnection (Idea 3)

- In your (or others') experience searching for missing family, what has been the most difficult or painful part?
- What information are you comfortable using for matching? (Nickname, relationship, last seen time/place, appearance description, on-device photo/voice features) Does "on-device processing without uploading raw biometrics" increase your trust?
- Before contacting a potential match or stranger, what safety measures are essential? (Double consent, delayed disclosure of sensitive locations, human verification)
- If there's a false match or harassment, how should the system respond? (Quick revoke, block, volunteer review)

Safety, privacy, and consent

- What data are you willing to share, and for what purposes? What would you never share?
- What privacy safeguards do you expect? (Clear notices, withdraw anytime, data minimization, offline-first)
- Is local storage with later sync acceptable in low-connectivity settings? What boundaries should apply to syncing and sharing?

Accessibility and usage context

- What noise and risk environments are you typically in? Is voice interaction feasible there? What assists do you need (high volume, directional audio, haptics, short commands)?
- Do you need dialect/accent support or special modes (children, elders)? Any other accessibility needs?
- Which form factor would you most likely use? (Mobile app, public terminal, volunteer handheld, notice board/broadcast)

Trust and human-in-the-loop

- What would make you trust or distrust an AI system? (Institutional backing, transparency, explainability, community ratings, offline operation)
- In which moments must a human be involved? (High-risk psychological crisis, confirming family matches, abnormal triage)
- If errors or misuse occur, what appeal and correction mechanisms do you expect?

Value and success criteria

- What outcomes would mean "this system helped you"? (Safer route, reduced panic, shorter waiting, successful reconnection)
- What minimum response times and success rates do you expect? Under what conditions would you use or recommend it again?

Closing and co-creation

- If you could change one thing about such a system, what would you change first?
- Is there anything important we didn't ask about?
- Would you be open to participating in follow-up co-design or prototype testing?

Interview tips (for your team)

- Use open-ended, non-leading questions; allow pauses and opting out of sensitive topics.
- Provide content warnings for potentially triggering questions; have support resources ready.
- Record contextual variables (language/dialect, noise level, device access) to inform design.
- Reiterate privacy and withdrawal rights at the end; ask consent for future contact.

### **3\. What to Ask**

**A. Core Needs & Practicality**

- Which option best meets your most urgent need?
- If only 2-3 features, which are essential?
- Which is most practical in your context (hospital, shelter, volunteer mgmt)?

**B. Cognitive Load & Usability**

- Which option is simplest under stress?
- Which communication mode (voice, voice+text, menus) is clearest?

**C. Trust & Reliability**

- Which design inspires most trust? Should it show data source/timestamp?
- If it fails, what fallback do you prefer (human contact, safety guidance)?

The final Idea 1, the **Voice Agent for Psychological Support**, is designed to deliver immediate, trauma-informed psychological first aid and survival guidance in hostile, low-connectivity environments.

For prototyping human-robot interaction (HRI) solutions, core features must be fully implemented (**Vertical Prototyping**), while less critical or complex features can be demonstrated through simulation or mockups (**Horizontal Prototyping**).

Here is a breakdown of the suggested Vertical and Horizontal features for Idea 1, drawing extensively from the detailed project plan and requirements:

## **Vertical Features (Core Implementation - Must be Live Demo)**

Vertical prototyping requires the actual implementation of core interactions without using "Wizard-of-Oz" techniques, enabling a recorded live demonstration of the solution's key functionality. For Idea 1, the core interactions revolve around safe, evidence-aligned conversational support:

| **Feature Category** | **Specific Vertical Implementation** | **Source Support** |
| --- | --- | --- |
| **Core Conversational Flow** | **Immediate Calming Techniques:** Full implementation of structured dialogue to guide users through initial coping strategies like breathing exercises and grounding techniques (e.g., 5-4-3-2-1 sensory exercises). |     |
| --- | --- | --- |
| **Dialogue Engine Safety** | **Trauma-Informed Dialogue:** Implementation of the conversational rules, ensuring a calm, warm, and non-judgmental tone, while strictly avoiding prohibited actions (e.g., asking for trauma details, giving unsolicited advice). |     |
| --- | --- | --- |
| **Critical Functionality** | **Offline Mode Operation:** The core psychological support and access to the offline content library must be functional without any internet connection, demonstrating reliability in hostile conditions. |     |
| --- | --- | --- |
| **Basic Crisis Detection** | **Vocal Feature Monitoring (Reflection):** Implementation of basic voice analysis to detect vocal features (e.g., pace or pauses) and reflect them gently to the user as a signal (e.g., "Your voice sounds strained... let's slow your breathing together"). |     |
| --- | --- | --- |
| **Information Dissemination** | **Psychoeducation Delivery:** Providing pre-scripted, evidence-aligned psychoeducation content that normalizes trauma responses ("What you're feeling is a normal reaction to abnormal circumstances"). |     |
| --- | --- | --- |
| **Interface Modality (If Applicable)** | **Simplified Interface (App):** If implemented as an app, developing the simplified interface with large buttons and high-contrast display for operation under stress. |     |
| --- | --- | --- |

## **Horizontal Features (Simulated, Mocked, or Wizard-of-Oz)**

Horizontal prototyping allows the design vision to be broadened by representing features through sketches, mock data, or manual manipulation (Wizard-of-Oz), especially for complex or infrastructural components.

| **Feature Category** | **Specific Horizontal Implementation (Simulated or Mocked)** | **Source Support** |
| --- | --- | --- |
| **Advanced Crisis Detection** | **Multi-dimensional Crisis Detection:** Simulation of complex detection inputs, such as analyzing behavioral patterns (midnight distress calls), complex language patterns (suicidal ideation, dissociation symptoms), or integrating optional physiological data (abnormal heart rate/breathing via mock flags). |     |
| --- | --- | --- |
| **Tiered Escalation** | **Human-in-the-Loop Verification and L2-L4 Response:** Critical alerts requiring Level 2 (peer volunteer), Level 3 (professional mental health worker), or Level 4 (emergency intervention) contact can be mocked or flagged in a staff UI, with the full verification/alert system being simulated. |     |
| --- | --- | --- |
| **Hostile Hardware Specs** | **Ruggedized Design/Advanced Hardware:** The physical properties of the device (e.g., 72-hour extended battery life, MIL-STD-810G shock resistance, Bone conduction microphone, Directional speakers) can be described via product illustrations or technical specifications rather than fully built and tested. |     |
| --- | --- | --- |
| **Navigation and Real-time Alerts** | **Danger Zone Marking/Crowd-sourced Updates:** The integration of real-time conflict data or user-reported unsafe routes for navigation features should be represented by using pre-cached mock data to demonstrate functionality, rather than implementing live API integration. |     |
| --- | --- | --- |
| **Advanced LLM/Long-Term Support** | **Long-term Resilience Building/Grief Support:** The protocols for long-term psychological resilience building or grief support and the use of reinforcement learning with a database can be outlined and shown via mock content menus, as the full therapeutic efficacy requires long-term validation and scaling. |     |
| --- | --- | --- |
| **Technical Optimization** | **Model Optimization and Progressive Enhancement:** The use of quantized LLMs (e.g., Llama 3.2 or Phi-3-mini) for offline performance or sophisticated progressive enhancement (working better with connectivity) can be detailed in the technical architecture, but the resource optimization itself does not need a live demo comparison. |     |
| --- | --- | --- |

Final idea (idea 1)

Oct 13 TODO (Deadline Oct 15, 10am)

Online Research: (Main PICs written, others help find relevant info if have time)

- Info searching
  - Needfinding on social media (posts about how people feel in war, what happens, what have they experienced) e.g. reddit, quora
    - Jenson
  - More background information on war and disaster (how do things actually happen?)
    - Harry
  - Impact on health, statistics about trauma, mental health issues, etc in war
    - Angel
- Developing the psychological support model
  - Current solutions/methods, existing models
    - Offline chatbot, need to consider limited access to information (firewall, no internet in bomb shelters, etc)
    - Yuhua
  - Conceptualization (about counselling, psychological support, etc)
    - Angel

Info Organization

- Summarize and organize insights & needs from interview transcripts
  - Voiressa

Needfinding on reddit

[Here's a story from someone who lived through 3 civil wars in West Africa. : r/preppers](https://www.reddit.com/r/preppers/comments/hvgemh/heres_a_story_from_someone_who_lived_through_3/)

The source presents a firsthand account from a "prepper" who lived through civil wars in three West African nations-Liberia, Sierra Leone, and Gambia-to offer survival insights. A central theme is the speed of **societal deterioration** and the shift from denial to **extreme desperation** within about a week of a crisis, making personal safety paramount. The author emphasizes that **basic necessities** like rice, clean water, and simple commodities such as coffee and sugar become the most valuable assets, more so than large caches of weaponry, which can actually make a small group a **target for armed robbers**. Ultimately, the narrative stresses the importance of **banding together and laying low** with like-minded allies, focusing on community and maintaining a sense of normalcy, rather than drawing attention with excessive defense or high-value, non-essential goods.

[How would you prepare if another civil war broke out in US? : r/preppers](https://www.reddit.com/r/preppers/comments/wqvi66/how_would_you_prepare_if_another_civil_war_broke/)

This Reddit thread from the r/preppers subreddit centers on a hypothetical discussion about **preparing for a modern civil war in the U.S.**, distinguishing it from typical natural disaster scenarios. Many commentators agree that any conflict would not resemble the large-scale, defined frontlines of the 1860s, but rather involve **isolated pockets of fighting, domestic terrorism, and anarchy**, particularly concentrated in urban areas. Key themes include the debate over whether to **"bug out" to another country** (considered the safest option by some) or **"bug in"** and defend a location, with various contributors emphasizing the need for robust supplies, including food, water, and security gear. There are differing opinions on the likelihood of such a war, with some suggesting a transition to **martial law** or a warlord-like feudal system due to the collapse of state structures, while others focus on maintaining basic self-reliance preparations that apply to any major grid-down event.

[Syrians, what did you experience during the civil war? Do you think that reconciliation is possible in the future?](https://www.reddit.com/r/AskMiddleEast/comments/13nprq9/syrians_what_did_you_experience_during_the_civil/)

This source is an excerpt from a Reddit thread on the r/AskMiddleEast subreddit, posing a direct and serious question to Syrians about their **experiences during the civil war** and the potential for **future reconciliation**. The resulting conversation reveals profoundly traumatic personal stories, including accounts of lost relatives, widespread family dispersal across continents, and the collapse of the economy and infrastructure within Syria. The comments also spark a debate regarding the **culpability for the devastating conflict**, with some blaming the Assad regime's violent suppression of initial protests and others pointing to the detrimental role of foreign intervention and the funding of extremist groups like ISIS by regional powers. Collectively, the responses paint a bleak picture of an **irreversible scar** on the nation, highlighting that while the war may be physically winding down, the deep-seated political divisions, economic destitution, and pervasive fear mean that a true return and recovery seem nearly impossible for many displaced Syrians.

[My mother, who survived a brutal civil war as a teen, has been extremely spooked lately.](https://www.reddit.com/r/TwoXPreppers/comments/1impz84/my_mother_who_survived_a_brutal_civil_war_as_a/)

This collection of Reddit comments from the subreddit "TwoXPreppers" reveals a community intensely focused on **prepping for societal or governmental collapse**, with an emphasis on the distinct and heightened threats faced by women and minorities. Drawing on the traumatic historical experiences of ancestors who survived events like the Rwandan genocide, the Holocaust, and civil wars, posters express a pervasive sense of **fear and pattern recognition**, noting alarming similarities between current political trends in the US and the precursors to past authoritarian regimes. Key discussions revolve around practical survival strategies, such as securing **critical documents, storing emergency funds in gold or foreign currency**, and the difficult decision of whether to **flee the country or stay and resist**. The consensus highlights a perceived difference in preparedness and awareness, suggesting that men in the general prepping community are less alarmed because they are less likely to be immediately or severely impacted compared to women, particularly minority women.

[r/changemyview on Reddit: CMV: The global outrage over some civilian deaths while ignoring others reveals selective morality, not true empathy.](https://www.reddit.com/r/changemyview/comments/1kh09qd/cmv_the_global_outrage_over_some_civilian_deaths/)

This source presents a "Change My View" discussion from Reddit, centered on the argument that global condemnation of civilian deaths in conflict is characterized by **selective outrage** driven by political alignment rather than genuine, universal empathy. The original poster contends that while tragedies in places like Gaza and Ukraine receive intense global media coverage and activism, comparably horrific terrorist attacks in India, such as Pulwama or 26/11, are largely ignored or deemed "complicated" due to **geopolitical factors** involving Pakistan. Commentary on the post suggests that this perceived inconsistency stems less from a lack of inherent human empathy and more from **selective media presentation** and the scale of the conflict, pointing out that Western involvement and the sheer magnitude of casualties in conflicts like Gaza and Ukraine naturally draw greater attention than lower-casualty, less-publicized events in other regions. Ultimately, the debate explores whether the visible global response to suffering is a true measure of moral concern or simply a product of **political narratives** and media prioritization.

[Civilian Experiences in the Bosnian War : r/preppers](https://www.reddit.com/r/preppers/comments/17xxqy4/civilian_experiences_in_the_bosnian_war/)

This source is a collection of excerpts from the book **_Logavina Street: Life and Death in a Sarajevo Neighborhood_**, shared on a prepper forum to highlight **real-life civilian experiences** during the Bosnian War. The primary focus is the **extreme scarcity of resources**, particularly food and electricity, in Sarajevo, illustrating how residents adapted to survive the siege. Desperate measures included creating substitutes for expensive goods, such as frying lentils to imitate coffee, and resorting to eating pigeons; moreover, a major crisis occurred when a heatwave caused a massive loss of hoarded food due to **interminable blackouts**. Ultimately, the prolonged struggle for basic needs forced residents to cross ethical lines, notably by **stealing electricity** from the Bosnian prime minister's private home, reflecting the profound moral degradation caused by the war.

[The Realities of War - part 3.2 (How Civilians Die) : r/IsraelPalestine](https://www.reddit.com/r/IsraelPalestine/comments/1d4bscs/the_realities_of_war_part_32_how_civilians_die/)

This text is an excerpt from a Reddit post titled "The Realities of War," which aims to provide readers with a **pragmatic and informed framework** for analyzing current conflicts by sharing the author's military expertise. The core of the post is a detailed, fictionalized scenario placing the reader in the role of an infantry company commander, "Viper Actual," during a routine urban operation where a series of compounding factors, including a **critical miscommunication** and time pressure from higher command, leads to a tragic, unintended outcome. Despite the mission's tactical success with no reported military casualties, the commander's necessary but hurried decision to employ **artillery against a suspected enemy building** results in the collapse of the structure, unknowingly killing an innocent civilian family, illustrating the inevitability of **"Fog of War"** incidents and collateral damage in dense urban combat zones. Ultimately, the author argues that outside observers often mistake such unavoidable tragedies for "war crimes" because they lack the contextual understanding of the split-second decisions and **imperfect information** that characterize urban warfare, which is exacerbated when enemies deliberately operate among civilians.

[Every conflict in history has had traumatic loss of civilian life. Gaza is not even close to being the worst in history.](https://www.reddit.com/r/TrueUnpopularOpinion/comments/1bmb8i3/every_conflict_in_history_has_had_traumatic_loss/)

This source is an excerpt from a Reddit discussion thread titled "Every conflict in history has had traumatic loss of civilian life. Gaza is not even close to being the worst in history," which is marked as an **"Unpopular in General"** opinion. The primary purpose of the thread is to debate the **scale and moral equivalence of the current Gaza conflict** compared to historical and contemporary wars, particularly questioning the intense global focus on Gaza versus other humanitarian crises like those in Sudan or Yemen. Commenters intensely dispute whether Israel's actions constitute **genocide** and accuse proponents of both sides of using **propaganda** to frame the narrative, with some arguing that Hamas deliberately uses civilians to draw condemnation on Israel, while others claim Israel is a "genocidal colonizer state." A secondary theme is the **nature of anti-war sentiment**, with one comment highlighting the mistreatment of WWI veterans after a celebratory return, contrasting the public perception of war versus its actual human cost.

[People forget that war sucks. : r/Israel](https://www.reddit.com/r/Israel/comments/1d35c24/people_forget_that_war_sucks/)

​​This Reddit discussion from the r/Israel subreddit centers on the fundamental belief that **war is inherently unjust and brutal**, with the primary poster suggesting that younger generations are having a disproportionately strong, visceral reaction because the current conflict is their **first exposure to the inhumanity of war**. The core argument claims that while all wars are terrible, the ongoing conflict is "unusually kind" or "cleaner" than historical or contemporary Middle Eastern wars, citing Israel's unusually low combatant-to-civilian casualty ratio and efforts to provide aid as evidence of a higher **moral baseline** than typically seen in warfare. The commenters largely agree with the premise that modern audiences are generally **unaware of war's true brutality**, leading to misunderstanding and accusations against Israel, which the submitter attributes to propaganda and a lack of historical context. One counter-argument is that the visceral reaction stems from antisemitism or a lack of empathy among younger people, rather than simple inexperience with the historical horror of war.

[Civil unrest preparedness, what does this look like? : r/preppers](https://www.reddit.com/r/preppers/comments/1e3zzcb/civil_unrest_preparedness_what_does_this_look_like/)

This collection of online comments from a prepper community discusses **preparedness for civil unrest and large-scale disasters**, centering on the difficult choice between **sheltering in place versus evacuating** a metropolitan area. A key theme revolves around the need for **self-sufficiency and essential supplies**, especially maintaining a full gas tank and having accessible cash reserves, since core public services like transit, water, and electricity are expected to fail. Many contributors advocate for **blending in and remaining discreet** to avoid becoming a target, while others debate the safety of suburbs versus central city locations and share practical tips for fortifying a home or creating a disguised storage area for emergency rations.

Here's a concise point-form summary of each source:

### **1\. Firsthand Account: Surviving 3 Civil Wars in West Africa**

- **Useful**
- **Source:** r/preppers
- **Key Points:**
  - Societal collapse happens **rapidly** (within a week), shifting from denial to desperation.
  - **Basic necessities** (rice, clean water, coffee, sugar) become more valuable than weapons.
  - Large weapon caches can make you a **target** for armed robbers.
  - **Community is crucial**: Band together with like-minded allies, avoid drawing attention, and maintain normalcy.

### **2\. Preparing for a Modern US Civil War**

- **Somewhat useful**
- **Source:** r/preppers
- **Key Points:**
  - Conflict would likely involve **isolated pockets of fighting, terrorism, and urban anarchy**-not traditional frontlines.
  - Debate: **"Bug out" (leave the country) vs. "bug in" (stay and defend)**.
  - **Essential supplies**: Food, water, security gear, and self-reliance preparations.
  - Some predict **martial law or feudal warlord systems** if state structures collapse.

### **3\. Syrian Civil War Experiences & Reconciliation**

- **Useful**
- **Source:** r/AskMiddleEast
- **Key Points:**
  - **Traumatic personal stories**: Lost relatives, family dispersal, economic/infrastructure collapse.
  - **Blame is divided**: Assad regime's violence vs. foreign intervention/extremist funding.
  - **Reconciliation seems impossible**: Deep political divisions, economic ruin, and fear persist even as fighting winds down.

### **4\. Mother's Trauma from Civil War Sparks Prepping**

- **Useful**
- **Source:** r/TwoXPreppers
- **Key Points:**
  - **Focus on threats to women/minorities** in societal collapse scenarios.
  - **Practical strategies**: Secure documents, store gold/foreign currency, debate fleeing vs. resisting.
  - **Gender divide in prepping**: Women often more alarmed due to historical vulnerability.

### **5\. Selective Outrage Over Civilian Deaths in Conflicts**

- **Not useful**
- **Source:** r/changemyview
- **Key Points:**
  - **Global outrage is selective**: Gaza/Ukraine get attention; Pulwama/26/11 (India) are ignored.
  - **Why?** Media focus, scale of conflict, and Western involvement drive visibility.
  - **Debate**: Is it moral inconsistency or just media/geopolitical bias?

### **6\. Bosnian War: Civilian Survival Realities**

- **Useful**
- **Source:** r/preppers (excerpts from _Logavina Street_)
- **Key Points:**
  - **Extreme scarcity**: Food, electricity, and basic goods became luxuries.
  - **Adaptations**: Fried lentils as coffee, eating pigeons, stealing electricity.
  - **Moral degradation**: Survival forced ethical compromises.

### **7\. How Civilians Die in War (Fictionalized Scenario)**

- **Useful**
- **Source:** r/IsraelPalestine
- **Key Points:**
  - **"Fog of War"**: Miscommunication and time pressure lead to tragic civilian casualties.
  - **Urban warfare risks**: Collateral damage is inevitable; enemies exploit civilian presence.
  - **Public perception**: Observers often mislabel unavoidable tragedies as "war crimes."

### **8\. Gaza Conflict: Scale vs. Global Attention**

- **Not useful**
- **Source:** Reddit (Unpopular Opinion)
- **Key Points:**
  - **Gaza is not the worst conflict historically**, but receives disproportionate focus.
  - **Debate**: Is Israel's actions genocide? Or is Hamas using civilians as shields?
  - **Anti-war sentiment**: Public often lacks context on war's true brutality.

### **9\. War is Inherently Brutal**

- **Not very useful**
- **Source:** r/Israel
- **Key Points:**
  - **Younger generations** react strongly because they've never experienced war's horrors.
  - **Israel's conflict is "cleaner"**: Lower civilian-to-combatant ratio, aid efforts.
  - **Misunderstanding**: Lack of historical context fuels accusations against Israel.

### **10\. Civil Unrest Preparedness**

- **Somewhat Useful**
- **Source:** r/preppers
- **Key Points:**
  - **Shelter in place vs. evacuate**: Weigh risks of urban vs. suburban locations.
  - **Essentials**: Full gas tank, cash, self-sufficiency, and discretion.
  - **Home fortification**: Hide supplies, blend in, and prepare for service failures.

Insights from Interview

| **Name** | **Basic Infos** | **War Experience** | **Needs** | **Key Takeaways** |
| --- | --- | --- | --- | --- |
| **Jane** | **Ukranian,**<br><br>25 yrs old, f<br><br>Unemployed,<br><br>Witness of war | Lived through bombings, blackouts, and displacements;<br><br>moved multiple times since 2022. | **Safety & Control:** Needs clear, real-time updates to feel secure and reduce anxiety.  <br><br>**Mental Support:** Open to AI for comfort and companionship, though avoids war-related topics.  <br><br>**Cultural Fit:** Prefers Ukrainian; warmth and empathy matter more than flawless tech.  <br><br>**Trust:** Mild privacy concern; transparency appreciated but not critical.<br><br>**Kids-mode** would be helpful | Users want **emotional grounding**, not just crisis information.  <br><br>The agent should act as a **companion and coping aid**, offering calm, presence, and understanding.  <br><br>**Localized language and empathy** are critical to trust and sustained use.  <br><br>Focus on **resilience and psychological continuity**, not just emergency response. |
| --- | --- | --- | --- | --- |
| **Misrete** | **Kosovo-Albanian,**<br><br>46 yrs old, f<br><br>Housewife,<br><br>Witness of war | Schools closed after murders; friends killed. Brother fled to avoid army draft. She and siblings hid with relatives; father and uncle stayed to protect home and animals. | **Basic Security:** Needs during war-safe shelter, food, healthcare, education, contact with humanitarian aid.  <br><br>**Psychological Need:** Deep mistrust from past trauma; struggles to trust people or technology.  <br><br>**Emotional Outlet:** Values the idea of a **_private diary_** to document experiences-both for memory and emotional healing.  <br><br>**Access Limitations:** Concerned about losing access when technology or networks fail. | Misrete represents **low-tech, trauma-affected** users who need **emotional expression** more than complex AI features.<br><br>The most valuable functions: **safe listening, diary keeping, reassurance, and trust-building**-not information delivery.<br><br>For such users, **simplicity, empathy, and privacy assurances** outweigh sophistication or speed. |
| --- | --- | --- | --- | --- |
| **Mary** | **Syrian,**<br><br>20 yrs old, f<br><br>Student,<br><br>Witness of War | Lived through the Syrian Revolution as a child - witnessed bombings, looting, and gunfire; fled multiple times within Syria. Family home was looted but survived. | **Mental Health Recovery:** Needs a sense of safety, calm, and emotional regulation to cope with trauma.<br><br>**Trust & Security:** Sensitive about data privacy; needs reassurance and control over what's shared.<br><br>  <br>**Human Connection:** Would respond well to emotionally intelligent, empathetic, and validating communication.<br><br>  <br>**Cultural Context:** Feels comfortable in English, but carries deep emotional and cultural trauma tied to war and displacement. | **Emotional Sensitivity:** Design with trauma-aware language-calm, grounding, and validating.  <br><br>**Trust Architecture:** Emphasize transparency, privacy, and visible human oversight.  <br><br>**Modality Flexibility:** Offer both text and voice; allow private, low-pressure interaction.  <br><br>**Therapeutic Role:** Focus on safety reinforcement, emotional reflection, and self-regulation-help users like Mariam rebuild a sense of inner security after prolonged exposure to war. |
| --- | --- | --- | --- | --- |
| **Ahmad** | **Syrian,**<br><br>20 yrs old, m<br><br>Student,<br><br>Witness of War | Lost grandmother and friends; displaced four times.  <br><br>Family lost wealth and stability.  <br><br>Witnessed violence and humiliation.  <br><br>Now safe but carries lasting trauma. | **Core Needs During War:** Safety (shelters, food, medical aid, fuel, gas masks).  <br><br>**Ongoing Emotional Needs:  <br>Processing grief, loss, and displacement**.  <br>Coping with **financial stress** and disrupted life goals.  <br>Rebuilding **trust and stability** after witnessing corruption and violence.  <br>Providing comfort to others-he takes on **emotional labor** by consoling war victims.  <br><br>**Psychological Themes:** Survivor's guilt, resilience under instability, suppressed anger toward injustice. | Ahmad represents **young survivors balancing recovery and responsibility**.<br><br>Values **safety, dignity, and neutrality** above all.<br><br>Would respond best to a chatbot that feels **secure, humanly understanding, and apolitical**-a calm, private space for resilience and healing. |
| --- | --- | --- | --- | --- |
| **Christy** | **HongKongness,**<br><br>21 yrs old, f<br><br>Student,<br><br>Volunteer | Volunteer in education and disaster relief projects (e.g., Indonesia, Vietnam). | **Communication Clarity:** Needs **accurate, real-time transcription and translation** tools to overcome language and cultural barriers with locals and coworkers.  <br><br>**Information Flow:** Requires **consistent, centralized communication** during operations-unclear instructions from coordinators slow response.  <br><br>**Emotional Support:** Believes volunteers **need mental and emotional check-in systems**, but notes people rarely use them due to low awareness or motivation.  <br><br>**Trust & Security:** Wants transparent systems but doubts corporate reliability; supports **legally backed privacy protection**.  <br><br>**Efficiency Tools:** Seeks digital aids that **simplify coordination and task management** under pressure, especially in multilingual teams. | **Language Barriers:** Main obstacle; real-time translation and transcription are key to coordination.<br><br>**Usefulness First:** Volunteers adopt tech only if it clearly improves speed and clarity.<br><br>**Emotional Labor:** Present but secondary to operational efficiency.<br><br>**Trust Gap:** Needs transparency and accuracy, not corporate promises.<br><br>**Design Focus:** Prioritize clear communication, live updates, and simple workflows. |
| --- | --- | --- | --- | --- |

**Core Insights**

| **Emotional Support Over Information Delivery** | Users need emotional companionship and psychological grounding, not just crisis information. The AI should act as a companion and coping aid, providing calm, presence, and understanding to help users build psychological resilience and emotional continuity. |
| --- | --- |
| **Trauma-Informed Design is Critical** | For trauma-affected, low-tech users like Misrete, trauma-aware language is essential-calm, grounding, and validating. Core functions should focus on safe listening, diary keeping, reassurance, and trust-building. Simplicity, empathy, and privacy assurances outweigh complex features. |
| --- | --- |
| **Trust Architecture and Localized Empathy** | Emphasize transparency, privacy protection, and visible human oversight. Localized language and cultural empathy are critical to building trust and sustained use. Users like Ahmad need a space that feels secure, dignified, and politically neutral for recovery and healing. |
| --- | --- |
| **Multimodal Flexibility, Self-Regulation Support, and Age-Appropriate Design** | Offer both text and voice modalities, allowing private, low-pressure interaction. Play a therapeutic role focused on safety reinforcement, emotional reflection, and self-regulation to help users rebuild inner security after prolonged war exposure.<br><br>**Specialized modes for different age groups (especially children) are essential**, using age-appropriate language, interaction styles, and emotional support strategies to meet developmental psychological needs. |
| --- | --- |
| **Volunteer Scenario: Practicality and Clear Communication** | For volunteer coordination scenarios, language barriers are the main obstacle-real-time translation and transcription are key. Volunteers only adopt technology that clearly improves speed and clarity. Design should prioritize clear communication, live updates, and simple workflows over corporate promises. |
| --- | --- |

**Core Needs**

| **Real-Time Safety & Situational Awareness** | Users need clear, immediate updates on threats, safe zones, shelter locations, food distribution, and medical aid to feel secure and reduce anxiety. Timely information is critical for survival and decision-making during active conflict. |
| --- | --- |
| **Emotional Support & Companionship** | Users are open to AI for comfort, mental support, and companionship during isolation and trauma. They need validation, empathetic listening, and a calm presence-but prefer to avoid triggering war-related topics unless they initiate them. |
| --- | --- |
| **Private Emotional Outlet & Documentation** | A secure, private space for diary-keeping and emotional expression is deeply valued. Users want to document experiences for both memory preservation and emotional healing, without fear of exposure or judgment. |
| --- | --- |
| **Mental Health Recovery & Self-Regulation** | Users need tools that foster a sense of safety, calm, and emotional regulation to cope with ongoing trauma. This includes grounding techniques, reassurance, and support for processing grief, loss, displacement, and survivor's guilt. |
| --- | --- |
| **Trust, Privacy, & Transparent Control** | Deep mistrust from past trauma makes data privacy and transparency non-negotiable. Users need clear reassurance about what's shared, visible human oversight, and legally backed privacy protections. They want control over their information and doubt corporate reliability. |
| --- | --- |
| **Localized Language & Cultural Sensitivity** | Users prefer communication in their native language (e.g., Ukrainian) with culturally aware empathy. Warmth, emotional intelligence, and cultural understanding matter more than flawless technology. Language barriers must be addressed with real-time translation for effective coordination. |
| --- | --- |
| **Age-Appropriate & Developmentally Sensitive Design** | A dedicated children's mode is essential, with age-appropriate language, interaction styles, and trauma-informed content. Different age groups require tailored emotional support strategies that match their developmental psychological needs. |
| --- | --- |
| **Human Connection & Emotional Intelligence** | Users respond best to communication that feels humanly understanding, validating, and emotionally intelligent. They need to feel heard and supported, not processed by a machine. Empathy and presence are more important than speed or sophistication. |
| --- | --- |
| **Reliable Access & Offline Functionality** | Users are concerned about losing access when technology or networks fail during crisis situations. They need systems that work with limited connectivity, have backup options, and don't disappear when infrastructure is compromised. |
| --- | --- |
| **Practical Coordination Tools for Volunteers** | Volunteers need efficient, simple tools for multilingual team coordination-accurate real-time transcription, translation, centralized communication channels, and clear task management systems. They adopt technology only when it demonstrably improves operational speed, clarity, and effectiveness under pressure. |
| --- | --- |

Logistics

# Disaster Management logistics

In general, there are 5 phases for emergency management (not just for war situations)

- **Prevention**
- **Mitigation**
  - measures or actions that can prevent an emergency, reduce the chance of an emergency or reduce the damaging effects of unavoidable emergencies
- **Preparedness**
  - continuous cycle of planning, organizing, training, equipping, exercising, evaluating and taking corrective action
  - readiness to respond to all hazards, incidents and emergencies
  - increase a community's ability to respond when a disaster occurs
- **Response**
  - saving lives, reducing economic losses and alleviating suffering
- **Recovery**
  - bring the affected area back to some degree of normalcy

Organisations such as the United Nations and the International Committee for the Red Cross, as well as local governments, provide various protection services to people in need.

## Specific steps taken by various organisations/governments

### United Nations High Commissioner for Refugees (UNHCR)

The UNHCR performs various activities for protecting refugees and people in war situations

- **Conflict analysis:** understand underlying causes and context of a conflict
  - Understanding the conflict and its context, including root causes,
  - Knowing the communities and leaders involved and their context,
  - Identifying the main parties to the conflict and their interests including needs, fears, concerns and aspirations,
  - Understanding the motivations behind any deliberate attacks on civilians.
- **Protection analysis:** identifying the main protection risks for & needs of affected people
- **Protection monitoring:** looks at changes in the protection situation over time, and identifies relevant patterns and protection incidents
- **Dialogue and engagement:** humanitarians engage with armed actors and other duty bearers to limit the effects of the conflict on civilians, and promote the rights of individuals
- **Protection by presence**, usually in synergy with other approaches such as Community Support Projects (CSPs) and protection monitoring,
- **Reinforcing self-protection mechanisms,** such as community policing, mobile courts and community-based contingency plans for cyclical displacement,
- **Humanitarian evacuations (last resort)**
  - Never constitute in itself a durable solution and must be carried out only after careful decision-making, planning and risk management
- **Risk management**
  - "Mistakes and ill judgement can lead to death, injury or reputational damage. It is essential that strategies, alliances, engagement and operations are based on careful risk and benefit assessment and respect the do-no-harm principle. Strict adherence to humanitarian principles is a must." ([see here](https://emergency.unhcr.org/protection/protection-mechanisms/protection-armed-conflict#:~:text=Mistakes%20and%20ill%20judgement%20can%20lead%20to%20death%2C%20injury%20or%20reputational%20damage.%20It%20is%20essential%20that%20strategies%2C%20alliances%2C%20engagement%20and%20operations%20are%20based%20on%20careful%20risk%20and%20benefit%20assessment%20and%20respect%20the%20do%2Dno%2Dharm%20principle.%20Strict%20adherence%20to%20humanitarian%20principles%20is%20a%20must.))
- **Post emergency phase**
  - "Integral to this effort is the development of conflict-sensitive preparedness, contingency plans and protection analyses, along with meaningful engagement and partnerships with key actors. Active engagement with peace and development actors during the transition from emergency to post-emergency phases is crucial in the overarching goal of peacebuilding.  
        <br/>Many return movements will occur within a post-emergency phase. However, refugees and IDPs may not always return after all causes of displacement have disappeared. Thus, protection in armed conflict may still be relevant during return movements." ([see here](https://emergency.unhcr.org/protection/protection-mechanisms/protection-armed-conflict#:~:text=Integral%20to%20this,during%20return%20movements.))

### International Committee for the Red Cross (ICRC)

The ICRC designs and implements various protection activities as well as activities for reducing/eliminating violations of the IHL (international humanitarian law)

### Governments (Example: UAE government)

The UAE government provides various services and guides for people in the country during/before an emergency.

In a pamphlet found online (see \[4\]) outlying the steps that people in the UAE may take when encountering emergency situations, the government provides these services and guides:

- **Water, food and gas distribution**
- **Blood donation**
- **Public warning system**
- Guides to **providing, setting up and protecting shelters**
- Guides on **defensive precautions**

# References

- **5 phases of emergency management**  
    <https://www.unr.edu/organizational-resilience/phases>
- **UNHCR: Protection in Armed Conflict**  
    <https://emergency.unhcr.org/protection/protection-mechanisms/protection-armed-conflict>
- **Enhancing protection: for civilians in armed conflict and other situations of violence**  
    <https://www.icrc.org/sites/default/files/external/doc/en/assets/files/other/icrc_002_0956.pdf>
- **(UAE) National Emergency Crisis and Disaster Management Authority: Emergency Guide**  
    <https://www.ncema.gov.ae/content/documents/ENGLISH/War-Emergencies.pdf>

Health

- **Three years of war: rising demand for mental health support, trauma care and rehabilitation  
    **[**https://www.who.int/europe/news/item/24-02-2025-three-years-of-war-rising-demand-for-mental-health-support-trauma-care-and-rehabilitation**](https://www.who.int/europe/news/item/24-02-2025-three-years-of-war-rising-demand-for-mental-health-support-trauma-care-and-rehabilitation)
- **As Russian troops cross into Ukraine, we need to remind ourselves of the impact of war on health**  
    <https://www.bmj.com/content/376/bmj.o499>  
    (Notes)
- **Prevalence of depression, anxiety and post-traumatic stress in war- and conflict-afflicted areas: A meta-analysis  
    **[**https://www.frontiersin.org/journals/psychiatry/articles/10.3389/fpsyt.2022.978703/full**](https://www.frontiersin.org/journals/psychiatry/articles/10.3389/fpsyt.2022.978703/full)The aggregate prevalence rates among populations experiencing war and conflict for mental health conditions are:
  - Depression: 28.9%
  - Anxiety: 30.7%
  - Post-traumatic stress symptoms (PTSD): 23.5%

Civilians have a significantly higher prevalence of depression (around 33.3%) and anxiety (38.6%) compared to military personnel (depression 24.0%, anxiety 16.2%). The difference in post-traumatic stress prevalence between civilians (25.7%) and military (21.3%) was not significant.

The prevalence of depression and anxiety is significantly higher during wars than post-war. For instance, depression prevalence during wars is about 38.7%, dropping to 29.1% post-war; anxiety is 43.4% during wars, declining to 30.3% post-war.

- **Scars Unseen: The Enduring Effects of War on Children's Mental Health**  
    <https://www.psychiatryadvisor.com/features/psychological-effects-of-war-on-children/>  
    Overview with info and statistics from many different studies  

- Carpiniello B. **The mental health costs of armed conflicts-a review of systematic reviews conducted on refugees, asylum-seekers and people living in war zones.** Int J Environ Res Public Health. 2023;20(4):2840. doi:10.3390/ijerph20042840  
    <br/>"individuals [exposed to armed conflict](https://www.neurologyadvisor.com/features/conflict-and-health/#xd_co_f=N2QzYzY1YTEtMWQwMi00OTA5LWJiMTktOTQ5N2YwYTVkYTIz~) are 3 times as likely to develop post-traumatic stress disorder (PTSD), anxiety disorders, or major depression, and women and children demonstrate increased vulnerability to these outcomes"  

- Kovnick MO, Young Y, Tran N, Teerawichitchainan B, Tran TK, Korinek K. **The impact of early life war exposure on mental health among older adults in northern and central Vietnam.** J Health Soc Behav. 2021;62(4):526-544. doi:10.1177/00221465211039239  
    <br/>Investigators assessed 5 distinct categories of wartime stress exposures (loss of family and friends, witnessing death, malevolent living conditions, life threat and personal endangerment, and moral injury). Loss of family and friends, witnessing death, and malevolent living conditions posed greatest risk of increasing psychological distress.  

- Amsalem, D., Haim-Nachum, S., Lazarov, A. _et al._ **The effects of war-related experiences on mental health symptoms of individuals living in conflict zones: a longitudinal study.** _Sci Rep_ 15, 889 (2025). <https://doi.org/10.1038/s41598-024-84410-3>  
    <br/>Examined effects of war-related experiences on mental health of individuals living in conflict zones in Israel following the attack on Oct 7 2023 and the subsequent war.  
    <br/>Assessed symptoms of anxiety, depression, PTSD. Longitudinal study over three months with sample size = 1052, individuals aged 18-40.  
    <br/>Over 75% of participants reported above-threshold symptoms of anxiety, depression, or PTSD at the outset, with a slight decrease over the three months but remaining high.  
    <br/>Some groups of individuals showed higher symptoms of anxiety, depression, PTSD:
  - Women
  - Those experiencing traumatic losses, forced displacement, or economic hardships
  - Ethnic minority groups  

Current Solution

- Title (link) A digital self-help tool to promote mental well-being for Ukrainians affected by war - Assessing predictors of stress

link:<https://www.sciencedirect.com/science/article/pii/S2772408524001546>  
Paper summary (concise)

- Context: Early months of the Ukraine war. The team deployed a Telegram chatbot ("Friend") delivering digital Psychological First Aid (PFA) to civilians.
- Goal: Identify early predictors of baseline stress during the "golden window" (first 3 months post-trauma) and observe short-term stress reduction from a brief digital intervention.
- Participants: 3,740 Ukrainian civilians (18-80), March-May 2022. Subsample (n=817) had pre-post stress ratings.
- Intervention: Scripted, modular PFA integrating WHO PFA Guide, RAPID model, mhGAP components, and MBSR techniques. Modules included safety check, psychoeducation, grounding/breathing, social connectedness, hope/strengths messages, and referral to free online counseling.
- Results:
  - Stress reduced in the pre-post subsample from M=6.25±2.22 to M=4.25±2.76; Cohen's d=0.73 (moderate-to-large).
  - Predictors of higher baseline stress: parenthood, feeling unsafe, and loneliness/isolation.
- Takeaways: Digital PFA is feasible under crisis conditions and can reduce short-term stress. Priority support should target parents, those who feel unsafe, and those who feel lonely.
- Limitations: Online convenience sample, self-report bias, limited control of confounders (prior MH, exposure intensity), early-phase only (no long-term effects), chatbot limits with complex trauma; generalizability constrained. Ethics: data minimization, encryption, local legal compliance.  

- The so called #1 therapist bot with positive clinical trial results:  
    <https://www.trytherabot.com/products>

Models

- <https://github.com/pychatbot-therapy/pychatbot-therapy>

Techs possible

# **Building a Crisis Emotional Support Chatbot: Required Resources & Implementation Plan**

## **I. Required Resources & Materials**

### **1\. User Research & Requirements Documentation**

- ✅ User personas (Misrete, Ahmad, volunteers, etc.)
- ✅ Core needs and insights summary
- Still needed:
  - Specific needs for different age groups (especially children)
  - Cultural taboos and sensitive topics list
  - Typical conversation scenarios

### **2\. Trauma-Informed & Mental Health Resources**

- Trauma-Informed Care (TIC) principles and guidelines
- Conversation frameworks for PTSD, anxiety, grief counseling
- Psychological First Aid (PFA) protocols
- Self-regulation and grounding techniques
- Crisis escalation procedures (when human intervention is needed)
- Child developmental stages and corresponding support strategies

### **3\. Localization & Cultural Adaptation**

- Professional translation resources for target languages (Ukrainian, Arabic, etc.)
- Cultural advisors and local reviewers
- Cultural sensitivity guidelines in war contexts
- Religious and cultural practice considerations

### **4\. Technical & Data Resources**

- Secure, reliable cloud infrastructure (GDPR-compliant)
- End-to-end encryption technology
- Offline functionality support (local caching, PWA)
- Speech-to-text and multilingual translation APIs
- Sentiment analysis and risk detection models

### **5\. Content & Training Data**

- Trauma-sensitive conversation template library
- Positive and negative examples (what to say/what NOT to say)
- Conversation style samples for different age groups
- Human-reviewed high-quality conversation data
- ⚠️ Note: Avoid using real users' trauma experiences as training data to protect privacy

### **6\. Compliance & Ethics Documentation**

- Privacy policy and user agreements
- Data Protection Impact Assessment (DPIA)
- Ethics review and risk assessment
- Human oversight and escalation mechanisms
- Child protection policies

## **II. Technical Implementation Plan**

### **Architecture Design**

User Interface Layer

├── Web/Mobile App (PWA for offline support)

├── Voice input/output interface

└── Multi-language switching

AI Agent Core

├── Large Language Model (Claude/GPT, etc.)

│ ├── Trauma-informed prompt engineering

│ ├── Age-adaptive mode switching

│ └── Cultural sensitivity constraints

├── Emotional Detection Module

│ ├── Emotion recognition

│ ├── Crisis risk assessment

│ └── Escalation triggers

└── Conversation Management

├── Context memory

├── Diary functionality

└── Session history

Support Services Layer

├── Real-time translation API

├── Speech-to-text services

├── Secure storage (encrypted)

└── Human oversight interface

Infrastructure Layer

├── End-to-end encryption

├── Offline data synchronization

├── Backup & recovery

└── Logging & audit

### **Core Module Implementation**

#### **1\. Trauma-Informed Dialogue Engine**

**Prompt Engineering Example:**

System Prompt Framework:

You are a trauma-informed emotional support companion designed for people

experiencing war and crisis.

Core Principles:

\- Always maintain a calm, warm, non-judgmental tone

\- Prioritize validating user emotions ("Your feelings are completely normal")

\- Avoid giving unsolicited advice

\- Use grounding and present-moment language ("You are safe right now")

\- Never minimize their experiences

Prohibited Actions:

\- Don't say "I understand how you feel" (unless user says it first)

\- Don't provide medical or legal advice

\- Don't ask for trauma details (let users lead sharing)

\- Don't use military or violent language

Escalation Triggers:

If suicidal ideation, child harm, or acute crisis is detected,

immediately trigger human intervention.

Age Modes:

\[Child Mode\] Use simple language, metaphors, gamification elements

\[Teen Mode\] Respect independence, provide peer-like support

\[Adult Mode\] Professional, respectful, empowerment-oriented

#### **2\. Age-Adaptive System**

\# Pseudocode example

class AgeAdaptiveAgent:

def \__init_\_(self):

self.modes = {

'child': ChildMode(), # Ages 5-12

'teen': TeenMode(), # Ages 13-17

'adult': AdultMode(), # Ages 18+

}

def select_mode(self, user_age):

if user_age < 13:

return self.modes\['child'\]

elif user_age < 18:

return self.modes\['teen'\]

else:

return self.modes\['adult'\]

def generate_response(self, user_input, user_age):

mode = self.select_mode(user_age)

\# Adjust language complexity

response = mode.adjust_language(user_input)

\# Apply age-specific emotional support strategies

response = mode.apply_support_strategy(response)

return response

class ChildMode:

def adjust_language(self, text):

\# Simplify vocabulary, use metaphors and stories

return simplified_text

def apply_support_strategy(self, text):

\# Use gamification, animal metaphors, color-based emotion expression

return child_friendly_text

#### **3\. Emotional Monitoring & Risk Assessment**

class EmotionalSafetyMonitor:

def analyze_risk_level(self, user_message, conversation_history):

risk_indicators = {

'self_harm': self_harm_detector(user_message),

'acute_distress': distress_level(user_message),

'dissociation': dissociation_signs(conversation_history),

'child_safety': child_risk_detector(user_message)

}

if any(risk_indicators.values() > CRITICAL_THRESHOLD):

return self.trigger_human_intervention()

return self.provide_grounding_support()

def trigger_human_intervention(self):

\# Notify human moderators

\# Provide emergency resource links

\# Maintain AI companionship until human takeover

pass

#### **4\. Multilingual & Offline Support**

// Progressive Web App (PWA) Implementation

// Service Worker for offline caching

self.addEventListener('install', (event) => {

event.waitUntil(

caches.open('crisis-chatbot-v1').then((cache) => {

return cache.addAll(\[

'/offline-responses.json',

'/grounding-exercises.json',

'/emergency-contacts.json',

'/core-translations.json' // Offline translations of key phrases

\]);

})

);

});

// Provide basic support when offline

self.addEventListener('fetch', (event) => {

event.respondWith(

caches.match(event.request).then((response) => {

return response || fetch(event.request);

})

);

});

#### **5\. Privacy & Security Architecture**

class PrivacyFirstArchitecture:

def \__init_\_(self):

self.encryption = EndToEndEncryption()

self.anonymization = DataAnonymizer()

self.audit_log = AuditLogger()

def store_conversation(self, user_id, message):

\# End-to-end encryption

encrypted_message = self.encryption.encrypt(message)

\# Anonymized storage

anonymous_id = self.anonymization.hash_user_id(user_id)

\# Audit log (without content)

self.audit_log.log_access(anonymous_id, timestamp)

return self.database.store(anonymous_id, encrypted_message)

def handle_deletion_request(self, user_id):

\# GDPR compliance: users can delete all data

anonymous_id = self.anonymization.hash_user_id(user_id)

self.database.delete_all(anonymous_id)

self.audit_log.log_deletion(anonymous_id)

#### **6\. Volunteer Coordination Mode**

class VolunteerCoordinationMode:

def \__init_\_(self):

self.translator = RealTimeTranslator()

self.task_manager = TaskCoordinator()

def facilitate_communication(self, message, source_lang, target_lang):

\# Real-time translation

translated = self.translator.translate(

message,

source_lang,

target_lang,

context="humanitarian_aid"

)

\# Extract critical information

urgent_tasks = self.extract_urgent_tasks(translated)

\# Centralized notifications

self.task_manager.broadcast_update(urgent_tasks)

return translated

## **III. Implementation Roadmap**

### **Phase 1: Foundation MVP (2-3 months)**

- Build basic conversation system (single language, adult mode)
- Implement core emotional support features
- Establish privacy and encryption infrastructure
- Small-scale user testing (20-50 people)

### **Phase 2: Feature Expansion (3-4 months)**

- Add multilingual support (Ukrainian, Arabic)
- Develop child and teen modes
- Integrate voice input/output
- Implement diary and emotional tracking features
- Establish human oversight and escalation system

### **Phase 3: Volunteer Tools (2-3 months)**

- Develop volunteer coordination mode
- Real-time translation and task management
- Multi-user collaboration features

### **Phase 4: Optimization & Scaling (Ongoing)**

- Enhance offline functionality
- Performance optimization and scalability
- Continuous cultural adaptation and user feedback
- Long-term mental health tracking

## **IV. Critical Success Factors**

✅ **User Co-Creation**: Continuously collaborate with real users throughout development ✅ **Ethics First**: Every feature must pass ethical and safety review ✅ **Cultural Experts**: Hire local cultural advisors and mental health professionals ✅ **Gradual Rollout**: Start small, iterate based on feedback ✅ **Transparency**: Clearly communicate AI capabilities and limitations to users ✅ **Human-AI Collaboration**: AI doesn't replace human support-it enhances and bridges

This system requires close collaboration from an interdisciplinary team (technology, psychology, humanitarian aid, localization), always prioritizing user safety, privacy, and wellbeing above all else.

## **V. Technology Stack Recommendations**

### **AI/ML Layer**

- **LLM**: Claude (Anthropic) or GPT-4 (OpenAI) with custom fine-tuning
- **Emotion Detection**: Hugging Face Transformers + custom models
- **Translation**: Google Cloud Translation API or DeepL
- **Speech**: Whisper (OpenAI) for STT, Azure Neural TTS

### **Backend**

- **Framework**: Python (FastAPI) or Node.js (Express)
- **Database**: PostgreSQL (encrypted) + Redis (caching)
- **Security**: Let's Encrypt SSL, bcrypt, JWT authentication

### **Frontend**

- **Framework**: React or Vue.js
- **PWA**: Workbox for service workers
- **UI**: Tailwind CSS for accessibility and responsiveness

### **Infrastructure**

- **Cloud**: AWS or Azure (HIPAA/GDPR compliant regions)
- **CDN**: Cloudflare for global access
- **Monitoring**: Sentry for error tracking, Prometheus for metrics

### **Compliance Tools**

- **Encryption**: Age encryption library, Vault by HashiCorp
- **Audit**: ELK Stack (Elasticsearch, Logstash, Kibana)
- **Testing**: Pytest, Jest, Cypress for E2E testing

This comprehensive plan provides a roadmap for building a trauma-informed, culturally sensitive, and technically robust crisis support chatbot that prioritizes human dignity and safety.

Psychological Support

- Different prompts for different age groups
  - For children - some contents should not be discussed, would require multimodal assistance for expressing feelings (due to limited vocabulary)
  - For elderly - would need more patience, they probably like to share more
  - For teens - avoid using the word 'why'
- Different prompts for different culture groups
  - For Middle-Eastern regions
  - For Eastern European regions

Features

&lt;name&gt; App Features:

Main themes / needs

- Mental Support
- The functions need to align with their cultural background
- We need to build trust & sense of security with the users
- Users need a way to let out their emotions privately
- Need a way to reach emergency services when necessary
- Unstable internet
- Entertainment that promotes positivity

Functions (corresponding to the index of themes / needs)

- Chatbot / Voice Agent
- Select different modes for different regions
- Login system / freedom of choosing between online / offline functions
  - Privacy policy: all information stored locally
- Private diary (Strictly offline)
- Emergency SOS function
  - Auto-redirects to phone call
- Offline mode with all basic functions working

Offline / Online Mode

- Introduction
  - Offline → fully functional without internet, secure
  - Online → privacy is ensured, more functions, can access online information and other's posts
- Offline Mode
  - Offline chatbot / voice agent
  - Emergency SOS function (auto-redirects to phone call)
  - Offline therapeutic music / mini-games
  - Daily message of encouragement
  - Personal Diary
- Online Mode
  - Online chatbot / voice agent
  - Online support community w/ volunteers helping out with reviewing posts and engaging supportively in conversations

Chatbot / Voice Agent

- Offline (Baseline)
  - Psychological support
- Online
  - Might be more interactive, has searching functions

UI Description

Initial / Register:

- Welcome message
- select your region, ethnicity, religion, gender, age, preferred language, current state(can be updated anytime)
- No identity info verification required
  - Purpose: increase sense of security with personal credentials

Login:

- Welcome message
- Users can choose to stay logged in, or re-login every time they come back
  - Could show, Hi, "their name"
- Preferred nickname
- Choose preferred online/offline mode
- User terms & cookies & information, security concerns
- Tutorials, user manuals

Main Interface

- Daily encouragement sentence
- Navigation
- Chatbot
- Explore
  - - My Diary
      - Therapy space
        - Therapeutic music / mini-games
        - [Breathing exercises](https://www.breathwrk.com/#:~:text=Breath%20Hold%20%26%20Exhales%20%2B%20unlimited%20customizations&text=The%20app%20saved%20and%20changed,myself%20and%20my%20mental%20health.&text=So%20easy%20to%20use%20and%20helps%20me%20to%20feel%20calm%20and%20relaxed.&text=I%20have%20a%20chaotic%20schedule,and%20is%20so%20worth%20it.)
      - Mood meter
        - <https://www.vantagefit.io/product-updates/mood-meters/>
      - Self-test (ptsd, depression, …)
      - Emergency SOS (medical hotline, mental health hotline, etc)
- Settings
  - - Profile
      - Language
      - Issue report
  - Help

Chatbot

- Online/offline selector
- Language selector
- Usual normal chatbot conversation UI + option for Voice message input/output

Chatbot (emergency triggered)

- Message asking if want to call emergency sos -> two buttons below for accept / reject options

My Diary

\- After entering diary space: enter password

o => need no.3 (sense of security)

\- After password

o write new diary (with drawing functions)

o view saved diaries

o for each diary, include select emoji and color

Online forum (optional function)

\- Browsing: Discover / Followed

\- Write new post (can be anonymous)

\- Comment on others' posts

\- Instead of 'like button', put a 'hug' or 'support' button

Final Design

Prompt

Name

Got it - thanks for laying out the full vision. The name should capture **safety, trust, emotional support, and resilience**, while also being culturally adaptable and not intimidating (since "disaster psycho bot" sounds a bit harsh for users seeking comfort). Here are some strong naming directions:

### **🌱 Calming & Supportive**

- **ArtificialHaven** - a safe place in times of crisis
- **SoulSpace** - private, secure, and personal
- **InnerLight** - guiding users through dark times
- **Serenity** - calmness and peace, even in disaster

### **🛡️ Safety & Trust**

- **SafeMind** - emphasizes both mental health and security
- **Guardian Voice** - protective and supportive chatbot/agent
- **TrustCircle** - community and privacy combined
- **Anchor** - stability during emotional storms

### **🌍 Resilience & Recovery**

- **Resilio** - resilience + support
- **RiseAgain** - hope and recovery after hardship
- **MindHaven** - mental refuge, always accessible
- **Phoenix** - rebirth and strength after disaster

### **🎶 Positivity & Uplift**

- **BrightPath** - guiding toward positivity
- **EchoCare** - voice agent that listens and responds with care
- **JoyNest** - a safe nest for comfort and encouragement
- **Lumos** - light in the darkness (short, memorable, universal)

💡 If you want something **short, global, and easy to remember**, I'd recommend **Haven**, **Lumos**, or **Resilio**. If you want something **warm and community-oriented**, then **TrustCircle** or **SoulSpace** would be great fits.

Would you like me to **narrow this down to one final name** with a tagline (like how it would appear in an app store), or would you prefer a **set of culturally adaptable names** that can be localized for different regions?

Usability

Usability Testing Survey

- Age
- Experience with war (?)
- Experience with Generative AI

Likert (1-5)

- I think that I would like to use this system frequently.
- I thought the system was easy to use.
- I thought there was too much inconsistency in this system.
- I would imagine that most people would learn to use this system very quickly.
- I felt very confident using the system.
- I felt secure using the system.
- Any comments or suggestions regarding the system?

  Paste or append the full COMP4461 Project 2 notes here (the long text you provided).

</details>
<!-- markdownlint-enable MD033 -->