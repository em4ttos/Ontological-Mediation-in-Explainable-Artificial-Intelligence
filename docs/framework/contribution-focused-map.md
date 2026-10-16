# Contribution-Focused Conceptual Map

**Related paper:** *Ontological Mediation in Explainable Artificial Intelligence: Concept-Based Models and Ontology-Grounded Explanatory Justification*  
**Authors:** Eduardo M. P. Coelho; Marcello Peixoto Bax  
**Preprint:** SciELO Preprints  
**DOI:** 10.1590/SciELOPreprints.18206  
**Status:** Supplementary visual artifact  
**Version:** 0.1 — October 2026  
**Documentation license:** CC BY 4.0

```mermaid
flowchart TB
    CR["**Conceptual Rule**<br/>Predictive and formal<br/>artifact derived from<br/>the model representing<br/>concepts"]
    OU["**Ontological Unpacking**<br/>Makes assumptions and commitments explicit"]
    OM["**Ontological Mediation**<br/>Coordinates learned conceptualizations with explicit<br/>ontological commitments"]
    OMCR["**Ontologically Mediated Concept Rule (OMCR)**"]
    WT["**Weak Truthbearer**<br/>Semantic epistemic<br/>property of an OMCR:<br/>supports justificatory<br/>claims but does not fully<br/>determine truth"]
    NEC["**Normative Epistemic Context**<br/>Historically situated horizon of the epistemic community | Shared domain knowledge accumulated across generations | Intersubjective normative commitments (commitments & entitlements) | Scientific practices and accepted methods | Evidential standards and inferential norms | Institutional and ethical norms | Continuously revised by empirical findings and critical evaluation"]
    JA["**Justificatory Assessment**<br/>Evaluates coherence, admissibility, relevance, and epistemic stability"]

    CR -->|is mediated by| OM
    OU -->|supports| OM
    OM -->|selects, activates and operationalizes| OMCR
    WT -->|underpins| OMCR
    NEC -->|grounds| OMCR
    OMCR -->|supports| JA

    classDef contribution fill:#fff0b8,stroke:#111,stroke-width:4px,color:#111;
    classDef context fill:#f8e5d8,stroke:#111,stroke-width:2px,color:#111;
    class OM,OMCR,WT,JA contribution;
    class CR,OU,NEC context;
```

*Figure 2. Focused conceptual map of the core ontology-mediated justification pathway. The diagram shows how a Conceptual Rule, together with Ontological Unpacking, is mediated into an Ontologically Mediated Concept Rule (OMCR), grounded in the Normative Epistemic Context and underpinned by weak-truthbearer semantics, to support Justificatory Assessment. Yellow blocks with thick outlines indicate the authors’ principal contributions.*

## Note

This focused view isolates the core mediation and justification pathway from the broader conceptual architecture. The repository version uses a GitHub-rendered Mermaid representation so that the artifact remains directly viewable and editable.
