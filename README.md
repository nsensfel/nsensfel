## Welcome to my GitHub profile
I am currently completing a PhD on the analysis of interference caused by cache coherence in COTS multi-cores, at ONERA.

I am currently looking for a career opportunity in software development for projects in the EU space industry. Here's [my LinkedIn account](https://www.linkedin.com/in/nathana%C3%ABl-sensfelder-24485b1a1/), and [my personal website](https://noot-noot.org).

The collection of repositories here is mostly restricted to projects I do in my spare time. These do not generally involve anything related to embedded systems programing, and this is on purpose, to void any risk of conflict with my actual work.

Below is a list of projects I am currently working on. Do not be fooled if GitHub indicates that the last commit was made a while back: it doesn't account for branches, and I tend to make very long branches which I merge back into `master` only when I deem the branch's feature has been fully completed.

### ![Tacticians Online](https://noot-noot.org/to-logo.svg)
Multiplayer browser game.

[Server](https://github.com/nsensfel/tacticians-server) coded in Erlang, [client](https://github.com/nsensfel/tacticians-client) coded in Elm. Playable demo available at https://tacticians.online, except when my dying router has a breakdown.

Creating a multiplayer game is always a nice, endless source of challenges. It might not get down to low-level programming, but it does involve tackling issues from a wide range of programming fields that complement those I handle at work, be it networking, database management (see my Ataxia project), GUI, procedural asset creation, multi-threading, web development, or system administration.

While this is a pet project, I do take it seriously and learn about legal procedures/obligations in order to ensure its success, be it data privacy laws or trademarks (which I registered in both the EU and the US).

**Website:** https://tacticians.online

**Related repositories:** [client](https://github.com/nsensfel/tacticians-client), [server](https://github.com/nsensfel/tacticians-client), [data set](https://github.com/nsensfel/tacticians-data), [browser plugin](https://github.com/nsensfel/tacticians-extension), [database management system](https://github.com/nsensfel/ataxia), [misc. design stuff](https://github.com/nsensfel/tacticians-design), [narrative scripting](https://github.com/nsensfel/tonkadur).

____
### ![Tonkadur](https://tonkadur.of.tacticians.online/images/tonkadur_logo_black_as_path.svg)
Narrative scripting language.

Coded in Java. Still in early stages.

This is an alternative to Inkle's Ink and Yarn Spinner: a language allowing you to easily describe the narrative of a game, which is then interpreted by the game engine to present the player with scenes, characters, dialogues and reply options.

Tonkadur distinguishes itself by not being a single language, but two: Fate and Wyrd.

Fate is what one would expect for narrative scripting (with some extra bells and whistles, of course). It's a strongly typed declarative language with clear LISP inspirations. The objective for Fate is to provide the user with as much tool as they need to concisely describe their narrative, while also providing tools to greatly reduce the risks of mistake. It goes beyond what is usually available for this type of language, with reference manipulation, loops, and structures.

Wyrd is closer to a RISC assembly language. Very few instructions are available when writing in Wyrd, and it's a good thing: the objective here is to make it extremely easy to add support for Wyrd to an existing engine. Tonkadur simply compiles Fate to Wyrd, allowing users to have access to a very large array of instructions when writing while not having to worry about the implied complexity this adds to properly supporting the language.

Of course, this comes with a price: performance is not as good as if Fate was interpreted directly. However, in the context of narrative scripting, WCET is not exactly considered a critical factor.

This project is meant to be used in Tacticians Online, but as with Ataxia, it is completely separate and can be used by anyone.

**Website:** https://tonkadur.of.tacticians.online/

**Related repositories:** [main repository](https://github.com/nsensfel/tonkadur), [demo engine for Python 3](https://github.com/nsensfel/tonkadur-python-interpreter).

____
### Ataxia
Distributed NoSQL database for Erlang.

Coded in Erlang. Still missing the most important features.

This is meant to be the database interface for Tacticians Online. The targeted environment is that of a large collection of heterogeneous small servers (e.g. some cheap ARM development boards) interconnected by some pretty basic Ethernet (so bandwidth usage is the main scalability limiter). The whole database has to be kept consistent even when a transaction fails (well, the whole ACID properties are meant to be verified) as well as when a node goes down (those are cheap boards, after all).

It uses its own language for queries, where the user basically builds the abstract syntax tree of a function to either select of modify a particular item.

This project is still in its early stages of development. Indeed, the whole "distributed" and "fault-tolerance" parts are still missing. I do already use it for Tacticians Online though, with it running on a single node with all the limitations that I expect will end up being required in its final form (e.g. each query can only access a single entry).

**Website:** Not available yet.

**Related repositories:** [main repository](https://github.com/nsensfel/ataxia)

____
### relabsd

Daemon that turns your input devices into joysticks by converting relative axes into absolute ones.
It was originally intended as a tool to allow the use of the SpaceNavigator (a 3d mouse, which is definitely an oddity) as a 6 directional joystick (something supported by every input library), but I made it generic enough that it can be used for other purposes.

**Website:** Not available yet.

**Related repositories:** [main repository](https://github.com/nsensfel/relabsd)
