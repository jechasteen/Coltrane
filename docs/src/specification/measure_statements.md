# Measure Statements

A measure consists of a series of chord expressions. These chord expressions can be explicit, denoting the beginning and ending point, the triad, and any additions, but there are also methods for abbreviating them. The basic formula for a chord statment is:

```
[BeginLocation]:[Triad]^[Additions]:[EndLocation]
```

If the chord extends to the following change, `[EndLocation]` may be omitted. If there are no additions `^[Additions]` may be omittied.

`1:vii^7b5 3:III^7b5` constitutes a complete measure statement. Supposing Each chord is a quarter note, with a quarter rest in between we would write `1:vii^7b5:2 3:III^7b5:4`. Please note that the `[EndLocation]` component is not inclusive, the chord ends *on* that beat or subdivision.

## Location Component

The location component can be expressed as an integer (if the note begins/ends on the beat) or a float (if the note begins/ends on an off beat). Typical values are increments of 0.25, 0.33, 0.125, etc. These are divisions of the note expressed as a float. For example, a dotted quarter note: `1:V^7b5:2.5`.

## Triad Component

This is the RNA portion of the measure statement. The options here are relatively limited. It consists of a roman numeral between 1 and 7, with an optional flat or sharp alteration prefix. For example `bVII` or `iv`. Capital letters denotes a major triad, lower case a minor triad.

>There is an exception in the case of the literal `vii`, which is a diminished chord diatonically. Otherwise, we denote a diminished chord with a `b5` alteration as in `V7b5`

If there is a `b` or `#` prefix, the root is lowered or raised by one semitone, respectively. There is no `dd` or `##` (double flat/sharp). In that instance, the next lower step should be used. The intent is to represent the notes from the perspective of the key center. If there is a triad based upon a natural step of the scale, it should be preferred over a flatted or sharped triad.

There are 12 tones total in the western temperament.

```
1     2     3     4     5     6     7     8     9     10    11    12
C     C#/Db D     D#/Eb E     F     F#/Gb G     G#/Ab A     A#/Bb B
I           II          III   IV          V           VI          VII
```

For each tone not in the diatonic scale, the root can be written using either a flat or sharp prefix. Again, it is typical to decide this based on the current key center. For flat keys, prefer the flat prefix and for sharp keys, prefer the sharp prefix. Both chords are otherwise equivalent.