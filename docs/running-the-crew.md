# Running the Original Skill-Driven Crew

[Back to README](../README.md) · [Recorded completed run](recorded-run.md)

## Included implementation

Open **`crew/` as the working folder** in a compatible agent host. It contains the original five `.codex/agents/*.toml` definitions, all six `.agents/skills/*/SKILL.md` workflows and their local reference instructions, shared collaboration/access contracts, ship prompt template, and the selected scout subject/style images. [crew/AGENTS.md](../crew/AGENTS.md) supplies the coordinator's scoped execution contract. Definitions are executable host instructions, not a standalone shell program.

The host must load those role definitions and expose real agent delegation, actual image context, image generation, file inspection and the host's `imagegen` skill. Check that `character-concept-artist` and `art-director` are available before starting; if missing, load/reload the project roles using the host's supported mechanism. Do not replace an unavailable role with a pretend transcript. Model/package stages additionally require configured Tripo service access, an explicit model-call/credit budget, and Godot import/render capability. Service credentials and installed applications are environment dependencies and are not included.

## Minimal three-agent production invocation

Submit this request to the main coordinator in that folder:

```text
$create-character-concept
해신 정찰선의 새로운 컨셉 한 장을 제작해줘.
subject_reference: _workspace/shared/references/ships/scout/design-reference.png
style_reference: _workspace/shared/style/source/wanderburg_style_ref.png
asset_id: scout
이번 실행은 coordinator + character-concept-artist + art-director가 반드시
각자 역할을 수행하는 위임 경로로 실행해줘. 메인 직접 제작 fallback은 사용하지 마.
새 batch_id와 미사용 버전으로 기록하고, 실제 호출 식별자·응답·입출력 해시·
독립 검수·최종 납품 상태를 보존해줘. 컨셉 단계에서 종료해줘.
```

For the complete model/package route, request `$create-unit-assets` with `asset_ids: [scout]`, `end_stage: package` and an explicit service budget instead. The included catalog is the original full-system catalog; other units require their own supplied reference files. Use the supplied scout references for this selected run, not unavailable original game paths. Resume state only from actual local run records.

For portraits, use `$create-officer-portrait` with two actual subject/style images and require coordinator + portrait-artist + art-director. Both required portrait reference guides are included. The original portrait subject has a documented source attribution, but its generation-time subject/style attachments were not saved; the example is historical evidence, not a self-contained replay input pair.

## Expected evidence and completion

1. The coordinator fixes input hashes and scope and records the actual specialist invocation.
2. The specialist consults the independent director, produces the requested candidate and submits actual images, hashes and self-review.
3. The director returns a verdict tied to that candidate. Corrections create the next version within the existing limit.
4. The specialist publishes its files and handoff; the coordinator verifies them and reports the actual final status. Model/package requests also preserve task IDs, model review and Godot checks.

Inspect the new run's own files and responses; do not substitute the supplied historical examples for newly generated output. Approval, technical target, user selection and game integration remain separate. This documentation revision included no new paid image/model generation and does not claim a fresh clean-environment execution.
