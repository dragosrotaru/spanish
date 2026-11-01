# spanish

An unfinished attempt to model Spanish grammar in TypeScript, written while I was learning the language. It uses TypeScript types and annotated data to describe parts of speech, gender, articles, pronouns, tenses and moods.

> Archived: no longer maintained. Kept for reference.

## What it is

Part study notes, part data model. Each file in `src/grammar/` covers one area of the grammar. A long explanatory comment comes first, followed by types and example data:

- `parts-of-speech.ts`: a `PartOfSpeechType` union and a list of definitions with Spanish examples.
- `tense.ts` / `moods.ts`: indicative, subjunctive and imperative moods. Each tense entry has its mood, simple or compound form (perfect/anterior), a description and examples.
- `pronouns.ts`: pronoun categories (subject, object, reflexive, possessive, demonstrative and more) and the subject pronouns.
- `articles.ts` / `gender.ts`: definite and indefinite articles by gender and number, and notes on how gender agreement works.
- `nouns.ts`: a `Noun` shape plus notes on pluralisation rules (loanwords, words ending in s/x, esdrújulas), partly sketched as a `getPluralForm` function.
- `conjugation.ts` / `adjectives.ts` / `sentence-structure.ts`: notes on conjugation, adjective agreement and word order, with a stub `conjugateVerb(verb, tense, pronoun)` signature.

The idea was to turn grammar rules into something a program could use, such as generating or checking conjugations. That logic never got past stubs.

## State

This is a sketch and does not build:

- There is no `package.json` or `tsconfig.json`.
- Files rely on types from each other without importing them.
- `conjugateVerb` and the pluralisation logic are not implemented.

It is best read as structured notes on Spanish grammar, not as a working library.

## Tech stack

TypeScript (types and plain data only, no dependencies).

## Context

Started in March 2023 and last edited in October 2023, as a side project while studying Spanish.
