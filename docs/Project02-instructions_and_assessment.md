# Project 02: Stable orbits in the Saturnian atomic model


## *Project overview*
The goal of this project is to develop and answer a research question that guides a phase-space investigation related to stable orbits in the Saturnian atomic model using `solve_ivp`. The focus of this project is on the quality and depth of your investigation, as opposed to building in additional physics interactions or extending the context.


## *Backstory*
You have been transported back in time to the office of Hantaro Nagaoka at Tokyo Univeristy in 1904 shortly after the discovery of the electron, but before the development of quantum mechanics. Thankfully your computer---with python installed---made the trip with you. Hantaro is working on his "Saturnian" model for the structure of the atom. In this model, the electron orbits a positively charged center similar to the rings of saturn.  You've offered to use python to help him work on his theory.   

Lucky for you and Hantaro, before you were transported back in time, you were learning how to work with `solve_ivp` to play electric field hockey in Physics 210. The code you made for that serves as a great starting point for exploring the Saturnian model!


## *Project details*
Your task is to explore which parameters support stable orbits in the Saturnian model. You will develop one or more research questions that explore the phase space (sets of input parameters) that support stable orbits in this model. A key challenge in this project will be to develop the code that discriminates between stable and unstable orbits.

Your project must include a minimum of three particles: one electron and two fixed-postion nuclei, or one fixed-position nucleus and two electrons. Your phase-space exploration should focus on finding ranges of initial conditions over which stable orbits occur. The most interesting investigations will typically include detailed explorations of the regions where there are transitions from stable to unstable orbits.

You are not required to work at an atomic distance scale for this project. You can work at distances between the electons and nuclei that more closely resemble those used in the Electric Field Hockey tasks or to use atomic distance scales. It is up to you.

**Hint:** You will likely want to develop your code so that you can easily change parameters/initial conditions and then determine if a stable orbit has occurred. Consider making a function that allows you to change initial conditions easily and returns something that tells you about the properties of the orbit.


## *Developing and completing your project*

1. Develop some code that uses `solve_ivp` to model the behaviour of your multi-particle system. Note that it is much more challenging to establish stable orbits with two electrons orbiting one stationary particle as opposed to having one electron orbiting two stationary particles. You may wish to engage in a brief exploration with each type of setup before making your decision on which setup to use in your investigations.<br><br>

1. Develop a research question related to stable vs unstable orbits that you find interesting and which can be answered with your simulation. <br><br>

