---
name: lem
description: lemmatisation + données
---

# Lemmatisation (grec ancien)

Lemmatiser les formes du corpus et produire un TSV à trois colonnes.

## Entrée

- Fichier : `data/corpus/train/GRC_train.tsv`
- Colonnes : `text_form`, `form`, `lemma`, `pos` — séparées par des tabulations, fins de ligne CRLF, avec une ligne d'en-tête à conserver.

## Sortie

- Un tableau TSV à trois colonnes, toujours dans l'ordre `form`, `lemma`, `pos`, séparées par une tabulation.
- Recopier `form` telle quelle ; remplir `lemma` avec le lemme de la forme.
- Le POS-tagging se fait ensuite avec le skill `tag`.

## Référence

- Modèle de configuration (PIE) : `references/lemma.json`. Les chemins (`modelpath`, `input_path`, `dev_path`) y sont des placeholders à remplacer par les vrais chemins du corpus avant utilisation.
