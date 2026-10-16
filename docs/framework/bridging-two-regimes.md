# Bridging Two Computational and Epistemic Regimes

**Related paper:** *Ontological Mediation in Explainable Artificial Intelligence: Concept-Based Models and Ontology-Grounded Explanatory Justification*  
**Authors:** Eduardo M. P. Coelho; Marcello Peixoto Bax  
**Preprint:** SciELO Preprints  
**DOI:** 10.1590/SciELOPreprints.18206  
**Status:** Supplementary visual artifact  
**Version:** 0.1 — October 2026  
**Documentation license:** CC BY 4.0

```mermaid
flowchart LR
    subgraph SUB["SUB-SYMBOLIC REGIME"]
      TD["**Tabular Data**<br/>(raw dataset)"]
      CEM["**Neural architectures that generate conceptual representations**<br/><i>CEM</i>"]
      RE["**Rule extraction**<br/>(compositional rules)<br/><i>Deep Concept Reasoners (DCR)/Logic-Explained Networks</i>"]
      CSI["**Conceptual-symbolic Interface**<br/>(learned/elicited)"]

      TD -->|Inputs| CEM
      CEM -->|Activations| RE
      RE -->|Candidate symbolic rules| CSI
    end

    subgraph SYM["SYMBOLIC REGIME"]
      DM["<i><b>Dictionary Mapping (SDD Core)</b></i><br/><i>col → ontology term / IRI<br/>value → Class/Property</i>"]
      CB["<i><b>Codebook & Code Mapping</b></i><br/><i>(values, units)</i>"]
      KG["<i><b>RDF/Knowledge Graph</b></i><br/><i>(triples, instances)<br/>SPARQL/SWRL</i>"]
      ONT["**Ontology**<br/>(classes, relations,<br/>axioms, constraints)"]
      SIV["**Symbolic Inference & Validation**<br/>(consistency,<br/>constraints)"]

      DM -->|Mappings| CB
      CB -->|Serialization| KG
      DM -->|Vocabulary & constraints| ONT
      KG -->|Query/rule-based inference| SIV
      ONT -->|Axioms| SIV
    end

    CSI -->|Ontological unpacking| ONT
    ONT -->|Ontologically-Mediated Concept Rules (OMCR)| CSI
    SIV --> JUST["**Justification**"]
    CSI --> JUST

    classDef case fill:#fff,stroke:#0b5a7a,stroke-width:2px,color:#b64d00;
    classDef node fill:#fff,stroke:#0b5a7a,stroke-width:2px,color:#0b4f70;
    classDef iface fill:#f5c4a8,stroke:#0b5a7a,stroke-width:2px,color:#0b4f70;
    classDef just fill:#b8f29a,stroke:#0b5a7a,stroke-width:2px,color:#0b4f70;
    class DM,CB,KG case;
    class TD,CEM,RE,ONT,SIV node;
    class CSI iface;
    class JUST just;
```

*Figure 3. Bridging two computational and epistemic regimes. Concept-based rules extracted or reconstructed from neural models are ontologically unpacked and transformed into Ontologically Mediated Concept Rules (OMCRs), which support symbolic inference, validation, and justificatory assessment of neural predictions. The ontological and conceptual artifacts instantiated in the case study are highlighted in orange italics (here, CEM and SDD).*

## Note

This repository version uses a GitHub-rendered Mermaid representation of the figure so that the conceptual structure remains directly viewable and editable in the repository.
