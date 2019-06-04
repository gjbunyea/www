---
title: "Debugging Tutor"
excerpt: "A tutor designed to break-ground on debugging as a teachable process"
header:
#   image: /assets/images/zipper/zipper_main.png
  teaser: /assets/images/debugging_tutor/debug_zoom.png
sidebar:
  - title: "Role"
    text: "Researcher, Designer"
  - title: "Duration"
    text: "2 months"
  - title: "Team Members"
    text: "[Ryan Emberling](https://emberling.education/#/about), [Emilio Vargas-Vite](https://github.com/Eleutherado)"
  - title: "What I Learned"
    text: "Cognitive Task Analysis, Sequence Modelling, Prototyping" 
---

## Description
Debugging Tutor is an intelligent tutor that breaks down debugging into several steps. As computer scientists, all three of us felt that debugging is poorly taught, often focusing on how to debug a specific item (loop for example). The tutor is the result of research to better understand how debugging is a process, like medical diagnosis or scientific inquiry. This work was done for Vincent Aleven's Advanced Topics in Personalized Online Learning course, Spring 2019. 

## Problem
Currently, debugging is rarely taught as its own discrete skill set. Students are expected to get better at debugging by virtue of having to debug a lot. There are many tips on how to debug, what to look for, and what to do for a specific bug, but they are disparate and not taught systematically in programming courses. We believe expertise in debugging follows a cohesive process with specific strategies that can be taught explicitly. 

## Research  
### Exploratory
We began more exploratory research by talking with several experts:
- Sharon Carver, a previous professor of ours who's dissertation involved debugging tasks in LOGO. Sharon helped us narrow the scope to teaching print debugging and connected us various resources to help us arrive on a research strategy.

- [David Kosbie](http://www.kosbie.net/cmu/), Director of CMU CS Academy. David provided insight into common problems he’s observed with students in both 15-110 (conceptual intro CS course) an 15-112 (programming-heavy intro CS course) and initial validation that this was indeed something that would be valuable in intro CS education.

- [Kelly Rivers](http://www.krivers.net/), Assistant Teaching Professor. Kelly is currently teaching 15-112, provided us with the current state and needs of the course.


### Cognitive Task Analysis
Through our conversations with these experts, we decided that a Cognitive Task Analysis (CTA) with a focus on developing a Sequence Model would be the primary research needed to unpack debugging. David and Kelly helped to provide us with access to 112 and 110 Teaching Assistants as participants. 

We began by creating a theoretical CTA, exploring our own intuitions about how we debug code. 

We then designed 4 debugging tasks and recruited participants for our study. Our tasks involved unfamiliar code with an existing bug in it (either logical or runtime bugs)--we would have participants debug and think aloud so we can understand their process.

We conducted 6 CTAs in total: 1 Expert, 4 TAs as near experts, and 1 novice. 

![Video of Kelly Rivers' CTA]()

## Sequence Model
We drew on our CTA data to create a Sequence Model representing the steps and decision-points that experts use to locate a bug in a program. Our model describes the iterative process whereby a programmer uses their existing knowledge to inform their evaluation of the state of the program to formulate hypotheses about the problem and to test their hypotheses in order to increase their knowledge of the program.

### Debugging Sequence Model
Below is our Sequence Model. The model is analogous to medical diagnosis or the scientific method as it involves collecting evidence, forming hypotheses, and using information to test those hypotheses.

![Sequence Model for Debugging]()

## Tutor Development
We opted to focus on logical errors, because they are the most difficult to approach (since interpreters/compilers can’t point you to a problematic line for these bugs) and also the hardest to teach students to debug. Logical errors require the broadest range of techniques to diagnose.  As much of how debugging is taught centers around modeling the process inductively with worked examples, we felt that students were likely to reap the most benefit from explicit instruction and practice debugging logical errors.

We used the sequence model to develop the following four learning objectives:
1. Students will identify a model of a program’s control flow that correctly sequences the order of the function calls and characterizes decision points and/or possible repetition of function calls.
2. Students will create a hypothesis that explains the symptoms observed by a program’s output.
3. Given a buggy program, its expected and actual output, and a hypothesis explaining the bug, students will identify a print statement and a line in which to put it that will confirm or reject the hypothesis as an explanation of the bug.
4. After choosing a print statement, students will determine whether the output produced confirms a hypothesis that explains the bug, i.e. they will correctly identify whether the bug has been found after testing their hypothesis.

Our tutor is designed to explicitly scaffold these skills by encouraging students to approach debugging with the following steps:
1. Model the program’s control flow
2. Compare the actual and expected output to identify failed test cases
3. Construct a hypothesis that explains the failed tests
4. Identify which function(s) could be the problem if the hypothesis were correct  
  a. First identify which functions could be the problem  
  b. Then pick one to focus on and test first
5. Check the hypothesis by constructing a print statement
6. Evaluate whether the hypothesis was correct/determine if bug has been identified (if not return to step 4)

## Evaluation
We tested our tutor with 1 competent novice programmer. Our tester completed the tutor but was unable to complete either the pre or post assessment tasks in the allotted 10 minute intervals. This helped us to characterize the challenges to proper assessment of debugging: improvement of this skill will likely take persistent practice over time, and it is not entirely clear how to measure improvement when the difficulty of finding two bugs cannot be compared in a standardized way. 

Despite these difficulties, our tester was receptive to the tutor, and reported appreciated that it sought to scaffold the thinking process she should use to debug code, as this was not something in which she had previously received explicit instruction.

## Conclusion
Our main takeaway is that “good debugging” is difficult to define. This hinges primarily on the fact that it's difficult to create authentic debugging assessments, and as such it’s difficult to measure who is better or worse at debugging. But another component to defining debugging is even knowing what to assess. Possible metrics could be time used for debugging, precision of debugging (fewest moves), clearest hypothesis, but none of these take into account the possibility of how difficult a bug is, which is difficult to define in itself.

Should this work continue, we would need to think much more about how to evaluate debugging. This could include developing a taxonomy of bugs, a listing of types of bugs and how to best go about solving them as well as which bugs are harder than others. Knowing difficulty levels of different bugs would help us to give better pre/post assessments to determine whether or not someone has improved at debugging. 

![Debugging Tutor Image](/assets/images/debugging_tutor/debug_tutor.png)