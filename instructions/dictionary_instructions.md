---
applyTo: "1dictionary.md"
---

# Instructions for Copilot for 1dictionary.md

This file is a French English dictionary with exactly 3 columns:
1. Français
2. Prononciation
3. English

## Rules for the table
- No index column
- All cells start with lowercase unless the word is a proper name
- There should not be any duplicate entries

### Français column
  * add curly brackets after the word indicating type {N} {V} {Adj} {Adv} {Interj} {Num} {Prep} {Pron} {Conj}
  * nouns must include the definite article for example une mère {N} un père {N} les parents {N} (M) if gender is clear from the article then no need to add (M) or (F)
   * if plural then after {N} add gender in uppercase M or F
   * if elided form l’Université still include gender marker
   * if the noun is about people then add both versions first for male and then for female (le serveur / la serveuse {N})
   * adjectives list both masculine and feminine forms separated by a slash even if identical for example gentil / gentille {Adj}
   * verbs after {V} add R for regular or IR for irregular for example avoir {V} (IR) étudier {V} (R)

### Prononciation column
* use International Phonetic Alphabet IPA
* must include liaison indications

### English column
* give the English translation
* if used only in Quebec French mark with Quebec after the word for example une blonde {N} (F) girlfriend (Quebec)

## Ghost text behavior
- When the user starts typing in the Français column Copilot should automatically suggest the rest of the row including the rest of Français column, IPA pronunciation and English translation following the rules above


## Instructions for OCR-based French Vocabulary Extraction

When I upload an image containing French vocabulary arranged in rectangles, extract the content and produce a Markdown table following these rules:

1. Do not include header row dicitionary table.
2. Each rectangle title must be the first row of its section and formatted exactly like:
   | **Les produits à la pharmacie** {Loc} | [lez pʁɔdɥi a la faʁmasi] | products at the pharmacy |
   – The title must be bold, include {Loc}, have an IPA transcription in square brackets, and an English translation.
3. Under each title, list all vocabulary items from that rectangle in the original order.
4. Every table row must contain exactly 3 columns:
   - Column 1: French word/expression with type tag {N}, {V}, {Adj}, {Adv}, {Loc}, {Prep}, {Conj}, {Interj}, or {Num}.  
     *Include definite/indefinite articles.  
     *Nouns: show article; if plural, add gender after {N} (M/F).  
     *Adjectives: show masc/fem forms (e.g., animé / animée {Adj}).  
     *Verbs: {V} followed by (R) or (IR).*
   - Column 2: IPA transcription inside square brackets, with liaisons.
   - Column 3: English translation (lowercase, concise, natural).
5. One line per vocabulary item except logically linked phrases.
6. No blank lines between sections.
7. Use standard IPA conventions.
8. Keep the order of rectangles and entries exactly as in the image.

The output must be a clean, copy-ready Markdown table that fits directly into the dictionary file.