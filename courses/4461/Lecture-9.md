---
layout: default
title: "Lecture 9: Design: Prototyping"
---

This is a comprehensive summary and lesson on **Prototyping Methods and Practices** based on the slides you provided.

***

## Summary Notes: Prototyping Methods and Practices

Prototyping is a core stage in **Human-Centered Design (HCD)**, following **Empathize** (learning about customers), **Define** (constructing a point of view), and **Ideate** (brainstorming solutions). The goal of prototyping is to **Build a representation of your solutions** before moving to the final **Test** stage (putting prototypes in front of users for feedback).

### I. Purpose and Definition of a Prototype
* **Definition:** A prototype is a representation of a solution that is **Fast, Focused,** and **Expressive**.
* **Prototyping helps you:**
    * **Express and realize** a design concept.
    * **Communicate** and **Evaluate** design ideas.
    * **Produce something tangible** to **Encourage user feedback**.
    * **Assess usability** and **Test User experience**.
* **What to prototype in HCI:** You can prototype the **Task Design and User Flow**, **Layouts and Content**, **Look and Feel**, **Technical Aspects**, and **Controversial/Critical Areas** (e.g., security and privacy).

### II. The Prototyping Process Dimensions
Prototypes can be classified based on how they progress:

| Dimension | Type | Description |
| :--- | :--- | :--- |
| **Across Iterations (Design Breadth)** | **Serial** | **Depth-first** approach, refining one design over several versions (Iterative). |
| | **Parallel** | **Breadth/Diversity-first** approach, creating and testing multiple different designs simultaneously before converging on one. |
| **Range of Capabilities (Design Depth)** | **Horizontal** | Prototypes featuring a **wide range of features** without the full "implementation" of any single feature. Focuses on the scope of the interface/different features. |
| | **Vertical** | Prototypes where **selected feature(s) are "implemented" all the way through**. Focuses on a deep dive into the functionality of a single scenario. |

### III. The Spectrum of Fidelity (Low- to High-Fidelity)
Fidelity refers to how closely a prototype resembles the final product in terms of appearance and functionality.

| Fidelity | Key Characteristics | Goals | Examples/Methods |
| :--- | :--- | :--- | :--- |
| **Low-Fidelity** | Quick, cheap, non-digital, minimal visual design. | Gain **concept and consensus** quickly. Test information architecture, functionality, and patterns. | **Sketch/Paper Prototypes**. |
| **Medium-Fidelity** | Interactive pages (e.g., clickable wireframes). | Simulate **"Real" Experiences** (Look and feel, User testing). | **On-Screen Interactive Wireframe** (using tools like InVision, Sketch, etc.). |
| **High-Fidelity** | Functioning software/mockups, representative visual design, code may be reusable. | Provide a representative (if limited) **user experience**. Enable **interaction and navigation**. Used for **Evaluation and marketing**. | **Software** with partial functions, **Digital Mockups**. |

### IV. Specific Prototyping Methods
* **Storyboards:** Useful for prototyping the **User Flow**.
* **Paper Prototype:** Low-fidelity method focusing on form factors, UI components, and workflow, offering *some* interactivity for user feedback and interface evaluation.
* **Video Prototype:** Used to prototype the **Overall experience**. It allows you to prototype functionality **without needing to be physically present**, but is limited to a scenario.
* **The Wizard of Oz Technique:** Uses **(hidden) humans to imitate a complex automated process** (like AI or speech recognition). This allows you to test if people would want the experience ("Would people actually want this?") before investing in the technical innovation ("Can we do this?").

***

## Lesson: Mastering the Prototyping Mindset

The core lesson from these slides is that **prototyping is not just about building; it's about asking and answering questions efficiently.** Your goal is to fail fast and learn quickly by building minimum representations of your idea.

### 1. The Prototyping Mantra: Fast, Focused, Expressive
To truly benefit from prototyping, adopt the mindset behind its three attributes:

* **Fast (Speed):** The quicker you build and test, the more iterations you can fit into your design cycle. Early prototypes (like a 3-minute sketch) should be disposable. This minimizes your investment in bad ideas.
* **Focused (Purpose):** Every prototype should be built to answer one specific question.
    * Are you questioning the menu structure? Build a **Horizontal prototype** to show all menu paths.
    * Are you questioning the usability of a single key feature, like the checkout process? Build a **Vertical prototype** that only implements that feature deeply.
* **Expressive (Communication):** The prototype must clearly communicate the *idea* you are testing. A simple sketch is expressive enough to communicate flow (Low-Fidelity), while a functional mock-up is required to test visual design details (High-Fidelity).

### 2. Matching Method to Question (The Fidelity Spectrum)

The most important decision is choosing the right fidelity. You should start **Low-Fidelity** and only move to **High-Fidelity** once you've gained confidence in your fundamental design decisions.

| Question You're Asking                                                                      | Best Fidelity/Method                                                            | Why?                                                                                                                                                                                   |
| :------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **What are the screens and how do they connect?** (User flow, Information Architecture)     | **Low-Fidelity:** Sketching or Paper Prototypes.      | It's cheap and quick to change. Users focus on structure, not appearance. You avoid the caution of users/testers being "misled if the prototype is too perfect". |
| **What does it feel like to use this futuristic feature?** (AI, complex system)             | **Specialized Method: Wizard of Oz.**                     | This allows you to test the *experience* of the AI/system before you build the complex, expensive technology.                                                                          |
| **How does the user interact with the final visual design?** (Look and Feel, Interactivity) | **High-Fidelity:** Digital Mockups/Interactive Pages. | The visual design (look and feel) is a key component of the test. Materials from these prototypes can often be reused in the final implementation.               |

### 3. Key Takeaway: Iteration and Parallelism

The most effective design approach often begins with a **Parallel** strategy, where multiple initial concepts are explored and tested with **Low-Fidelity** methods (breadth-first). Once the best ideas are identified, the team converges and continues with a **Serial** (depth-first) and **Iterative** refinement of the chosen concept, gradually increasing the fidelity of the prototype until the final product is released.