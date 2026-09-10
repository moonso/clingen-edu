# Variant Effect Prediction
# Short historic overview
## Context (pre 2000s)

Variant interpretation relied on 
- conservation between species
- Biochemical properties of amino acids
- Known functional domains
- Small-scale functional assays

There where no dedicated variant effect prediction tools available just yet, mostly relied on expert judgement and bioinformatics.
There where some early use of multiple sequence alignment and domain databases such as [Pfam][pfam] (founded by Sonnhammer et al from Scilife!) and [PROSITE][prosite] 
to infer the potential impact of genetic variations.
This set the conceptual basis for later tools: **conservation**, **structure** and **function**.

## First-generation in silico tools (Early 2000s)

### [SIFT][sift] - Sorting Intolerant From Tolerant 
**Concept:** Uses sequence homology and conservation to predict whether an amino acid substitution is tolerated or deleterious.
**Key idea:** Strongly conserved positions are likely functionally important; changes there might be deleterious.

### [PolyPhen][polyphen]/[Polyphen-2][polyphen2]
**Concept:** Combines sequence conservation, protein structural features and annotation to classify missense variants.
**Key idea:** Integrate multiple features (sequence + structure) and uses probabilistic models.

SIFT and PolyPhen were among the first routinely used tools in diagnostic pipelines, but with known limitations such as discordant predictions and no calibration
for clinical validity.

## Expansion to broader variant types and ensemble methods (mid-2000s-2010s)

### Conservation scores (PhastCons, PhyloP)
Used as input features or independent evidence of constraint. Helped extend variant effect prediction beyond coding regions.


# Appendix

## Glossaey

Deleterious (variant) - a genetic change that is predicted or shown to harm normal gene or protein function and is therefore more likely to contribute to disease.
Pathogenic (variant) - a genetic change that has sufficient evidence to be causally linked to a disease or clinical phenotype in humans.

[prosite]: https://en.wikipedia.org/wiki/PROSITE
[pfam]: https://en.wikipedia.org/wiki/Pfam
[sift]: https://pmc.ncbi.nlm.nih.gov/articles/PMC168916/
[polyphen]: https://pmc.ncbi.nlm.nih.gov/articles/PMC137415/
[polyphen2]: https://www.nature.com/articles/nmeth0410-248
