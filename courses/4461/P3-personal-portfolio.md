
# 🌊 Project 3: Social Extended Reality (XR) for Local Community

*Name of groupmates are anoymized*

## Part I: Project Summary & Design Process Analysis

Project Title: EverPresence: Reimagining Long-Distance Relationships (LDRs) for University Students with Social XR

Final Solution: An Asynchronous Virtual Shared Home and Companion Pet for long-distance partners, focusing on persistence and subtle cues across time zones.

### 1. Group Activities and Deliverables Overview

Our group followed a rigorous design process, resulting in key insights, three tested concepts, and a final functional prototype.

- **Needfinding (Empathize):** We identified the target community as university students in Long-Distance Relationships (LDRs). We conducted 7 semi-structured interviews to understand how current tools fail to recreate a sense of "shared context." The primary finding was the desire for immersive, but low-effort, ways to feel co-present across time zones.
- **Ideation and Storyboarding:** We generated three core concepts—the Haptic Suit, the VR Reconciliation Space, and the VR Shared Space/Sandbox Game (which became our final solution). As the storyboard drawer, I used AI tools and iterative prompting to create the visuals for these concepts, particularly the VR Game narrative.
- **Storyboard Visualization:** The core narrative for the chosen VR Game/Shared Space concept was visualized through a sequence of panels showing how presence is maintained across time zones.
- **Evaluation (Speed Dating):** We tested these concepts and gathered feedback from three external participants, which confirmed that the Shared Space concept was the most feasible and desirable, provided it prioritized simplicity and persistent engagement.
- **Final Prototype (EverPresence):** The final prototype, despite the reliance on the unstable Spatial SDK, demonstrated the persistent shared virtual space, the co-owned digital pet, and the key asynchronous VR-to-AR memo system.
- **Final Prototype Visualization:** The final functional prototype demonstrated the persistent shared virtual space and the interaction with the companion pet.

### 2. Ideation and Final Solution

We generated several ideas, including Haptic Suits, a VR Reconciliation Space, and the VR Shared Space/Sandbox Game.

<img src="/courses/4461/4461 P3 Storyboard: VR Game.png" alt="Interview screenshot" style="display:block;margin:0 auto;max-width:640px;width:100%;height:auto;" />


- **My Thinking & Advocacy:** I strongly advocated for the **VR Shared Space / Sandbox Game** idea because I believed the primary success factor for any XR solution in a relationship is sustained engagement. If the environment is *fun* (like a sandbox game where you can co-create and explore), partners will be motivated to use it consistently. The final design, which evolved into the "Asynchronous Virtual Shared Home," retained this crucial element of a persistent, co-owned, and customizable space, aligning closely with my initial push for a playful, engaging platform.

### 3. Final Reflection and Design Principles (Take-Home Messages)

The project reinforced two key design principles:

1. **Augmenting Routine, Not Replacing Reality:** High-fidelity XR (like Haptics) was rejected because it was too high-cost and too difficult to implement convincingly. The adopted solution succeeds by augmenting low-effort, high-impact routines (like leaving a note or tending a virtual pet), making it easier for partners to maintain presence without requiring a full-scale, dedicated virtual date.
2. **The Priority of Asynchronicity:** For LDRs facing severe time zone differences, the most practical features are those that facilitate presence without requiring synchronous interaction (e.g., the VR->AR Memo system).

### 4. Future Work and Prototype Expansion

The foremost priority for future development is addressing the technical debt and unreliability encountered late in the project:

- **Switching to a Robust Tech Stack:** The most critical lesson learned during the final push was the failure of the chosen development environment. The **Spatial SDK server went down unexpectedly right before the submission deadline**, causing significant stress and jeopardizing the final demonstration. Compounding the problem, the course provided very few tutorials on using the Spatial SDK and Unity—particularly an older, unsupported version of Unity where documentation is scarce—which made setup and debugging considerably harder for our group. Future work must begin by migrating the entire project to a **more robust, stable, and self-hosted multiplayer framework** (e.g., Photon, Mirror, or a custom backend) to ensure the continuity and reliability of the social, co-present experience, thereby eliminating external single points of failure.

Beyond the tech stack, future development would focus on enhancing the depth and fidelity of the shared experience:

- **Gamified Co-Creation:** Implementing a simple **"Quest" or "Goal" system** around the shared virtual pet (e.g., daily care tasks) and the shared home (e.g., decorating challenges) to encourage sustained, cooperative interaction.
- **Photo Wall and Memory Integration:** A dedicated feature for uploading and sharing real-world photos and videos within the virtual home, turning the space into a true digital scrapbook of their relationship.
- **Calendar and Time Zone Synchronization:** Integrating the memo feature with real-world calendar apps to allow partners to leave time-zone-aware cues, such as "Wake up soon!" memos that appear precisely when the partner's alarm is due to ring.

## Part II: Personal Diary, Process, and Critique

### My Project Roles and Deliverables

