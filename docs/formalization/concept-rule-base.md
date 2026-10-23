# Concept-Rule Base (CRB)

## Conceptualization, Knowledge Graphs, Generalization, and Research Scope

*Supplementary Conceptual and Methodological Note*

**Related paper:** *Ontological Mediation in Explainable Artificial Intelligence: Concept-Based Models and Ontology-Grounded Explanatory Justification*  
**Authors:** Eduardo M. P. Coelho; Marcello Peixoto Bax  
**Preprint:** SciELO Preprints  
**DOI:** 10.1590/SciELOPreprints.18206  
**Status:** Post-preprint supplementary development  
**Version:** 0.2 — October 2026  
**Documentation license:** CC BY 4.0

> **Terminological and architectural note.** The published article uses **Conceptual Rule** for the explicit concept-level representational unit associated with an inferential or decisional structure. **Concept-Rule Base (CRB)** is a post-preprint generalization introduced in this supplementary material. A CRB may contain or organize one or more Conceptual Rules and their associated concept-level relations, or encode a conceptual structure from which such rules can be derived. CRB therefore does not retroactively replace the terminology of the published article. Importantly, **CRB is not an additional processing stage within the Ontological Mediation framework**. It is a conceptual and methodological reference used to characterize whether a computational artifact exposes, generates, or permits the faithful reconstruction of the kind of concept-level structure required for the framework to be applicable beyond the motivating CEM case.

## Contents

