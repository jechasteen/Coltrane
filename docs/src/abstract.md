# Abstract

This paper describes a language for expressing the abstracted chord progression and linear control flow of musical compositions.
Coltrane is written in a simple, human-readable plain text format using [roman numeral analysis (RNA)](https://en.wikipedia.org/wiki/Roman_numeral_analysis) tokens and control flow structures.
Melodic content is beyond the scope of the language.

The ideas behind Coltrane -- RNA and chord alteration/augmentation -- are well established music theory.
However, there is [some disagreement](https://xkcd.com/927/) among theorists as to what can and should be expressed in the analysis and how.
A computer requires the programmer to tell it exactly what to do.
A computer makes no mistakes, as the saying goes.
This unfortunately means that we must make decisions because the computer can't, at least not yet.
It would be burdensome and error-prone to support the parsing of multiple RNA styles, therefore there can only be one set of rules.
This, of course, does not preclude future rule additions and/or alterations.
For instance, support could be added for two syntactically different ways to write the same chord expression.

Although there is a wealth of jazz education literature in the form of method books, etudes, and play-a-longs, there is yet an opportunity to further advance pedagogy with computing power.
The computer can do some of the thinking, which leaves more time for the woodshed.
Developers could theoretically use the language interpreter to create an infinite number of exercises based on a chord progression!

John Coltrane, for the uninitiated, was a saxophonist who they say practiced 12 hours a day and was 20 feet tall.
The motivation behind the development of this language is to help us to find new relationships between chords and musical lines **by playing our  instruments**.