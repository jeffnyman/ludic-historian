# Wumpus

The exact origins of Hunt the Wumpus are hard to pin down. Most sources say Gregory Yob created it while a student at the University of Massachusetts at Dartmouth in 1972.

Some people remember seeing Hunt the Wumpus on time sharing systems in 1972 and some say that Yob wrote it on the Dartmouth Time Sharing System (DTSS). But this is most likely a bit of confusion because the Dartmouth in DTSS referred to Dartmouth College in Hanover, New Hampshire, not the University of Massachusetts at Dartmouth. On the other hand, some sources say that Yob created Hunt the Wumpus at Dartmouth College, not the University of Massachusetts at Dartmouth.

But Gregory Yob wrote in Creative Computing that he first envisioned Hunt the Wumpus in California, not Massachusetts. According to Yob, it all began when he visited the People’s Computer Center at Menlo Park, California (probably in 1973). The People’s Computer Center (also known as PCC) was the brainchild of Bob Albrecht.

Bob Albrecht created three different entities that were abbreviated PCC, making some accounts a bit confusing:

- The People’s Computer Center, the computer storefront in Menlo Park, California
- The People’s Computer Company, a computer newsletter which ran from 1972 to 1977 (and later as People’s Computers and Recreational COMPUTING) and spawned Dr. Dobb’s Journal
- The People’s Computer Company, a non-profit organization

Created in the late 1960’s, it was one of the first places in the world where ordinary people could stop by and use computers. Not surprisingly, people liked to play games at the Center, and three popular games in 1973 were Hurkle, Snark, and Mugwump. All three games involved locating something in a 10 by 10 grid, a concept which Yob disliked.

> Two years ago I happened by People's Computer Company (PCC) and saw some of their computer games such as Hurkle, Snark, and Mugwump. My reaction was: "EECH!!" Each of these games was based on a 10 x 10 grid in Cartesian co-ordinates and three of them was too much for me. I started to think along the lines of: "There has to be a hide and seek computer game without that (exp. deleted) grid!!" In fact, why not a topological computer game - Imagine a set of points connected in some way and the player moves about the set via the interconnections.

That's from his Creative Computing article in Sep/Oct 1975.
creative-computing-v01n05-sep-oct-1975

Rather than use a simple grid, he decided to base Hunt the Wumpus on a dodecahedron.

wumpus1-dodecaedron.gif
wumpus1-squashed-dodecahedron.jpg

The same Creative Computing article includes a transcript with maps that look a lot like the “tree branching” of Caves.

wumpus1-caves-like-design-001.jpg
wumpus1-caves-like-design-002.jpg

Gregory wrote this in 2005:

> > 71 was a long time ago. Teletypes were the main interactive terminal, lucky people had “glass teletypes” which could hold 80 columns by 40 lines of text. games? nothing much – blackjack. or PCC’s litle edugames like mugwump and hurkle which were very simpleminded.

> About the time I wrote Wumpus, a version of StarTrek came along, it wasn’t bad. Versions of aventure for CP/M personal computers came along 5 years later. You know, like using a pencil in pre calculator days, duh.

This is a little bit odd becasue Star Trek came out in 1971. Mugwump and Hurkle weren’t even written until 1973 — and they were based on a game from 1972.

But consider how this appeared in the September 1973 issue of PCC,

pcc-genealogy-of-games.jpg

There Wumpus appears to be in the lineage of Caves.

Yet Yob never mentions it. Deliberate?

Keep in mind the Creative Computing article was 1975 and so the question is: was there enough motivation in 1975 to be revisionist about the connection with Caves? Probably not.

We do know that Robert Culley wrote in a letter to PCC in January of 1974:

> Your 'WUMPO' appears to be identical to a program I tried at the National Computer Conference here in New York last June. It was included in the catalogs of Basic Timesharing Inc. I don't know how long it took the Wumpus to cross the U.S., but as you can see the Wumpus proliferation rate is quite high.

It's hard to tell since we don't know what game is being compared to. Given that Wumpus, at least to our historical knowledge, is first mentioned in late 1973, that would suggest some quick proliferation enough so that there was enough popularity to it to not have any reason to exclude Caves.

After finishing Hunt the Wumpus, Yob gave it to the People’s Computer Center. The next he heard of the game was one month later at a conference in Stanford (according to the Creative Computing 1975 article):

> PCC had a few terminals running in a conference room and I dropped by. To my vast surprise, all of the terminals were running Wumpus and scraps of paper on the floor with scrawled numbers and lines testified that much dedicated Wumpus-hunting was in progress. I had spawned a hit computer game!!!

Hunt the Wumpus was published in the November 1973 and the January 1975 issues of the People’s Computer Company newsletter. It also appeared in the September/October 1975 issue of Creative Computing. Hunt the Wumpus was a staple of BASIC game collections, appearing “officially” in books by the People’s Computer Company and Creative Computing and in modified versions in several other books.

