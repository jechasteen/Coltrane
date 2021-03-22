# Data Structure

The Coltrane library takes a plain text file that contains a section marked `[changes]`, which is parsed to create a tree data structure.
Each leaf of the tree represents a customized version of the same generic object.

The common functions for this generic object are

* `Option(NextObject)`
* `Option(PreviousObject)`
* `Do()` function/callbacks
    
    The do function can make changes to the underlying data structure. e.g. to remove/alter a branch after a certain number of passes.

## Built-in Components

### Chord Expression

### Jump

### 