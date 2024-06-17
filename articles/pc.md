# A Solo Approach to Computing

An initiative and experimental program called Project Solo (sometimes written as "SOLO") was launched in 1970 by Thomas Dwyer. This project, one of the many aligned with educational computing, provides an interesting start to a history that focuses on a path from mathematical games to topographical navigation games to adventure games.

project-solo-logo.jpg

Project Solo was initially formed as part of the Special Interest Group on Computer Uses in Education (SIGCUE) within the Association for Computing Machinery (ACM). SIGCUE was an offshoot of the Special Interest Group on Computer Science Education (SIGCSE), founded in 1969. You can read a [history post about the organization](https://sigcse.org/events/50years.html) and, from there, read some of the founding documents.

Dwyer published the inception document for the project in the society's newsletter _Interface_ (volume 4, issue 1) in February 1970. This document is titled "Project Solo: A Statement of Position Regarding CAI and Creativity," where "CAI" refers to "Computer-Assisted Instruction."

project-solo-inception.pdf

Dwyer characterized educational programming as having two modes: dual and solo. The "Project Solo" name was meant to reference the transition of a pilot learning to fly, going from "dual flying" with an instructor to "solo flying" alone.

At the end of 1973, Project Solo transformed and reemerged as Solo Works (sometimes written as "Soloworks"). The new project, officially titled "A Computer-Based High School Mathematics Laboratory," described itself in issue 23 of the Project Solo newsletter, which was published in November 1973.

> Soloworks is officially a project to develop new approaches to high school mathematics education.

A technology focus was clearly the driving factor. The project ultimately envisioned a future where it could augment the computing world by considering different interfaces.

project-solo-lunar-lander-expand-computers.jpg

One such idea, expressed in the above image, was that of a lunar lander that might present an actual visual user interface. Behind the scenes, that interface is driven by a series of mathematical calculations. The mathematical underpinning of this was quite crucial. The Solo project came to focus on the "critical transitional period in math education."

soloworks-transitional-math.jpg

This focus on mathematics will be interesting when we consider some of the initial games and simulations we look at here.

In early 1970, after the inception document was published, a paper written by Thomas Dwyer was published that was called "Some Principles for the Human Use of Computers in Education."

project-solo-no-01-ERIC-ED053566.pdf

[ERIC Source](https://eric.ed.gov/?id=ED053566)

The version I link to here is a [reprint of that paper](https://www.sciencedirect.com/science/article/abs/pii/S0020737371800032) from the _International Journal of Man-Machine Studies_ (volume 3, issue 3), published in July of 1971.

The paper brings up an interestingly significant point.

> One of the most interesting uses of computers we have employed in our high school work involves the creation of tutorial, review, **gaming and simulation programs** by students (not teachers) for the improvement and individualization of various courses.

The emphasis there is mine. The idea of games and simulations was important as it was a way to engage students. In issue 8 of the newsletter, from January 1971, we can see an example of how learning-as-a-game occurred.

project-solo-learning-as-game.jpg

Further, in issue 22 of the newsletter, from June 1972, we read the following:

> Distinctions can be made between games and simulations, although the programs students write in these areas often combine both concepts. The real fun begins when students modify, or better yet create the programs behind simulations and games. For this reason, we believe that listings of such programs should always be furnished to students.

## Hiding and Seeking

In fact, issue 22 of the Project Solo newsletter has another interesting focus. Specifically on the mention of “four computer games: hide-and-seek, NIM, MODULO, and space war.”

project-solo-announce-modules-jun-1972-issue-22.jpg

I want to focus on _Hide and Seek_, also known as “Project Solo module #201” as this will start us down an interesting path. That path shows some common threads as a particular style of game -- text-based adventure games -- came on the scene. First, check out the Hide and Seek program description and listing from the newsletter.

project-solo-hide-and-seek.pdf

### Implementation

We don’t know the exact author but the article tells us that the _Hide and Seek_ program was written in BASIC for the PDP-10. You can see the original Hide and Seek source code.

hideseek-original.bas

Jason Dyer has provided a slightly modified _Hide and Seek_ source version should make the BASIC a bit easier to run on modern BASIC interpreters.

hideseek-modified.bas

You can also try to play a version compiled for both Mac and Windows. It’s a simple executable created with the use of QB64 by compiling the modified version.

hideseek (Mac)
hideseek.exe (Windows)

Now let's dig into this very early progenitor.

### Ludic Experience

As the game instructions print out, the goal is to “FIND THE FOUR PLAYERS WHO ARE HIDDEN ON A 10 BY 10 GRID.” The game gives the player ten guesses to find these other players. It’s worth noting that these are fictional players, not actual game players. No multiplayer quite yet! Those players are nothing more than point locations on a grid.

The ludic experience here is that with each guess, the player picks a point on the grid, and then the program will indicate the distances to each hidden player. If the player’s guess matches precisely the location of a hidden player, then they get credit for finding that “person.”

The player doesn’t see the grid displayed as part of the game but the game gives you some idea of the concept.

```
HOMEBASE WILL BE THE POSITION AT (0,0) AND ANY GUESS
YOU MAKE SHOULD CONTAIN TWO NUMBERS.  THE FIRST GIVES
THE UNIT DISTANCE RIGHT OF THE HOMEBASE AND THE SECOND
IS THE UNIT DISTANCE ABOVE HOMEBASE.
```

Thus the grid structure is the first, or top-right, quadrant of the Cartesian coordinate system, with the origin point (0,0) being on the lower left of the grid. Thus, all player guesses will be to the right and up from the origin.

hide-and-seek-grid.jpg

While the Project Solo article gives an example play session, I think it might be instructive to walk through one to show the ludic experience and also talk about the strategy. The article mentions “triangulation” and that does seem to make some sense. Another strategy that seems to make sense is trilatertion.

NOTE: Triangulation is a method used to determine the location of a point by measuring angles. Trilateration, on the other hand, determines the position of a point by measuring distances, not angles.

Here is how things started for me.

```
TURN NUMBER 1 , WHAT IS YOUR GUESS?
? 3,3
YOUR DISTANCE FROM PLAYER 1 IS 1.4 UNIT(S).
YOUR DISTANCE FROM PLAYER 2 IS 6 UNIT(S).
YOUR DISTANCE FROM PLAYER 3 IS 5 UNIT(S).
YOUR DISTANCE FROM PLAYER 4 IS 3 UNIT(S).
```

At the prompt you can see I chose `3,3` as a starting point. You can see the distance of the players from the point I chose. It’s helpful to focus on finding one player at a time. Thus one strategy that immediately suggests itself is to draw a circle of radius 1.4 with a center at `3,3`.

hide-and-seek-play-001.jpg

This approach aligns well with geometric intuition and the concept of distance in Cartesian coordinates. By focusing on the area within this circle, I can effectively narrow down the possible locations for Player 1, allowing me to adjust my subsequent guesses based on the feedback received from this initial move. So now I try my second guess.

```
TURN NUMBER 2 , WHAT IS YOUR GUESS?
? 7,2
YOUR DISTANCE FROM PLAYER 1 IS 5.3 UNIT(S).
YOUR DISTANCE FROM PLAYER 2 IS 8.6 UNIT(S).
YOUR DISTANCE FROM PLAYER 3 IS 2 UNIT(S).
YOUR DISTANCE FROM PLAYER 4 IS 5.6 UNIT(S).
```

At this point, the game responds that the first player is 5.3 units away from the new point I tried. So, employing the same strategy as before, I now draw a circle of radius 5.3 units away from `7,2`.

hide-and-seek-play-002.jpg

By doing this, I’m effectively narrowing down the potential location of Player 1 even further. The intersection between the circle drawn from the first guess and the circle drawn from the second guess should give me a smaller area where Player 1 is likely “hiding.” This iterative approach of refining my search based on the distances obtained from each guess is an effective way to zero in on the hidden players systematically. In terms of design, this demonstrates a fairly thoughtful use of geometric principles to optimize the search process. Now I can try my third guess.

```
TURN NUMBER 3 , WHAT IS YOUR GUESS?
? 5,7
YOUR DISTANCE FROM PLAYER 1 IS 4.2 UNIT(S).
YOUR DISTANCE FROM PLAYER 2 IS 3.6 UNIT(S).
YOUR DISTANCE FROM PLAYER 3 IS 7.2 UNIT(S).
YOUR DISTANCE FROM PLAYER 4 IS 2.2 UNIT(S).
```

Now, the first player is said to be 4.2 units away from the point I tried. I can thus draw a circle of radius 4.2 units away from `5,7`.

hide-and-seek-play-003.jpg

If the mathematical strategy holds, where the three circles intersect must be the exact location where that player “hides.” Here’s the output if I provide that intersection as my fourth guess:

```
TURN NUMBER 4 , WHAT IS YOUR GUESS?
? 2,4
YOU HAVE FOUND PLAYER 1
YOUR DISTANCE FROM PLAYER 2 IS 5 UNIT(S).
YOUR DISTANCE FROM PLAYER 3 IS 6.4 UNIT(S).
YOUR DISTANCE FROM PLAYER 4 IS 2.2 UNIT(S).
```

Sure enough, that did it, and I’ve found one of the hidden players.

With the approach looked at above for the gameplay, what I did was leverage trilateration to pinpoint the likely location of Hidden Player 1. In trilateration, the point where three circles intersect is a strong candidate for the actual location because it satisfies the distance constraints from each guess. If you find the intersection point of the circles drawn from `3,3`, `7,2`, and `5,7`, this point likely corresponds to the hiding place of Hidden Player 1.

The fact that, in the game, each guess provides information about the distances from the chosen point to all four hidden players is a crucial aspect that supports the soundness of the strategy.

Thus we can see how the idea of design provides a particular way of providing a ludic experience. What this suggests is that different designs could provide a different ludic experience.

### The Idea of Variants

One thing that will come up in my history of early ludic experiences is the idea of variants. This concept means a programmer reworks an existing program, either a lot or a little, to create a variant implementation.

While no student created a variant of the _Hide and Seek_ game in the immediate time frame, at least so far as we know, we can easily imagine a variant. In our hypothetical variant, the game could provide a list of distances to the four hidden players without specifying which distance corresponds to each player. That approach would add an extra layer of complexity and challenge, increasing the difficulty of the game because players would no longer receive explicit information about the identity of each hidden player with each guess. Instead, players would have to infer the associations between the distances and the individual hidden players.

With this approach, players would need to develop more sophisticated strategies to infer the relationships between distances and hidden players. That would require more careful analysis and deduction than with the original game. Let’ss consider a few examples of what that would mean.

With this approach, keeping track of the distances from each previous turn would become crucial. (Keeping track of things will come up soon in PICO.) Recognizing patterns in the changes in distances would aid the player in making informed decisions in subsequent turns. With each turn, players could iteratively refine their understanding of the hidden players’ locations based on the evolving list of distances. This iterative inference process would add some depth to the gameplay. The absence of direct feedback about the identity of the hidden players would also challenge the player to rely on indirect clues and logical deductions, which would encourage a more strategic and deductive approach. Finally, the trilateration approach mentioned earlier would become more challenging since the distances would have to be associated with specific hidden players, adding complexity to the geometric reasoning in narrowing down the possibilities.

Overall, this variant could introduce an intriguing challenge requiring deductive reasoning, memory recall, and strategic thinking. It would likely appeal to players who enjoy puzzles with a higher level of complexity and ambiguity than is found in the original game. What you can see here is why it might appeal to a programmer to create a variant in the first place. As the history of early ludic experiences shows, there was a great deal of experimentation around creating variants of games that students or educators made available to the public.

NOTE: Consider that Zork was essentially a variant of Adventure. As we later get into the PLATO style RPGs, you’ll find that many of these were a string of variants of each other.

As with the original design itself, a key design goal of any variant is to balance challenge and enjoyment while keeping the gameplay interesting and engaging. There’s also some onus on the variant being recognizably a variant as opposed to something entirely new.

## Narrative Experience

We looked at the ludic aspects of the game, but what about the narrative? In one sense, this program is nothing more than a mathematical exercise. The opening text for it claims that “this game encourages students to become familiar with the Cartesian Coordinate system.” Yet, even given that focus, the game is situated in the context of the children’s game “Hide and Seek.” As such, that aspect, simple as it may be, does provide the barest hints of a narrative.

The program could have just said, “Find four points on a grid.” Instead, the game says there are “four players” who are “hidden.” Thus, with a bit of imagination, you can imagine that some characters are actively playing with you as part of the game. The instructions to the game also suggest carrying on the “playing a game with others” conceit if you lose.

```
IF AFTER 10 TRIES YOU ARE UNABLE TO CARRY OUT
THIS TASK YOU MAY CONTINUE TO BE 'IT', BUT THE
PLAYERS WILL BE PERMITTED TO MOVE TO NEW
LOCATIONS.
```

This idea of situating mathematical exercises in a fictional context will reappear in people’s computing. Since, as I argue, people’s computing got started in the educational context, this is not terribly surprising. Many of these programs were created for some pedagogical purpose.

It might seem odd to focus so much attention on what was such a simple program, but, as noted above, players _could_ use a strategy and even a better or worse strategy depending on the game’s design. This idea of a strategy is certainly a motif that would dominate many later game design discussions. Further, a programmer could implement a minimal narrative while allowing players to engage with the ludic experience. The game tried to situate its mechanics in the context of a fun game like _Hide and Seek_.

Another reason I focus on this very early game is that this provides an entry point into considering the barest hint of topographical style games that would, ultimately, lead to the concept of the “adventure game,” even though that was never a plan at this (or, really, any) stage and the path itself certainly wasn’t a direct linear one. The _Hide and Seek_ game would be referenced again as at least an inspiration of sorts for the next stage of games I will consider.

NOW WE HAVE TO INTRO PCC
