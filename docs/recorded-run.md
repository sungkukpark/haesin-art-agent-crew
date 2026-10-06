# Recorded Three-Agent Run — Scout Ship

[Back to README](../README.md) · [Run instructions](running-the-crew.md)

The representative graded crew is **coordinator + character-concept-artist + art-director**, producing the scout ship for HAESIN. Monster, environment and portrait specialists are alternative production routes in the broader architecture, not extra mandatory participants in this scout run. The portrait page remains a second, particularly visible revision example.

## Actual retained execution evidence

The byte-identical [original coordinator pipeline](../evidence/scout/original-pipeline.json) records `batch_id: fleet-001`, `asset_id: scout`, `owner: coordinator`, `design_role: character-concept-artist`, `requested_end_stage: package`, `status: completed`, and `current_stage: package`. Its concept, multiview, model and package stages are all recorded as completed; independent concept/multiview/model reviews identify `/root/art_director`.

| Participant | Actual record and contribution | Downstream dependency |
| --- | --- | --- |
| Coordinator / main agent | [Generated-image publication](../evidence/scout/handoffs/fleet-001-scout-concept-v002-generated/coordinator/handoff.json), pipeline, model task IDs and [final package publication](../evidence/scout/package-coordinator-handoff.json) | Provides fixed inputs, service execution, state and verified delivery. |
| `character-concept-artist` | [Concept prompt, attempt and self-review](../evidence/scout/handoffs/fleet-001-scout-concept-v002/character-concept-artist/handoff.json), [accepted four-view handoff](../evidence/scout/handoffs/fleet-001-scout-multiview-v001-approved/character-concept-artist/handoff.json) | Supplies ship-specific design instructions and reviewed views needed by the model stage. |
| `art-director` | [Concept verdict](../evidence/scout/handoffs/fleet-001-scout-concept-review-v002/art-director/handoff.json), [four-view set verdict](../evidence/scout/handoffs/fleet-001-scout-multiview-review-v001-set/art-director/handoff.json), [model verdict](../evidence/scout/model-director-handoff.json) | Independently accepts or returns the candidate; downstream work depends on its actual verdict. |

In this historical run, the coordinator also published tool-generated images, while the specialist supplied design work, prompts and self-review. The architecture sequence describes the specialist-led route; it is not a literal replay of every historical tool caller. These records show the practical division without relabeling tools as agents.

The final model hash is `5d8ffbf81eaea965ff8911163c84868c9665beaaf5db8456e18cca5724fa29c5`, matching the [included GLB](../examples/scout/scout.glb), model verdict and pipeline. The [package report](../evidence/scout/package-report.md) records successful original and relocated Godot checks. The run reached delivery; this is evidence of completed coordination, not a claim that every historical service call was error-free. The model-review publication records a recovered handoff serialization issue; that event is preserved.

The pipeline retains original absolute source paths as historical strings. The links above and the source manifest locate the portable copies in this repository. Original transcript-level coordinator and specialist runtime IDs were not retained in these records; roles, publications, artifact hashes and the director ID are retained. No missing transcript or new execution is fabricated.

## Why the three roles are required in the submitted route

The [submission execution contract](../crew/AGENTS.md) selects the existing delegated branch and disables the generic main-agent production fallback for this demonstration. Removing the specialist leaves no design/self-review handoff; removing the director leaves no independent approval; removing the coordinator leaves no routing, model service or verified package delivery. This is a scoped invocation of the original system. Its historical skills remain unchanged and still describe their broader fallback capability.
