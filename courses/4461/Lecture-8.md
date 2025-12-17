---
layout: default
title: "Lecture 8: Human-Robot Interaction (HRI)"
---

### Overview of the PDF: HCI-12 - Human-Robot Interaction (HRI)
This PDF is a lecture from COMP4461 (Human-Computer Interaction) taught by Xiaojuan Ma at HKUST in 2025. It explores HRI, building on HCI principles like those from previous lectures (e.g., multimodal interaction). The focus is on how humans and robots interact, from types of robots to design considerations for autonomy, social skills, and intelligence. It starts with historical references (Asimov's laws) and current (2025) examples via videos, then dives into technical and ethical aspects. The lecture emphasizes user-centered design in robotics, linking to real-world applications like collaboration and education. It's richly illustrated with examples, diagrams, and links to demos.

I'll summarize and teach this step-by-step as a lesson, explaining concepts, providing examples from the slides, and highlighting tips. At the end, a recap table for quick reference.

#### 1. Introduction: Robots and Their Evolution
The lecture opens with foundational ideas and modern context to set the stage for HRI.

- **Asimov's Three Laws of Robotics (1941)**: From the novel *I, Robot*, these are ethical guidelines:
  - A robot may not injure a human or allow harm through inaction.
  - A robot must obey human orders unless it conflicts with the first law.
  - A robot must protect its existence unless it conflicts with the first or second law.
  - **Teaching Tip**: These laws highlight early concerns about safety and ethics in HRI, which remain relevant today.

- **Robots in 2025**: Examples of advanced robots, with video links:
  - Boston Dynamics' Spot (dog-like robot in crowds).
  - Dancing robots in performances (e.g., CCTV show).
  - Chinese video on humanoid robots.
  - Question posed: "Are we ready to co-live with robots (and AI)?" with a demo of a smiling robot.
  - **Examples**: Movies like *Robot Dreams* and *The Wild Robot* illustrate cultural perceptions.

- **Teaching Tip**: HRI isn't just sci-fi; by 2025, robots are integrated into daily life (e.g., assistants, delivery drones). Consider how multimodal inputs (from previous lecture) enable natural interactions.

#### 2. Types of Robots
Robots are classified by form and function, influencing how humans interact with them.

- **Virtual Robots (Agents or Avatars)**:
  - Spiders (e.g., Googlebot for web crawling).
  - Chatbots (e.g., WeChat bots, removed for privacy issues).
  - Intelligent Personal Assistants (e.g., Siri).
  - Example: Movie *Her* shows emotional bonds with virtual AI.

- **Physical Robots**:
  - **By Appearance**: Machine (e.g., NASA's Mars Rover), vehicle (e.g., DJI Drone), animal (e.g., Google Dog, Zoomer Dino), humanoid (e.g., Henn-na HRP-4C, Nao).
  - **By Function**: Industrial (e.g., Hyundai robots at KIA), service (e.g., daVinci surgical robot, Amazon PrimeAir drone, rescue robots), social/personal (e.g., Aldebaran's Pepper, Jibo).
  
- **Teaching Tip**: Choose robot type based on context—humanoids for social tasks (empathy-building), machines for precision (e.g., surgery). Design for user familiarity to reduce the "uncanny valley" effect (more on this later).

#### 3. Humans' View of Robots: Tool or Actor?
Humans anthropomorphize robots, affecting interaction design.

- **As Tools**: Functional aids (e.g., exoskeletons for hiking, ATMs with virtual tellers).
- **As Actors**: Social entities (e.g., CMU Roboceptionist blending info and personality; "No Fair!" robot demo showing child-like reactions).
- **Level of Autonomy**: Spectrum from direct control (e.g., minimal-invasive surgery) to dynamic autonomy (e.g., care support robots in uncontrolled environments).
  - Diagram: Teleoperation → Mediated/Supervisory/Collaborative control → Peer-to-peer collaboration.

- **Teaching Tip**: View impacts trust—tools for efficiency, actors for engagement. In HRI, balance autonomy to avoid over-reliance or fear (e.g., robots disobeying unsafe commands).

#### 4. Interaction Design in HRI
Focuses on low- and high-level perception, motion, and intention for seamless HRI.

- **Perception Pipeline**: Sensing → Pre-processing → Modeling → Interpretation.
  - Targets: Self, others, environment.
  - Challenges: Data/features must be dense, robust to occlusions/view changes, avoid false positives.

- **Key Elements**:
  - **Appearance**: E.g., Baxter's friendly face for collaboration.
  - **Uncanny Valley**: Mori's theory—human-like robots can evoke unease if not perfect (e.g., zombies vs. healthy humans).
  - **Motion**: E.g., Shadow Robot Hand grasping/hand-over; Boston Dynamics' robots navigating.
  - **Intention**: Inferring human goals (e.g., robot arm choosing drinks based on preference).

- **Teaching Tip**: Use perception for intuitive interactions (e.g., Sony AIBO recognizing owners). Test for robustness—weak links in the pipeline can fail the whole system.

#### 5. Social Interaction Design
Extends multimodal concepts to social cues for empathetic HRI.

- **Facial Expression**: Based on Ekman's Facial Action Coding System (action units for emotions like surprise, anger).
  - Examples: MIT Nexi/SEER mirroring emotions at SIGGRAPH.

- **Bodily Expression**: Gestures, posture, head movement, touch, space.
  - Quality/quantity matter (e.g., Disney's "Illusion of Life" principles for animation).
  - Examples: Keepon expressing via simple movements; autonomous vehicles reading pedestrian body language.

- **Gaze**: Establishes attention, follows gestures, emphasizes info (theme vs. rheme).
  - Examples: Shifts, aversion, coordination, adaptivity in robots.

- **Proxemics**: Personal space zones (intimate 0-0.46m, personal 0.46-1.2m, social 1.2-3.7m, public 3.7m+).
  - Characteristics: Egg-shaped, influenced by relationships/gender/culture.
  - Implications: Robots respect space to avoid discomfort (e.g., Ameca reacting to invasions; Roomba navigating around people).

- **Teaching Tip**: Social design builds trust—e.g., gaze for engagement, proxemics for safety. Cultural sensitivity is key (e.g., closer spaces in warm cultures like Italy).

#### 6. Intelligence Design
Covers cognitive and emotional aspects for "smart" robots.

- **What Makes a Robot Intelligent?**:
  - **Learnability**: Gather knowledge (e.g., AlphaGo via neural networks).
  - **Curiosity**: Find questions (e.g., manga example of exploratory robots).
  - **Empathy**: Build self/other awareness (Theory of Mind: explain/predict actions).

- **Learning Methods**:
  - Unsupervised, Supervised, Reinforcement (RL: agent-environment loop with rewards).
  - Learning from Demonstration (LfD/Imitation): Humans teach via actions (e.g., assembling furniture).
  - Transfer Learning: Apply knowledge from related domains.
  - Collective Intelligence: Internet of Robots sharing models/languages.

- **Challenges**: AI learns correlations, not always causality—noise/biases/hacks (e.g., Tay bot turning Nazi-like).

- **Teaching Tip**: RL suits dynamic environments (exploitation vs. exploration). For HRI, empathy (ToM) enables better collaboration—e.g., robots understanding human emotions.

#### 7. Discussion and Ethical Considerations
Addresses broader implications.

- **HRI in Use**: Tasks like conversation, collaboration; mechanical/natural communication.
- **Other Issues**: Safety, privacy, policy, ethics.
- **Three Laws Revisited**: Robots may disobey for safety (e.g., refusing unsafe walks).

- **Threat to Humanity?**: Debates on AI risks, with movie clips.

- **Teaching Tip**: Ethics is crucial—design robots with safeguards. Discuss: How to balance autonomy and human control?

#### Recap and Key Takeaways
HRI applies HCI to robots, emphasizing user empathy, multimodal design, and intelligence for safe, natural interactions. It's iterative, like design thinking from earlier lectures.

| Section                  | Key Concepts                                                                 | Examples/Tools                                                                 | Advantages/Limitations |
|--------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------|
| **Types & Views**       | Virtual/physical; tool/actor; autonomy levels                                | Siri, Pepper, Baxter; autonomy spectrum                                        | Enhances tasks but risks unease (uncanny valley) |
| **Interaction Design**  | Perception pipeline, appearance, motion, intention                           | AIBO sensing, Shadow Hand grasping, Anca Dragan's intent inference             | Intuitive but data challenges (occlusions, biases) |
| **Social Design**       | Facial/bodily expression, gaze, proxemics                                    | Nexi emotions, Keepon gestures, Ameca space reaction                           | Builds trust; cultural/gender variations |
| **Intelligence Design** | Learnability, curiosity, empathy; RL, LfD, transfer                          | AlphaGo, Moley kitchen, collective robot nets                                  | Adaptive but prone to hacks/biases |
| **Discussion/Ethics**   | Safety, privacy, Three Laws                                                  | Disobeying robots, AI threats in movies                                        | Promotes co-living; needs policies |

- **Overall Lesson**: HRI makes robots partners, not just tools. Apply empathy from design ideate lecture—immerse in user needs for ethical, effective robots.
- **Pro Tips**: Watch linked videos for demos (e.g., Sophia's social skills). In projects, prototype with low autonomy first, scale to social intelligence.

If you'd like deeper dives (e.g., on a video summary or relating to prior PDFs), ask!