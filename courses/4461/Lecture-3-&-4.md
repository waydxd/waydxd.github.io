### Lesson: Understanding Humans in Human-Computer Interaction (HCI)

Hello! Based on the provided PDF lecture notes by Xiaojuan Ma (from COMP4461, dated around 2025), I'll teach you the key concepts in a structured, engaging way. This is a two-part lecture on human capabilities and their implications for designing effective HCI systems. I'll break it down into sections mirroring the PDF's structure, explaining concepts clearly, highlighting examples, and noting HCI implications. I'll use bullet points for clarity, tables for comparisons, and bold key terms. At the end of major sections, I'll include recap questions to reinforce learning (inspired by the PDF's interactive style).

The overall theme: Humans are complex—our senses, memory, cognition, and emotions shape how we interact with technology. Good HCI design leverages human strengths while mitigating weaknesses. The lecture references critical technologies like Human-Machine Interfaces (from a 2022 White House list) and emphasizes that understanding humans leads to better usability.

---

#### Introduction: Why Understand Humans in HCI?
- **The Human-Computer-Interaction Triad**: Humans bring perceptions, imagination, knowledge, and comprehension. Computers provide tools. Interaction involves use, context, social factors, adaptation, design processes, evaluation, and implementation.
  - Example: A diagram shows "Belief" (human side) vs. "Truth" (computer side), with interaction as a curtain reveal—design must bridge this gap.
- **User Experience Models**: 
  - **Implementation Model**: How the system works internally (e.g., gears and code)—worst for users.
  - **Representation Model**: How it's presented (e.g., icons like a trash can for delete)—better.
  - **Mental Model**: User's internal idea of how it works—best when it matches reality.
  - Progression: From perception (senses/awareness) to imagination (ideas/concepts) to knowledge (experience/reasoning) to comprehension (language/communication).
- **Cognitive Science Word Cloud**: Key fields include perception, memory, cognition, neuroscience, language, interaction, etc. HCI draws from these to make tech intuitive.
- **Statistic Insight**: 80% of what people remember is what they **see/do**, 20% what they **read**, 10% what they **hear**—visual/interactive design matters!

**Quick Question**: Based on the intro, why might a confusing app icon lead to poor user experience? (Hint: Mental model mismatch.)

---

#### Human Capabilities Overview
Humans process information in three main ways:
- **Received/Responded via Senses**: Vision, hearing, touch, smell, taste, motion/movement.
- **Stored in Memory**: Short-term (working) and long-term.
- **Processed/Applied in Cognition**: Attention, learning, problem-solving, language, etc.—all influenced by emotion.

**Good Human Traits for HCI**: Multiple senses, infinite long-term memory, high learning potential, strong pattern recognition, rich emotions.
**Bad Traits**: Limited short-term memory, error-prone processing, slow cognition, emotional biases.

The lecture focuses on leveraging these for better interfaces.

---

#### Part I: Sensory Systems (The Five Senses)
We receive info through senses, but capabilities vary (e.g., deficiencies like color blindness affect 8% of males). HCI must accommodate this.

##### I.I Vision System
Vision is dominant (80% of sensory input). Key capabilities:
- **Sensitivity**: Detects luminance from 10^-6 to 10^7 mL (very dark to bright).
- **Acuity**: Detects angles/focus for alignment; tracks movement.
- **Adaptation**: Adjusts to distance/lighting, but causes fatigue.
- **Deficiency**: Age-related decline, short/far-sightedness, color blindness (0.5% females).

**Visual Information Processing** (Ware, 2019):
- Stage 1: Features (e.g., edges, colors).
- Stage 2: Patterns (grouping).
- Stage 3: Gist (overall meaning, using visual/verbal memory and egocentric maps).

**Gestalt Principles**: Mental shortcuts for perceiving wholes from parts ("Gestalt" means "shape/form" in German). Humans group elements to simplify complexity. Designers use these for intuitive layouts.