1. [Initial CRB Conceptualization and Generalization](#1-initial-crb-conceptualization-and-generalization)
2. [Candidate AI Model Families for CRB Generation or Reconstruction](#2-candidate-ai-model-families-for-crb-generation-or-reconstruction)
3. [Can a Knowledge Graph Qualify as a CRB?](#3-can-a-knowledge-graph-qualify-as-a-crb)
4. [Ontological KG, Query/Reasoning, and CRB Extraction](#4-ontological-kg-queryreasoning-and-crb-extraction)
5. [Broader Importance: CRB as an Applicability and Generalization Framework](#5-broader-importance-crb-as-an-applicability-and-generalization-framework-for-ai-kg-xai-and-neuro-symbolic-systems)
6. [Consolidated Synthesis](#6-consolidated-synthesis)

---

# 1. Initial CRB Conceptualization and Generalization

Building on the terminological distinction above, the **Concept-Rule Base** should not be defined from the specific syntax observed in a Concept Embedding Model (CEM). The CEM is a representative example, but it should not determine the formal limits of the CRB. A more robust strategy is first to characterize what makes a structure qualify as a Concept-Rule Base, and then to treat conjunction, disjunction, polarity, weights, fuzzy degrees, thresholds, and regression relations as different expressive capabilities of a concept-rule language.

## 1.1 Core conceptual role

The central idea is that a model may remain sub-symbolic in its internal mechanism while its decision can still be expressed, or faithfully reconstructed, at an explicit concept level. The motivating CEM case provides one concrete instance of this situation, but it should not determine the limits of framework applicability.

The CRB concept was introduced to characterize the broader class of computational artifacts whose outputs, internal structures, or reconstructed relations satisfy the relevant concept-level conditions. Its role is therefore **diagnostic, classificatory, and scope-defining**, rather than procedural within the Ontological Mediation architecture.

```text
Candidate Computational Artifact
        |
        v
CRB Admissibility Criteria
        |
        +--> qualifies --> suitable concept-level explanatory structure
        |                   may enter the Ontological Mediation framework
        |
        +--> does not qualify --> framework not directly applicable in the same form
```

For the motivating CEM case, the internal explanatory sequence remains:

```text
CEM -> Conceptual Rules -> Ontological Unpacking
    -> Ontological Mediation / OMCRs -> Justificatory Assessment
```

Accordingly, **CRB is not an intermediate processing layer between Conceptual Rules and Ontological Unpacking**. It is a generalization used to determine whether artifacts from CEMs or other computational families provide the kind of concept-level structure to which the framework can be applied.

## 1.2 Preliminary definition

A preliminary formulation is:

> **Concept-Rule Base (CRB).** A Concept-Rule Base is a structured representation of the concept-level regularities, dependencies, or decision relations that are natively expressed by, extracted from, or faithfully reconstructed from a computational decision or inference process, such that model inputs, intermediate conceptual representations, or outputs can be related through explicit compositions of human-interpretable concepts.

## 1.3 Why CRB cannot mean only a classical rule set

If a CRB were restricted to rules of the form $C_1 \land C_2 \rightarrow y$, it would fit the CEM/rule-extraction case but would exclude other concept-level structures that may satisfy the same general applicability conditions for subsequent use within the Ontological Mediation framework.

Examples include:

$$
(C_1 \land C_2) \lor C_3 \rightarrow y
$$

$$
0.8C_1 + 0.3C_2 - 0.6C_3 \ge \tau \rightarrow y
$$

$$
T(\mu_{C_1}(x),\mu_{C_2}(x)) \ge \tau \rightarrow y
$$

$$
P(y=1\mid C)=\sigma\left(\beta_0+\sum_i\beta_i C_i\right)
$$

$$
\hat{y}=\beta_0+\sum_i\beta_i C_i
$$

All of these may qualify if the concepts are explicitly recoverable and the relation between them and the output is sufficiently explicit. Therefore, **rule** should be understood broadly as an explicit concept-level relation relevant to a computational conclusion, rather than only as a material-implication-like expression.

## 1.4 Parametric Concept-Rule Language

A promising abstraction is:

$$
CRB=(\mathcal{C},\mathcal{Y},\mathcal{L},\mathcal{R})
$$

where:

- $\mathcal{C}$ is a concept vocabulary;
- $\mathcal{Y}$ is an output/conclusion space;
- $\mathcal{L}$ is a **Concept-Rule Language**;
- $\mathcal{R}$ is the set of Conceptual Rules expressed, extracted, or reconstructed in that language.

Because provenance is central but need not be constitutive of the tuple itself, source relativity can be represented explicitly by an external relation such as:

$$
DerivedFrom(CRB,SourceProcess)
$$

This makes an important distinction possible: the **CRB schema is source-agnostic**, because the same abstract representational form can be instantiated from neural, statistical, symbolic, graph-based, or hybrid sources; each **concrete CRB is source-relative**, because its admissibility and fidelity depend on the decision or inference process from which it was derived.

The language $\mathcal{L}$ may vary across systems, for example:

$$
\mathcal{L}_{Bool},\;\mathcal{L}_{Weighted},\;\mathcal{L}_{Fuzzy},\;\mathcal{L}_{Regression},\ldots
$$

This avoids saying that every CRB must contain weights, fuzzy membership, or disjunction. These become **orthogonal expressive capabilities**.

## 1.5 Polarity, weight, and fuzzy degree must remain distinct

Polarity is not classical negation. The existing distinction should be preserved:

$$
polarity(C_i)\in\{positive, nonPositive, unspecified\}
$$

A non-positive contribution should not be identified with $\neg C_i$. It indicates **contribution semantics**, not logical negation.

Similarly, weight and fuzzy membership are not the same thing:

$$
weight(C_i)\neq membershipDegree(C_i,x)
$$

A weight may represent predictive contribution magnitude, while a fuzzy degree expresses graded satisfaction or instantiation. Both may coexist, for example $w_i\cdot\mu_{C_i}(x)$.

## 1.6 CRB families should not be treated as mutually exclusive

**Table 1. Family-similarity criteria for CRB adequacy**

| Family | Typical form | Preserved structure |
|---|---|---|
| Logical CRB | $C_1 \land C_2 \rightarrow y$ | Logical composition |
| Polarized CRB | $C_1^{+} \land C_2^{np} \rightarrow y$ | Qualitative contribution direction |
| Weighted / Fuzzy CRB | $F(w_i,\mu_i(C_i)) \rightarrow y$ | Magnitude and/or degree |
| Functional CRB | $y=f(C_1,\ldots,C_n)$ | Quantitative / functional relation |

These are better understood as **overlapping capabilities** than as a closed type enumeration.

## 1.7 Fidelity and traceability

A CRB cannot be an arbitrary conceptual story invented after the model has produced an output. At minimum, the representation should satisfy:

```text
Explicitness + Interpretability + Fidelity (+ Traceability)
```

This leads to a stronger general definition:

> **Concept-Rule Base (CRB).** A Concept-Rule Base is a structured, source-relative representation of explicit concept-level relations that are natively expressed by, extracted from, or faithfully reconstructed from a computational decision or inference process. A CRB specifies human-interpretable concepts, their relevant relations or compositions, and their connection to conclusions or outputs. Depending on the underlying source and reconstruction method, Conceptual Rules may employ logical conjunction and disjunction, qualitative contribution polarity, quantitative weights, graded or fuzzy concept satisfaction, thresholds, or functional relations such as those occurring in classification and regression. These representational structures remain computationally and representationally relative: they do not by themselves constitute ontological commitments or justificatory constraints. Qualifying as a CRB therefore indicates that the relevant kind of concept-level structure is available; it does not insert a CRB stage into the internal Ontological Mediation process.

```text
CRB ≠ Ontology
CRB ≠ OMCR
Predictive Contribution ≠ Justificatory Support
```

---

# 2. Candidate AI Model Families for CRB Generation or Reconstruction

The CRB generalization is not intended as a universal explanation framework for arbitrary computational artifacts or scientific theories. Its purpose is narrower: to identify which computational artifacts provide, or permit the faithful reconstruction of, a sufficiently explicit concept-level structure to make the Ontological Mediation framework potentially applicable.

The motivating target is a predictive system whose decision can be reconstructed at the level of human-interpretable concepts. More precisely, the framework addresses cases in which lower-level features are associated or composed into decision-relevant concepts and these concepts support a classification, prediction, diagnosis, recommendation, or other computational conclusion.

Native concept-based architectures, such as CBMs, CEMs, and neural concept reasoners, provide direct candidate instances of this setting; post-hoc concept-based methods may also qualify when they recover a faithful and sufficiently explicit conceptual structure from a conventional black-box model. Although the motivating work is primarily concerned with neural black-box models, the CRB criteria allow the applicability question to be asked of intrinsically interpretable, symbolic, probabilistic, graph-based, and hybrid systems as well.

## 2.1 Candidate model families

The table does **not** claim that every model belonging to the listed families intrinsically produces CRBs. Rather, it identifies model families whose internal representations, explicit rules, intermediate concepts, prototypes, latent structures, or observable decision mechanisms may support the reconstruction of a CRB when the relevant elements satisfy the required semantic and conceptual admissibility conditions.

### Compatibility levels

> **Classification status.** The compatibility levels below are an analytical device introduced in this supplementary development. They are not presented as an established taxonomy of the corresponding model families.

- **Direct (D):** concepts or conceptual predicates participate explicitly in the architecture or decision.
- **Strongly Conditional (SC):** the structure is particularly suitable for conceptual reconstruction, but it must be demonstrated that its elements effectively correspond to concepts.
- **Conditional (C):** the model can originate a CRB only through additional interpretation or reconstruction of variables, factors, rules, or representations.

**Table 2. Model families potentially generating CRBs or serving as sources for CRB reconstruction**

| No. | Model / family | Relevant representation | Route to CRB | Compat. | Admissibility condition as CRB source | Main semantic risk | Fundamental / representative reference |
|---:|---|---|---|:---:|---|---|---|
| 1 | Concept Bottleneck Models (CBMs) | Explicit vector of intermediate concepts | Final prediction expressed as a function of bottleneck concepts | D | Each bottleneck dimension must correspond to an identifiable and interpretable concept | Annotated concepts may be shallow, incomplete, or operationally defined | Koh et al. (2020), *Concept Bottleneck Models*, ICML |
| 2 | Concept Embedding Models (CEMs) | Embeddings explicitly associated with concepts | Rule reconstructed from conceptual activations/embeddings and the decision | D/SC | The embedding must preserve sufficiently determinate conceptual identity | Embedding may carry residual information not belonging to the declared concept | Espinosa Zarlenga et al. (2022), *Concept Embedding Models*, NeurIPS |
| 3 | Intervention-Aware CEMs (IntCEMs) | Intervenable concept embeddings | CRB derived from the conceptual state after interventions | D | Interventions must correspond to semantically legitimate changes in concepts | Operational correctness of an intervention does not guarantee ontological correctness of the concept | Espinosa Zarlenga et al. (2023), *Learning to Receive Help*, NeurIPS |
| 4 | Hierarchical CEMs / hierarchical concepts | Explicit concept hierarchies | CRB may use concepts at different granularity levels | D | Hierarchical relations must have a defensible semantic interpretation | Learned hierarchy may reflect statistical correlation rather than ontological subsumption | Hill, Espinosa Zarlenga & Jamnik (2026), *Hierarchical Concept-based Interpretable Models*, ICLR |
| 5 | Post-hoc Concept Bottleneck Models (PCBMs) | Conceptual space projected onto a pretrained model | Concepts are fitted to an existing latent representation and used in the decision | SC | Projections must represent concepts and preserve enough information to explain the decision | Post-hoc concepts may rationalize rather than reflect the original mechanism | Yuksekgonul, Wang & Zou (2023), *Post-Hoc Concept Bottleneck Models*, ICLR |
| 6 | Language-guided Concept Bottlenecks | Linguistically obtained/described concepts | A language model proposes concepts that feed an interpretable bottleneck | SC | Linguistically generated concepts must be semantically validated/adopted | Linguistic fluency may mask spurious, redundant, or ontologically inadequate concepts | Yang et al. (2023), *Language in a Bottle*, CVPR |
| 7 | Deep Concept Reasoner (DCR) | Predicates/concepts with truth degrees | Logical-conceptual rules are explicitly learned over concepts | D | Predicates must possess identifiable domain semantics | A logically readable rule may operate over semantically fragile concepts | Barbiero et al. (2023), *Interpretable Neural-Symbolic Concept Reasoning*, ICML |
| 8 | Neuro-symbolic models based on conceptual predicates | Logical or fuzzy predicates grounded in neural representations | CRB corresponds to implications or formulas over predicates | D/SC | Predicates must possess conceptual interpretation beyond merely numerical grounding | Continuous grounding may be confused with ontological grounding | Serafini & Garcez (2016), *Logic Tensor Networks* |
| 9 | SENNs | Interpretable concepts/bases + relevance scores | Local explanation combines concepts with case-specific relevances | SC | Learned bases must be semantically intelligible and relatively stable | Components called “concepts” may be only latent mathematical factors | Alvarez-Melis & Jaakkola (2018), *Self-Explaining Neural Networks*, NeurIPS |
| 10 | Self-attributing models with feature groups | Self-attributed feature groups | CRB reconstructed from relevant groups and their weights/contributions | SC | Groupings must map to coherent conceptual units | A statistical feature group is not automatically a concept | You et al. (2025), *Sum-of-Parts*, ICML |
| 11 | ProtoPNet and derived families | Visual prototypes associated with parts/examples | Decision expressed through similarity between input parts and prototypes | SC | Prototypes must be interpretable as domain-relevant types, parts, or concepts | Visual similarity does not imply conceptual identity | Chen et al. (2019), *This Looks Like That*, NeurIPS |
| 12 | Transparent Embedding Spaces / TesNet | Prototypes and transparent subspaces | CRB derivable from associations among embeddings, prototypes, and classes | SC | The space structure must correspond to relevant conceptual distinctions | Interpretable geometry may remain semantically underdetermined | Wang et al. (2021), *Interpretable Image Recognition by Constructing Transparent Embedding Space*, ICCV |
| 13 | Concept Whitening | Latent axes aligned with concepts | Activation along conceptual axes informs the decision | SC | Alignment of each axis with a concept must be demonstrated | Forced alignment does not guarantee conceptual purity or independence | Chen, Bei & Rudin (2020), *Concept Whitening*, Nature Machine Intelligence |
| 14 | Sparse concept recovery / concept dictionaries | Sparse bases or dictionaries of features/concepts | CRB extracted from sparse combinations of interpretable units | SC/C | Recovered components must correspond to stable conceptual units | Sparsity and monosemanticity are representational properties, not ontological guarantees | Yeh et al. (2020), *Completeness-aware Concept-Based Explanations*; Bricken et al. (2023), *Towards Monosemanticity* |
| 15 | CAVs / TCAV | Vector directions associated with concepts | CRB reconstructs the relation between concept presence/direction and output | SC | The CAV must adequately discriminate examples of the concept | Linear separability may not equal internal representation of the concept | Kim et al. (2018), *TCAV*, ICML |
| 16 | CAVLI / local concept-based explanations | CAVs and local associations | Local CRB relates detected concepts to an individual decision | SC | Local concepts must be valid and causally/relevantly connected to the case | Local explanation may be unstable or merely correlational | Shukla, Bharati & Turk (2023), *CAVLI*, CVPR Workshops |
| 17 | Concept generation / automatic concept discovery | Automatically discovered clusters/segments | CRB formed from discovered concepts and their importance for classes/decisions | SC/C | Clusters must be interpretable and adopted as concepts | Statistical cluster may not correspond to a real or relevant concept | Ghorbani et al. (2019), *Towards Automatic Concept-Based Explanations*, NeurIPS |
| 18 | Interaction Concepts | Interaction patterns among variables/units | CRB reconstructed from recurring interpretable interactions | SC | Mathematical interaction must have a coherent conceptual interpretation | A “concept” may correspond only to an algebraic interaction | Li & Zhang (2023), *Does a Neural Network Really Encode Symbolic Concepts?*, ICML |
| 19 | Part-based neural networks | Parts or local components | CRB uses presence/configuration of parts to infer class | SC | Detected parts must constitute relevant conceptual units | Visual region ≠ ontological part; part ≠ concept automatically | Zhang, Wu & Zhu (2018), *Interpretable Convolutional Neural Networks*, CVPR |
| 20 | Object-centric models | Latent slots/objects | CRB relates detected entities and properties to prediction | SC/C | Slots must correspond stably to recognizable objects or entities | A learned slot may not represent a consistent individual object | Locatello et al. (2020), *Object-Centric Learning with Slot Attention*, NeurIPS |
| 21 | Capsule Networks | Capsules representing entities/properties | CRB reconstructed from activations and part-whole relations | SC/C | Capsules must have verifiable semantic interpretation | Vector structure does not guarantee consistent conceptual representation | Sabour, Frosst & Hinton (2017), *Dynamic Routing Between Capsules*, NeurIPS |
| 22 | Disentangled representation models | Disentangled latent factors | CRB derived from factors interpreted as properties/concepts | C | Each factor must have empirically justified conceptual correspondence | Statistical disentanglement ≠ semantic separation | Higgins et al. (2017), *β-VAE*, ICLR |
| 23 | Concept-based / self-explainable GNNs | Concepts associated with nodes, edges, subgraphs, or patterns | CRB derives relations between structural concepts and graph prediction | D/SC | Graph concepts must be semantically identifiable | Frequent motif/subgraph may not correspond to a meaningful concept | Magister et al. (2023), *Concept Distillation in Graph Neural Networks*, xAI |
| 24 | Hypergraph neural networks | N-ary relations / hyperedges | CRB possible when hyperedges and attributes admit conceptual interpretation | C | Modeled relations must correspond to domain-conceptual relations | Formal relational structure does not imply conceptual interpretation | Feng et al. (2019), *Hypergraph Neural Networks*, AAAI |
| 25 | Vision-language models | Multimodal representations aligned with language | CRB obtained from recovered or generated linguistic/visual concepts | C/SC | Textualized concepts must be identified and critically adopted | Text-image alignment may import biases and spurious semantic associations | Radford et al. (2021), *Learning Transferable Visual Models From Natural Language Supervision*, ICML |
| 26 | Large Language Models | Tokens, embeddings, and generated linguistic representations | CRB produced/reconstructed as a proposition or conceptual rule expressed linguistically | C | Concepts and rules must be treated as candidates and subjected to critical adoption | Linguistic generation does not confer epistemic authority; hallucination and rationalization risks | Vaswani et al. (2017), *Attention Is All You Need*; Brown et al. (2020), *Language Models are Few-Shot Learners* |
| 27 | Logistic regression | Observed variables + coefficients | Conceptual rule reconstructed from variable contributions and decision threshold | C | Variables must possess adequate conceptual interpretation | An operational feature may be mistaken for a concept; coefficient does not imply causality | Cox (1958), *The Regression Analysis of Binary Sequences* |
| 28 | Generalized linear models | Conceptually named variables + link function | CRB obtained from the parameterized relation between concepts and response | C | Predictors must correspond to concepts and the relation must be interpretable in the domain | A statistical link may be reified as a conceptual or causal relation | Nelder & Wedderburn (1972), *Generalized Linear Models* |
| 29 | Generalized additive models | Univariate/additive functions by attribute | CRB expresses conceptually interpretable conditions and contributions | C/SC | Variables must be conceptual and functions sufficiently intelligible | An intelligible curve does not guarantee adequate attribute semantics | Hastie & Tibshirani (1986), *Generalized Additive Models* |
| 30 | Explainable Boosting Machines | Additive functions by feature and selected interactions | CRB reconstructed from attribute/interaction functions | SC | Features and interactions must have conceptual interpretation | Functional transparency may hide proxies, correlations, and construct mismatch | Nori et al. (2019), *InterpretML*; Lou et al. (2013), *Accurate Intelligible Models with Pairwise Interactions* |
| 31 | Lasso / Elastic Net | Sparse set of predictors | CRB generated from selected variables and coefficients | C | Selected predictors must correspond to concepts | Sparse selection does not imply conceptual importance or stability | Tibshirani (1996), *Lasso*; Zou & Hastie (2005), *Elastic Net* |
| 32 | Scoring models / scorecards | Points assigned to explicit conditions | Rule already approximates “if condition, add score” form | SC | Score items must represent valid properties/concepts | Discretization and weights may create a false impression of conceptual grounding | Ustun & Rudin (2016), *Supersparse Linear Integer Models* |
| 33 | Decision trees | Explicit tests over attributes | Root-to-leaf path can be converted directly into a rule | SC | Each split must correspond to a semantically acceptable predicate | A syntactically readable condition may be semantically arbitrary | Breiman et al. (1984), *Classification and Regression Trees* |
| 34 | Rule lists / decision sets | Explicit propositional rules | Model rules can directly assume CRB form | SC/D | Antecedents and consequents must be conceptually interpretable | Explicit rule ≠ ontologically grounded rule | Letham et al. (2015); Lakkaraju, Bach & Leskovec (2016) |
| 35 | Fuzzy systems | Linguistic variables, fuzzy terms, and rules | Fuzzy rules may constitute graded CRBs | D/SC | Linguistic terms and membership functions must have domain interpretation | Membership degree may be confused with degree of ontological truth | Mamdani & Assilian (1975), *An Experiment in Linguistic Synthesis with a Fuzzy Logic Controller* |
| 36 | Naïve Bayes | Observed variables and conditional probabilities | CRB reconstructed from conceptual evidence and probabilistic relation to class | C | Features must represent appropriate concepts | Conditional independence is a statistical assumption, not a conceptual domain structure | Domingos & Pazzani (1997), *On the Optimality of the Simple Bayesian Classifier* |
| 37 | Bayesian networks | Variables/nodes and probabilistic dependencies | CRB derived from explicitly structured probabilistic relations | SC/C | Nodes must have conceptual meaning and arcs an appropriate interpretation | Probabilistic dependence may be incorrectly interpreted as causal or ontological | Pearl (1988), *Probabilistic Reasoning in Intelligent Systems* |
| 38 | Probabilistic graphical models | Variables and factors in a graph structure | CRB extractable from conceptually named dependencies and factors | C | Nodes/factors must have explicit semantics | Formal graph structure does not determine the ontological nature of relations | Koller & Friedman (2009), *Probabilistic Graphical Models* |
| 39 | LDA / QDA | Discriminant combinations of attributes | CRB reconstructed from discriminative attributes and decision boundaries | C | Variables must have conceptual meaning and the combination must be interpretable | Linear/quadratic combination may lack a natural conceptual reading | Fisher (1936), *The Use of Multiple Measurements in Taxonomic Problems* |
| 40 | Linear SVM | Hyperplane defined by feature weights | CRB reconstructed from signs, weights, and threshold | C | Features must have conceptual meaning and appropriate scaling | Geometric margin has no semantic meaning by itself | Cortes & Vapnik (1995), *Support-Vector Networks* |
| 41 | Prototype- and neighbor-based models | Exemplars/prototypes and similarity measures | CRB may express conceptual similarity to cases/prototypes | SC/C | Distance and prototypes must reflect semantically relevant properties | Geometric similarity ≠ conceptual similarity | Cover & Hart (1967), *Nearest Neighbor Pattern Classification* |
| 42 | Latent factor models | Hidden factors extracted from observations | CRB possible after interpreting factors as concepts | C | Factors must be stable, identifiable, and semantically interpreted | Rotation, non-identifiability, and polysemy of factors | Lee & Seung (1999), *Learning the Parts of Objects by Non-negative Matrix Factorization* |
| 43 | Structural equation models (SEM) | Observed/latent variables and structural relations | CRB derives explicit relations among constructs | SC/C | Latent constructs must be theoretically and ontologically characterized | A statistically identified construct may remain conceptually ill-defined | Jöreskog (1970), *A General Method for Analysis of Covariance Structures* |
| 44 | Latent class / mixture models | Latent classes/components | CRB obtained by interpreting each class/component as a conceptual type | C | Components must correspond to conceptually defensible categories | Probabilistic cluster/component ≠ ontological kind, type, or class | McLachlan & Peel (2000), *Finite Mixture Models* |
| 45 | Case-based reasoning systems | Structured cases and similarity/adaptation relations | CRB generalized from recurring patterns among cases | SC/C | Case representation and similarity criteria must have a conceptual basis | Pragmatic similarity among cases may not support conceptual generalization | Aamodt & Plaza (1994), *Case-Based Reasoning* |
| 46 | Neuro-symbolic and logical models | Symbols, predicates, rules, neural structures, and reasoning | CRB may coincide with symbolic rules extracted, learned, or combined with neural components | D/SC | Symbols and predicates must have explicit conceptual interpretation | Logical formalization does not guarantee ontological grounding or epistemic adequacy | d’Avila Garcez, Lamb & Gabbay (2009), *Neural-Symbolic Cognitive Reasoning* |

## 2.2 Methodological families by route to CRB

These model families can in turn be grouped according to the **route by which a CRB is obtained**. The table below shows that only a limited number of general mechanisms are needed for a computational structure to provide the raw material for a CRB.

**Table 3. Candidate methodological families for Concept-Rule Base reconstruction**

| Methodological family | Route to CRB | Examples |
|---|---|---|
| Explicit concept bottleneck | Concepts are intermediate components of the architecture itself | CBM, CEM, IntCEM, HiCEM, PCBM |
| Reasoning over concepts/predicates | Decision occurs explicitly over conceptual units | DCR, LTN, neuro-symbolic models |
| Learned interpretable concepts, bases, or prototypes | The model learns intermediate units—such as concepts, interpretable bases, parts, prototypes, or aligned directions—that may support CRB reconstruction when those units satisfy semantic admissibility conditions | SENNs, ProtoPNet, TesNet, Concept Whitening |
| Post-hoc concepts | Concepts are projected onto or discovered within an already trained representation | TCAV, ACE, CAVLI, concept dictionaries |
| Semantically recoverable latent structures | A factor, slot, or capsule must later be interpreted as a concept | Slot Attention, β-VAE, latent factors |
| Transparent rules over features | The decision structure is already explicitly readable | Decision trees, rule lists, fuzzy systems, scorecards |
| Transparent parametric models | CRB results from conceptual interpretation of variables and coefficients/functions | Logistic regression, GLM, GAM, EBM, Lasso |
| Probabilistic structures | CRB results from conceptual interpretation of probabilistic dependencies | Naïve Bayes, Bayesian networks, PGMs |
| Similarity / exemplar-based structures | Decision is based on prototypes, neighbors, or cases | k-NN, LVQ, case-based reasoning |
| Linguistic / multimodal generation and grounding | Linguistic or multimodal models provide candidate concepts/rules | VLMs, LLMs, language-guided bottlenecks |
| Relational and graph-based structures | Concepts and relations are explicitly represented, inferred, or learned over graph or hypergraph structures and may support the reconstruction of a concept-level inferential or decisional structure | Knowledge Graphs, ontology reasoners, GNNs, hypergraph neural networks |
| Statistical latent constructs and structures | Latent factors, classes, or constructs require theoretical and semantic interpretation | Structural Equation Models (SEM), mixture models, latent factor models |

Consequently, **model-level interpretability is neither necessary nor sufficient by itself for conceptual admissibility**. A transparent decision structure may still manipulate semantically inadequate variables, whereas a less transparent model may expose intermediate representations that can be legitimately reconstructed as concepts.

A CRB may therefore be better characterized **not by the class of model that produces it, but by the properties of the reconstructed artifact**. In that case, a CBM, decision tree, LLM, or regression model ceases to be constitutive of the definition and instead becomes a possible **provenance mechanism**.

The following section examines one increasingly important case: **Knowledge Graphs**.

---

# 3. Can a Knowledge Graph Qualify as a CRB?

A Knowledge Graph can instantiate or realize a CRB, but a Knowledge Graph as such is not automatically a CRB. The rigorous distinction is:

```text
KnowledgeGraph ≠> CRB
KnowledgeGraph + Explicit Concept-Level Decision Structure + Output Linkage + Fidelity => CRB
```

## 3.1 Why an ordinary KG is not automatically a CRB

A Knowledge Graph may represent entities, relations, types, attributes, and axioms. This is sufficient for knowledge representation, but not for CRB status if it does not expose how a conceptual configuration is related to a conclusion or output.

```text
Patient123 --hasFinding--> HippocampalAtrophy
```

This may be semantically rich, but it does not yet state:

```text
HippocampalAtrophy -> DementiaPrediction
```

nor the compositional relation:

```text
HippocampalAtrophy AND LowMMSE AND AdvancedAge -> DementiaPrediction
```

## 3.2 Three relevant cases

**Table 4. KG cases relevant to CRB status**

| Case | CRB? | Reason |
|---|---|---|
| Purely descriptive / ontological KG | No, not by itself | Represents knowledge but not necessarily a decision-relevant concept structure |
| KG enriched with predictive / inferential relations | Possibly | May explicitly encode Conceptual Rules |
| KG faithfully reconstructing a decision in concept terms | Yes, provided the CRB admissibility conditions are satisfied | Can qualify when explicitness, interpretability, fidelity, and the relevant traceability/provenance conditions are satisfied |

## 3.3 KG as realization, not identity

```text
CRB ≠ KnowledgeGraph
KnowledgeGraph may realize / encode / express a CRB
```

This distinction allows the CRB to remain at the semantic-abstraction level while graphs, formulas, decision trees, equations, and other structures remain representational realizations.

## 3.4 Conceptual Rule as a representation-independent structure

A Conceptual Rule should therefore not be identified with only one syntax such as $(C_1 \land C_2)\rightarrow y$. It is better understood as a representational entity expressing an explicit concept-level inferential or decisional structure.

Possible realizations include:

- logical formulas;
- decision-tree paths;
- weighted expressions;
- regression equations;
- graph patterns;
- Knowledge Graph fragments.

## 3.5 Graph-native representation of contribution semantics

A KG can naturally reify contribution, polarity, weight, thresholds, and composition. For example:

```text
C1 --positiveContribution--> Y
C2 --nonPositiveContribution--> Y
Contribution(C1, Y) with polarity = positive and weight = 0.72
```

This makes the KG an excellent carrier structure for heterogeneous CRBs.

## 3.6 Domain edges and model-relative edges must remain distinct

A graph must distinguish domain-semantic relations from decision/predictive relations. Otherwise, the architecture risks collapsing reality, representation, and prediction. In the examples below, `--relation-->` denotes a directed, labeled graph edge; the hyphens are purely graphical and do **not** denote negation or subtraction.

```text
Person --hasAge--> Age                         (domain)
Age --positiveContribution--> Prediction      (model-relative)

Reality ≠ Representation ≠ Prediction
```

## 3.7 A single graph may contain multiple layers

$$
G=G_{CRB}\cup G_{Ont}\cup G_{Mapping}
$$

where:

- $G_{CRB}$ may represent what the computational process does;
- $G_{Ont}$ may represent the ontological meaning of the concepts;
- $G_{Mapping}$ may represent explicit mediation between them.

This layered graph representation may make explicit both a CRB-qualifying concept structure and the ontological resources relevant to later mediation. It should not, however, be interpreted as making CRB an internal processing stage of the broader architecture.

---

# 4. Ontological KG, Query/Reasoning, and CRB Extraction

A purely ontological KG can still be a source from which a CRB is derived. The decisive point is not whether predictive edges are explicitly stored in advance, but whether a query or reasoning process can recover the conceptual structure that connects case conditions to a conclusion.

## 4.1 From ontological entailment to conceptual rule

Suppose an ontology $\mathcal{O}$ and patient data $A_p$ entail:

$$
\mathcal{O}\cup A_p\models DementiaCondition(p)
$$

A query or reasoner may recover the conditions that support that conclusion, yielding a concept-level structure such as:

$$
C_1(p)\land C_2(p)\land C_3(p)\Rightarrow DementiaCondition(p)
$$

At this point, the recovered structure **may qualify as a Conceptual Rule**, provided the relevant conceptual and derivational conditions are satisfied.

## 4.2 Multiple justifications can generate multiple rules

In Description Logic terms, a justification $J$ may be a subset of $\mathcal{O}\cup A_p$ such that:

$$
J\models D(p)
$$

and:

$$
\forall J'\subset J,\;J'\not\models D(p)
$$

Projecting one or more minimal justifications to the concept level can produce:

$$
r_1:C_1\land C_2\land C_3\Rightarrow D
$$

$$
r_2:C_1\land C_4\Rightarrow D
$$

$$
CRB_{p,D}=\{r_1,r_2,\ldots\}
$$

Disjunction can arise naturally from the plurality of inferential paths, although it may be preferable to preserve the alternatives as separate rules rather than immediately collapse them into one disjunctive expression.

## 4.3 Concept retrieval is not yet a CRB

```text
Concept Retrieval ≠ CRB
Concept-Relation Reconstruction => CRB   (under the required conditions)
```

A query that merely returns `MMSE`, `CDR`, `Age`, `nWBV`, and `Dementia` retrieves concepts. A CRB emerges when the query or reasoner reconstructs the structure linking conditions to a conclusion.

## 4.4 KG as source and CRB as derived structure

```text
KG --query/reasoning--> concept-level inferential structure --> CRB
```

The KG is the source structure; the CRB is the explicit concept-rule representation derived from it. In some implementations, the KG may also persistently realize the CRB, but the two should not be identified by definition.

## 4.5 Generalizing fidelity

For a neural model, one may want:

$$
FaithfulTo(CRB,M)
$$

For an ontology reasoner, the more general requirement is **derivational faithfulness**: the CRB must faithfully represent the concept structure actually used, licensed, or reconstructed by the decision/inference process.

$$
DerivationalFaithfulness(CRB,SourceProcess)
$$

## 4.6 Generalizing model-relative to inference-process-relative

The phrase **model-relative** may be too narrow. A reasoner over an ontology is not necessarily a predictive model in the same sense as a CEM.

A more general formulation is:

> **A CRB is decision-process-relative / inference-process-relative.**

This allows neural, statistical, symbolic, graph-based, and hybrid sources to instantiate the same abstract layer.

## 4.7 Domain knowledge and conceptual-rule representation remain distinct

Even if the ontology contains a definition such as:

$$
DementiaCondition\equiv C_1\sqcap C_2
$$

the corresponding extracted rule:

$$
C_1(p)\land C_2(p)\Rightarrow DementiaCondition(p)
$$

should not be ontologically identified with the ontology axiom itself. One is domain knowledge; the other is a concept-rule representation of an inferential structure.

```text
Domain Knowledge ≠ Conceptual Rule Representation
```

## 4.8 General definition suggested by this case

> **Key generalization.** A CRB should not be characterized by the origin of the rule or by the type of system that generates it. It should be characterized by the explicit conceptual structure that makes a conclusion reconstructible in terms of concepts and their relations or compositions.

---

# 5. Broader Importance: CRB as an Applicability and Generalization Framework for AI, KG, XAI, and Neuro-Symbolic Systems

The generalization above is potentially more important than merely extending a CEM-oriented rule description. It provides a way to ask whether heterogeneous computational systems expose, generate, or permit the faithful reconstruction of the kind of concept-level structure required by the Ontological Mediation framework.

The central contribution of CRB at this stage is therefore **not to add another layer to the framework's processing pipeline**, but to characterize a broader class of potentially compatible source artifacts.

## 5.1 The community trend and the relevant conceptual gap

Knowledge Graphs are being used across knowledge representation, reasoning, neural-symbolic integration, explanation, retrieval, and grounding. Yet “ontologizing” outputs from connectionist AI may refer to very different operations:

```text
NeuralRepresentation -> KG
NeuralOutput -> OntologyConcept
Embedding <-> KG
LLM -> KG Retrieval -> Reasoning
```

These operations are not semantically equivalent. In particular, mapping a prediction to an ontology class does not necessarily expose the concept-level structure of the decision. The CRB conceptualization helps formulate an applicability question prior to Ontological Unpacking or Ontological Mediation: **is there an explicit, interpretable, faithful, and traceable concept-level structure available to be analyzed?**

## 5.2 CRB as an applicability test rather than an intermediate layer

The distinction should be represented as:

```text
Candidate Source Artifact
        |
        v
Does it satisfy the CRB admissibility criteria?
        |
        +--> Yes: a suitable concept-level structure is available
        |        and the Ontological Mediation framework may be applicable
        |
        +--> No: the framework is not directly applicable in the same form
```

This should not be rewritten as:

```text
Source -> CRB -> Ontological Unpacking -> Ontological Mediation
```

because that notation incorrectly turns CRB into a mandatory processing stage.

For the motivating CEM case, the relevant internal sequence remains:

```text
CEM -> Conceptual Rules -> Ontological Unpacking
    -> Ontological Mediation / OMCRs -> Justificatory Assessment
```

The CRB generalization operates at another analytical level: it tells us whether non-CEM artifacts can provide concept-level explanatory material sufficiently similar in the relevant respects to serve as starting material for the same framework.

## 5.3 Source-agnostic criteria, source-relative instances

At the level of its abstract schema, CRB is **source-agnostic**: the criteria are not defined by one particular model family. At the level of each concrete instance, however, CRB status is **source-relative**, because fidelity, provenance, and admissibility must be assessed with respect to the computational process from which the concept-level structure was obtained.

Potential source families include:

- Concept-Based Models (CBM, CEM, neural concept reasoners);
- post-hoc concept methods;
- linear/logistic regression and GAMs;
- decision trees;
- rule systems;
- Knowledge Graphs and ontology reasoners;
- neuro-symbolic systems;
- LLM + KG systems.

> **LLM-specific caution.** LLM-generated conceptual rules should be treated as **candidate CRB content** unless derivational fidelity to the relevant source process can be established. Linguistic generation alone does not confer conceptual admissibility or epistemic authority.

The commonality is therefore not a shared internal architecture. It is the availability of a concept-level explanatory structure satisfying the relevant admissibility conditions.

## 5.4 Knowledge Graphs may occur as sources, representations, or external resources

A Knowledge Graph may occur in several distinct roles:

```text
KG + Reasoner -> candidate concept-level structure -> CRB assessment
Predictive Model -> reconstructed concept-level structure -> CRB assessment
Qualifying concept-level structure -> later use of KG / ontology resources during mediation
```

These roles should not be collapsed. A KG may be the source of a CRB-qualifying structure, may represent such a structure, or may provide ontology-based resources relevant to later mediation. None of these possibilities requires CRB to become a processing layer in the Ontological Mediation framework.

## 5.5 Comparison across heterogeneous mechanisms

If a neural model and a knowledge-based reasoner both yield structures satisfying the CRB criteria, they become comparable at the concept-rule level rather than only at incompatible implementation levels such as vectors versus OWL axioms.

$$
CRB_{CEM}\leftrightarrow CRB_{KG}
$$

This enables questions such as:

- concept overlap;
- structural agreement;
- ontological compatibility;
- rule conflict;
- explanatory divergence.

Such comparison is a use of the CRB abstraction itself; it is conceptually distinct from applying Ontological Unpacking, Ontological Mediation, or Justificatory Assessment to a qualifying explanatory artifact.

## 5.6 Clarifying “ontologization”

A useful conceptual distinction remains:

```text
Annotation ≠ Semantic Grounding ≠ Ontological Unpacking ≠ Ontological Mediation
```

**Annotation** may map an output to an ontology concept. **Semantic grounding** links a model-level concept to a domain referent. **Ontological Unpacking** exposes commitments in a Conceptual Rule or other qualifying concept-level explanatory structure. **Ontological Mediation** relates that content to the relevant ontological, empirical, contextual, and epistemic-normative resources for subsequent assessment. Treating all four as “ontologization” obscures important differences.

The CRB conceptualization precedes these distinctions at the level of applicability: it asks whether the source artifact provides the kind of explicit concept-level structure to which these operations can meaningfully be applied.

## 5.7 Provenance and independence remain important

A CRB-qualifying artifact should retain enough provenance to establish the process from which its concept-level relations were derived. This becomes especially important when the same Knowledge Graph, language model, database, or institutional resource appears both in the derivation of the conceptual structure and later in ontological or justificatory processing.

A circular pattern such as:

```text
Source Resource -> candidate conceptual structure
same Source Resource -> sole basis for later "justification"
```

may compromise epistemic independence where such independence is required. CRB provenance therefore supports later analysis, but CRB itself does not perform Justificatory Assessment.

## 5.8 Potential autonomous research contribution

The emerging hypothesis is that CRB may constitute an autonomous conceptual contribution as a **source-agnostic applicability and classification framework for concept-level computational structures**.

It can be stated conservatively as:

> **CRB characterizes a class of explicit, interpretable, source-relative, and derivationally faithful concept-level structures through which heterogeneous computational systems can be assessed for potential compatibility with the Ontological Mediation framework.**

This preserves the CEM as the canonical motivating example without allowing that example to define the limits of the theory.

- **CRB** = the broader class of Concept-Rule Bases, independent of any particular model family.
- **CEM-CRB** = the subclass of CRBs reconstructed from, instantiated by, or exemplified through Concept Embedding Models (CEMs).

```text
CEM-CRB ⊆ CRB
```

The hyphen in `CEM-CRB` is part of the compound label and does not denote subtraction. The conservative relation `⊆` states that CEM-derived CRBs belong to the broader CRB class. A **proper-subset** claim (`CEM-CRB ⊂ CRB`) should be asserted only once at least one non-CEM CRB instance is independently established under the proposed admissibility criteria.

> **Example guides the theory, but does not define its limits.**

## 5.9 Research caution

The conceptual direction appears strong, but claims of scientific novelty should only be made after a targeted literature review. The immediate contribution is therefore best treated as a **research hypothesis and scope generalization** to be tested against existing work in concept-based XAI, rule extraction, Knowledge Graph reasoning, neuro-symbolic AI, explanation graphs, and concept-level representational abstractions.

---

# 6. Consolidated Synthesis

Across the analyses above, the CRB evolves from a CEM-oriented notion of reconstructed concept rules into a broader, representation-independent **applicability and classification construct** characterized by explicit concept-level inferential or decisional structure.

Its defining properties are not:

- the syntax of the rule;
- the technology that generated it;
- whether the source is neural or symbolic.

The relevant criteria are:

- **concept explicitness**;
- **interpretability**;
- **structured relation to conclusions**;
- **derivational faithfulness**;
- **source/process relativity**;
- **traceability**.

The resulting relation to the Ontological Mediation framework should be represented at two distinct levels.

At the level of applicability:

```text
Candidate Computational Artifact
        -> CRB Admissibility Assessment
        -> qualifying / non-qualifying concept-level structure
```

At the level of the internal framework, once suitable concept-level explanatory material is available:

```text
Qualifying Concept-Level Explanatory Structure
        -> Ontological Unpacking
        -> Ontological Mediation / OMCRs
        -> Justificatory Assessment
```

For the motivating CEM case, the qualifying explanatory structure is supplied by reconstructed Conceptual Rules. Other computational families may provide analogous structures if they satisfy the CRB criteria.

Therefore:

```text
CRB characterizes applicability; it does not constitute a processing stage.
CEM is a motivating instance; it does not define the framework's limits.
CRB ≠ Ontology
CRB ≠ OMCR
Predictive Contribution ≠ Justificatory Support
```

This formulation leaves open the exact ontological status of `ConceptualRule`, which should be addressed separately. A promising working hypothesis is that `ConceptualRule` is a **representational entity** that expresses a concept-level inferential/decisional structure and may be realized by formulas, equations, decision paths, graph fragments, or other formal artifacts.

---

## Status

This document is a **research consolidation draft**. It records the current conceptual generalization of the Concept-Rule Base and is intended to support subsequent formalization, literature review, and integration with the broader Ontological Mediation framework.

The bibliographic entries in the model-family tables are retained in their current abbreviated form for this draft and have **not yet undergone a final source-by-source bibliographic verification**.