# JavaScript: Crypto Square

Implement the classic method for composing secret messages called a square code.

Write a program that, given an English text, outputs the encoded version
of that text.

First, the input is normalized: the spaces and punctuation are removed
from the English text and the message is downcased.

Then, the normalized characters are broken into rows.  These rows can be
regarded as forming a rectangle when printed with intervening newlines.

For example, the sentence

> If man was meant to stay on the ground, god would have given us roots.

is normalized to:

> ifmanwasmeanttostayonthegroundgodwouldhavegivenusroots

The plaintext should be organized in to a rectangle.  The size of the
rectangle (`r x c`) should be decided by the length of the message,
such that `c >= r` and `c - r <= 1`, where `c` is the number of columns
and `r` is the number of rows.

Our normalized text is 54 characters long, dictating a rectangle with
`c = 8` and `r = 7`:

```plain
ifmanwas
meanttos
tayonthe
groundgo
dwouldha
vegivenu
sroots
```

The coded message is obtained by reading down the columns going left to
right.

The message above is coded as:

```plain
imtgdvsfearwermayoogoanouuiontnnlvtwttddesaohghnsseoau
```

Output the encoded text in chunks.  Phrases that fill perfect squares
`(r X r)` should be output in `r`-length chunks separated by spaces.
Imperfect squares will have `n` empty spaces.  Those spaces should be distributed evenly across the last `n` rows.

```plain
imtgdvs fearwer mayoogo anouuio ntnnlvt wttddes aohghn sseoau
```

Notice that were we to stack these, we could visually decode the
cyphertext back in to the original message:

```plain
imtgdvs
fearwer
mayoogo
anouuio
ntnnlvt
wttddes
aohghn
sseoau
```

These tests use jasmine-node, which is a testing framework written for Node.js.

You will need:

* Node.js
* The Node Package Manager (NPM)
* jasmine-node

You can install both Node.js and NPM with a download from nodejs.org: https://nodejs.org/en/download

Use NPM to install jasmine-node:

    npm install jasmine-node -g

To work on an exercise, change to the directory of the exercise:

    cd hello-world

This contains the files for the exercise.

    .
    ├── README.md
    └── hello-world.spec.js

To run a test file, pass it as an argument to the `jasmine-node` command:

    jasmine-node hello-world.spec.js

## Source

J Dalbey's Programming Practice problems [http://users.csc.calpoly.edu/~jdalbey/103/Projects/ProgrammingPractice.html](http://users.csc.calpoly.edu/~jdalbey/103/Projects/ProgrammingPractice.html)

This exercise is from the [JavaScript][javascript] track on [Exercism][exercism]

[exercism]: http://exercism.io
[javascript]: http://exercism.io/languages/javascript