## Ludic Experience

His game featured a cave with twenty rooms with connections between the rooms. Each room had three tunnels to other rooms. The goal was to use a “crooked arrow” to shoot the Wumpus, a creature which was in one of the rooms. The Wumpus remained in the same room unless you moved into his room or fired an arrow. If you did, there was a 75% chance that he would move to another room. If that happened to be your room, the game was over. To complicate matters, two rooms had deadly bottomless pits and two rooms had Superbats which would move you to a random room. (Yob described Superbats as a “sort of rapid transit system gone a little batty.") The Wumpus was unaffected by both pits and Superbats.

The twenty rooms are arranged in a "squashed dodecahedron" shape. You have six arrows, and your goal is to hit the Wumpus with an arrow. In addition to the Wumpus itself being hazardous (it eats you if it is in the same room as you) there are bats which can randomly drop you in a new room and bottomless pits that can drop you to your death. If you are in a room adjacent to bats, you will get the message "BATS NEARBY!" Next to a bottomless pit, the game will say "I FEEL A DRAFT". Next to the Wumpus, "I SMELL A WUMPUS."

If you play carefully (and don't get unlucky) it's possible to chart via deduction where hazards are without stepping into them, and shooting the Wumpus without missing. That "and don't get unlucky" part is very real. For example, your game can start like this:

```
I FEEL A DRAFT
BATS NEARBY!
YOU ARE IN ROOM 1
TUNNELS LEAD TO 2 5 8
```

So basically only one of the rooms you can move to is safe and you really have no way of determining which is which. That said, assuming you don't get a situation like that, if you play carefully (and don’t get unlucky) it’s possible to chart via deduction where hazards are without stepping into them, and shooting the Wumpus without missing.

Wumpus represents a radical change in perspective from games like Hurkle. While the player viewed those games from on-high, Wumpus places her in its storyworld. You are there, creeping from room to room in the darkness. Wumpus offers the merest stub of a narrative, but that stub combined with the switch from a third-person to a first-person perspective gives it a very different feel from Hurkle and its companions. Those games feel like abstractions; Wumpus is a much more immersive experience. It wasn't quite the first game to put its player inside a storyworld &mdash; The Oregon Trail, at least, preceded Wumpus by about a year and was possessed of a much more full-bodied narrative in addition &mdash; but it's nevertheless a significant departure from the norm of its time.

Wumpus is a prototype version of the system of geography that is still with IF today: a set of discrete, self-contained rooms linked together by connectors the player can use to pass from one to another. Compass directions are not yet here, but the rest of the scheme is. Wumpus is all about mapping.

<em>Hunt the Wumpus</em> became the most influential game out of PCC. It showed up not only in derivative versions (like <em>Treasure Hunt</em>) but in adventure games like Zork (referencing the superbats in the 1980 edition), Adventure 501 (where the Wumpus is an actual enemy you must run away from), and Hunter, In Darkness (an Andrew Plotkin game from 1999 which could be considered a remake).

Let'c consider a transcript:

I feel a draft!
You are in room 10.
Tunnels lead to: 2 9 11

I'm a bit unluckly here. I have no idea which room may contain the pit.
I have to guess.

--> Where to? 2

Bats nearby!
You are in room 2.
Tunnels lead to: 1 3 10

Sheesh. Well, I know 10 is safe because I just came from there.
Either 9 or 11 could contain a bottomless pit.
Either 1 or 3 could contain the bats.

--> Where to? 3

You are in room 3.
Tunnels lead to: 2 4 12

Whew. That worked out.

So:
10 safe.
2 safe.
3 safe.

No apparent immediate hazards here so either 4 or 12 should be good.

--> Where to? 4

You are in room 4.
Tunnels lead to 3 5 14

So:
10 safe.
2 safe.
3 safe.
4 safe.

--> Where to? 5

I smell a wumpus!
Bats nearby!
You are in room 5.
Tunnels lead to 1 4 6

I know the Wumpus can't be in 4 because that's safe.
I believe the bats must be in 1 because I got that message earlier.
So the Wumpus is likely in 6.

Shoot or Move (S/M)? s
Number of Rooms (1-5)? 1
Room number? 6
Aha! You got the Wumpus!

Hee hee he - The Wumpus'll getcha next time!!

Hunt the Wumpus having been originally written in HP Time-Shared BASIC. I was able to locate it along with its monster-hunting predecessors on tapes preserved by Bob Brown and Michael Gemeny of the HP-2000 Yahoo! Group. Its BASIC code was first published in a mid-1973 issue of the People's Computer Company magazine, and later appeared in the October, 1975, issue of Creative Computing. The program that appeared there is almost identical to that which we found on the tape, with the only notable difference being some REM and PRINT statements found in the printed version that attribute it to Yob and plug Wumpus 2 and Wumpus 3, two sequels Yob had written by that time.

wumpus1-creative-computing.bas
