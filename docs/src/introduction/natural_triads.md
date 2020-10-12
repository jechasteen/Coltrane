# Natural Triads

RNA provides a method of abstracting a chord progression away from the key it was composed in. In this system, each step or degree of the scale has an associated triad that is built upon by stacking diatonic thirds. We give these steps a Roman numeral to represent the numerical degree of the scale.

For example in the key of C Major:

| Root | Roman | Spelling |
|------|-------|----------|
| C | `I`   | C E G |
| D | `ii`  | D F A |
| E | `iii` | E G B |

.. and so on. For each key, we could spell the natural chords above each step of the scale in the same way and all of them would result in the same RNA . We denote a **major triad** with upper case numerals, and a **minor triad** with lower case numerals.

The natural triads exhibit three permutations of triad:

* Major `(I, IV, V)`
* Minor `(ii, iii, iv)`
* Diminished `(vii)`

There are 1320 permutations of three notes in the western temperament, but these are by far the most important of the permutations. This will be referred to as the "quality" of the triad or chord.

The same can be done for any degree of the scale. Go to any degree and start counting from `I/i`, matching the quality of the major scale at that degree. For example this is the aeolean mode or natural minor:

| Major | Minor |
|-------|-------|
| `I`   | `III` |
| `ii`  | `iv`  |
| `iii` | `v`   |
| `IV`  | `VI`  |
| `V`   | `VII` |
| `vi`  | `i`   |
| `vii` | `ii`  |

The diminished triad that occurs naturally at the seventh degree of the major scale does not have any distinguishing feature in Coltrane; it is written in lower case numerals just like a minor triad.

> Assumption: The RNA token `vii` is always a **diminished** triad. In Coltrane, `vii` must be altered to be a natural minor: `vii^#5`

Since this may be a point of contention -- perhaps less with music theorists than with Coltrane composers -- the decision bears explanation. The system Coltrane uses is predicated upon a relationship to the major scale. The language specifically defines a relationship to, or distance from, that scale. The RNA tokens used are based upon degrees of that scale, the seventh of which is naturally diminished.

The spelling of a triad can be expressed in terms of distance in semitones from the root.

|Major|Minor|Diminished|Augmented|
|-----|-----|----------|---------|
|`[0, +4, +7]`|`[0, +3, +7]`|`[0, +3, +6]`|`[0, +3, +8]`|

These three categories form the basis of the Coltrane RNA system. 

>Assumption: we can reduce any musical composition to a series of triads from which further alterations are made.

We are building triads on the same roots, but the tonic differs.
We essentialy transform the roman numerals using a ROT-6 cipher.