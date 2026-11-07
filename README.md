# Ensomi Research

Research archive and results index for [Ensomi](https://github.com/ensomi-labs).
Start with the [research index](research/README.md) for each line of work and
the [source map](docs/source-map.md) for where its code and evidence live.

This repository connects research questions, reports, source versions, models
and evaluation evidence. Development continues in the source repositories.
An entry here can begin with verified links and grow as its materials are
curated; inclusion alone makes no claim of reproducibility or publication.

## Start here

| Entry | What is available here |
| --- | --- |
| [R2](research/r2/README.md) | links to the released system's report, data provenance, source lineage and model distribution; open gaps in the research archive |
| [Research index](research/README.md) | R2, earlier work and the N1 development entry point |
| [Source map](docs/source-map.md) | a dated assessment of ensomi-model's organization and the limits of that assessment |

## Scope and principles

- Keep concise research summaries, relationships between results, source
  references, limitations and pointers to supporting materials here.
- Keep maintained code in its owning repository. Link existing reports
  instead of maintaining a second copy. Copy material only when a concrete
  archive needs it, with its origin and permissions recorded.
- Record a full source commit for a version-specific statement. A branch link
  is useful for discovery but is not a frozen research version. An observation
  commit is not automatically a training or release commit.
- Distinguish a source report's claims from checks performed for this archive.
  State what was checked, on which inputs and environment, and what remains
  unknown. Preserve negative results and evaluation limits.
- Link model files and large artifacts at their owners. Record revisions and
  checksums when verified; do not infer that files were preserved or tested.
- Keep private notes, datasets, audio and per-item research records outside
  this repository. Link public data descriptions and permitted aggregates.

## Add an entry

Use the [entry template](templates/research-entry.md) when there is a concrete
result or body of work to index. Create `research/<name>/README.md`, retain
unknown fields explicitly, and add it to the [index](research/README.md).
Start with the evidence available; additional directories should hold actual
materials rather than empty plans.

## Archive status

This is an initial documentation and provenance index. It contains no source
snapshot, model weights or independently reproduced research result. There is
no snapshot-generation workflow, archive CI, or Zenodo integration. Those can
be considered when a specific result needs a release.

No paper, DOI, author list or citation metadata is assigned by this
initialization. The licence for new archive text remains to be selected;
linked code, models and documents retain their own licences. Linking a
resource does not relicense it or establish data redistribution rights.
