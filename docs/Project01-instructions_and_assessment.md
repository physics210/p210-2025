# Project 01 - Destructive Collisions: Instructions & Assessment Guidelines
**Last update:** Sep 17, 2025

## *1. Description of the project*

The goal of this project is to develop a research question, answered using a simulation involving one or more collisions, **as well as one or more objects that will be destroyed if they experience too large of a force during one of the collisions**. The motion of one or more objects **before and after** one of your collisions should be integral to your simulation. Below we provide you with some starter code for you to modify. This code uses Euler's method, but you are welcome to use more advanced algorithms---such as RK4---as long as you adhere to a format where you build your own loops, step size logic, and mathematical operations. You are not allowed to use a pre-built ordinary differential equation solver (e.g., you cannot use `solve_ivp()`). 

The destruction aspect of the collision is included for a couple of reasons. First, it necessitates making multiple assumptions about real-world quantities. **An extremely important example of this is that you will need to make decisions about how long the collisions last, and justify these decisions as part of your report.** Second, the use of a categorical outcome in your simulation (e.g., is the object destroyed or not) provides a useful anchor for research questions where you vary one or more independent variables. Speak to Joss if you have an alternate constraint to an object being destroyed that you would like to use in your simulation.

An example research question that combines all these ideas is **"At which speeds and angles can I bounce a water balloon off the ground, such that it doesn't explode and such that it hits a target on the wall."**

The incomplete starter code found below is intended to simulate what happens when two objects (balls) collide with each other (this part does not work yet) and with barriers on either side (this part works). You will need to update this code so that it works as intended, and then extend the code to incorporate destructible elements, additional physics and to answer your research question. Please see Canvas for a gallery of Project 01 posters showing examples of the creativity that last year's students brought to their physical situations, physics extensions and research questions.

## *2. Completing your project*

As part of developing your final project report, you will submit two intermediate documents showing your progress. 

### 2.1. Stage 1: Update the starter code and add some plots (Due Mon., Sep. 22)

Your Homework 05 assignment has three primary tasks, which will also be restated in the Homework 05 notebook.

* **Task 1:** Update the starter code in the Project 01 Tempate so that the collision between the two objects is handled correctly.<br><br>
* **Task 2:** Add one or more well-captioned and labeled plots (not animations) that show the kinematic behaviour of the two objects. It's up to you exactly what you plot, but the idea is that these plots provide you (and the reader) with insight into the behaviour of these objects within the simulation. These types of plots can also be extremely valuable in troubleshooting your code, or otherwise validating that your simulation is behaving as intended.<br><br>
* **Task 3:** Try at least two different sets of initial conditions that you feel could result in unexpected behaviour in your simulation. Examples include making values--such as the initial kinematic quantities or physical properties---significantly smaller or larger than the ones provided. In each case describe which values you changed, why you thought these values might result in unexpected behaviour, and if they did actually result in any unexpected behaviour. If the unexpected behaviour is something that should be fixed, try your best to fix it.

### 2.2. Stage 2: A first, very early draft of your project for peer feedback (Due Wed., Sep. 24)

Using the Project 01 Report Template notebook, you will submit a very early draft of your project showing the initial development of your project ideas. Your notebook should contain at least:

1. An expansion of the physics in the code in at least one substantive way. Examples include (but are not limited to) making the collisions not perfectly elastic, adding an incline, incorporating friction, adding acceleration panels, connecting the balls with a spring, or working in more than one dimension. <br><br>
1. A research question that you find interesting and which is related to the expansions of the physics that you have implemented. Your research question should be built around varying one or more independent variables (we will refer often to this as a phase-space investigation).

In addition to these required elements, you might incorporate some of the Stage 3 elements in your submission since the further along that your project is, the more valuable the feedback will be that you receive from your peers in class on Sep. 24. 

### 2.3. Stage 3: A complete draft of your project (see the syllabus for project deadlines)

Continuing in your Project 01 Report notebook, refine your Stage 2 ideas and perform one or more investigations to answer your researh questions. Communicate your investigation and findings in the form of a project report.

There is some flexibility in the structure of your project report, but here are the key formatting instructions:

1. It should start with an Introduction or Overview to provide the reader with a brief overview of the project, your research question and the context needed to make sense of your research question. <br><br>

1. It should end (before acknowledgements, bibliography or appendices) with a Summary of Results or Conclusion, which should remind the reader what you research question was and then provide the answer to it. This section should refer back to the evidence in the rest of the project to support your answer. This section should also include a **discussion of limitations**, and the **next steps** you would take with this project if you had more time. <br><br>

