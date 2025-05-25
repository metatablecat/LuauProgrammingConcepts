# Motivations

I wanted to outline my motivations with this repository, this is **NOT** the foreword chapter, but just my initial motivations.

The main motivation of this book is to provide a resource to people looking to dive into Luau, either for Roblox, for some other usage (ie Lune), or
modding a game like Farming Simulator 25, which uses Luau, which is cool. Another goal was to hopefully get parts of this book on Roblox's creator docs,
as the current Luau documentation there is a bit fragmented. (and also misses a lot of stuff with Luau).

The book wont focus on any domain (excluding a few references to Roblox in a possible userdata section), since it would be better to teach the syntax of
Luau itself, instead of focusing on a single implementation of Luau.

Potentially in the future, a chapter could also be dedicated to the typechecking syntax, but due to Roblox constantly evolving this part of Luau, it would
be silly to include it for the time being, until its more concretely defined.

## Why not just read a Lua book?

The reason I want to do this rather than forwarding people to a Lua 5.1 book is that Lua and Luau have quite a few differences that set them apart,
it is true that most Lua 5.1 code will run under Luau, but theres a lot of stuff that *wont*, and theres stuff in Luau that wont run in Lua 5.1. The
differences might not be as notable as C/C++, for example, but in my opinion, the differences are notable enough to warrant their own book.

Some notable things in Luau that aren't in 5.x:

* Generalised iteration, being able to iterate by using `in` on a table directly with `__iter`
* `continue` statement
* Memory buffers with the buffer library

Looking at the current RFCs on Luau, Luau continues to drift away from Lua 5.x cross-compatibility with the addition of native vectors, and removing,
to be fair, low-level components, like `__gc`, most of the `dbeug` library and changing how `__eq` works. Luau ports features from each major version
of Luau, but chooses to omit things that hurt cross-compat, bitwise operators is a good example here.

Until it was open-sourced in late 2021, Luau was a DSL reserved only for Roblox, but now that its been opened up and general tooling built around it 
is starting to get built, it would be useful to have a book that targets this domain specifically.

The Luau website outlines what 5.x code wont run in Luau, but it'd be better if we had a book that just ignored 5.x stuff not included in Luau, and
instead focused on Luau directly.