| Principle       | Description | Example in HCI | 
|-----------------|-------------|----------------|
| **Closure**    | Brain fills gaps to see complete shapes. | Dotted outlines perceived as full circles (e.g., loading icons). |
| **Similarity** | Similar items (color/shape) grouped. | Menu items with same color seen as related. |
| **Continuity** | Elements aligned in lines/curves seen as connected. | Flowcharts or navigation paths. |
| **Common Fate** | Items moving together grouped. | Animated UI elements syncing. |
| **Proximity**  | Close items grouped. | Buttons in a toolbar. |
| **Figure/Ground** | Foreground vs. background distinction. | Pop-up modals standing out. |
| **Symmetry/Common Region** | Symmetric or enclosed items grouped. | Cards in a dashboard. |

Additional rules: Emergence (simple first), Reification (whole from incomplete), Multistability (dominant view), Invariance (recognize despite changes).

**Color Vision**:
- **Photoreceptors**: Cones (color) in fovea; rods (light changes) in periphery.
- Sensitivity peaks at green-yellow (0.4-0.7 micrometers wavelength).
- Affected by: Surroundings, stress/fatigue, culture, eyewear.
- **Psychology**: Colors evoke emotions (e.g., red = danger/excitement). Blue light disrupts sleep; mood lighting calms (e.g., airlines).
- **Sensitivity/Deficiency**: Just Noticeable Difference (JND) for colors; 108 million web users color-blind—simulate in design.
- Example: "White + Gold or Blue + Black" dress illusion shows contextual perception.

**HCI Implications**:
- Ensure legibility/accessibility (e.g., high contrast).
- Use pop-out features (color/shape for alerts).
- Processing fluency (easy-to-read = feels closer/trustworthy).

**Teaching Example**: In a UI, apply proximity by grouping related buttons—users "see" them as one unit without effort.

##### I.II Hearing
Best-case capabilities:
- Pitch (20-20,000 Hz), loudness (30-100 dB), location (5° separation), timbre (sound type).
- **Cocktail Party Effect**: Focus on one voice amid noise (selection/detection).

Examples: Wake-word detection (e.g., "Hey Siri"); 3D audio books for immersion.

**HCI Implications**:
- Use speech/music/environmental/synthesized sounds wisely.
- Leverage location/timbre for alerts (e.g., spatial audio in VR).
- Balance volume to avoid discomfort.

##### I.III Touch
Receptors for:
- Pressure (normal), intense pressure (pain), temperature.

Body parts vary: Fingertips highly sensitive; back less so.

Examples: Rising keyboards for tactile feedback; AIREAL (free-air haptics for virtual touch).

**HCI Implications**:
- Input (gestures), output (vibrations).
- "Fool" senses (e.g., illusions for richer feedback).

##### I.IV Smell and Taste
Less common in HCI, but emerging.
- Scenarios: Feasibility, social appropriateness.
- As alternatives (e.g., augment vision for blind users).
- Natural/synthesized stimuli; ensure safety.

Example: Virtual cocktail system syncing electric taste with visuals.

##### I.V Motor (Movement)
Capabilities: Range, reach, speed, strength, dexterity, accuracy.
- Principles: Need feedback; minimize eye-hand shifts.
- Errors: Wrong button (resolution), double-click confusion (similarity).

Example: YouTube moved "Skip Ad" countdown to avoid accidental clicks.

**Fitts’s Law**: Time to target = a + b * log2 (distance/width + 1). Bigger/closer targets = faster.

Examples: Mobile thumb zones (easy reach); keypad layouts (phone vs. calculator differ for habit).

**HCI Implications**: Design for natural movements; optimize layouts.

**Recap Question**: Why is Fitts’s Law useful for button placement? What Gestalt principle explains grouping icons in an app?

---

#### Part II: Memory, Cognition, and Emotion

##### II. Memory Systems
Types:
- Perceptual buffers (brief impressions).
- Short-term (conscious, 4-5 chunks; declines with age).
- Long-term: Episodic (events), semantic (facts/skills).

