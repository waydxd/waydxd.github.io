### Overview of the PDF: HCI-11 - Multimodal Interaction
This PDF is a set of lecture slides from COMP4461 (Human-Computer Interaction) taught by Xiaojuan Ma at HKUST in 2025. It focuses on **multimodal interaction** in HCI, emphasizing how humans interact with computers using multiple senses beyond just visual or textual input/output. The content is divided into three main parts: **Visual Interaction** (pages 1-55), **Sonification** (pages 56-80), and **Haptic Communication** (pages 81-110), with a brief on multimodal integration. It explores definitions, advantages, limitations, psychological foundations, design methods, and examples in HCI contexts like GUIs, wearables, and pervasive computing.

The lecture highlights how multimodal approaches address limitations of single-modality systems (e.g., when vision is blocked or overloaded). It includes references to research papers, YouTube videos for demos, and practical examples. I'll summarize and teach this step-by-step, like a lesson, explaining key concepts, providing examples, and noting tips. At the end, I'll recap with a table.

#### 1. Visual Interaction: Picture is Worth a Thousand Words (Pages 1-55)
This section introduces visual communication as a core HCI element, linking it to graphic, interaction, and communication design.

- **Definition and Types**:
  - Visual communication conveys ideas via forms that can be "read or looked upon" (e.g., signs, pictograms, logos, graphs, illustrations for graphical; media/art like photos, billboards for pictorial).
  - In HCI, it handles **status** (e.g., battery icon), **content/function** (e.g., app icons), **operation/navigation** (e.g., buttons, menus), and **notifications** (e.g., badges on apps).
  - Relation to HCI: Overlaps with graphic design (aesthetics), communication design (conveyance), and interaction design (interactivity). Examples: Tabs/pads/boards in mobile/car/TV interfaces.

- **When Words Fail (Linguistic Breakdowns)**:
  - Issues: Disability, degeneration, low literacy/language skills, cultural differences, abstract info.
  - Limitations of text: Time/space constraints, limited field of view, attention span, cognitive load.
  - Visuals help when words are "more than enough" (e.g., dashboards summarizing data).

- **Advantages**:
  - **Task Performance**: Improves efficiency/accuracy (e.g., icons for quick recognition).
  - **User Experience**: Enhances physical/psychological aspects (e.g., appealing UI reduces frustration).

- **Limitations**:
  - Ambiguity (e.g., "I do not like rock and roll" could be misinterpreted visually).
  - Non-imageable concepts (abstract ideas hard to depict).
  - Individual differences: Age, culture (e.g., red light means vacant taxi in HK but occupied in China; stock market "up" is red in Japan but green elsewhere).

