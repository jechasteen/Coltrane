# Additions and Alterations

## Additions

Chords are not limited to three notes; we can add notes above the chord in thirds (3 or 4 semitones).
The most common of these alterations is the 7th. We can continue upward to the 9, 11, and 13 before coming full circle.

>Assumption: any chord with additions -- `(9, 11, 13)` -- also contains the chord tones between the noted addition and the triad. 

For instance, a `13` chord also contains `[7, 9, 11]`.
The intended side-effect of this approach is that the language is equipped to analyze jazz compositions rather than generalized for a broader approach.
The language can be used with or without chord alterations for any tonal or non-tonal composition, it simply makes assumptions about chord spellings that are based upon the jazz idiom.

The reasoning behind this decision is simple and pragmatic: we intend to draw scales from these expressions, so the language forces you to be specific.
The "color" of the chord and scale is based upon these extension notes, so it is very important that the language is concrete in the referencing of extension notes.
Any chord can be spelled through alteration expressions, but for brevity and ergonomics we can omit any diatonic additions between the 7th and the last alteration.

## Alterations

Any note in a chord can be targeted with an alteration, whether a component of the triad or an addition.
Adding a `#` or `b` before the degree number to raise or lower it by a semitone.
The degree can be entered as any number 1-13, although `[9, 11, 13]` are preferred over `[2, 4, 6]`.
This property could be use to create tones an octave +/- 1 semitone apart.

An extreme example of alteration and dissonance: `1:IV^b5,b9,b10,#13`.