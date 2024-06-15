Peter S. Langston writes the first Empire program at Evergreen State College.

A source for this is: http://wolfpackempire.com/peter.langston.on.birthdate.txt
Reproduced here: peter.langston.on.birthdate.txt

Ben Norton, Chuck Douglas, Mike Rainwater and several others contribute to this project.
A source for this is: http://wolfpackempire.com/versionshowing1978empire.txt
Reproduced here: version.showing.1978.empire.txt
(Search for "HP Empire")

From that source, note that something called "PSL Empire" runs on the PDP 11/70.
(Search for "Old Empire" || Search for "PSL Empire")
A note on it says:

```
Written by Peter Langston long ago.  This is the version of
empire that started it all.  It was distributed in binary
form for many years.
```

Peter never released the source code to this version.
The only direct evidence we thus have for a specific date of Empire is 1972.
And that's confirmed by Peter Langston.

One thing to notice that is not mentioned in the "birthdate" reference above is anything called "Wander." By itself, that may not be odd since it would not necessarily fit in the category of games being described.

There are some comments about "Wander" on the net.game newsgroup.
Source: https://groups.google.com/g/net.games/c/8FgvJMDReLg/m/aRGD7WqH7SgJ

This one is from 4 November 1985 by Sean Casey:

```
We have a binary of Peter Langston's adventure interpreter "wander". I
like it a lot, but it seems to have a few bugs. The most annoying is
that "s" is not an abbreviation for "south" and cannot be forced to be
"south" by a pre or post action. Another is that a pre or post action
that prints a string also prints out "m=" prepended to the string.

Does anyone have a version of this that has these bugs fixed? Does
anyone have (gasp) sources?
```

An even earlier reference can be found.
Source: https://groups.google.com/g/net.games/c/JtiAHcDT9IM/m/-4xkLRFkHWcJ

This is from 25 and 28 April 1983. Someone named Eric Holtman writes:

```
Is there anyone out there with any intrest in
Peter Langston's 'Wander' games. I was thinking
of writing an adventure for it, but don't want to waste
my time if there's no one willing to play it.
```

Geo Swan responds and mentions four "wander databases" that were known:


```
castle: you explore a rural area and a castle searching
for a beautiful damsel.
a3: you are the diplomat Retief (A sf character written
by Keith Laumer) assigned to save earthmen on
Aldebaran III
library: You explore a library after civilization has been destroyed.
tut: the player receives a tutorial in binary arithmetic.
```

There is a software distribution from the Usenix 1980 conference.
Source: http://mirror.cc.vt.edu/pub2/Ancient_Unix/Applications/Shoppa_Tapes/usenix_80_delaware.tar.gz

This was found by Doug Merritt. It contains the "wander databases" mentioned in the post from Geo.
There's a lot of random-looking stuff that was distributed there; the part of interest is in delaware/langston/WAND or the whole of delaware/langston.

Of note: nothing in that source lists anything older than 1978.

This would make sense: Wander clearly seems to build on the ideas of Adventure. Yet, it's not quite that simple.

Graham Nelson wrote a manual for <em>Inform 6</em>, his interactive fiction programming system, called the <em>Inform Designer's Manual</em>. This was written in July 2001. In that manual, specifically §46 ("A Brief History of Interactive Fiction"), Nelson refers to:

> Peter Langston's 'Wander' (1974), a text-based world modelling program included in his PSL games distribution for Unix and incorporating rooms, states and portable objects, was at least a proto-adventure.

Jason Dyer was curious about this reference and has stated:

> I first picked up on Wander in a reference by Graham Nelson who called it a proto-adventure system in 1974. I asked but Nelson was not able to recall where he found his reference.

Given that we have the PSL games distribution, it's quite possible -- and even likely -- that Nelson was simply not remembering the date correctly. And since he can't remember where he actually got his reference, his source has little to no historical value.

