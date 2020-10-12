# Unnatural Triads

In practice, chord progressions are not limited to the natural triads. 
Composers are at liberty to choose whatever quality of triad, in whatever inversion, with whatever additions or alterations, at whatever point in the chromatic scale, at any time in a progression with complete disregard for conventional tonality.
The roman numeral system and Coltrane do not directly address this fact. To reiterate, we are expressing a relationship to the **current key**.

Still, we must be able to represent chords that do not belong to a key.
An example should help to understand how this works in Coltrane.
The cornerstone of tonal music, the `V-I` authentic cadence, which creates a feeling of resolution.
It is common for a composer to "target" a certain degree as if resolving to that key using what is known as a borrowed chord.
In both dorian and aeolian minor, the fifth degree is naturally minor, but we borrow `V` as if we are creating a `V-I`.
This is what would be considered a deceptive cadence, and is often found somewhere prior to an authentic cadence.
Consider: `A Dm G C` and `VI ii V I`.
Notice the `VI` chord; the sixth degree would naturally be `vi`.
This is how the Coltrane language represents a "five of two" and other borrowed chords.
A Coltrane RNA token is based on the **quality** and **degree** and can be made to describe any chord in terms of **semitones from tonic**.
To be more specific, unless the composer specifies an explicit key change, we require that chords be expressed in the context of the specified key.

For example, all 12 notes in the C Major context:

|1|2|3|4|5|6|7|8|9|10|11|12|
|-|-|-|-|-|-|-|-|-|--|--|--|
|C|C#/Db|D|D#/Eb|E|F|F#/Gb|G|G#/Ab|A|A#/Bb|B|
|`I`|`#I/bII`|`II`|`#II/bIII`|`III`|`#III/bIV`|`IV`|`V`|`#V/bVI`|`VI`|`#VI/bVII`|`VII`|

Note: The numerals above are all capital, but they could be either major or minor.