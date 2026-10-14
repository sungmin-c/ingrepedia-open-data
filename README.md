# Ingrepedia open data

This repository publishes the **derivative database** that the Ingrepedia app
builds its ingredient dictionary from, as required by the
[Open Database License (ODbL) v1.0](https://opendatacommons.org/licenses/odbl/1-0/)
of its source.

## Contents

| File | What it is |
|---|---|
| `off_taxonomy.json` | An extract of the [Open Food Facts](https://world.openfoodfacts.org/) ingredients taxonomy (retrieved 2026-07-31): ingredient ids, display names in en/ko/es/pt/zh/ja/id, E-number canonicalization and synonyms. |

### How it differs from the source

- Only the fields and languages listed above are kept; synonyms are capped
  per entry.
- Chinese names (`names.zh`) are converted to Taiwan Traditional Chinese with
  [OpenCC](https://github.com/BYVoid/OpenCC) (`s2twp`); the original form is
  kept in `aliases`.

## Licence

This database is made available under the **Open Database License (ODbL)
v1.0**: <https://opendatacommons.org/licenses/odbl/1-0/>. Any rights in
individual contents of the database are licensed under the
[Database Contents License](https://opendatacommons.org/licenses/dbcl/1-0/).

It contains information from **Open Food Facts**, which is made available under
the ODbL. Open Food Facts data is crowd-sourced and may contain errors; it
carries no allergen or diet judgement and must not be used as one.

This repository contains data only. The Ingrepedia app, its code, its curated
allergen/diet tags and rules, and its design are not part of this release.
