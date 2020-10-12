# Music's Control Flow Mechanisms

Musical language, much like programming languags, has flow from one point to another. It can be expressed as a flow chart, we can visualize the branching and decision making tree. In the case of music, we express this as a rigid decision tree for which every branch of the tree is reached. 

The language, however is not rigid. It has no specific requirement that all branches must be reached and does not expect the tree to be constant during runtime. We could reach into the running code and directly alter the values contained in the data structures of our "running" composition.

We have an entry point: the first measure. From there we proceed measure by measure until we reach a control flow statement.

## Repeats

There are two kinds of repeats that the language can express: barline repeat and branching repeat. In musical symbols the barline repeat looks something like `||:  :||`. A branching repeat uses barline notation and has different endings, marked above the staff with a numbered bracket. A composition can have any number of repeats, with any number of branches. Thankfully, most music can be expressed with simple control flow, but the language supports arbitrary levels of nested repeats. The interpreter will error if the repeats provided in the source do not resolve.

## Jumps

The language provides a jump statement that causes the control flow to jump to the specified measure, optionally an arbitrary number of times. In musical notation this construct is known as "del signo al coda", "del capo al fine", etc. If our jump takes us to a point prior to any *repeat* expression, the repeats will be reset to their original state unless specified.

## Ending

In musical notation, especially sheet music, it is simple to determine where the end is. In musical performance, the story is completely different. During rehearsal performers will decide how many choruses to play, how many times to repeat the head, unwritten interludes, etc. The language permits "unwritten changes" and arrangement by virtue of the code being intuitive to write. We can parse the code again and then update the data structure while running.

A composition ends either when we run out of measures or we encounter an activated `fine` keyword. The language doesn't directly support the idea of an infinite loop, but one could simply max out the repeat count value. The language is not concerned with the ending of the composition. The code is parsed and then we simply run the resulting data structure through an interpreter. The interpreter with come to a stopping point, whether that be the specified ending or some sort of error.