Dyer had put up a post (https://bluerenga.blog/2015/03/19/lost-mainframe-games/) asking about information regarding "lost mainframe games" of which <em>Wander</em> was at the top of his list. Someone who goes by the name "Ant" (Anthony Hope) comes up next in the story.

https://ahopeful.wordpress.com/2015/04/22/wander-1974-a-lost-mainframe-game-is-found/

> Jason's description of Wander on his blog was so intriguing, and the thought that there might still be a chance of finding it again was so tantalising, that I felt I just had to try to get in touch with the original author and programmer, Peter Langston -- which proved to be remarkably easy to do.

Notice how both Dyer and Hope are assuming the 1974 that Nelson mentioned, even though there really is no evidence for this at all.

Langston did respond with the following:

> I'm not sure I would even know where to look anymore. It's possible that some archivist type from the early Bell Labs and Unix days (circa 1975-80) would have a copy or two of the “PSL Games Tape” that included Empire, StarDrek, Wander, FastFood, Convoy, the Oracle, etc. I can also ask a couple of people who were particular fans of Wander if they have any remaining bits of it.

The context for all this, I should note, was back in early 2015. Langston further comments:

> I probably have the whole archive of early versions of the various PSL games on 8mm tape and/or cassettes and/or 9-track tape, but it's unlikely that any of them are still readable. I did uncover a 1980s C implementation of Wander that Lou Katz had preserved in email messages which he archived.

That's the source we looked at from the 1980 archive. Langston continues:

> As I remember I came up with the idea for Wander and wrote an early version in HP Basic while I was still teaching at the Evergreen State College in Olympia, WA (that system limited names to six letters, so: WANDER, EMPIRE, CONVOY, SDRECK, GALAXY, etc.).

Consider that earlier birthday source which doesn't list Wander at all. Which makes me wonder if Langston is conflating things as the years go on.

> Then I rewrote Wander in C on Harvard's Unix V5 system shortly after our band moved to Boston in 1974. I got around to putting a copyright notice on it in 1978.

That, too, matches what we see in the 1980 archive.

> It compiles with a bit of tweaking (C compilers are a bit more persnickety now and there was a whole PSL games subroutine library available back then) but the documentation uses ancient nroff macros and will take a bit more tweaking. The worst part is that I only have the partial Aldebaran III world (a3) that I used to include in the distribution as an example. There are still one or two more people who may have those files archived.

When asked when the HP BASIC version happened, Langston specifically says:

> That was just before the band decamped to Boston so 1974, possibly even late 1973, I'm not sure.

The move to Boston is a distinct event so 1974 as a start date is definite, at least from the statements of the author. The problem being that there really is no evidence of this and it's at least possible, given the sources we've seen, that Langston was adding Wander into some of his previous work that was demonstrably from 1974 and earlier.

Anthony relates that Langston sent a file named "Wander.tgz" and this file contained source code and documentation for a 1980s release of <em>Wander</em>. It was also around this same time that Merritt found the software distribution from the Usenix 1980 conference.

Another inevitable question follows: did Wander in its 1978-80 form look like that in 1974? More specifically: how much did it change, assuming there was some previous versions? Peter says "the concept didn’t change, but implementation got better and the worlds got easier to create."

It's important to note that Peter fully admits he doesn't have a good recollection of all of the details, though, so he can't answer questions like "which features got added first" and "did anything get tweaked after the release of Adventure." What this means is that even if we get different versions of the source code, if those are absent dates, then we really can't trace the evolution to determine earlier and later vresions.

Probably the best way to verify the early state would be to somehow track down the HP BASIC version, which was never revised post-1974, according to Langston.

Peter did a very incomplete port of Crowther and Woods Adventure called advent dated at 1981. See: advent-world.zip.

So obviously this would mean post-Adventure.

Another way to frame this: was Wander distributed widely enough for Will Crowther and/or Don Woods to have had the opportunity to see it before they wrote ADVENT?

If the answer is no, then does that mean there’s something fishy going on? Surely two people couldn't independently have come up with the idea of a textual game of exploration where you navigate using compass directions?

I'm not too sure about that, hwoever. What else would you use, if not NORTH, SOUTH, EAST and WEST? Well, actually, you might use LEFT, RIGHT, FORWARD and BACK. Okay, so it is possible to make a text adventure game with a different set of navigational commands, but compass directions are probably easier for the player to use and for the programmer to implement. Also, for Will Crowther, compass directions might have been the natural choice when he was writing ADVENT because he was a caver who used a compass to map out underground cave systems in real life.

But what about Peter Langston? If he started working on Wander in or before 1974, did he implement compass directions from the beginning? We may never know – unless the earliest source code is found, which seems unlikely.

So, do we know anything else at all about the origins of Wander? Well, I did ask Peter that very question (before finally realising that I ought to leave him in peace now). His reply:

> As to Wander’s inspiration, as I was writing other games, I got to thinking about the non-deterministic non-linear story experiments I had heard of the French doing in the 1920s, where the reader made choices that determined how the story went. I figured that fairytales like Rapunzel or science fiction like the Retief stories would be a good basis for such stories and computers would be the perfect way to present them, but it would require a great deal of programming skills along with the storytelling skills. So Wander was an experiment to see if the programming part could be made easier by pre-coding the common kinds of actions and consequences. I had the vague idea that I could make it easy to use and then coax some real authors like Robert Sheckley into writing some wanders. I never got that far, of course.

A concern I have: I know that date is claimed by a lot of people. I know the author of the system "recollects" doing things in 1974 and I'm not suggesting to doubt that in a categorical sense. But historically, all that matters is tangible evidence. Do we have accounts of people playing this system in 1974? Do we have files that are dated as being created in 1974? So far all I've ever seen are things that date from 1978 (maybe 1977) up to 1980. I don't see direct, tangible evidence that the system truly pre-dates Adventure.

Jason Dyer had the following good points on that:

> I first picked up on Wander in a reference by Graham Nelson who called it a proto-adventure system in 1974. I asked but Nelson was not able to recall where he found his reference.

> Unfortunately, because the original BASIC code doesn’t survive, we do have to rely on the word of Peter Langston on this one. However, I am fairly believing because a.) he never came forward in a way that indicated he was trying to brag, we had to seek him out and he almost was puzzled people would care b.) he had very distinct life events surrounding it (a year “float” is not unusual with this sort of thing but here that would be in reverse, from 74 to 73, because he moved locations setting a hard limit) and c.) he had earlier work from 71 which does survive so we know he was actively developing.

> There is a lot of missing material out there from when programs were developed only on one mainframe. People fortunately cared about adventures enough to make lots of copies (although there are fair number of adventure variants missing), but if we take the larger set of software out there about 90%+ is gone, I’d say? We have catalogs with material we can only read about.

> Still of course possible the original Castle is buried on a backup tape somewhere. If nothing else even though the current extant material exists post-Adventure, it feels very much like a “different track” of development — the coding is radically different and the game design of a3 in particular does things that don’t appear elsewhere until 1982 or so.

So there is _possibly_ one known program that predated Adventure and featured exploration of a series of rooms using simple commands called WANDER. As the original 1974 source code is lost, it is impossible to ascertain how the program functioned at launch, and it is possible the later versions that are preserved were influenced by Adventure. Regardless, it only achieved limited distribution, and Crowther has confirmed he did not see it before creating his game.
