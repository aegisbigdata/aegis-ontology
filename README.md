# aegis-ontology

Purpose: Formalization of the column contents of tabular datasets,
in order to automatically detect combinable datasets.

Rationale:
Big Data is also about gaining new insights by *combining* datasets.

Assumption: For the time being, focus on *tabular* datasets only (CSV etc.).

Two tabular datasets can be combined (i.e. correlated, joined)
if they have semantically compatible columns in common;
e.g., if both have a column with geo coordinates in the same region.
This situation is the basis for a correlation or a DB join.

In order to detect such cases automatically,
a formalization of the semantics of column contents of tables is useful.
This is the purpose of the ontology presented here.
