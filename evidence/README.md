# Source Records and Traceability

[Back to README](../README.md)

The linked definitions are byte-identical snapshots of the project’s actual role and workflow instructions. Skills and shared contracts use `.txt` here so that historical links inside them are not presented as working links in this documentation repository. The original relative paths are retained in the source manifest. These snapshots preserve historical source evidence. Host-facing copies with their instruction dependencies are also included in `../crew/`; see the [run guide](../docs/running-the-crew.md).

## Definitions

- [character-concept-artist.toml](definitions/character-concept-artist.toml) — original `.codex/agents/character-concept-artist.toml`
- [monster-concept-artist.toml](definitions/monster-concept-artist.toml) — original `.codex/agents/monster-concept-artist.toml`
- [environment-concept-artist.toml](definitions/environment-concept-artist.toml) — original `.codex/agents/environment-concept-artist.toml`
- [portrait-artist.toml](definitions/portrait-artist.toml) — original `.codex/agents/portrait-artist.toml`
- [art-director.toml](definitions/art-director.toml) — original `.codex/agents/art-director.toml`
- [create-unit-assets.SKILL.txt](definitions/create-unit-assets.SKILL.txt) — original `.agents/skills/create-unit-assets/SKILL.md`
- [create-ship-asset.SKILL.txt](definitions/create-ship-asset.SKILL.txt) — original `.agents/skills/create-ship-asset/SKILL.md`
- [create-character-concept.SKILL.txt](definitions/create-character-concept.SKILL.txt) — original `.agents/skills/create-character-concept/SKILL.md`
- [create-ship-multiview.SKILL.txt](definitions/create-ship-multiview.SKILL.txt) — original `.agents/skills/create-ship-multiview/SKILL.md`
- [create-monster-asset.SKILL.txt](definitions/create-monster-asset.SKILL.txt) — original `.agents/skills/create-monster-asset/SKILL.md`
- [create-officer-portrait.SKILL.txt](definitions/create-officer-portrait.SKILL.txt) — original `.agents/skills/create-officer-portrait/SKILL.md`
- [agent-workflow.txt](definitions/agent-workflow.txt) — original `_workspace/shared/agent-workflow.md`
- [workspace-access.txt](definitions/workspace-access.txt) — original `_workspace/AGENTS.md`
- [model-stage.txt](definitions/model-stage.txt) — original `.agents/skills/create-ship-asset/references/model-stage.md`
- [delivery.txt](definitions/delivery.txt) — original `.agents/skills/create-unit-assets/references/delivery.md`
- [batch-state.txt](definitions/batch-state.txt) — original `.agents/skills/create-unit-assets/references/batch-state.md`

## Production evidence

- [Portrait v002 manifest](portrait/v002-manifest.json), [review](portrait/v002-review.md), [actual edit prompt](portrait/v002-prompts.md), [input record](portrait/v002-inputs-manifest.json), and [handoff](portrait/v002-handoff.json).
- [Portrait v003 follow-up review](portrait/v003-review.md) and [output metadata](portrait/v003-output.json).
- [Player package summary](player/package-summary.json), [scout summary](scout/package-summary.json), and [kraken summary](kraken/package-summary.json).

Package summaries are explicitly derived portable extracts. Original portrait records retain their historical IDs and paths; paths inside historical JSON are production context, not instructions to access other workspaces. The source manifest maps each copied example to its actual original location and byte hash.

## Integrity

[source-manifest.json](source-manifest.json) records SHA-256 for copied sources and examples. It also records diagram-source hashes. Human-readable pages summarize those materials and link back to them. Generation model and seed remain unknown where not reported; no synthetic execution transcript is added.
