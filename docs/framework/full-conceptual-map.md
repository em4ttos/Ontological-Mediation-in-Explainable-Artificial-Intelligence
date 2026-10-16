# Full Conceptual Map

**Related paper:** *Ontological Mediation in Explainable Artificial Intelligence: Concept-Based Models and Ontology-Grounded Explanatory Justification*  
**Authors:** Eduardo M. P. Coelho; Marcello Peixoto Bax  
**Preprint:** SciELO Preprints  
**DOI:** 10.1590/SciELOPreprints.18206  
**Status:** Supplementary visual artifact  
**Version:** 0.1 — October 2026  
**Documentation license:** CC BY 4.0

```mermaid
flowchart TB
    RR["**Raw Reality (World)**<br/>The world as it exists,<br/>independent of our theories.<br/>Accessed through natural<br/>perception or artificial sensors."]
    DATA["**Data**<br/>Empirical observations<br/>and measurements"]
    CBM["**Concept-based Model**<br/>Learns concept<br/>representations from<br/>data"]
    CR["**Conceptual Rule**<br/>Predictive and formal<br/>artifact derived from<br/>the model representing<br/>concepts"]

    NEC["**Normative Epistemic Context**<br/>Historically situated horizon of the epistemic community | Shared domain knowledge accumulated across generations | Intersubjective normative commitments (commitments & entitlements) | Scientific practices and accepted methods | Evidential standards and inferential norms | Institutional and ethical norms | Continuously revised by empirical findings and critical evaluation"]
    DR["**Domain Reality and Empirical Configuration**<br/>Entities, qualities, relations,<br/>processes and states of affairs<br/>instantiated in the domain.<br/>Their actual configuration<br/>constrains reference, truth and<br/>explanatory adequacy"]
    ONT["**Ontology**<br/>Formal representation of domain knowledge.<br/>Concepts, relations, identity criteria, axioms,<br/>and domain commitments"]
    OG["**Ontological Grounding**<br/>Aligns explanatory entities and relations<br/>with domain reality"]
    SG["**Semantic Grounding**<br/>Connects concepts and relations to their meaning,<br/>denotation and interpretation within the domain,<br/>and context"]
    OU["**Ontological Unpacking**<br/>Makes assumptions and commitments explicit"]

    OM["**Ontological Mediation**<br/>Coordinates learned conceptualizations with explicit<br/>ontological commitments"]
    WT["**Weak Truthbearer**<br/>Semantic epistemic<br/>property of an OMCR:<br/>supports justificatory<br/>claims but does not fully<br/>determine truth"]
    OMCR["**Ontologically Mediated Concept Rule (OMCR)**"]
    JA["**Justificatory Assessment**<br/>Evaluates coherence, admissibility, relevance, and epistemic stability"]

    RR -->|encoded as| DATA
    DATA -->|processed by| CBM
    CBM -->|reconstructs| CR
    CR -->|is mediated by| OM

    NEC -->|constrains admissible semantic interpretations| ONT
    NEC -->|anchors| DR
    DR -->|shapes| NEC
    ONT -->|provides| OG
    ONT -->|provides| SG
    ONT -->|guides| OU
    OG -->|supports| OU
    SG -->|supports| OU
    OU -->|supports| OM

    OM -->|selects, activates and operationalizes| OMCR
    WT -->|underpins| OMCR
    NEC -->|grounds| OMCR
    DR -->|supplies empirical instances for justificatory evaluation| WT
    OMCR -->|supports| JA
    DR -->|constrains explanatory and justificatory adequacy| JA

    subgraph FP["FUNDAMENTAL PRINCIPLES"]
      DA["**Dual Anchoring**<br/>Explanations are anchored both in the domain reality (ontic constraint) and in the epistemic community (normative constraint)"]
      CP["**Complementary Roles**<br/>Models learn only from data. Normative criteria and ontologies guide interpretation, mediation, and evaluation, but do not feed into the learning model"]
      FR["**Fallibilist Realism**<br/>Knowledge is historically situated and revisable, yet accountable to the domain reality that constrains truth and explanatory adequacy"]
    end

    classDef contribution fill:#fff0b8,stroke:#111,stroke-width:4px,color:#111;
    classDef context fill:#f8e5d8,stroke:#111,stroke-width:2px,color:#111;
    classDef neutral fill:#fff,stroke:#111,stroke-width:2px,color:#111;
    class OM,WT,OMCR,JA contribution;
    class NEC,DR,ONT,OG,SG,OU,CR context;
    class RR,DATA,CBM neutral;
```

*Figure 1. High-level conceptual map of the proposed ontology mediated justification framework. The diagram illustrates how domain reality shapes normative epistemic contexts, how ontological structures constrain admissible semantic interpretations, and how Ontological Mediation operationalizes Ontologically Mediated Conceptual Rules (OMCRs) to support context-dependent justificatory assessments through weak truthbearers. The blocks with a yellow background and thick outline indicate the authors’ contributions.*

## Note

This repository version uses a GitHub-rendered Mermaid representation of the conceptual map so that the artifact remains directly viewable and editable in the repository.
