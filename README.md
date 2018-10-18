# MorphoDiTa POS Tag Explainer

Czech POS Tagger MorphoDiTa uses POS tags in PDT (Prague Dependency Treebank) format. Since the format is not very intuitive, applications and tools relying on such tags are usually hard to debug. This tool alleviates the pain by validating and explaining the tags in a user-friendly way.

## Example Sentence Tagged in PDT Format
```
Noc         NNFS1-----A----
byla	    VpQW---XR-AA---
touhou	    NNFS7-----A----
přesycená	AAFS1----1A----
a       	J^-------------
vábila  	VpQW---XR-AA---
a           J^-------------
lákala      VpQW---XR-AA---
.           Z:-------------
```

## Single Tag Validated and Explained
```
POS tag syntax valid.
Full tag: VpQW---XR-AA--- 

Index Category   Value Description
0     POS        V     Verb
1     SUBPOS     p     Verb, past participle, active (including forms with the enclitic -s, lit. 're (are))
2     GENDER     Q     Feminine (with singular only) or Neuter (with plural only); used only with participles and nominal forms of adjectives
3     NUMBER     W     Singular for feminine gender, plural with neuter; can only appear in participle or nominal adjective form with gender value Q
4     CASE       -     Not applicable
5     POSSGENDER -     Not applicable
6     POSSNUMBER -     Not applicable
7     PERSON     X     Any person
8     TENSE      R     Past
9     GRADE      -     Not applicable
10    NEGATION   A     Affirmative (not negated)
11    VOICE      A     Active
12    RESERVE1   -     Not applicable
13    RESERVE2   -     Not applicable
14    VAR        -     Not applicable (basic variant, standard contemporary style; also used for standard forms allowed for use in writing by the Czech Standard Orthography Rules despite being marked there as colloquial)
```

# Prerequisites
- Python 3.6
- pip

# Installation 
- Make sure your `virtualenv` is activated.
- `pip install -r requirements.txt`

# Usage
- Pass POS tag as a positional argument to the script: 
`$ python explainer.py NNFS1-----A----`

# Resources
POS tag reference guide:
https://ufal.mff.cuni.cz/pdt/Morphology_and_Tagging/Doc/hmptagqr.html

MorphoDiTa project page:
http://ufal.mff.cuni.cz/morphodita

MorphoDiTa online demo: 
http://lindat.mff.cuni.cz/services/morphodita/