1. In between the two sections described above should be the main body of your investigation, consisting of the markdown and code cells needed to describe what is going on, and to perform the actual investigation. <br><br>

1. Make use of section titles to help orient and guide the reader.<br><br>

1. A bibliography of any references cited in your project. The formatting of the bibliographic information is not strict. It just needs to be sufficiently easy for a person to track down your source based on the information provided. <br><br>

1. You should use inline citations to indicate which bibligraphic entry is being used as a source for all equations, data, figures, theories, or ideas that aren't your own original work or aren't common knowledge in physics. For example: "Recent measurements show the Hubble constant to be 67.4 km/s/Mpc [1]." Have a look at almost any page on Wikipedia to see how inline citations are used and connected to the biblography.<br><br>

1. As an appendix to your project report (please see the Project 01 Report Template and example report), you will share 2-3 ways that you validated the behaviour of your simulation. By this we mean we want you to put some energy into convincing yourself that your simulation behaves as you intended, from the perspective of the physics and the code. In the process of building and debugging your simulation you will have used some combination of common sense, by-hand calculations, visualizations, debugger interactions and targeted print statements to build up your confidence that things are all behaving correctly. We don't need to see every single one of these validation tasks. Instead, we are asking you to highlight the 2-3 most compelling of these validation / debugging / error-testing steps or tasks.

   - For Project 01, your first validation task is to choose two different sets of starting parameters and compare some behaviour in your simulation to corresponding by-hand calculations to convince yourself that aspect of your simulation is behaving correctly across multiple conditions. For example, if you have multiple collisions within the simulation, focus on what your perceive to be the most important of these collisions. 
   - The other one or two of these validation tasks should focus on behaviours of your simulation that don't make sense to validate using by-hand calculations. <br><br>

1. As a second appendix in your project report, answer a series of reflection questions (provided in the Project 01 Report Template). These questions are designed to help you check your project report against the criteria and expectations before submission and to help us better understand where you extended yourself in completing this project.<br><br>

1. An Acknowledgements section that provides attribution for the help you received in completing your project. This section MUST INCLUDE a statement regarding if and how generative AI was used in completing your project. 

   * If you **did not** use generative AI in completing your project, a statement such as "generative AI was not used to support any aspect of the work submitted in this project report."
   * If you used generative AI, describe how you used it. You should be specific about whether you used it to generate initial code/text, to modify code/text, to troubleshoot code and/or to revise text, and which specific code blocks or sections of text benefited from your use of generative AI. As a reminder, use of generative AI to support your work is allowed, but the expectation is that you have made significant intellectual contributions toward the final project that you submit.<br><br>

1. Other formatting details, such as how code should be formatted and commented, are described in the assessment section below.


<br>Some other key aspects of your project report are:

1. The use a context or situation that you find interesting to help motivate your investigations and research questions.<br><br>

1. Making sure that one or more of the objects is destructible with some well-defined **maximum forces they can tolerate**. These maximum forces should be grounded in real-world examples. You are asked to provide references and justifications for your choice(s). <br><br>

1. You will also have to make many other assumptions along the way. Examples of some of the assumptions you will need to make and justify with real-world examples:

   * Is the collision elastic or inelsatic, and if inelastic how much energy is lost?
   * How long does it take for each of your collisions to occur? This will not necessarily be the same as the time step `dt`.
   * An example of an insufficient justification would be "0.1s seems like a reasonable duration for the collision" <br><br>
  
1. Your report must include a well-captioned and well-labeled **static multi-panel graph** (no animations) which provides insight into the behaviour of your simulation for a given set of parameters and initial conditions. Be creative! This graph should be a concise visual representation that summarizes the behaviour of your simulation for a typical set of parameters and initial conditions, and which highlights one or more interesting things about the behaviour of your simulation (interactions, changes in quantities, etc). When you are building and debugging your simulation, it is likely you will use many more visualizations than just these ones, but in your final submission you want to present a concise visual representation, as described. <br><br>

1. Your report must also include a well-caption and well-labeled graph that provides the main evidence / information used to answer your research question. For most research questions, this graph will represent the findings of your simulation as you vary one or more parameters in your simulation (such as initial velocity). This can be a single- or multi-panel graph.<br><br>

1. Your report should be a working Jupyter notebook, meaning that a person should be able to run your notebook to produce all of the relevant results, graphs, etc. It must contain all of the code needed to 

    * Show how your simulation works,
    * Produce all data that you will be analyzing, and
    * Have the code and data needed to produce any plots that you include. 

