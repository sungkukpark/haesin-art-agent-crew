# Portrait Production

**How does a portrait preserve identity while incorporating reviewer feedback?**

[All diagrams](../README.md#architecture-guide) · [Mermaid source](../diagrams/04-portrait-sequence.mmd) · [Rendered SVG](../diagrams/04-portrait-sequence.svg)

```mermaid
sequenceDiagram
    autonumber
    actor U as User
    participant C as Coordinator
    participant P as portrait-artist
    participant D as art-director
    participant I as Image tool
    U->>C: Subject reference, style reference, optional extra prompt
    C->>P: Portrait brief and actual reference context
    P->>D: Identity, costume, framing and target consultation
    D-->>P: Preservation priorities and review criteria
    P->>I: Generate transparent portrait from two reference roles
    I-->>P: Candidate v001
    P->>P: Check framing, alpha and 128/256 face previews
    P->>D: Candidate images, version, hash and self-review
    D-->>P: changes_requested and concrete correction
    P->>I: Edit previous result, preserve identity and style brief
    I-->>P: Candidate v002
    P->>D: Revised image, previews and updated evidence
    D-->>P: approved_for_next_stage (art judgment)
    P-->>C: Publish versioned PNG, manifest and review handoff
    C->>C: Verify hashes and preserve delivery records
    C-->>U: Portrait and separate art / technical / selection statuses
    Note over P,D: Example: mounted-officer<br/>Later cataloged as kato-kiyomasa
```

This is the specialist-led route documented by the portrait skill. The skill also allows the coordinator to execute directly with independent director review. In the selected example, the recorded producer is portrait-artist. The v002 image call used v001 as its actual edit input; the original subject/style roles remained in the brief. Their original file bytes were not retained. See the case study for the exact historical limitations.

[Read the actual portrait revision case](portrait-case-study.md).

## Evidence basis

[portrait-artist.toml](../evidence/definitions/portrait-artist.toml) · [create-officer-portrait.SKILL.txt](../evidence/definitions/create-officer-portrait.SKILL.txt)
