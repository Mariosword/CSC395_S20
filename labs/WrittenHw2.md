CSC395 Real-Time Embedded Systems
Written Homework 2
Due: Thursday, April 23, end of day

It might be useful to do the following to tune your gains:
- Use only P. Start with a very low gain so that the motor runs very slowly and takes its time getting to the set position.
- Increase the gain to get a fast response (i.e. get to your set point quickly). Then increase it a little more to oscillate.
- Add in D to dampen the response and eliminate oscillation.

1. Experiment with the gains using two extreme reference positions. For each, establish reasonable gain values for both kP and kD (reasonable meaning you get to the set point pretty quickly without major overshoot).
  - Tune your gains for a reference position of 720 degrees.
  - Tune your gains for a reference position of 4 degrees.

  - a. What were your values for each of the reference positions? Did you select different gains for the different positions?
  - b. For each, what was the _steady state_ error -- meaning how many encoder values were you from your reference position when the motor settled?

2. Experiment with the PD controller frequency. Start with a frequency of 2 ms and continue to increase it by 20ms until the motor is not functioning. (TIP: you can do this through the UI rather than recompiling each time).

  - a. Describe the change in behavior of the motor as you increased the period.
  - b. What was the breaking period of the controller (meaning at what period did the motor seem not controllable)?
  - c. Explain why the motor is behaving in this way.

3. Create a trajectory of +360, -90, +5. Log the reference, measured, and torque values as the motor moves through these trajectories. To log means to print the terminal -- choose a "reasonable" period for printing. There are commands that allow you to capture and save the terminal output to a file. Graph the data using your favorite graphing software (e.g. Excel). If necessary, adjust the scale of the positional or torque information so that both are visible on the same graph.
  - a. Include your graph.
  - b. Pick one element of the graph that is surprising or interesting to you and explain why it captured your attention.
