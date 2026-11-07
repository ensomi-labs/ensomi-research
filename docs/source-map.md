# ensomi-model: source organization and archive gaps

Checked against GitHub on **2026-11-07**. The main-branch observation is
[`af65de8892899563698962473ca629dd73b6608a`](https://github.com/ensomi-labs/ensomi-model/tree/af65de8892899563698962473ca629dd73b6608a).
This is a structural review of tracked files, public documentation and selected
development references. It does not assess model quality or certify unused
code, correct experiments or reproducibility.

## Main-branch organization

The current [README](https://github.com/ensomi-labs/ensomi-model/blob/af65de8892899563698962473ca629dd73b6608a/README.md)
already maps the major components. The recursive Git tree contains 237 files
under `src/ensomi_model/` and 136 under `tests/`; these counts include all
tracked file types in those directories.

| Location | Role and implication for a research reader |
| --- | --- |
| `src/ensomi_model/audio_rows/` | timing and head rows; part of the full R2 system, despite living outside `r2/` |
| `src/ensomi_model/r2/` | arrangement model, training, evaluation and export; a model-family directory still holds several research and execution roles |
| `src/ensomi_model/system/` | end-to-end generation, corpus prior and controls; needed to understand what actually runs |
| `src/ensomi_model/research/` | 85 tracked files of earlier research and shared chart/replay foundations; the name alone is not evidence that code can be removed |
| `evaluation/`, `service/`, `export/` under the source package | evaluation infrastructure, model serving and runtime export; distinct execution and evidence paths |
| `scripts/`, `experiments/` | operational helpers and reconstruction recipes alongside the package; some require surviving local assets |
| `docs/research/`, `docs/formulation/` | public reports and the problem definition; the research index already maps historical lines to refs |

There is a package layout, component tests and a documented history. The
remaining difficulty is following a research result across those places.
A directory tree alone cannot identify which configuration, checkpoint,
dataset split or evaluation belongs to a claim.

## Version and asset boundaries

R2's [lineage](../research/r2/README.md#source-lineage) separates two training
commits from released inference code. Its report warns that later defaults do
not define the rows training run. Earlier work is reached through `legacy/v2`,
tags and archived refs described by the
[historical index](https://github.com/ensomi-labs/ensomi-model/blob/af65de8892899563698962473ca629dd73b6608a/docs/research/README.md).
Do not classify all non-main branches as current experiments: a branch list
alone says neither whether work was merged nor whether it was superseded.

The source [.gitignore](https://github.com/ensomi-labs/ensomi-model/blob/af65de8892899563698962473ca629dd73b6608a/.gitignore)
excludes `artifacts/`, `dataset/` and `uv.lock`. A source checkout therefore
does not by itself supply the local research assets or a committed dependency
lock. The
[vacation-input recipe](https://github.com/ensomi-labs/ensomi-model/blob/af65de8892899563698962473ca629dd73b6608a/experiments/vacation_rebuild/README.md)
explicitly depends on surviving local caches and does not recover historical
checkpoint bytes or claim equivalent training.

The [ecosystem guide](https://github.com/ensomi-labs/ensomi-model/blob/af65de8892899563698962473ca629dd73b6608a/docs/ecosystem.md)
assigns model-package, runtime, protocol and client facts to their own owners.
An archive entry should link those owners rather than silently treating the
Python repository as a complete released application.

## N1 development

N1 is not present as `n/` on the inspected main commit. The observed
[`codex/n1-gpu` tip, `8f2b0f0bb1f5c368da446dde2669064581eed1d2`](https://github.com/ensomi-labs/ensomi-model/tree/8f2b0f0bb1f5c368da446dde2669064581eed1d2)
contains a separate `n/` distribution, `scripts/n1/` and experiments under
`n/experiments/n1_redesign/gpu/`. Its
[N-line README](https://github.com/ensomi-labs/ensomi-model/blob/8f2b0f0bb1f5c368da446dde2669064581eed1d2/n/README.md)
states an intentional separation between `ensomi_n` and `ensomi_model`, with
its own licence. This is a reason to preserve ownership when indexing it.

At inspection, GitHub compared that tip as 56 commits ahead and 8 behind the
observed main commit; the observed `n1/v01` tip,
[`b51a9ff236b2c78c0ad1983ff4f842f38911e5ea`](https://github.com/ensomi-labs/ensomi-model/tree/b51a9ff236b2c78c0ad1983ff4f842f38911e5ea),
was 41 ahead and 8 behind. These samples establish divergence, not which
branch contains a final result. Other N1 branch names were listed, but their
experiments and result claims were not reviewed.

## What the archive adds

The useful first step is a research entry that joins question, source lineage,
artifact locations, evidence and limitations. R2 now has that entry. N1 remains
a development pointer until a result and its authoritative sources are selected.
Historical reports stay at their owners and are linked from this index.

This review did not inspect private notes or datasets, scan local artifacts,
run the model or tests, audit every development branch, or fetch every archived
ref. It supports the need for a research index; it does not support deleting,
moving or duplicating source code. Source reorganization and automated snapshot
assembly remain separate work.