- **Interviewer:** Conducted the interview with **Interviewee Alex** and contributed to the synthesis of the seven interview results.
- **Storyboarding:** Was one of the primary storyboard drawers, specifically creating the visual narrative for the **VR Game** concept during the Ideation stage.
- **Presentation Drafting:** Wrote the initial presentation draft, structuring the flow according to the P3.2 requirements (Needfinding, POV, Ideation, Final Proposal). Note that the three POVs were authored by the **POV Lead** (Team Member C).

### Reflection on AI Tool Usage

I utilized AI assistance for all aspects of my work where applicable. This included:

- **Content Structuring & Wording:** Using AI to help organize and structure raw interview notes into coherent findings, and refining the clarity, tone, and academic phrasing of research summaries, POV construction (based on the content provided by the **POV Lead**), and this final reflection report.
- **Idea Generation & Storyboarding (Image Generation):** AI tools were used to generate the visual panels for the storyboards (specifically the **VR Game** concept). This was not a simple one-off process but involved a detailed **trial-and-error process** using iterative prompts to ensure the images accurately depicted the user scenario, emotional tone, and specific XR interactions required for the storyboards, making the ideation visuals clearer and more compelling for the speed dating evaluation.

The AI acted as an important assistant for rapid documentation, organizational tasks, and creating high-quality visual assets, allowing me to focus my efforts on the qualitative research and ideation aspects of the project.

### Critical Reflection on Teamwork (Stress on Own Thinking)

This project was severely undermined by poor team collaboration and a near-total breakdown in communication between team members. My own contributions were impacted by an inability to align expectations and a lack of trust within the group.

- **The Collaboration Failure & Prototyping Conflict:** A formal division of labor was non-existent. My previous experience being criticized for my Project 2 prototyping work made me unwilling to take on the Unity development for Project 3. The developers (**Developer A** and **Developer B**) isolated themselves and adopted a flawed strategy: they insisted on building **extensive, fully functional code** to demonstrate features, refusing to use proven, low-fidelity techniques like **Wizard of Oz** or stable, accessible platforms like **Roblox or Minecraft**, which I was familiar with and suggested as alternatives. The project deliverables primarily required a presentation and a video, meaning effort should have been focused on a compelling demonstration rather than deep code implementation, especially given the lack of VR goggles and the instability of the chosen SDK. This insistence on technical depth over effective presentation resulted in tremendous effort being spent on features that were ultimately **not clearly showcased** in the final video.
- **The Root of Criticism:** The sudden failure of the Spatial SDK server before the deadline created immense pressure and frustration for the developers (**Developer A** and **Developer B**). This technical crisis was likely the **root cause** of their emotional outburst and subsequent behavior. While I was always the most responsive (replying ASAP, attending meetings face-to-face, offering help for the video demo), I became an easy target for their misplaced criticism, instead of the teammates who were passive or disappeared. This experience solidified my realization: good technical knowledge is useless without basic professional collaboration skills. **I was tortured by this course for the whole semester.**
- **My Response and Efforts:** I attempted to bridge this gap, actively reaching out to the marginalized teammates who were continuously asking to help. While their subsequent contributions were criticized by the developers, my intent was to ensure that everyone had a role and felt included. Despite my efforts to request clear expectations for my own work (like the presentation draft), the lack of concrete replies made it impossible to meet their shifting standards, leading to criticism that felt unjust.
- **Lesson Learned:** The greatest lesson from this course, and this project in particular, is that **collaboration skills are as critical as technical or domain knowledge.** A team member with excellent technical knowledge who refuses to collaborate, trust their peers, or maintain communication can be more detrimental to a project's success and team morale than a less-skilled but engaged member. Future projects will necessitate prioritizing potential teammates based on communication reliability and a demonstrable belief in teamwork. This group project experience was a nightmare, and the primary takeaway is the importance of finding collaborators who reply and believe in shared effort, rather than those who centralize control and resort to sudden criticism.

### Peer Evaluation Reflection and Criteria (New Section)

The peer evaluation criteria for P3.2 focused on Human Centricity, Soundness of Topic, Practicality of XR, Effect on Augmenting Humans, and Demo Quality. Reflecting on these criteria:

- **Strengths (Soundness & Practicality):** Our core strength was the **Soundness of the Topic** and the **Practicality of XR** as a solution. By pivoting away from high-cost, high-effort ideas (like Haptics) toward a low-cost, mobile-first approach emphasizing asynchronous presence (VR->AR Memo), we ensured the solution was practical for the target demographic (budget-conscious students) and directly addressed their most significant need (time zone friction).
- **Weaknesses (Demo Quality):** Given the developers' refusal to use simpler prototyping methods (like Wizard of Oz or accessible platforms) and the major technical setback with the Spatial SDK, the **Demo Quality** was likely a point of concern. The prototype, while containing tremendous implemented features, failed to showcase those features effectively in the final demonstration video. This strategic misalignment—focusing on *implementation* instead of *demonstration*—prevented us from achieving the high level of polish expected.

<video controls preload="metadata" style="display:block;margin:0 auto;max-width:640px;width:100%;height:auto;">
  <source src="/courses/4461/91587861e924d262a9c319d94e8ea1c9.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