1. Produce a project report (a computational narrative in Jupyter notebook form) using the Project 02 template (it is a copy of the Project 01 template). This project report should ask and answer your research question, with the body of the providing the evidence and information needed to support your answer to the research question. The [Assessment Overview](https://physics210.github.io/p210-2025/Project01-instructions_and_assessment.html#5-assessment-overview) from the Project 01 Instructions applies for this project as well, and lays out the key features that should be in this report. <br><br>

## *Key project formatting details*

1. It should start with an Introduction or Overview to provide the reader with a brief overview of the project, your research question and the context needed to make sense of your research question.<br><br>

1. It should end (before acknowledgements, bibliography or appendices) with a Summary of Results or Conclusion, which should remind the reader what you research question was and then provide the answer to it. This section should refer back to the evidence in the rest of the project to support your answer. This section should also include a discussion of limitations, and the next steps you would take with this project if you had more time.<br><br>

1. In between the two sections described above should be the main body of your investigation, consisting of the markdown and code cells needed to describe what is going on, and to perform the actual investigation. Ensure that your code would be easy for a peer to follow through the a combination of descriptive variable names, comments in your code, and/or a descriptive "code block summary" written in Markdown before the code block. It is often a good idea to break your code into smaller code block within the notebook so that it is easier to summarize the purpose of each chunk of code.<br><br>

1. Make use of section titles to help orient and guide the reader.<br><br>

1. A single- or multi-panel visualization should provide the main evidence / information used to answer your research question. For most research questions, this visualization will represent the findings of your simulation as you vary one or more parameters in your simulation (such as initial velocity). Make effective use of titles, annotations and/or captions so that the reader can easily understand and correctly interpret your visualization.<br><br>

1. A **static** multi-panel vlsualization (no animations) should be included to provide insight into the behaviour of your simulation across at least two sets of parameters and initial conditions. Be creative! Each panel should be a concise visual representation summarizing the behaviour of your simulation for a typical set of parameters and initial conditions. Again, make effective use of titles, annotations and/or captions so that the reader can easily understand and correctly interpret your visualizations. As a reminder, visualizations used for debugging your simulation should not be included in the body of the project report, but may be used in the appendix as part of communicating your validation tasks.<br><br>

1. An Acknowledgements section that provides attribution for the help you received in completing your project. This section MUST INCLUDE a statement regarding if and how generative AI was used in completing your project. 
   * If you **did not** use generative AI in completing your project, a statement such as "generative AI was not used to support any aspect of the work submitted in this project report."
   * If you used generative AI, describe how you used it. You should be specific about whether you used it to generate initial code/text, to modify code/text, to troubleshoot code and/or to revise text, and which specific code blocks or sections of text benefited from your use of generative AI. As a reminder, use of generative AI to support your work is allowed, but the expectation is that you have made significant intellectual contributions toward the final project that you submit.<br><br>

1. A bibliography of any references cited in your project. The formatting of the bibliographic information is not strict. It just needs to be sufficiently easy for a person to track down your source based on the information provided. <br><br>

1. You should use inline citations to indicate which bibligraphic entry is being used as a source for all equations, data, figures, theories, or ideas that aren't your own original work or aren't common knowledge in physics. For example: "Recent measurements show the Hubble constant to be 67.4 km/s/Mpc [1]." Have a look at almost any page on Wikipedia to see how inline citations are used and connected to the biblography.<br><br>

1. As an appendix to your project report, share 2-3 ways that you validated the behaviour of your simulation. By this we mean we want you to put some energy into convincing yourself that your simulation behaves as you intended, from the perspective of the physics and the code. In the process of building and debugging your simulation you will have used some combination of common sense, by-hand calculations, visualizations, debugger interactions and lots of targeted print statements to build up your confidence that things are all behaving correctly. We don't need to see every single one of these validation tasks. Instead, we are asking you to highlight the 2-3 most compelling of these validation / debugging / error-testing steps or tasks. Unlike with Project 01, we do not require a comparison with a by-hand calculation for this project.<br><br>

1. As a second appendix in your project report, answer a series of reflection questions (provided in the Project 02 Report Template). These questions are designed to help you check your project report against the criteria and expectations before submission and to help us better understand where you extended yourself in completing this project.



## *Tips*

1. **Start with a 1 proton + 1 electron system if you are struggling at all to get things up and running.** This system is like a simple Earth + satellite system where you just need to pick a distance scale (initial distance between the proton and electron) and there will be a single, unique speed that corresponds to a circular orbit. And you can calculate the period of this orbit as well. This gives you starting points and order of magnitude constraints for your initial velocities in the more complicated systems and for how long to run the simulation since you won't usually want it to be much more than an order of magnitude larger than the period of this simple orbit. Then, add your next particle and use these values as your starting points.<br><br>

1. **Symmetry is your friend.** If you are using a multi-electron system, start with systems that are highly symmetric, such as each of your electrons having the same initial speeds and distances from the central charge, while being evenly spaced out around the central charge. Once you have found some stable orbits in this symmetric system, then try to make your system asymmetric.<br><br>

1. **You are in charge of defining what a stable orbit is and how to detect it.** Nuff said.<br><br>

1. **Zoom in on your central charge when you expect a somewhat stable orbit, but don't observe it.** When you observe your moving charge moving directly away from the central charge(s), zoom in on the central charge as it may reveal some initial quasi-stable orbital behaviour.<br><br>

1. **Set your `atol` and `rtol` tolerances value nice and small.** Small values for these forces the precision of the solution to be as high as possible. The ensures, for example, that the simple system of one electron orbitting one proton will have a stable, energy-conserving, circular orbit. If your precision isn't high enough, you might end up with non-physical behaviours such as the electron spiralling toward the proton. Example:
   * `sol = solve_ivp(diff_eqns, t_span, state0, max_step=dt, rtol=1e-9, atol=1e-9)`<br><br>