## *3. Further advice on developing your project*

**Don't try to build all of the complexity into your simulation at once!** Make the simplest viable version first and make sure it works as intended. Once you understand the amount of work involved in having done that, you will have a much better idea of how much work it will be to incorporate all of your other great ideas.

For those interested in elevating their project to earn distinction points, my experience has been that this often comes naturally through the process of you developing a project that you find interesting and motivating. For many students, it can be helpful to try to come up with a project that has a clear path to being "A" quality (remember "Publish" is equivalent to "A" quality), but which also has room to add further complexity. This allows you to proceed confidently with your project knowing that you can achieve "Publish" while also still having the option to invest the additional effort to elevate it into the distinction point realm. 

## *4. Starter code*

```python
### Starter code for Project 01

import numpy as np

# Constants
t0 = 0      # s
dt = 0.1    # s
t_max = 100 # s
n_steps = int( (t_max - t0) / dt) + 1 # Total number of steps
left_barrier = -10 # m
right_barrier = 10 # m

# Arrays to save simulation information
t = np.zeros(n_steps)
x1 = np.zeros(n_steps)
x2 = np.zeros(n_steps)
v1 = np.zeros(n_steps)
v2 = np.zeros(n_steps)

# Object 1
x1_initial = -5 # m
v1_initial = 2  # m/s
r1 = 0.05 # m
m1 = .01 # kg
x1[0] = x1_initial 
v1[0] = v1_initial 

# Object 2
x2_initial = 7  # m
v2_initial = -1 # m /s
r2 = 0.02 # m
m2 = .001 # kg
x2[0] = x2_initial 
v2[0] = v2_initial 


for i in range(1,n_steps):
    
    # Update kinematic variable for both objects
    x1[i] = x1[i-1] + v1[i-1] * dt
    x2[i] = x2[i-1] + v2[i-1] * dt
    v1[i] = v1[i-1]
    v2[i] = v2[i-1]
    t[i]  =  t[i-1] + dt

    # Check for collisions and update kinematic quantities as needed
    if x1[i] + r1 >= right_barrier or x1[i] - r1 <= left_barrier:
        v1[i] = -v1[i]

    if x2[i] + r2 >= right_barrier or x2[i] - r2 <= left_barrier:
        v2[i] = -v2[i]
```

## *5. Assessment Overview*

The project report should follow some loose structural guidelines, as described above.

