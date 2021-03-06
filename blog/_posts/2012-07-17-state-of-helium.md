---
layout: blog
title: Helium release cycle and future plans
author: Scala IDE team
---

It's been a while since our last major release, and the time for Milestone 2 is near. It's time to have a look
at what's been hapening lately, and our plans for the near future.

# What's been keeping us busy

Just before ScalaDays, in April this year, we released [Helium Milestone 1][release-notes-m1], with a swath of new features
like [semantic highlighting][semantic], [implicit highlighting][implicit], a [Scala debugger][debugger] and fresh-from-the-oven [refactorings][new-refactorings]!
The reactions were overwhelmingly positive, with more than 4000 downloads until now!

We've continued working towards Milestone 2, and we've been following closely the development of Scala 2.10.0.
The next release of Scala will be a major update (macros and reflection, plus a new pattern matcher, just to name a few!), and
keeping the IDE aligned with Scala development has proven to be both essential and time consuming.
As time passed it became clear that some of our plans
won't be possible while staying compatible with 2.9, so today we're re-evaluating our roadmap and 
release schedule.

# Helium release cycle

Milestone 2 will be released end of July, and will contain all the elements in the inital plan except for
the compiler services API (a.k.a. model). The main reason is that the 2.9 presentation compiler is too different
from the 2.10 compiler, and shoving them both under the same API is too difficult. In addition, the 2.10 API
is still a moving target, and it won't stabilize before 2.10.0 is out. Any effort to target both would be 
doomed to fail.

We decided to move the model (and the dependent `Outline` view) to the next major IDE release, as trying to 
do it now would jeopardize quality and delay the good things we have even more.
In addition, Milestone 2 is the **last milestone** in Helium, and we
will work towards a **final release** with the aim to go in RC-mode when Scala 2.10.0 is released. The amount of
new features (better [Scala debugger][debugger], Find References,[ Implicit Hyperlinking][implicit-hyperlinking], 
[Type of Selection][show-type], 2.10 support, [Source generators][source-gen]) already warrants a true, stable, IDE release, with the usual quality guarantees. There is 
nothing to gain by delaying it further, and forcing people into the difficult choice of using milestones or waiting.

As planned, Helium will target both 2.9 and 2.10.

# Lithium

All the items in Milestone 3 are deferred to the next release, code-named Lithium. Lithium will target 2.10, and all new features will be targetting only 2.10 or greater (2.11 is just around the corner!). Of course, we will continue to support Helium with bugfix releases, as we did for the 2.0 release, so if you need to keep using Scala 2.9 you will still benefit from these bugfix releases.

As we get closer to the release, we'll define milestones and more fine-grained goals.

For a more detailed picture, have a look at the updated [Roadmap][roadmap] document.

# Stay tuned

The Scala IDE eco-system is growing, and we'll soon be able to show what other have been building on top of the Scala IDE in an integrated update site!

[scala]: http://www.scala-lang.org/
[release-notes-m1]: /blog/release-notes-2.1-Milestone-1.html
[changelog-scala-m5]: http://www.scala-lang.org/node/12735
[roadmap]: http://scala-ide.org/docs/dev/roadmap.html
[semantic]: http://scala-ide.org/docs/helium/features/semantic-highlighting/index.html
[implicit]: http://scala-ide.org/docs/helium/features/implicit-highlighting/index.html
[debugger]: http://scala-ide.org/docs/helium/features/scaladebugger/index.html
[new-refactorings]: http://scala-ide.org/docs/helium/index.html
[debugger]: http://scala-ide.org/docs/helium/features/scaladebugger/index.html
[implicit-hyperlinking]: http://scala-ide.org/docs/helium/features/implicit-hyperlinking/index.html
[show-type]: http://scala-ide.org/docs/helium/features/show-type.html
[source-gen]: http://scala-ide.org/docs/helium/features/source-generators/index.html