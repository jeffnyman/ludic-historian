# Wander

## A Pre-Adventure Adventure?

Consider the text adventure game as it came to be in the mid to late 1970s. Was there something natural and inevitable about the act of moving a character around a world with verb-noun commands? Certainly prior to this we had various types of cave crawls.

A lot of people place Will Crowther's _Adventure_ as the first in this category.

But some people feel there's a system that predates that. Peter Langston is alleged to have designed the _Wander_ system starting in 1974 or even possibly as early as 1973. If that's true, then it would certainly have to be the first computer game that is recognizable as what came to be known as a "text adventure." In fact, it might even be the case that _Wander_ was the earliest known precursor to development systems for adventures.

If true, that would be a pretty big coup of the long accepted chronology. Which means we have to view it with some skepticism.

## Finding Wander

So here's how this appears to have started. Graham Nelson wrote a manual for _Inform 6_, his interactive fiction programming system, called the _Inform Designer's Manual_. In that manual, specifically in section §46 ("A Short History of Interactive Fiction"), Nelson refers to:

> Peter Langston's 'Wander' (1974), a text-based world modelling program included in his PSL games distribution for Unix and incorporating rooms, states and portable objects, was at least a proto-adventure.

Jason Dyer was curious about this reference and has stated:

> I first picked up on Wander in a reference by Graham Nelson who called it a proto-adventure system in 1974. I asked but Nelson was not able to recall where he found his reference.

Dyer had put up a post asking about information regarding ["lost mainframe games"](https://bluerenga.blog/2015/03/19/lost-mainframe-games/) of which _Wander_ was at the top of his list. Someone who goes by the name "Ant" (real name: Anthony Hope) comes up next in the story. Anthony wrote ["a lost mainframe game is found"](https://ahopeful.wordpress.com/2015/04/22/wander-1974-a-lost-mainframe-game-is-found/) in which he says:

> Jason's description of _Wander_ on his blog was so intriguing, and the thought that there might still be a chance of finding it again was so tantalising, that I felt I just had to try to get in touch with the original author and programmer, Peter Langston -- which proved to be remarkably easy to do.

Langston did respond [with the following](https://bluerenga.blog/2015/03/19/lost-mainframe-games/#comment-1498):

> I'm not sure I would even know where to look anymore. It's possible that some archivist type from the early Bell Labs and Unix days (circa 1975-80) would have a copy or two of the “PSL Games Tape” that included Empire, StarDrek, Wander, FastFood, Convoy, the Oracle, etc. I can also ask a couple of people who were particular fans of Wander if they have any remaining bits of it.

The context for all this, I should note, was back in early 2015. Langston [further comments](https://bluerenga.blog/2015/03/19/lost-mainframe-games/#comment-1503):

> I probably have the whole archive of early versions of the various PSL games on 8mm tape and/or cassettes and/or 9-track tape, but it's unlikely that any of them are still readable. I did uncover a 1980s C implementation of Wander that Lou Katz had preserved in email messages which he archived. As I remember I came up with the idea for Wander and wrote an early version in HP Basic while I was still teaching at the Evergreen State College in Olympia, WA (that system limited names to six letters, so: WANDER, EMPIRE, CONVOY, SDRECK, GALAXY, etc.). Then I rewrote Wander in C on Harvard's Unix V5 system shortly after our band moved to Boston in 1974. I got around to putting a copyright notice on it in 1978. It compiles with a bit of tweaking (C compilers are a bit more persnickety now and there was a whole PSL games subroutine library available back then) but the documentation uses ancient nroff macros and will take a bit more tweaking. The worst part is that I only have the partial Aldebaran III world (a3) that I used to include in the distribution as an example. There are still one or two more people who may have those files archived.

When asked when the HP BASIC version happened, Langston [specifically says](https://bluerenga.blog/2015/03/19/lost-mainframe-games/#comment-1508):

> That was just before the band decamped to Boston so 1974, possibly even late 1973, I'm not sure.

Anthony relates that Langston sent a file named "Wander.tgz" and this file contained source code and documentation for a 1980s release of _Wander_. Around this same time, a guy named Doug Merritt found a software distribution from the Usenix 1980 conference. There's a lot of random-looking stuff that was distributed there; the part of interest is in "delaware/langston" directory and even more specifically in the "WAND" subdirectory.

See WAND.zip

Everything in there is from 1980 so far as can be told. The "READ_ME_TOO" document does list the following:

> wander.c  2.12   with ftell() last mode 4/9/80 -- (c) psl 1978

So, again, we see 1978. Granted, Langston does say "I got around to putting a copyright notice on it in 1978." But, in the end, that's all we really have: a late 1970s date. Certainly not one that predates _Adventure_.
