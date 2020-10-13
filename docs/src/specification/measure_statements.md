# Measure Statements and Chord Expressions

A measure statement consists of a series of chord expressions.
These chord expressions can be explicit, denoting the beginning and ending point, the triad, and any additions, but there are also methods for abbreviating them.

The basic formula for a chord statement is:

```
[BeginLocation:][Triad][^Additions][:EndLocation]
```

If the chord extends to the following change, `[:EndLocation]` may be omitted. If there are no additions `[^Additions]` may be omitted.

For example, `1:vii^7b5 3:III^7b5` constitutes a complete measure statement.
Supposing each chord is a quarter note, with a quarter rest in between we would write `1:vii^7b5:2 3:III^7b5:4`.
Please note that the `[EndLocation]` component is not inclusive, the chord ends *on* that beat or subdivision.
To make a rest or no chord (NC), leave a gap between one chord expression's end and the next one's start.

If a statement begins with a chord expression it must contain only chord expressions.

## Chord Expressions

### Start and End Component (aka location)

A chord's location can be expressed as an integer if the note begins/ends on the beat or a float if the note begins/ends on a subdivision of the beat.
These are divisions of the note expressed as a float. For example, a dotted quarter note: `1:V^7b5:2.5`.

For reference, the following table shows common float values:

| Name           | Float |
| -------------- | ----- |
| 𝅘𝅥𝅯 16th triplet | 0.167 |
| 𝅘𝅥𝅯 16th         | 0.25  |
| 𝅘𝅥𝅮 8th triplet  | 0.33  |
| 𝅘𝅥𝅮 8th          | 0.5   |
| 𝅘𝅥𝅯𝅭 dotted 16th  | 0.375 |
| 𝅘𝅥𝅮𝅭 dotted 8th   | 0.75  |

Off-beat chords are not very common, even in jazz, beyond the 8th note.
A 2-bar excerpt from Wayne Shorter's "Armageddon" shows a common off-beat rhythm:

```
$ Key is not marked, assuming B7 -> E7 = E mixolydian
$ :: means "continue last chord for a full measure"
1:I^7 2.5:bII^7 4.5:IV^7#11
::
```

Two chords can overlap; the second starts at the same location as the end of the first.
That is, you can explicitly state the end location to be the same as the next chord, but it optional.
It would be the same result to omit it.

Chords can span the bar line, as shown in the example above.
If the chord carries over the bar  line, but is not a full measure chord, simply add the next chord, e.g. `:: 3:V^7`

If a chord is valid for the entire measure, simply write the triad and additions omitting start and end values.
For example: `V^7b5` or `ii^7`

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

### Additions and Alterations

### Inversions

### Slash Chords

### Superimposed Chords