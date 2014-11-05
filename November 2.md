# Design notebook for week ending November 2, 2014

Notebook entry for the week of November second:

This week I spent about 2 hours researching other coding
type games, for example the robot battle game Ari recommended
as well as code combat. In addition, I spent 2 hours working on
the writeup with Nathan. This is less than the required 9 hours
but we wanted to make sure that we got preliminary feedback
before we dived into the actual project. I'm confident that we'll
make up that time later on in the process.

I think the most pressing issue for our project right now is
the game engine. I've been looking into options and I found
a few different ways to approach the problem. My first line
of attack will be to try to use the spring engine, found here.

http://springrts.com/

The engine is an open source RTS game engine that will allow us to
program AIs. I think that this is a viable option, given that
there are well established APIs for determining AI behavior.

If that doesnt work, the second option is:

https://github.com/dunnololda/scage/

This is a basic graphics engine written in scala. If we have to
go with this option, we will be writing a 2D game, which is fine
since the game isn't really the point here. If we can't get either
of these options to work in a reasonable amount of time then we'll
just use a 2D c++ library. There are plenty of existing libraries that
will allow us to move pixels around on the screen (which is
all we really need).

We would love feedback about the design of the language from
our feedback partners. Do you guys have any ideas for where we
should steer the language? We're not doing turing complete,
and I think that we have an idea of the basic command options:
"If theres a unit in front of you attack it", ect. But we'd love
to hear more ideas.

Additionally I spent two hours working with Nathan on the 
DSL itself. We took what I think is a really cool approach to 
the problem. 

The main existential problem we had was that we didn't want
to limit the creativity of the user as they wrote their 
commands to their troops. On the other hand, we didn't want
to provide the user with all of the information about the
state of the game and let them make decisions based on that, 
because there is no way we could support API calls for
every behavior the user could want to have.

To deal with this, we decided that programs in our language 
should be broken into "behavior groupings".  Units have a 
default behavior for certain aspects of the game 
(for example which enemy to attack). When a user wants 
a unit to disobey those defaults, then they must spend IQ 
points. 

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I think the most pressing issue right now is twofold. We want to find windows so 
that we can commit to using spring, which seems like a very good option for us,
and we have to get a spring "hello world" example off the ground.

**What questions do you have for your critique partners? How can they best help
you?**

Take a look at our skeleton language specification. Do you think it covers 
all of the things you would want your units to base their decisions off
of in an RTS game? Do you have any suggestions?

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

I spent about 7 hours on the project this week (not counting critique). Much of that 
was spent trying to compile spring on mac (which I eventually gave up on), and the
rest was spent with Nathan figuring out what we want to do for our DSL. 

## Post-critique summary

## Post-critique reflection
