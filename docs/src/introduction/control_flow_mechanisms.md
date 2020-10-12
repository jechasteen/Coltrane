# Music's Control Flow Mechanisms

Musical language, much like programming languages, has flow from one point to another.
In the case of written music, we could express this as a rigid decision tree for which every branch of the tree is reached. 

Coltrane, however, is not rigid.
It has no specific requirement that all branches must be reached and does not expect the tree to be constant during runtime.
We could reach into the program and directly alter the values contained in the data structures of our "running" composition.

We have an entry point: the first measure. From there we proceed measure by measure until we reach a control flow statement.

## Repeats

There are two kinds of repeats that the language can express: bar line repeat and branching repeat.
A bar line repeat looks something like `||:  :||` and results in a simple loop.
A branching repeat uses the same bar line notation but has different endings, marked above the staff with numbered brackets.
A composition can have any number of repeats and any number of branches. 
Thankfully, most music can be expressed with simple control flow, but the language supports arbitrary levels of nested repeats.
If repeats are nested inside of each other, they resolve in a similar manner to parentheses, e.g. `(()(()))`
The interpreter will error if the repeats provided in the source do not resolve.

## Jumps

The language provides a jump statement that causes the control flow to jump to the specified measure, optionally an arbitrary number of times.
In musical notation this construct is known as *del signo al coda*, *del capo al fine*, etc.
If our jump takes us to a point prior to any *repeat* expression, the repeats will be reset to their original state unless specified.

Creating a *del signo al coda* requires:

|                                                              |             |
| ------------------------------------------------------------ | ----------- |
| 1. Jump that must be skipped once to activate                | *al coda*   |
| 2. Jump to a point in the progression prior to the *al coda* | *del signo* |
| 3. Target of 1                                               | *coda*      |
| 4. Target of 2                                               | *signo*     |

A jump can be set to jump any number of times, and a target will simply keep receiving it.
It could also be set to only jump on the nth pass.

## Ending

In musical notation, especially sheet music, it is simple to determine where the end is. In musical performance, the story is completely different.
During rehearsal performers will decide how many choruses to play, how many times to repeat the head, unwritten interludes, etc.
The language permits "unwritten changes" and arrangement by virtue of the code being intuitive to write.
We can parse the code again and then update the data structure while running.

A composition ends either when we run out of measures or we encounter an activated `fine` keyword.
A fine can optionally be set to activate after n passes for *al fine* jumps.
The language doesn't directly support the idea of an infinite loop, but one could simply max out the repeat count value.
The language is not concerned with the ending of the composition.
The code is parsed and then we simply run the resulting data structure through an interpreter.
The interpreter with come to a stopping point, whether that be the specified ending or some sort of error.