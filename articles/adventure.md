# The Crowther and Woods Adventure

This one has a bit of a tangled history, but it's an easy start to that history. Sometime in 1975, a guy named Will Crowther wrote a game called "Adventure" which was then expanded by another guy named Don Woods. The original version of this game, abandoned by Crowther in early 1976, was thought to be lost forever until it was unearthed in 2007. We can reconstruct some of the history from these recovered sources.

## The Initial History

Let's first frame the history.

Crowther was an active rock climber and caver, as was his wife, Patricia, who gained fame in caving communities in 1972. She did so by navigating a tiny, narrow passageway to prove that Kentucky's Flint Ridge Cave system connected to the Mammoth Cave, making it the largest cave complex in the world. Crowther integrated his caving with his computer work by spending evenings at his employer, Bolt Beranek and Newman, plotting out caving routes on a mainframe.

From an interview of unknown provenance, conducted in March 1994, Crowther says this about Adventure:

> This was related to the divorce ... and I was feeling kind of lonely and I wanted to write a game for my kids. Meanwhile, we had been playing Dragons & Dungeons game. You know, these role model, role playing games at the Dave Walden's house, and so I thought, "Gee, I'd make a computer version of the Dragons & Dungeon game," and that turned out to be Adventure. I happened to write it in Fortran which was quite portable. And I wrote the silly thing and I left it in a directory on a machine here at BB&N and then left.

will-crowther-interview-1994.pdf

Crowther developed a series of rooms based on the layout of the Colossal Cave in the Bedquilt Section of the Mammoth Cave complex and populated it with five treasures to collect, an ax-wielding dwarf that wandered the labyrinth, and three puzzles solvable by finding items within the caverns and using them in the right place and manner to proceed.

As computer terminals capable of more than character-based graphics were still rare in the mid-1970s, Crowther's game was entirely text-based. Each room featured a description of the environment and allowed the player to interact with certain objects by typing nouns and verbs into a text parser.

Crowther wrote his game in FORTRAN on a DEC PDP-10 computer, a mainframe released in 1966 that gained popularity in the 1970s due to its time-sharing operating system, TOPS-10. Due to filename length restrictions, he named the game ADVENT. It also went by "Colossal Cave" after the location where the game takes place. It has gone down in history as "Adventure."

### The Parser Idea

The fact that the game used a text parser is now something we take for granted, but it's an interesting development to consider in terms of why Crowther went with that interface.

Because the game he was developing was created for use by his daughters rather than fellow computer programmers, Crowther used plain language commands such as "GO SOUTH" and "GET LAMP" rather than the more complex inputs usually required to accomplish anything on a computer.

Contrast Adventure's limited parser with the one in, for example, ELIZA. A difference, however, is that ELIZA didn't have a world model that it had to sync up with. Then again, there wasn't much of a "world model" in the original Adventure.

So now let's get into the history a little more by considering some sources.

## Gathering Sources

