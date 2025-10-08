# Project 02: Stable orbits in the Saturnian atomic model


## *Project overview*
The goal of this project is to develop and answer a research question that guides a phase-space investigation related to stable orbits in the Saturnian atomic model using `solve_ivp`. The focus of this project is on the quality and depth of your investigation, as opposed to building in additional physics interactions or extending the context.


## *Backstory*
You have been transported back in time to the office of Hantaro Nagaoka at Tokyo Univeristy in 1904 shortly after the discovery of the electron, but before the development of quantum mechanics. Thankfully your computer---with python installed---made the trip with you. Hantaro is working on his "Saturnian" model for the structure of the atom. In this model, the electron orbits a positively charged center similar to the rings of saturn.  You've offered to use python to help him work on his theory.   

Lucky for you and Hantaro, before you were transported back in time, you were learning how to work with `solve_ivp` to play electric field hockey in Physics 210. The code you made for that serves as a great starting point for exploring the Saturnian model!


## *Project details*
Your task is to explore which parameters support stable orbits in the Saturnian model. You will develop one or more research questions that explore the phase space (sets of input parameters) that support stable orbits in this model. A key challenge in this project will be to develop the code that discriminates between stable and unstable orbits.

Your project must include a minimum of three particles: one electron and two fixed-postion nuclei, or one fixed-position nucleus and two electrons. Your phase-space exploration should focus on finding ranges of initial conditions over which stable orbits occur. The most interesting investigations will typically include detailed explorations of the regions where there are transitions from stable to unstable orbits.

**Hint:** You will likely want to develop your code so that you can easily change parameters/initial conditions and then determine if a stable orbit has occurred. Consider making a function that allows you to change initial conditions easily and returns something that tells you about the properties of the orbit.


## *Developing and completing your project*

1. Develop some code that uses `solve_ivp` to model the behaviour of your multi-particle system. Please note that it is much more challenging to establish stable orbits with two electrons orbiting one stationary particle as opposed to having one electron orbiting two stationary particles. You may wish to engage in a brief exploration with each type of setup before making your decision on which setup to use in your investigations.<br><br>

1. Develop a research question that you find interesting and which can be answered with your simulation. <br><br>

1. Produce a project report (a computational narrative in Jupyter notebook form) using the Project 02 template (it is a copy of the Project 01 template). This project report should ask and answer your research question, with the body of the providing the evidence and information needed to support your answer to the research question. The referee rubric for Project 01 will be used for this project as well, and lays out the key features that should be in this report. <br><br>

1. Develop a single- or multi-panel visualization to provide the main evidence / information used to answer your research question. For most research questions, this visualization will represent the findings of your simulation as you vary one or more parameters in your simulation (such as initial velocity). Make effective use of titles, annotations and/or captions so that the reader can easily understand and correctly interpret your visualizations.<br><br>

1. Develop a **static** multi-panel vlsualization (no animations) that provides insight into the behaviour of your simulation across at least two sets of parameters and initial conditions. Be creative! Each panel should be a concise visual representation summarizing the behaviour of your simulation for a typical set of parameters and initial conditions. Again, make effective use of titles, annotations and/or captions so that the reader can easily understand and correctly interpret your visualizations. As a reminder, visualizations used for debugging your simulation should not be included in the body of the project report, but may be used in the appendix as part of communicating your validation tasks.<br><br>

1. As an appendix to your project report, share 2-3 ways that you validated the behaviour of your simulation. By this we mean we want you to put some energy into convincing yourself that your simulation behaves as you intended, from the perspective of the physics and the code. In the process of building and debugging your simulation you will have used some combination of common sense, by-hand calculations, visualizations, debugger interactions and lots of targeted print statements to build up your confidence that things are all behaving correctly. We don't need to see every single one of these validation tasks. Instead, we are asking you to highlight the 2-3 most compelling of these validation / debugging / error-testing steps or tasks.<br><br>

1. As a second appendix in your project report, answer a series of reflection questions (provided in the Project 02 Report Template). These questions are designed to help you check your project report against the criteria and expectations before submission and to help us better understand where you extended yourself in completing this project.

## *Tips*

1. **Start with a 1 proton + 1 electron system if you are struggling at all to get things up and running.** This system is like a simple Earth + satellite system where you just need to pick a distance scale (initial distance between the proton and electron) and there will be a single, unique speed that corresponds to a circular orbit. And you can calculate the period of this orbit as well. This gives you starting points and order of magnitude constraints for your initial velocities in the more complicated systems and for how long to run the simulation since you won't usually want it to be much more than an order of magnitude larger than the period of this simple orbit. Then, add your next particle and use these values as your starting points.<br><br>

1. **Symmetry is your friend.** If you are using a multi-electron system, start with systems that are highly symmetric, such as each of your electrons having the same initial speeds and distances from the central charge, while being evenly spaced out around the central charge. Once you have found some stable orbits in this symmetric system, then try to make your system asymmetric.<br><br>

1. **You are in charge of defining what a stable orbit is and how to detect it.** Nuff said.<br><br>

1. **Zoom in on your central charge when you expect a somewhat stable orbit, but don't observe it.** Sometimes your simulation runs much longer than needed such that a particle that escapes looks like that is the only thing, but zooming in on the central charge may reveal some initial quasi-stable orbital behaviour.<br><br>

1. **Set your `atol` and `rtol` tolerances value nice and small.** This was advice given in Homework 10, but this is the difference between a sinple 1 proton + 1 electron orbit having a nice, stable, energy-conserving, circular orbit and one that has the electron spiraling toward the proton. This is forcing the precision of the solution to be as high as possible. You can see this in action in the Homework 10 solutions. Example:
   * `sol = solve_ivp(diff_eqns, t_span, state0, t_eval=times, rtol=1e-9, atol=1e-9)`<br><br>

1. **Use `max_step = dt` instead of `t_eval = times`.** This is something I discussed in the Worksheet 10 solutions, but I discovered recently that instead of specifying all of the evaluation times with `t_eval = times`, it is even better to use `max_step` to provide the maximum time step that `solve_ivp` should use. For most steps, this will use the same steps you would have specified with `t_eval = times`, but when the differentials are suddenly much higher than usual---such as when an electron is extremely close to a proton---`solve_ivp` will decrease the size of the time steps it is using, allowing it to calculate the trajectories much more accurately at the high accelerations. Note that you can use this in conjunction with `atol` and `rtol` settings. Example:
   * `sol = solve_ivp(diff_eqns, t_span, state0, max_step = dt)`
