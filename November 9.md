# Design notebook for week ending November 9, 2014

## Description

This week we fleshed out the design of our language and started messing around
in spring. 

We made some interesting design decisions in the implementation of our language.
We decided that the core decisionmaking processes we were interested in impelementing
could be abstracted into three main areas:

  1: Formation
  
  2: Movement
  
  3: Targeting

In essence we're saying that every behavior the user wants for their units should
fall into one of these three categories. Without going into too much detail, 
a program is a specification of a default behavior for each of these aspects of a unit's
AI. There is a (crappy) default behavior for each of these aspects, and it costs
an IQ point to specify a new default for any one of formation, movement, or targeting.
In addition, the user can spend IQ points on "conditionals", which specify a new
behavior to adopt when a condition is met. There are three different behaviors
for each of the areas above (for example a unit's movement can be move towards enemy,
move away from enemy, or hold ground) and there are about 10 universal conditionals 
(for example "when there are > 5 close enemies"). The full grammar is specified in 
the project folder. 

We feel like this system is good for us because it allows us to severely limit the
inputs of the user (which means we can actually implement this thing) 
while maitaining their creativity (for the most part). We took Ari's advice and
made the conditionals universal (as opposed to local to an area). I think this 
makes the language easier to learn, which is important. 

I think this is probably the most important design decision we made this week, 
and I'm excited about the language we have so far!

Besides language design, I spent a fair amount of time messing around with spring
trying to get that off the ground and made a great amount of progress! We have a 
cube moving around! This might not seem like much but the fact that we can run 
the engine, generate our own model, and specify that model's basic behavior (e.g. 
movement speed, ect.) is great! (A picture is included in the repo).

The next step is to replace the cube model and textures with something that looks
nice (which shouldnt be too dificult, open source models and textures already exist),
and then to make a bunch of them and come up with some kind of simplistic AI to
make them fight eachother (which is what I had in mind as the deliverable for
next week). Depending on how long that takes we might be able to flesh
out a bit more of the game design in terms of what units will exist. 

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I think the most pressing issue right now is how do we translate the user
generated code into something the AI API can run, which requires some research
of the AI API as well as some brainstorming from us. 

To say this in a more DSL-ey way the issue is to figure out what the IR looks
like as well as nail down the specifics of what IR->Evaluation looks like.

**What questions do you have for your critique partners? How can they best help
you?**

I have two questions. 

1. Take a look at the language specification. If you were writing an RTS AI is there
anything you would want to do that you cant do in our syntax.

2. What kind of units would you want in the game. For now I think I'm leaning towards
what is essentially a rock-paper-scissors style setup, where each side has three 
different units and they are each effective against one of the others. 

I think that at least as a starting point this would make sense, since it allows
for meaningful strategy decisions without too much complication.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

I think we spent about 4 hours working togeather on the language specification 
over a few nights, I also spent 3-4 hours working with spring on my own. And another
hour doing my notebook. I'm also planning on figuring out our PC situation with Dodds 
tomorrow morning. 

I didn't do a great job of writing down the hours in which I was working this week so
I'll try to do that more consistently next week. 

## Post-critique summary
Tyler brought up a lot of good things in his critique. He honed in on IQ as what makes our game unique, and brought up a lot of good design questions that we hadn't really considered. When we start building the game itself I think it will be critical to have some kind of well thought out plan for how many 5 IQ units it takes to bring the same value as a 10 IQ unit, etc., which is something Tyler pointed out. 

He also emphasized keeping game engine coding to a minimum - which is a fear we share. Luckily, I feel like we've had good success with spring so far which means we'll be able to use it instead of a text based approach, which also would have been totally fine. 

## Post-critique reflection
The feedback improved our project by making us consider important game design issues and deal with
them in an intentional way. We'll have a better end result if we consider Tyler's questions about IQ 
and decide how we feel about them before coding the actual game. 

I'd also like to give a shoutout to Ari's advice that we standardize the conditionals, which we 
did in our full language specification. 