One of the major sources of information for "Adventure" is ["Somewhere Nearby is Colossal Cave: Examining Will Crowther's Original 'Adventure' in Code and in Kentucky"](http://www.digitalhumanities.org/dhq/vol/001/2/000009/000009.html) by Dennis Jerz.

adventure-dennis-jerz.pdf

Important parts are stated in the abstract:

> This paper analyzes previously unpublished files recovered from a backup of Woods's student account at Stanford.

So that tells us we're dealing with some primary materials. The owner of the “student account” refers to the aforementioned Don Woods, who plays an important role in the history of this game. Also stated in the abstract:

> New interviews with Crowther, Woods, and their associates (particularly members of Crowther's family) provide new insights on the precise nature of Woods's significant contributions.

Once again, that tells us we're dealing with the primary sources.

The game's timing matters here from a historical chronology perspective. Interviews with Crowther and his family members – sister, two children, and ex-wife – all confirm that the game was created shortly after Crowther’s divorce, which they say happened in mid-1975. Crowther’s sister, Betty Bloom, recalls spending her sabbatical from school with Crowther when he created the game and has stated that she was a regular playtester. According to Bloom’s records, that sabbatical took place during the academic year of 1975 to 76.

In separate telephone interviews, Crowther’s children – Sandy (born in 1967) and Laura (born in 1970) – recall being eight and “less than six,” respectively, when they first played the game. This was during a school vacation when they were staying with their father. None of the family remembers which school vacations were involved. Betty Bloom and Sandy both indicate Laura had already turned six, which would place the creation of “Adventure” after Laura's sixth birthday, January of 1976.

From Jerz’s paper:

> All Crowther family testimony is consistent with the 1975-76 date range. Responding to a direct request via e-mail, Crowther (in 2001) dated his original "Adventure" to 1975, "give or take a year."

John Gilbert, one of Don Woods’ Stanford classmates, is on the record stating “I’m pretty certain it was between October and December 1975 when Don and I first ran across it,” referring to the original “Adventure.” This supports Laura’s memory of being “less than six” and thus makes a plausible case for 1975.

That brings us to Don Woods. In [an interview](https://www.avventuretestuali.com/interviste/woods-eng/), Woods recounts coming across the game:

> I don’t recall the exact day, but it was early in 1976, perhaps March or April. I was a graduate student in the Computer Science department at Stanford, and overheard another student talking about a game he had found on the Stanford Medical Center's computer. I had him fetch me a copy so I could try it on the Sail computer.

The “Sail computer” here likely refers to a Stanford Artificial Intelligence Laboratory computer.

As some of the history has it, sometime before 11 March 1977, Woods contacted Crowther, who gave him access to the source code. By 23 March, we see in Woods’ records a version with some twenty additional lines of code – effectively a low-level subroutine that Woods supplied to get the source to compile.

A 31 March 1977 set of source files again shows only minor tweaks. The evidence demonstrates Woods was working on Crowther’s source code during March, but we see no evidence of what would later be some substantive creative expansions.

In the previously mentioned interview, Crowther says that after he stored the game at BB&N he:

> Went off to go to Alaska and wound up after that working at Xerox.

When asked about how long he was there, he says:

> Oh, just a month or so.

Now, here’s what’s interesting and how Crowther describes the context of that trip:

> Meanwhile, a guy named Don Woods from Stanford, who was groping around looking at interesting things wherever he could find them, found my directory. Found this thing. Tried it out. Thought it was neat. Grabbed the sources. Doubled its size and spread it all over the country. So when I came back from Alaska, people were playing it everywhere.

What this suggests is that Woods must have been very busy during April. By mid-May, hackers at MIT had noticed the game. After they solved it, a guy named Tim Anderson said that "the true lunatics began to think about how they could do it better." Anderson is relevant because, by June, what would become “Zork” had already taken a recognizable form.

It sounds like Woods produced a 250-point version on his way to finalizing a 350-point version several months later. On 19 March 1996, in [a newsgroup chat](https://groups.google.com/g/alt.folklore.computers/c/mMo5knCw_Zk/m/GV-US5KEDBsJ), John Everett has this recollection:

> My best recollection is that ADVENT.EXE first appeared on the PDP-10s at ADP (the old First Data in Waltham, Mass.) in 1977. It was an incomplete version which only had about 250 points worth of treasure. I seem to recall that there was nothing past the troll bridge but an 'under construction' sign or some such. I believe our copy came from WPI, but word at the time was it was developed at Stanford. Two or three months later we got the full 350 point game.

So the way the story normally has it is that Woods came across the source code in 1977 and coded the "new Adventure" game to completion, with a maximum score of 350 points obtained by finding all the treasures and winning the endgame.

This is the version of the game that, in particular, came to the attention of Tim Anderson, Marc Blank, Bruce Daniels, and Dave Lebling. That’s relevant as they were the creators of Zork. However, as stated earlier, the first Crowther/Woods version didn’t go up to 350 points but rather 250.

In 2014, we got the [GDC 2014 - Zork Post-Mortem](https://adventuregamers.com/articles/view/26224). It shows a map that Dave Lebling drew.

adv-lebling-map-001.jpg

A close examination shows that the usual exit southwest of the Hall of the Mountain King, which led to the dragon, was absent. It’s also possible to spot something in the southwest corner:

adv-lebling-map-002.jpg

The chasm section of the map is missing, and the portion of the map is marked with an under construction sign. That consequently means this is a map of the first release of the Crowther/Woods "Adventure," essentially showing the state of the game as it was transitioning from the Crowther version to the full Woods version. Also very relevant is that this is the version Lebling played before starting the creation of Zork.

adv-lebling-full-map.jpg

It's worth noting that there aren’t a lot of differences here, other than the disconnect with the Hall of the Mountain King and that the maze of passages is absent. If you slice away the two treasures past the chasm (the golden chain and the spices) and cut the endgame (it also doesn’t show on the map), you get around 244 points. This is quite close to Everett's recollection of approximately 250 points.
