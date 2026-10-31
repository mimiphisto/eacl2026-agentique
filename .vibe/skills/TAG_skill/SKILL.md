---
name: tag
description: Appliquer des étiquettes de POS-Tagging sur les données, après la lemmatisation.
---

# POS-tagging (grec ancien)

Étiqueter chaque ligne lemmatisée et produire le TSV final à trois colonnes.

## Entrée

- Le TSV produit par le skill `lem`, après la lemmatisation.

## Sortie

- Un tableau TSV à trois colonnes, toujours dans l'ordre `form`, `lemma`, `pos`, séparées par une tabulation.

## Contrainte

- N'utiliser que les tags de la liste officielle : `data/tagsets/GRC_tagset.txt` (45 tags, format `TAG<TAB>description`). Tout tag hors de cette liste est invalide.

## Référence

- Modèle de configuration (PIE) : `references/pos.json`. Les chemins (`modelpath`, `input_path`, `dev_path`) y sont des placeholders à remplacer par les vrais chemins du corpus avant utilisation.
