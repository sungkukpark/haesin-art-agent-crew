# Agent Hierarchy

**Who does the work, who reviews it, and which components are tools?**

[All diagrams](../README.md#architecture-guide) · [Mermaid source](../diagrams/01-agent-hierarchy.mmd) · [Rendered SVG](../diagrams/01-agent-hierarchy.svg)

```mermaid
flowchart TB
    U["User: asset brief and requested end stage"] --> C["Coordinator / main agent
Routes skills; manages models and delivery"]
    C -->|"Ship design"| S["character-concept-artist"]
    C -->|"Creature design"| M["monster-concept-artist"]
    C -->|"Environment concept"| E["environment-concept-artist"]
    C -->|"Officer portrait"| P["portrait-artist"]
    C <-->|"Consultation and model review"| D["art-director
Independent reviewer"]
    S <-->|"Candidate / feedback"| D
    M <-->|"Candidate / feedback"| D
    E <-->|"Candidate / feedback"| D
    P <-->|"Candidate / feedback"| D
    S -.-> I(["Image generation tool"])
    M -.-> I
    E -.-> I
    P -.-> I
    C -.-> T(["Tripo: 3D model service"])
    C -.-> G(["Godot: import and render checks"])
    classDef reviewer fill:#fff0d6,stroke:#9d6400,color:#302000
    classDef tool fill:#f0f3f7,stroke:#697586,color:#263140
    class D reviewer
    class I,T,G tool
```

The coordinator is the main agent, not a sixth specialist TOML. Five specialist roles are defined. The art director reviews independently and returns findings to the responsible producer. Environment production is a configured capability; the examples in this documentation cover ships, a creature, and portraits. Dashed arrows identify tool use, not additional agents.

## Evidence basis

[agent-workflow.txt](../evidence/definitions/agent-workflow.txt) · [art-director.toml](../evidence/definitions/art-director.toml) · [environment-concept-artist.toml](../evidence/definitions/environment-concept-artist.toml)
