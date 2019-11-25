# Documentation Guidelines

This guideline describes best practices for code documentation in Polypheny.

## Language
The documentation must be written in English. Please write in simple and concise sentences (it is not a poem).


## What to document

> You shouldn't document what the code is doing, but you should document why it's doing it.

The purpose of code documentation is to allow other programmers to understand quickly what an element in the code is doing. 
If the purpose of piece of code is not obvious comment *why* it is required. The _why_ is often more important than the _how_!


## Do not comment the obvious
Do not write comments about obvious things. Remember that the documentation has to be maintained as well.


## Write better code
Self-explanatory code is always the better documentation! Therefore, if a comment can be avoided by renaming and/or refactoring the code, this is always the preferred approach. 

Nevertheless, this is should not be seen as an excuse for writing no comments. While, meaningful names can avoid many comments on _how_ things are working, there are constructs which are obscure by its own nature (DateTime formatters, RegExp, ...). Furthermore, also meaningful names do often not express the purpose of the code. 