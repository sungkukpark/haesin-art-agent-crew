# Ship and Monster Production

**What is handed from one agent to the next during a full requested production run?**

[All diagrams](../README.md#architecture-guide) · [Mermaid source](../diagrams/03-ship-monster-sequence.mmd) · [Rendered SVG](../diagrams/03-ship-monster-sequence.svg)

```mermaid
sequenceDiagram
    autonumber
    actor U as User
    participant C as Coordinator
    participant A as Assigned specialist
    participant D as Art director
    participant I as Image tool
    participant T as Tripo tool
    participant G as Godot tool
    U->>C: References, asset ID, end stage, model budget
    C->>A: Brief and permitted reference inputs
    Note over A,D: Ship: character-concept-artist<br/>Creature: monster-concept-artist
    A->>D: Pre-production consultation
    D-->>A: Preservation goals and review criteria
    loop Concept and requested multiview candidates within stage limits
        A->>I: Generate or edit using fixed references
        I-->>A: Actual image result
        A->>A: Self-review, record version and hashes
        A->>D: Actual images, brief, self-review and hashes
        D-->>A: Approve next stage, request changes, or request evidence
    end
    opt Modeling requested and inputs accepted
        A-->>C: Accepted four-view handoff with linked review
        C->>T: Model request, record request and task ID
        T-->>C: GLB and available service metadata
        C->>C: Inspect model, normalize, render, record hashes
        C->>D: Model renders, fixed design and inspection evidence
        D-->>C: Model review and required corrections
        opt Static package requested and model accepted
            C->>G: Isolated import, instance and GPU checks
            G-->>C: Logs, rendered views and relocation results
            C-->>U: GLB, wrapper, metadata and report
        end
    end
```

The image loop abbreviates separate concept and multiview reviews, including the complete four-view set. An unresolved review stops the affected stage; it does not fall through to modeling. Model corrections produce a new version and require fresh review. The coordinator owns model-service work and package validation. A request can stop earlier than the complete sequence shown.

## Evidence basis

[create-ship-asset.SKILL.txt](../evidence/definitions/create-ship-asset.SKILL.txt) · [create-monster-asset.SKILL.txt](../evidence/definitions/create-monster-asset.SKILL.txt) · [model-stage.txt](../evidence/definitions/model-stage.txt) · [delivery.txt](../evidence/definitions/delivery.txt)
