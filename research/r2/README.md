# R2: source and evidence

**Archive status: sources indexed; reproduction not rerun.**

R2 is Ensomi's released audio-to-osu!mania-4K system. Its public report
describes a timing system, a head-row model, a corpus prior and R2's note
arrangement. This page locates that material; the source report remains the
owner of the system description and its reported results.

## Read the sources

| Material | Source |
| --- | --- |
| System, research decisions, evidence and limitations | [R2 report](https://github.com/ensomi-labs/ensomi-model/blob/af65de8892899563698962473ca629dd73b6608a/docs/research/r2_system.md) |
| Training-data stages and attribution limits | [Data provenance](https://github.com/ensomi-labs/ensomi-model/blob/af65de8892899563698962473ca629dd73b6608a/docs/research/r2_data_provenance.md) |
| Source lineage and earlier work | [Research documents](https://github.com/ensomi-labs/ensomi-model/blob/af65de8892899563698962473ca629dd73b6608a/docs/research/README.md) |
| Problem definition | [V3 formulation](https://github.com/ensomi-labs/ensomi-model/blob/af65de8892899563698962473ca629dd73b6608a/docs/formulation/README.md) |
| Model distribution | [Hugging Face project](https://huggingface.co/sed-i/ensomi-r2), a moving project link; the source report's quick start names revision `r2-1.0.1` |

The documentation observation commit is
[`af65de8892899563698962473ca629dd73b6608a`](https://github.com/ensomi-labs/ensomi-model/commit/af65de8892899563698962473ca629dd73b6608a),
checked on 2026-11-07. It is distinct from the training and release sources
below.

## Source lineage

The report identifies the training sources. The full commits and tag targets
below were resolved against GitHub on 2026-11-07.

| Role | Source commit | Meaning |
| --- | --- | --- |
| Rows-model training source | [`cf753aafa92530f82915c936b88eecd31ef6535d`](https://github.com/ensomi-labs/ensomi-model/commit/cf753aafa92530f82915c936b88eecd31ef6535d) | the report says the run's recorded settings, rather than later defaults, are authoritative |
| R2 training source | [`39540317be42aa53104939c759e03610d64e6a3e`](https://github.com/ensomi-labs/ensomi-model/commit/39540317be42aa53104939c759e03610d64e6a3e) | source of the reported phase-N training; it is not the whole released system |
| First system release | [`d65a49f14d3b9bd0cef35cd302eeea47a8c7a444`](https://github.com/ensomi-labs/ensomi-model/commit/d65a49f14d3b9bd0cef35cd302eeea47a8c7a444) | resolved target of `timing-1.0` |
| System and rows-decoder fix | [`9e380a15f7c193476ff2063dfc10043e8484186a`](https://github.com/ensomi-labs/ensomi-model/commit/9e380a15f7c193476ff2063dfc10043e8484186a) | resolved target of both `r2-1.0.1` and `rows-1.0.1` |

## Evidence and open gaps

The report records reproduction of four inference examples from published
files on macOS arm64, as well as blind listening and diagnostic measurements.
Those are source-reported checks, not new checks by this archive. The report
also describes one listener, unvalidated automatic quality measures, a local
SciPy wheel repair and an untested Linux/CUDA path. Read its version-specific
qualifications before reusing any result.

The Python command, model service and Rust runtime also differ in arrangement
passes, as the report explains. Specify the execution path when comparing
outputs; a common model name does not establish identical behavior.

No training, evaluation or inference was run for this entry. Model bytes,
Hugging Face revision targets and file checksums were not independently
verified. Data access, the complete run configuration, environment and exact
evaluation inputs still need to be assembled before this can serve as a
reproduction package. The private training corpus is not included.

The next useful addition is one bounded research claim with its baseline,
configurations, input identities, expected result and a recorded attempt to
repeat it. Selection of that claim remains open.