**Models/Theories**:
- Spread-Activation: Concepts link like networks (e.g., "bread" activates "butter").
- Priming: Prior exposure influences later tasks (e.g., word completion biased by context).
- Serial Position Effect (Ebbinghaus): Better recall for first (primacy) and last (recency) items.
- Cliffhanger Effect: Unfinished tasks remembered better.
- Self-Reference: Personal relevance aids memory.
- Spatial Memory: Location/orientation/navigation (e.g., mental maps).

**HCI Implications**: Use context/practice for recall; familiarity enhances learnability (e.g., consistent icons).

##### III. Cognitive Systems
Processing info: Attention, learning, problem-solving, language.

**III.I Attention**:
- Span: Limited; focus shifts quickly.
- Nielsen’s Limits: 0.1s (instant), 1s (seamless), 10s (attention lost).
- Pareto Principle (80/20): 80% value from 20% features—prioritize.
- Scan Paths: Eyes follow F-pattern on pages.
- Blindness: Attentional (miss obvious, e.g., gorilla video); banner (ignore ads); inhibition of return (avoid revisited spots).

**HCI Implications**: Heatmaps for optimization; avoid overload.

**III.II Learning**:
- **Types of Learning**:
    - **Procedural**: Skill-based (e.g., typing); uses motor memory. HCI: Swiping gestures, VR surgery sims.
    - **Declarative**: Fact-based (e.g., app icons); uses recall. HCI: Duolingo visuals + text.
- **Facilitators**:
    - **Analogy**: Links new to old (e.g., "trash bin" = delete).
    - **Structure**: Chunks info (e.g., nested menus).
    - **Incremental**: Small steps (e.g., Rosetta Stone levels).
    - **Repetition**: Reinforces (e.g., Anki flashcards).
- **Hindrances**:
    - **Prior Knowledge**: Clashes (e.g., Mac to Windows).
    - **Beliefs**: Biases (e.g., distrust in AI).
- **Baby Duck Syndrome**: Users stick to first-learned system (e.g., iPhone vs. Android backlash). Counter with gradual UI updates.
- **Tech Impact**:
    - **General**: Shapes habits (e.g., Alexa confusion in kids).
    - **Passive Haptics**: Builds muscle memory (e.g., vibrating glove for piano).
**HCI Implications**: Tutorials with analogies; avoid conflicting habits.

**III.III Problem-Solving (Reasoning)**:
- Deductive (if-then), Inductive (generalize), Abductive (infer cause).
- Hick-Hyman’s Law: More choices = slower decisions.
- Default Effect: Defaults chosen more.

**HCI Implications**: Heuristics over algorithms; block bad paths; use cues for legacy bias.

**III.IV Language**:
- Natural: Structured words for communication.
- Characteristics: Clear (consistent mapping), Quick (abbreviations), Expressive (engage, e.g., slang), Processible (matching speaker/listener rates).
- Challenges: Ambiguity (e.g., "Hamlet" interpretations); slang evolution.

**HCI Implications**: LLMs bring opportunities (natural chat) but challenges (bias, speed).

##### IV. Emotion
Theories:
- Categorical: Basic emotions (Ekman: joy, sadness, etc.; Plutchik wheel).
- Dimensional: Valence (positive/negative) + arousal (high/low).
- Appraisal: Evaluate events for emotional response.

Elicitation (triggers), Response (actions/feelings), Moderation (affects perception/memory).

Other Theories: James-Lange (body first), Cannon-Bard (brain), Schachter-Singer (cognition + physiology).

Emotional Intelligence: Perceive, use, understand, manage emotions.

**HCI Implications**: Design for positive affect (e.g., smiles reduce stress); emotion-aware interfaces.

**Recap Question**: How does priming affect UI design? Why might too many menu options frustrate users (Hick-Hyman)?

---

#### Overall Recap: Human Capabilities
**Good**: Multi-sensory, infinite memory, adaptable learning, pattern recognition, emotions.
**Bad**: Limited resources, biases, errors, slowness, emotional overload.

HCI Goal: Design around these—e.g., intuitive, accessible, engaging.

References include books on visualization/perception and papers on tactile/smell tech.

If you'd like deeper dives (e.g., on a specific principle, examples, or videos from the PDF links), quizzes, or related real-world apps, let me know! What part interests you most?