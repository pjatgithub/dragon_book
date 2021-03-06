# The Lexical-Analyzer Generator Lex

## Exercise 3.5.2

Write a Lex program that copies a file, replacing each non-empty sequence
of white space by a single blank. 

[ws.l](/ch3/3.5_the_lexical-analyzer_generator_lex/ws.l)

## Exercise 3.5.3:

Write a Lex program that copies a C program,
replacing each instance of the keyword `float` by `double`.

[f2d.l](/ch3/3.5_the_lexical-analyzer_generator_lex/f2d.l)

## Exercise 3.5.4

Write a Lex program that converts a file to "Pig latin."
Specically, assume the file is a sequence of words (groups of letters) separated by whitespace. Every time you encounter a word:

1. If the first letter is a consonant, move it to the end of the
word and then add ay.

2. If the first letter is a vowel, just add ay to the end of the word.

All nonletters are copied intact to the output. 

[pig\_latin.l](/ch3/3.5_the_lexical-analyzer_generator_lex/pig_latin.l)

## Exercise 3.5.5

In SQL, keywords and identifiers are case-insensitive.
Write a Lex program that recognizes the keywords **SELECT**, **FROM**,
and **WHERE** (in any combination of capital and lower-case letters),
and token **ID**, which for the purposes of this exercise you may take to be
any sequence of letters and digits, beginning with a letter. You need not
install identifiers in a symbol table, but tell how the "install" functiou
would differ from that described for case-sensitive identifiers as
in Fig. 3.23.

[sql.l](/ch3/3.5_the_lexical-analyzer_generator_lex/pig_latin.l)

