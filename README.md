# Introduction

In the real world, you're often given little guidance on the best approach, and you instead have to make design choices yourself. This project folder contains a research paper laying out an algorithm to solve Rubiks cubes. Unfortunately this paper is... scarce on details, and you'll need to figure those out yourself.

Your goal is to implement a Rubiks cube solver following the design laid out by "Solving a Rukik's Cube Using Graph Theory" (included in this project folder). The broad structure should match the paper's, but the implementation details are up to you. All your design decisions should be justified — you'll write up a document justifying your approach and also make a video code walkthrough (described below).

The learning goal of this assignment is to design a complex algorithm and explain the decisions that make it efficient and correct.

# The Code

Your code must implement the algorithm laid out in the associated research paper. It does **not** need to be a parallel algorithm.

Your code should have a runnable main file which allows the user to (1) see a scrambled Rubiks cube, along with the steps needed to solve it and (2) see how fast your solver is by having it scramble and solve thousands of cubes, printing timing information.

Your Rubiks cube visual can be textual instead of graphical. [For example see this](https://github.com/vinicius/rubasciicube/blob/master/rubascii_cube_start.png).

# The Design Diary

This paper omits quite a few details. For example:

 - What's a good cost function to use?
 - What are good values for limitBFS end other variables?
 - What's an efficient way to represent a Rubiks cube in code?
 
As you program, you should keep a diary describing:

 - If you chose to implement or represent something in a certain way, why you chose that implementation.
 - Any experiments that you tried, using alternative approaches or values for variables, and what options ended up giving you the best results.
   - "Best results" is subjective. Did you optimize for speed, memory usage, or something else? Why?
 
# Video Walkthrough

After finishing your solver, you must submit a video that breaks down your project. It should:

 - Explain how to run your code, and some of the features of your solver.
 - Explain the structure of your code, including the inheritance structure and the purpose of each class / file / code section.
 - Explain how, if someone wanted to extend your code with new features, how they would do that, where additional code could go.
 - Explain what each group member's contribution was to the project
 
Your video should be sufficiently detailed that you could give it to a future 301 student who wants to extend your code, and they would understand your project.

# External Help and AI Use

Some parts of the project are auxilliary. You may use AI and external resources liberally, though you still need to (1) be able to explain what the code does, including any advanced java features used, and (2) justify the design decisions made by the code. Auxilliary project pieces include:

 - The cube visualizer
 - The code representation of the cube
 - Any "main file" code that glues things together.
 - Timing code / other code that inspects the efficiency of your algorithms.
 
Some parts of the project are core. You may use AI for debugging and asking questions, but code generation should only be for small, trivial sections of code that would be unchallenging to write yourself. Core project pieces include:

 - The data structures that represent the search for the path to solve your cube.
 - The code that builds and searches through those data structures. (Essentially, anything related to the main algorithm laid out in the paper).

If you use AI, save all chat logs and submit them alongside your project files. If you're unsure whether something is auxilliary or core, please ask me!

# Grading

You must submit a zipped folder with:

 - all code needed to run your project (if you use a complex build system and libraries, there should also be clear instructions on how to make your project runnable)
 - a design diary, as described above
 - a breakdown video, as described above
 - AI chatlogs and citations of external resources
 
Rubric:

 - Solver (50 points)
   - Rubiks cube represented efficiently in code, with a visualizer and functions to perform rotations on the cube (10 points)
   - Algorithm (40 points, 10 points each)
     - BFS from scrambled cube (10 points)
     - Scrambled cube cost calculation (10 points)
     - DLS utilizing cost calculations (10 points)
     - "Back-Tree", searching from the cube and mapping costs to cubes (10 points)
 - Design Diary (20 points)
   - Iteration and experimentation to find good variable values and code representations (10 points)
   - Justification of design decisions that you felt did not require iteration and experimentation (10 points)
 - Video Breakdown (30 points)
   - Good inheritance structure (8 points)
   - Understandable code, extendable by a fellow 301 student (8 points)
   - Well produced video with a good explanation of the code structure (8 points)
   - Explains how to run the code (3 points)
   - Explains each group member's contributions (3 points)
 - Possible points off (includes but not limited to):
   - Failure to cite AI generated code / code found on the internet. Failure to provide AI chat logs or other misuse according to the AI policy.
   - Egregiously bad code style (including overengineered code)
   - Inability to explain code or the design decisions made in the implementation of this project.
   
P.S. Some of the ideas in [this video](https://youtu.be/fy0HRViXZnE) might be helpful!