- **Why It Works (Psychological Foundations)**:
  - **Visual Perception**: Features like contour (shape/size, occlusion for depth), texture/shading (material/volume), color (subtle info), symbols (abstract/complex data). Combinations enhance interpretation.
  - **Gestalt Theory**: Principles like proximity, similarity, closure help group visuals (e.g., likes influencing herd behavior in social apps).
  - **Visual Attention**: Pre-attentive (fast, parallel; pop-out via color/shape/motion; "squint test"). Attentive (sequential, selective; bottom-up features vs. top-down goals; fixation-saccade).
  - Variables: Distractors (salient/similar), load (perceptual/cognitive). Example: YouTube video on attention (https://www.youtube.com/watch?v=L8XV8FiUlhY).

- **Factors Affecting Visual Communication**:
  - Message (type/purpose/quantity), context (lighting/distance/distraction), user (demographics/health/goal), hardware (resolution/storage/size).

- **Design & Evaluation Methods**:
  - **Rule-Based**: Guidelines like Material Design (Google) or Human Interface Guidelines (Apple) for consistency.
  - **Metric-Based**: Iterative, data-driven (e.g., GPS map design optimizing for driving safety; paper by Lee et al., 2007).
  - Involve users: Field evaluations from designer/user perspectives.

- **Teaching Tip**: Visuals leverage human perception for intuitive interfaces. Example: In a GPS app, highlight routes with color to reduce cognitive load. Test for cultural ambiguity—e.g., which restaurant sign signals "authentic local food"?

- **Recap Slide (Page 53)**: Covers definition, advantages, when/why to use, methods, examples.

- **Next Steps**: Video on visual design (https://www.youtube.com/watch?v=OxJpZtp2ItE).

#### 2. Sonification: Sound as Information Carrier in HCI (Pages 56-80)
Shifts to audio modalities, especially non-speech sounds, when visuals fail.

- **Definition**:
  - Sonification: Non-speech audio representing data/info (e.g., beeps for notifications).
  - Speech-based: Voice assistants like Siri, but risky in contexts like driving.
  - Silent speech: Subtle inputs (e.g., tongue gestures).

- **When to Use**:
  - Eyes blocked (e.g., blind users), occupied (e.g., multitasking), fooled (e.g., illusions), or insufficient alone (e.g., missing immersive details).

- **Why It Works**:
  - **Music Listening**: Pitch, loudness, timbre, changes.
  - **Everyday Listening**: Auditory events (sources, position, interactions; Gaver, 1993).

- **How to Sonify**:
  - **Computer Events**:
    - **Earcons**: Tonal patterns (pitch/timbre/rhythm) for UI actions (Blattner, 1989; Brewster, 1998).
    - **Auditory Icons**: Everyday sounds mapped to events (e.g., trash sound for delete; Gaver, 1989; Garzonis, 2009). Video demo: https://www.youtube.com/watch?v=WxNaUiEYzME.
  - **Real-World Events**:
    - **Musicons**: Music clips as reminders (e.g., "I'll Be There for You" for locking doors; McGee-Lennon et al., 2011).
    - **Soundnails**: Short sounds for actions/objects (e.g., chopping sound for "chop"; Ma et al., 2010).
  - **Large-Scale Data**:
    - Auditory displays: Sounds for data patterns (e.g., sonifying human movements for stroke rehab; https://www.xsens.com/...). Examples: Higgs Boson data as music; weather data as tones (https://www.youtube.com/watch?v=SXEnDM3hydM).

- **Design Guidelines**:
  - Distinctive, familiar, unambiguous sounds.
  - Consider individual differences (culture/age).
  - Combine with visuals (enhance or distract?).
  - Resources: Sonification Handbook chapters 15-16 (https://sonification.de/handbook/...).

- **Teaching Tip**: Sonification adds layers to HCI—e.g., in a fitness app, rising tones for increasing heart rate. Evaluate intuitiveness: Is a crowd sound better for a busy pool than a lake? References include Gaver (1986-1988), Brewster (1993).

#### 3. Haptic Communication: A Full Body Experience (Pages 81-110)
Focuses on touch-based interactions for immersion when sight/hearing are limited.

- **Definition**:
  - Haptics: Touch, tactile, force-feedback (force/resistance, texture, heat, vibration).
  - Augments info, increases immersion (applications: medicine, entertainment, education, robotics).

- **Haptics as Input**:
  - Touch (e.g., skin gestures; Harrison's work).
  - Midair gestures (e.g., ultrasound haptics; https://www.youtube.com/watch?v=dasYWMc3Nj8).
  - Others: Tongue devices for navigation.
  - Design: Modality + medium (e.g., wearables), sensors/features/models for detection/recognition, user evaluation.
  - Example: Text input on Google Glass via 1D handwriting (https://www.youtube.com/watch?v=l9FIXMPrjF8; CHI 2016 paper).
  - User- vs. Designer-Defined: Elicit gestures from users for intuitiveness (e.g., Augsburg Uni image).

- **Haptics as Output**:
  - Surround/embedded haptics (e.g., vibrations for game immersion; Israr et al., 2011; Lopes & Baudisch, 2013).
  - Videos: Tesla haptic feedback (https://www.youtube.com/watch?v=zo1n5CyCKr0), various demos (e.g., https://www.youtube.com/watch?v=R1lnHeWsSMU).

- **Multimodal Integration (Pages 104-110)**:
  - Combines senses: Info types (physical/psychological state, activities, context, data).
  - Mediums: Wearables (glasses/watch/jewelry) vs. ambient (chair/table).
  - Inputs: Light/sound/force/vibration/heat/texture/smell/taste.
  - Example: Video on multimodal HCI (https://www.youtube.com/watch?v=09yEQfa4Bqw).

- **Teaching Tip**: Haptics make interactions tangible—e.g., vibrating steering wheel for lane departure. Design space: Balance modalities to avoid overload. Evaluate human ability (e.g., how many vibration patterns can users distinguish?).

#### Recap and Key Takeaways
This lecture promotes multimodal HCI for robust, immersive systems. Visuals are primary but limited; audio/haptics complement when needed.

| Section              | Key Concepts | Examples/Tools | Advantages/Limitations |
|----------------------|--------------|----------------|-------------------------|
| **Visual**          | Perception (Gestalt, attention), design (rule/metric-based) | GPS maps, personas | Efficient but ambiguous/cultural-sensitive |
| **Sonification**    | Non-speech audio (earcons, icons, musicons) | Data sonification (Higgs Boson), reminders | Works when eyes fail; needs familiarity |
| **Haptic**          | Input/output via touch/force | Glass text entry, surround vibrations | Immersive; hardware-dependent |
| **Multimodal**      | Integration of senses/mediums | Wearables + ambient | Holistic UX; potential overload |

- **Overall Lesson**: Multimodal design addresses real-world constraints (e.g., driving, accessibility). Iterate with users, draw from psychology (e.g., Gestalt, everyday listening). Watch videos for demos.
- **Pro Tips**: For HCI projects, start with user needs—e.g., if designing for drivers, prioritize haptics/sonification. Check references for deeper research.

If you want focus on a section, examples, or relate to the previous PDF (e.g., ideating multimodal ideas), let me know!