As described in the [syllabus](https://physics210.github.io/p210-2025/syllabus.html), projects are given feedback by the graders and an overall Editorial Decision, such as Major Revisions or Accepted for Publication (aka Publish). Projects that have been accepted for publication can earn one ("Notable") or two ("Exemplary") distinction points by going above and beyond expectations and producing work that warrants sharing with the entire class. The process to apply to be considered for distinction points is detailed in the Project 01 Distinction Proposal Form on Canvas and distinction points are awarded by Joss (the "editor"), as opposed to the graders (the "referees").

Much like what happens when practicing scientists submit their work to academic journals, even a relatively high-quality first submission is likely to receive an Editorial Decision of minor or Major Revisions because the grader (referee) will inevitably have many suggestions to improve the overall quality of your project and its report.

### 5.1. Feedback categories

This section details the feedback categories that we will consider when reviewing your projects, which also provide a useful framework in which you can assess if your project is complete and ready to submit.

When looking at the way you have incorporated new physics, expanded the code in other ways or conducted your investigation, we want to consider multiple dimensions. We will look at ambition in terms of implementation difficulty and sophistication. We will also look at ambition in terms of breadth, meaning the number of different ways you expanded the simulation or the number of dimensions along which you performed your investigation. Finally, we will also look at the overall creativity of your investigation, of how you expanded the provided physics and code, and of how effectively you communicated your findings using visualizations and the written word. All of this will be placed in the context of how much you needed to extend yourself in completing this project, as communicated in the answers to your reflection questions.

The feedback you receive from the referees will fall into the following categories and sub-categories:

| Project 01 feedback categories | |
| :--- | :--- |
| **Simulation and simulation physics** | **Ambition and correctness:** How did you extend yourself to incorporate the physics used in your simulation (considerations include creativity, translating physics into code and new physics you learned or developed a more thorough understanding of)? Was your physics implemented correctly in the simulation? |
|  | **Communication of assumptions and context:** Is the simulation context sufficiently described such that the relevance of all incorporated physics ideas can be understood? Are relevant assumptions clearly stated and justified? Are references cited from within the text, as appropriate?
| **Coding** | **Ambition and application:** How well did you apply the coding techniques learned in this course or extend yourself to learn new-to-you techniques? Does the code run properly?
| | **Effective coding practices:** Was an appropriate effort made to make the code efficient, readable, concise and/or final (further details below)? |
| **Communication of investigation** | **Written:** Was a clear research question stated? Was the research question answered effectively via a conclusion or summary of results? Were your conclusions supported by the built-up evidence presented in the body of the report? Were limitations and next steps discussed in sufficient detail to provide an accurate picture of the results and actionable next steps? Is the overall report structured effectively, with section titles as appropriate? |
| | **Visualizations:** Is there a visualization that provides the main information used to answer your research question? Is there a static multi-panel graph that provides insight into the behaviour of the simulation? Is each visualization in the body of the project report important for and incorporated effectively into the overall communication of the investigation? E.g., redundant graphs are not included, graphs used for diagnostics and trouble-shooting are found only in the appendices. Is each individual visualization effective and efficient at communicating its intended information? Does each figure include a descriptive caption that communicates the take-home message to the reader? |
| **Quality of investigation** | **Scope and thoroughness:** Is the investigation some reasonable combination of thorough and ambitious in scope? Thoroughness refers to a combination of exploring phase spaces thoroughly and giving careful attention to interesting features. |
|  | **Validation of code:** Was an appropriate effort made to ensure that the code behaves as intended? Were the key steps of these validations communicated effectively in the project report appendix? |
| **Reflection** | **Acknowledgements and reflection questions:** Does the acknowledgement section contain a statement of if and how generative AI or other help was used to support development of this project? Do the answers to the reflection questions suggest a good faith effort to engage with them? Are the reflection questions answered to a sufficient level of detail as to provide the context needed to understand how efforful the various aspects of the completed project were? |

The sub-category of Effective coding practices (making code efficient, readable, concise and/or final) includes, but is not limited to, the following:
* Making variable names descriptive,
* Providing clear communication of the purpose of each chunk of code via a "code block summary" written in Markdown,
* Augmenting the descriptive variable names and "code block summary" with sufficient commenting to allow others in the course to easily understand what is going on whne reading through your code,
* Ensuring that any output provided by the code has its purpose described,
* Ensuring that diagnostic output from the code has been removed from the body of the project,
* Ensuring that diagnostic output included in the appendices is only what is needed for that specific validation task,
* Minimizing the need for repeating code,
* Using efficient coding practices (e.g., using a dynamic print statement in the Homework 03 motion diagram instead of a long if/elif conditional with individualized print statements for every possible case).


### 5.2. Meeting expectations vs earning distinction points by exceeding expectations

Earning distinction points:
To earn distinction points for an aspect of your report, you need to have clearly gone above and beyond expectations in terms of the creativity, complexity, effectiveness and/or thoroughness of your work. The ways in which you expand and extend your simulation should make sense in the context of your research question and not be included only to increase complexity. The expectation for a project to earn distinction points is that it should have a key element that has exceeded expectations to the point that the project warrants being used as an exemplar in a future year.

The following table provides some examples of project elements expected to earn Accepted for Publication (meeting expectations) and how those elements could be further extended to be considered for distinction points (exceeding expectations).

| Examples of meeting expectations | Examples of exceeding expectations |
| :--- | :--- |
| 2D collisions as the only additional physics | 2D or 3D collisions with some additional physics. The use of 2D/3D should enhance or be motivated by the research question, not be included only to increase complexity. |
| Incorporating a common textbook style physics effect, such as: making the collisions not perfectly elastic, adding an incline, incorporating friction, adding acceleration panels, connecting the balls with a spring, etc. | Bringing multiple physics effects together and having some of them use variable parameters such a research question can be built around exploring the phase space created by varying multiple of these parameters. |
| Incorporating a novel context that motivates the research question and additional physics. | Choosing a novel context and research question such that the addition of significant complexity is required. An example context from last year was a dying star with an expanding radius getting hit by a planet. |
| A multi-panel plot demonstrating different aspects of the simulation function, such as kinematic quantities vs time, histograms, motion diagrams, trajectories in 2D space. | A multi-panel plot making use of creative and novel visualizations that provide clear and deep insight into the behaviour of the simulation. An exampleof a novel visualization from a previous year was one that showed the effects of object deformation during the collision. |



