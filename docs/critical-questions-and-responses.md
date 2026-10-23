# Critical questions and responses

This document is organized as a set of targeted questions and responses concerning the conceptual, ontological, and epistemic commitments of the Ontological Mediation framework. The questions do not need to be read sequentially: readers may use the contents below to move directly to the issue relevant to their doubt. Each response is intended to be reasonably self-contained, so some deliberate redundancy is retained where needed for clarity.

## Contents

1. [Dual-process analogy: System 1 and System 2](#q1)
2. [Why the limitation of XAI is partly ontological](#q2)
3. [Explanation vs. Justificatory Assessment](#q3)
4. [Semantic Grounding, Ontological Grounding, and Ontological Unpacking](#q4)
5. [Important distinctions and clarifications regarding OMCRs](#q5)
   - [5.1. Are OMCRs universally necessary?](#q5-1)
   - [5.2. Why is an OMCR not simply another Conceptual Rule?](#q5-2)
   - [5.3. Why can OMCRs not be derived automatically from Conceptual Rules alone?](#q5-3)
   - [5.4. Why is a faithful Conceptual Rule not yet justificatorily sufficient?](#q5-4)
   - [5.5. What is the role of human and expert knowledge?](#q5-5)
   - [5.6. Where does normative authority come from?](#q5-6)
   - [5.7. Why is an OMCR not simply an ontology axiom?](#q5-7)
   - [5.8. Why can an OMCR not simply be replaced by an IF-THEN production rule?](#q5-8)
   - [5.9. What does Weak Truthbearer mean?](#q5-9)
   - [5.10. What does the Cognitive Reserve OMCR illustrate?](#q5-10)
6. [Ontological Unpacking within the framework](#q6)
   - [6.1. What is Ontological Unpacking and what does it do?](#q6-1)
   - [6.2. Why is Ontological Unpacking not simply formal translation?](#q6-2)
   - [6.3. What does Ontological Unpacking contribute to the architecture?](#q6-3)
7. [CRB and the broader applicability of the framework](#q7)
8. [The meaning of ~Age versus omission of Age](#q8)

<a id="q1"></a>

## 1. How do the authors map Daniel Kahneman’s Dual-Process Theory of Cognition (System 1 and System 2) onto the architecture proposed in the paper?

The framework draws on a heuristic analogy, also found in parts of the neuro-symbolic and hybrid AI literature, between Kahneman’s dual-process account of cognition and the two computational and epistemic regimes involved in the proposed architecture. The analogy is intended to clarify their different explanatory modalities; it is not a psychological claim that neural and symbolic AI literally instantiate human System 1 and System 2 cognition. Its main purpose is to contrast a regime in which model-relevant regularities are learned largely through implicit statistical representations with another in which semantic, ontological, and inferential commitments can be made explicit and critically inspected.

System 1-like processes are associated with the subsymbolic regime, represented here by neural networks and concept-based models. These systems learn statistical regularities from data and can generate predictions or concept-level representations without relying on explicitly programmed symbolic rules. The analogy concerns primarily characteristics such as implicit representation, pattern-based processing, tolerance to noisy or incomplete information, and reliance on statistically learned regularities rather than a literal correspondence in computational speed or cognitive dynamics.

System 2-like structures are associated with the symbolic regime and, in the present framework, particularly with formal ontologies, logical rules, explicit conceptual models, and inferential structures. Knowledge can thereby be represented through explicitly specified concepts, properties, relations, and constraints, making semantic and inferential commitments more accessible to inspection and critical assessment. These approaches typically require additional knowledge-engineering effort but can provide greater semantic explicitness, auditability, and structured reasoning.

The distinction between the two regimes is therefore not merely representational. Within the proposed architecture, the subsymbolic component is initially assessed mainly in terms of predictive and operational performance, while the symbolic-ontological layer introduces additional criteria concerning conceptual coherence, semantic adequacy, ontological grounding, and explicit inferential constraints.

The framework does not seek to replace one regime with the other, nor does it assume that symbolic representation is epistemically infallible. Instead, Ontological Mediation provides a structured interface through which model-derived conceptual relationships can be related to explicit domain, contextual, and epistemic-normative structures and subsequently subjected to critical assessment.

Within this architecture, Ontologically Mediated Concept Rules (OMCRs) should therefore not be understood simply as outputs of a symbolic “System 2.” They are mediated explanatory artifacts connecting model-derived conceptual relations with explicit ontological and epistemic-normative structures. Their representation and assessment lie closer to the symbolic regime, but their architectural role is precisely to mediate between the two regimes.

Accordingly, the System 1/System 2 parallel should be understood as an explanatory metaphor rather than a literal cognitive or computational equivalence. System 1-like processes contribute statistically learned patterns and predictions; System 2-like structures provide explicit semantic, ontological, and inferential resources for examining them. Ontological Mediation articulates the interface between these regimes without collapsing their distinct roles.

<a id="q2"></a>

## 2. Why do the authors argue that an important limitation of current Explainable AI (XAI) is ontological in nature?

The claim is not that the limitations of current XAI are exclusively ontological, nor that existing explanation techniques are inadequate in every respect. Rather, the argument concerns a large class of post-hoc and feature- or concept-oriented XAI methods that can make model behavior more accessible while leaving the ontological commitments of the resulting explanation insufficiently explicit.

The central point is simple: feature relevance is not the same as ontological meaning. Methods such as feature attribution, saliency maps, LIME, SHAP, and related techniques can identify variables, features, or internal representations that contributed to a prediction. This is useful for understanding model behavior. However, such information does not by itself determine what those features represent in the domain, what kinds of entities or properties they refer to, which relations and dependencies they presuppose, or how the resulting explanatory statement is intended to refer to domain reality.

This should not necessarily be regarded as a defect relative to the original design goals of these methods. The limitation becomes important when model-derived explanations are expected to support domain-level interpretation, scientific reasoning, auditing, regulation, or high-stakes decisions. In those contexts, knowing that a feature contributed to a prediction is not sufficient; one must also clarify what that feature commits us to ontologically.

This is where the work of [Guizzardi and Guarino (2023)](https://arxiv.org/abs/2304.11124) becomes especially relevant. They argue that symbolic descriptions can conceal ontological commitments and introduce Ontological Unpacking as a process for making those commitments explicit by identifying the entities, properties, relations, and states of affairs that function as their assumed truthmakers. Their approach therefore moves explanation beyond surface-level intelligibility toward the ontological structures presupposed by the explanatory content.

This perspective is particularly relevant to concept-based XAI. A concept-level explanation may be understandable at the level of labels or learned statistical relations while remaining ontologically underdetermined. Two variables may contribute to the same prediction while referring to fundamentally different kinds of properties, measurements, dispositions, social constructs, or contextual conditions. Without making such distinctions explicit, an explanation can appear semantically meaningful while concealing assumptions that become important when the explanation is interpreted as being about the domain rather than merely about the model.

[Confalonieri and Guizzardi (2025)](https://journals.sagepub.com/doi/epub/10.3233/NAI-240754) broaden this picture by examining several roles that ontologies can play in neuro-symbolic explanations, including reference modelling, common-sense reasoning, and knowledge refinement or complexity management. In this view, ontologies provide more than definitions: they can serve as semantic infrastructure for organizing, enriching, and refining explanations.

The present framework is intended as a complementary development of this line of work. Guizzardi and Guarino provide the basis for asking what ontological commitments a symbolic description presupposes and for making those commitments explicit through Ontological Unpacking. Confalonieri and Guizzardi show how ontologies can support explanation through semantic modelling, reasoning, and refinement. Our framework asks a further question: what happens after a model-derived explanation has been reconstructed and its relevant ontological commitments have been made explicit?

At that point, a different problem arises. An explanation may be ontologically coherent and still be epistemically weak, contextually inappropriate, normatively problematic, or insufficiently supported by evidence. The framework therefore distinguishes three related but non-equivalent questions:

1.  What does the model-derived explanation represent? This leads to concept-level explanation and Ontological Unpacking.

2.  How should those commitments be related to domain, empirical, and contextual structures? This leads to Ontological Mediation and OMCRs.

3.  Should the resulting explanatory claim be accepted within a particular epistemic and normative context? This leads to Justificatory Assessment.

The role of Ontologically Mediated Concept Rules (OMCRs) is therefore not simply to provide additional semantic information. They are introduced as mediated explanatory artifacts through which concept-level relations are situated relative to explicit ontological commitments, empirical configurations, contextual conditions, and epistemic-normative constraints.

The ontological limitation can therefore be stated more precisely: a model explanation may reveal which features or concepts matter without yet establishing what those concepts commit us to ontologically, how they are related to structures in the domain, or whether the resulting explanatory claim is epistemically and normatively admissible.

Ontologies help address the first part of this problem by making domain commitments explicit and structurally inspectable. The additional contribution of the framework is to connect that ontological clarification to subsequent mediation and justificatory assessment, thereby extending explainability from the intelligibility of model behavior toward the critical evaluation of model-derived explanatory claims.

<a id="q3"></a>

## 3. Why does the framework distinguish explanation from Justificatory Assessment, and how does this distinction change the epistemic role of model-derived conceptual rules and the interpretation of justificatory outcomes?

The framework distinguishes explanation from Justificatory Assessment because an explanation can be faithful to a model’s internal behavior without thereby being epistemically acceptable. In simple terms, explanation asks what the model-derived structure says, whereas Justificatory Assessment asks whether the resulting explanatory claim deserves acceptance under specified ontological, evidential, contextual, and normative conditions.

In concept-based XAI, an explanation typically aims to make explicit which concepts, attributes, or relationships contributed to a prediction. It therefore reconstructs or renders visible model-relevant structure. A concept-level explanation may be highly faithful to the model and still be problematic when interpreted in relation to the domain.

A reconstructed rule may, for example, accurately reflect what a model has learned while involving relations that are conceptually incoherent, biologically implausible, insufficiently supported by evidence, contextually inappropriate, or normatively unacceptable. These are different kinds of justificatory weakness, but they share a common consequence: predictive or explanatory fidelity does not entail epistemic adequacy.

This motivates Justificatory Assessment as a distinct evaluative stage. It does not merely ask whether the explanation accurately reflects the model’s internal dependencies. It asks whether the explanatory claim can be accepted given the relevant ontological commitments, empirical evidence, domain constraints, contextual conditions, institutional requirements, and epistemic-normative standards.

This distinction also changes the epistemic role attributed to model-derived conceptual rules. They are not treated as self-sufficient sources of explanatory authority or as final justificatory products. Rather, they enter the architecture as candidate explanatory structures whose status remains open to further examination.

Ontological Unpacking can make their implicit ontological commitments explicit. Ontological Mediation can relate those commitments to domain, empirical, and contextual structures. Justificatory Assessment can then evaluate the standing of the resulting explanatory claim within the relevant Normative-Epistemic Context.

The framework therefore rejects the idea that explanatory transparency alone is sufficient for epistemic acceptance. Within the proposed architecture, and particularly for the class of high-stakes or domain-sensitive problems that motivates it, Ontological Mediation and Justificatory Assessment are treated as conditionally necessary components whenever model-derived explanations must be evaluated not only for intelligibility, but also for ontological coherence, evidential support, contextual appropriateness, and epistemic admissibility.

This claim is not universal. The framework does not maintain that every AI explanation in every possible application requires the same degree of ontological and justificatory analysis, nor that Ontological Mediation can guarantee truth or correctness. The claim is narrower: when model-derived explanations are expected to support consequential epistemic or practical decisions, intelligibility alone may be insufficient.

This distinction is reflected in the provisional outcomes of Justificatory Assessment:

1.  Epistemically Admissible: the explanatory claim satisfies the relevant justificatory criteria under the specified evidential, ontological, contextual, and normative conditions.

2.  Inadmissible: the explanatory claim conflicts with one or more relevant justificatory constraints in a way that prevents its acceptance within that context.

3.  Epistemically Unstable: the available grounds do not support a sufficiently stable justificatory judgment because of unresolved conflicts, evidential insufficiency, contextual sensitivity, competing interpretations, or other defeaters.

A crucial point is that justificatory status is not equivalent to truth-value. Epistemically Unstable does not mean false, and Epistemically Admissible does not mean true. An explanatory claim may fail to achieve stable justificatory support without thereby being demonstrated false; conversely, a claim that is currently admissible is not thereby guaranteed to be true.

This distinction also clarifies the interpretation of the case study. Conflicting structural or contextual evidence may prevent the framework from treating the explanatory support offered for a classification such as *NonDemented* as justificatorily stable, even when those conflicts are insufficient to establish that the classification itself is false. The relevant question is therefore not simply whether the predicted category is true or false, but whether the explanation offered for it is adequately supported under the specified conditions.

The broader consequence is that concept-based explanations are repositioned within the architecture. They are not final epistemic products, but candidate explanatory structures whose standing remains open to ontological mediation and critical assessment.

In this sense, the framework extends XAI beyond the question “Why did the model produce this prediction?” toward the further question “Under what conditions should the resulting explanation be accepted?” The transition from explanatory reconstruction to justificatory assessment is one of the central commitments of the proposed framework.

This proposal is also continuous with, but not reducible to, the ontological-explanatory work of [Guizzardi and Guarino (2023)](https://arxiv.org/abs/2304.11124). Their account goes substantially beyond conventional feature-level XAI by asking what ontological commitments and assumed truthmakers underlie symbolic descriptions. The present framework introduces a subsequent question: given those commitments, the available evidence, the relevant context, and the applicable epistemic and normative standards, what justificatory standing should the resulting explanatory claim receive?

Accordingly, the framework should not be read as replacing ontological clarification, but as extending the explanatory path from model-derived explanation to ontological clarification, to ontological mediation, to justificatory assessment

The philosophical background of this distinction lies primarily in epistemology and the philosophy of science, where justification has long been treated as a question distinct from mere explanation or interpretation. Formal ontology contributes a complementary role by making explicit the ontological commitments that become objects of subsequent epistemic assessment. Strictly speaking, however, this is not a central concern of formal ontology as such. Even in Husserl, who developed an important account of justification and evidence, these issues belong primarily to his phenomenology and epistemology rather than to his formal ontology. In [Philosophical background](https://github.com/em4ttos/Ontological-Mediation-in-Explainable-Artificial-Intelligence/blob/main/docs/formalization/concept-rule-base.md) (*in preparation*) we outline some philosophical affinities between our framework and more recent discussions of justification, evidential support, defeasibility, and contextual dependence.

<a id="q4"></a>

## 4. What is the difference between Semantic Grounding, Ontological Grounding, and Ontological Unpacking, and why is semantic grounding alone insufficient for explanations in high-stakes domains?

The framework distinguishes Semantic Grounding, Ontological Grounding, and Ontological Unpacking because they address different explanatory problems. They are related, but they should not be treated as interchangeable operations or as different names for the same process.

A concise way to distinguish them is:

- Semantic Grounding asks: *What does this representation refer to?*

- Ontological Grounding asks: *What kind of entity, property, relation, or structure is that referent understood to be?*

- Ontological Unpacking asks: *What ontological commitments are implicitly presupposed by the representation or explanatory structure itself?*

A useful starting point is to avoid defining Semantic Grounding too narrowly. In the broader literature on the symbol-grounding problem, particularly following [Stevan Harnad (1990)](https://arxiv.org/html/cs/9906002) and subsequent discussions in the philosophy of information, semantic grounding concerns how symbols or internal representations acquire meaningful connections to what they represent rather than remaining defined only through relations to other symbols. Depending on the theoretical account adopted, this may involve perceptual, empirical, operational, or referential links.

Within the present framework, Semantic Grounding can therefore be understood in a more restricted explanatory sense as specifying or supporting a meaningful connection between a concept or representation and an empirical referent, measurement, observation, or domain phenomenon. It helps answer questions such as: *What does this variable or concept refer to in the empirical domain?*

For example, a variable such as *YearsEducation* may be semantically grounded by specifying what is measured, how it is operationalized, and which observations instantiate it. This prevents the variable from functioning merely as a formal symbol disconnected from its intended empirical interpretation.

Ontological Grounding addresses a different question. It concerns the ontological category and structural relations of the referent: whether it is understood as an entity, quality, relation, event, disposition, measurement result, social construct, or some other kind of domain element, and how it depends on or relates to other entities.

Ontological Grounding therefore connects an explanatory representation to an explicit domain ontology or ontological account capable of constraining its interpretation. Depending on the explanatory needs of the domain, this may make explicit distinctions involving identity and individuation, dependence, part-whole structure, participation, constitution, admissible relations, or other relevant structural constraints.

The difference can therefore be stated succinctly, Semantic Grounding connects a representation to what it denotes or measures; Ontological Grounding constrains how that referent is understood as part of a structured domain reality.

Ontological Unpacking, however, is a different kind of operation. Following [Guizzardi and Guarino (2023)](https://arxiv.org/abs/2304.11124), it is not simply the act of assigning a model concept to an ontology term. Its role is to expose and analyze the ontological commitments already implicit in a conceptual description or explanatory structure.

Ontological Unpacking therefore asks: *What must be presupposed about the entities, properties, relations, dependencies, identity conditions, or states of affairs involved for this explanatory representation to be meaningfully interpreted?*

This makes Ontological Unpacking meta-conceptual. Rather than merely locating an existing model variable within an ontology, it critically examines what the variable or rule itself commits us to.

The distinction becomes particularly clear in simple mappings. Assigning a model variable to an ontology class may provide useful Ontological Grounding while leaving important implicit assumptions unanalyzed. For example, mapping *nWBV* to an ontology term may specify what kind of quantity or measurement it represents, but it may still leave unexamined the relations among the patient, the biological quality, the measurement procedure, the measurement result, and the explanatory role attributed to that value. Ontological Unpacking is required when the objective is to expose those hidden commitments explicitly.

The three operations are therefore complementary but not reducible to a single linear sequence:

1.  Semantic Grounding establishes or specifies meaningful connection to empirical or referential content.

2.  Ontological Grounding situates that content within an explicit account of the kinds of entities, properties, and relations that constitute the domain.

3.  Ontological Unpacking analyzes the ontological commitments presupposed by the explanatory representation itself.

A concept may therefore be semantically grounded without being ontologically well specified. Likewise, a concept may be mapped to an ontology without the assumptions embedded in the corresponding explanatory rule having been fully unpacked.

This distinction is especially important in high-stakes domains. Empirical or semantic grounding alone cannot prevent a model from learning relationships that are statistically robust but scientifically misleading, contextually inappropriate, or dependent on confounding factors. For example, an association between *YearsEducatio***n** and a dementia-related classification may be statistically genuine and semantically well grounded as a measurement while still requiring deeper analysis of what education represents in the domain, how it relates to cognitive reserve, which population characteristics condition that relation, and how it should be interpreted within a specific diagnostic context.

An important boundary must also be preserved: Ontological Grounding does not establish causality. An ontology can constrain which kinds of relations are conceptually or ontologically coherent, but causal validity requires additional assumptions, evidence, or causal methodology. In other words, ontological coherence is a condition on interpretation, not evidence of causal validity.

Likewise, Ontological Grounding alone does not determine whether a relationship is ethically, institutionally, or epistemically acceptable. Those questions belong to the broader Normative-Epistemic Context and, ultimately, to Justificatory Assessment.

The insufficiency of Semantic Grounding can therefore be stated more precisely. A model-derived explanation may correctly refer to empirical phenomena without adequately specifying what kinds of entities and relations those phenomena instantiate, which ontological commitments the explanation presupposes, or whether the resulting explanatory claim is causally, contextually, epistemically, or normatively defensible.

Within the architecture, the three processes therefore perform distinct but complementary roles: Semantic Grounding connects representation to empirical meaning; Ontological Grounding situates that meaning within an explicit domain structure; Ontological Unpacking exposes the commitments presupposed by the explanatory representation. Their combination does not guarantee justification, but it makes model-derived explanations sufficiently explicit to become objects of subsequent Ontological Mediation and Justificatory Assessment.

<a id="q5"></a>

## 5. Important distinctions and clarifications regarding OMCRs

<a id="q5-1"></a>

### 5.1. Are OMCRs universally necessary for explanation, or only constitutive of the proposed architecture?

The framework does not claim that Ontologically Mediated Concept Rules (OMCRs) are universally necessary for explanation. Rather, OMCRs are constitutive components of the proposed architecture for a specific class of problems: cases in which model-derived conceptual relations are available, or can be reconstructed as a Concept-Rule Base, but their ontological, contextual, and justificatory commitments remain insufficiently explicit. The distinction is important because the paper contains claims at different levels of generality.

Some claims have a broader epistemic or philosophical scope. These include the distinction between explanation and justification, the defeasibility of justificatory standing, and the possibility that an explanatory claim may be truth-apt without being stably admissible under the relevant epistemic and normative conditions.

Other claims are architecture-specific. OMCRs belong to this second category. Within the proposed framework, they provide the representational mechanism through which model-derived conceptual relations are situated relative to explicit ontological commitments, empirical conditions, contextual restrictions, and epistemic-normative criteria prior to Justificatory Assessment.

The necessity claim is therefore internal and conditional rather than universal. OMCRs are necessary within this architecture because they perform a constitutive mediating role between reconstructed conceptual content and the subsequent justificatory process. However, the framework does not claim that every possible architecture connecting explanation and justification must contain OMCRs, nor that no alternative representational mechanism could satisfy similar epistemic requirements.

Accordingly, the contribution should be understood as proposing one engineered realization of a broader epistemic requirement: model-derived explanatory content may need to be situated relative to explicit domain, contextual, and justificatory commitments before it can support critical assessment.

The notion of Weak Truthbearer occupies a somewhat broader level. In the present work, it is instantiated through the OMCR–Justificatory Assessment architecture, but the underlying idea—that a truth-apt explanatory claim may remain defeasible and context-dependent in its justificatory standing—may have broader philosophical applicability. The present paper does not attempt to establish that broader generalization.

The framework should therefore be read as proposing a specific architecture for a delimited explanatory problem class, not as claiming that OMCRs are a universally necessary component of explanation or the only possible mechanism through which explanation and justification can be connected.

<a id="q5-2"></a>

### 5.2. Why is an OMCR not simply another Conceptual Rule?

A Conceptual Rule and an Ontologically Mediated Concept Rule (OMCR) play different epistemic roles within the framework. A Conceptual Rule expresses or reconstructs a concept-level relation that is relevant to the learned behavior of the model. It primarily tells us something about the model-derived explanatory structure.

An OMCR, by contrast, tells us how such a relation is to be interpreted and assessed within an explicit onto-epistemic context. It situates the model-derived relation relative to ontological commitments, empirical configurations, contextual restrictions, and epistemic-normative criteria.

The difference is therefore not merely one of annotation or additional metadata. An OMCR is not simply a Conceptual Rule with ontology labels attached. Ontological Mediation changes the epistemic role of the representation by placing the model-derived relation within a structured network of commitments that cannot be obtained from predictive behavior alone.

This distinction can be summarized as follows: a Conceptual Rule provides the model-derived relation; an OMCR provides a mediated representation of that relation under explicit ontological, empirical, contextual, and epistemic-normative conditions.

The information required for this mediation may depend on sources that are epistemically independent of the learned model, including formal domain ontologies, Ontological Unpacking of the relevant concepts, scientific or professional knowledge, external empirical evidence, contextual restrictions, institutional standards, admissibility criteria, known defeaters, and the relevant Normative-Epistemic Context. This epistemic independence is crucial because the source of the explanatory claim should not be identical to the source of its justificatory authority.

If all of the criteria used to assess a model-derived relation were inferred from the same predictive model that generated that relation, the framework would risk circularity: the model would effectively provide both the claim and the standards by which the claim is justified. The architecture deliberately avoids this collapse.

An OMCR should therefore not be understood as a reformatted or enriched Conceptual Rule. It is a mediated explanatory artifact in which a model-derived conceptual relation is situated relative to independently established domain and epistemic constraints so that it can later become the object of Justificatory Assessment.

The central distinction is therefore: Conceptual Rule is a model-derived explanatory relation. OMCR is an onto-epistemically situated representation of that relation for subsequent critical assessment.

<a id="q5-3"></a>

### 5.3. Why can OMCRs not simply be derived automatically from Conceptual Rules alone?

The central issue is not automation itself, but the source of the information and authority required to construct an Ontologically Mediated Concept Rule (OMCR).

A Conceptual Rule primarily represents or reconstructs a relation learned by the predictive model. By itself, it generally does not contain enough information to determine whether its concepts have been ontologically interpreted correctly, whether the relation is scientifically meaningful, whether independent evidence supports or defeats it, whether it applies only under particular contextual or population conditions, or whether its use satisfies relevant institutional, professional, ethical, or epistemic standards. For this reason, the transition from a Conceptual Rule to an OMCR cannot, in general, be understood as a purely syntactic or model-internal transformation.

Ontological Unpacking may first expose the ontological commitments implicit in the reconstructed rule. Ontological Mediation then relates those commitments to independently established domain structures, empirical evidence, contextual conditions, and epistemic-normative criteria. The OMCR provides the representational locus in which this mediated relation is articulated.

This does not mean that OMCR construction must necessarily be manual. Different implementation strategies are possible. Experts may pre-specify OMCRs, templates, constraints, or mediation structures that are later instantiated when compatible Conceptual Rules are encountered. Alternatively, parts of an OMCR may be constructed dynamically or automatically from validated ontological, empirical, and normative resources.

The crucial distinction is therefore between automation and epistemic self-authorization. An OMCR may be generated or instantiated computationally, but the ontological and normative resources that determine its interpretation and justificatory relevance must not derive their authority merely from the same predictive model whose explanation is being assessed.

Otherwise, the architecture would risk circularity: the model would effectively provide both the explanatory relation and the standards by which that relation is evaluated.

The framework therefore does not claim, *Conceptual Rule → OMCR* is impossible to automate. It claims instead, *Conceptual Rule alone → OMCR* is epistemically insufficient.

A more adequate representation is *Conceptual Rule + Ontological Unpacking + validated domain, empirical, contextual, and Normative-Epistemic resources → OMCR*

The exact construction process may be manual, semi-automatic, or automated. What matters is that the OMCR incorporates sources of interpretation and assessment that are not epistemically reducible to the predictive relation from which the original Conceptual Rule was reconstructed.

<a id="q5-4"></a>

### 5.4. Why is a faithful and human-interpretable Conceptual Rule not yet epistemically sufficient for justificatory purposes, and what role does an OMCR play in addressing this limitation?

A Conceptual Rule reconstructed from a concept-based model may faithfully represent relations that are relevant to the model’s predictive behavior and may express those relations through concepts that are readily understandable to humans. Within the proposed framework, however, predictive fidelity and conceptual interpretability do not yet establish justificatory sufficiency.

The distinction can be stated simply, faithfulness asks whether the Conceptual Rule adequately represents the model-derived relation; justification asks whether the resulting explanatory claim deserves acceptance under the relevant ontological, empirical, contextual, and epistemic-normative conditions.

A faithful Conceptual Rule can therefore provide important explanatory information about the model. It may show which concepts participate in a decision, how they are related, and how their configuration contributes to a prediction or classification. However, this does not by itself establish what kinds of entities, properties, relations, measurements, roles, disp ositions, social constructs, or other domain elements those concepts represent. Nor does it establish whether the relation expressed by the rule is compatible with relevant domain commitments, supported by independent empirical evidence, applicable under the circumstances of the case, or acceptable according to the relevant scientific, professional, institutional, ethical, or epistemic standards.

A Conceptual Rule may therefore be explanatorily informative while remaining ontologically underspecified and justificatorily indeterminate. This is the point at which Ontological Unpacking and Ontological Mediation become necessary within the proposed architecture.

Ontological Unpacking makes explicit the ontological commitments presupposed by the interpretation of the Conceptual Rule. Ontological Mediation then relates the model-derived conceptual content to explicit ontological, empirical, contextual, and epistemic-normative resources.

The Ontologically Mediated Concept Rule (OMCR) is the explanatory artifact produced through this mediating process. An OMCR should therefore not be understood as merely a more detailed Conceptual Rule or as the original rule supplemented with ontology labels. Its epistemic role is different.

The Conceptual Rule remains primarily linked to what has been reconstructed from the model or source process. The OMCR, by contrast, represents that model-derived explanatory relation as ontologically grounded and epistemically situated content, making explicit the additional conditions under which the explanatory claim can subsequently be assessed.

This distinction can be represented schematically as *Conceptual Rule → model-derived concept-level explanatory relation*; and *OMCR → ontologically grounded and epistemically situated representation of that relation*.

The transition does not imply that the original Conceptual Rule was defective. A faithful Conceptual Rule may already perform its representational function successfully. The issue is that model fidelity and conceptual intelligibility answer different questions from epistemic justification.

Similarly, the production of an OMCR does not itself establish that the explanatory claim is true or justified. Ontological Mediation makes the relevant commitments, conditions, constraints, evidence, and potential defeaters available for assessment, but the resulting justificatory status is assigned only through Justificatory Assessment.

The relevant sequence can therefore be represented as *Conceptual Rule → Ontological Unpacking → Ontological Mediation / OMCR → Justificatory Assessment* with each stage performing a distinct function.

The Conceptual Rule represents model-derived explanatory content. Ontological Unpacking increases the explicitness of its ontological interpretation. The OMCR situates that content relative to the relevant ontological, empirical, contextual, and epistemic-normative resources. Justificatory Assessment evaluates the epistemic standing of the resulting explanatory claim.

Accordingly, a faithful and human-interpretable Conceptual Rule can explain aspects of what the model has learned without yet being sufficient to justify the corresponding explanatory claim. The role of the OMCR is not to replace the Conceptual Rule, but to provide the onto-epistemically mediated explanatory artifact required for that claim to become an appropriate object of subsequent Justificatory Assessment.

The distinction can therefore be summarized as follows:

- *Conceptual Rule → faithful representation of model-derived conceptual content.*

- *OMCR → ontologically grounded and epistemically situated mediation of that content for subsequent Justificatory Assessment.*

<a id="q5-5"></a>

### 5.5. What is the role of human and expert knowledge in OMCRs?

Human and expert knowledge plays an important role in the framework, but not because every OMCR must be manually written or individually adjudicated by a domain expert. The more fundamental requirement is that the ontological, empirical, contextual, and normative resources used to mediate a model-derived explanation must have epistemic authority that is not reducible to the predictive model itself.

Experts may contribute to the construction, adoption, extension, alignment, or validation of domain ontologies; the identification of relevant empirical evidence; the specification of contextual applicability conditions; the formulation of institutional, professional, ethical, or regulatory constraints; the recognition of known defeaters; and the construction or validation of the relevant Normative-Epistemic Context.

Their role can therefore be understood in several complementary ways: as providers of domain knowledge, as participants in knowledge engineering, and as validators of the standards and constraints used during mediation and Justificatory Assessment.

However, the human expert, understood as an individual or group of individuals, is not the only locus in which such expertise may be available. Human expertise may be embodied directly in persons, but it may also be externalized, documented, and stabilized in validated scientific literature, clinical or technical guidelines, regulatory frameworks, curated knowledge bases, institutional policies, and other authoritative domain resources. These resources therefore do not constitute an alternative to human expertise; rather, they are artifacts through which human knowledge, judgment, and accumulated domain expertise are preserved and made available for subsequent use.

Importantly, once such expertise has been externalized in documented or computationally accessible resources, it may be retrieved, integrated, or operationalized through manual, semi-automated, or automated mechanisms**.** These may include information-retrieval systems, knowledge bases, rule engines, semantic technologies, and dedicated language models or other AI systems designed to access, synthesize, or mediate validated domain knowledge. Such computational mechanisms do not themselves constitute the ultimate source of epistemic authority. Their role is to retrieve, organize, transform, or make operational expertise whose authority derives from the underlying human-produced and independently validated sources on which they rely.

What matters, therefore, is that the provenance, authority, scope, and epistemic standing of the underlying resources remain explicit and independently assessable, regardless of whether access to them is performed by human experts, computational systems, or hybrid human-machine processes.

This distinction is important because expert knowledge should not be confused with a case-specific expert verdict. Experts do not need to decide in advance whether each model-derived explanation is admissible. Rather, they may help define or validate the background knowledge, constraints, evidence, and criteria against which particular explanatory claims are subsequently mediated and assessed. The framework therefore does not treat experts as authorities who simply override statistical learning. Their contribution is to provide kinds of knowledge that predictive performance alone cannot legitimately establish.

At the same time, expert knowledge is itself defeasible and revisable. Scientific knowledge may change, professional standards may evolve, and institutional or regulatory criteria may be revised. Expert contributions therefore participate in the same historically situated and intersubjective structure that characterizes the Normative-Epistemic Context.

Accordingly, the role of expertise can be summarized as follows: experts and other authoritative external resources help provide or validate the ontological, empirical, contextual, and normative conditions under which model-derived explanatory claims can be critically assessed.

The construction and application of OMCRs may then be manual, semi-automatic, or automated, provided that the relevant resources remain explicit, traceable, and epistemically independent of the predictive model whose explanation is being evaluated.

<a id="q5-6"></a>

### 5.6. Where does the normative authority come from that allows an OMCR to constrain, qualify, or trigger further assessment of a model-derived explanation?

OMCRs do not derive their normative force from ontologies alone. Ontologies contribute explicit domain commitments and structural constraints, whereas normative and justificatory criteria arise from the broader Normative-Epistemic Context (NEC)**.**

At the same time, OMCRs remain ontologically grounded: the entities, properties, relations, measurements, and domain categories to which they refer are interpreted through the relevant ontology. Thus, the ontology does not generate the normative rule; it provides the domain commitments under which that rule can be semantically well-defined.

The division of labor can be stated simply considering that the ontology tells us what the rule is about; the Normative-Epistemic Context provides the standards under which it should be assessed; the OMCR brings these dimensions together; and Justificatory Assessment determines the resulting justificatory status.

The Normative-Epistemic Context is understood as a historically situated, intersubjective, and revisable structure incorporating the standards and resources through which a relevant epistemic community evaluates claims. Depending on the domain, it may include scientific knowledge, evidential standards, shared domain commitments, professional practices, institutional requirements, ethical and regulatory constraints, methodological conventions, known limitations and defeaters, and the historically available state of knowledge.

These sources are heterogeneous and need not possess the same kind of authority. Scientific evidence, professional guidelines, legal requirements, institutional policies, and methodological standards may constrain an explanatory claim in different ways. The framework therefore should not assume that a criterion is epistemically legitimate merely because it is socially accepted. Its provenance, scope, authority, and contestability remain matters that must themselves be made explicit and remain open to revision.

The ontology and the NEC therefore play complementary but distinct roles. The ontology contributes semantic and ontological structure**:** it specifies the kinds of entities, properties, relations, dependencies, and constraints being assumed. The NEC contributes epistemic and normative standards of admissibility: it provides the background against which one may ask whether a model-derived explanatory claim is sufficiently supported, contextually appropriate, institutionally acceptable, or defeated by relevant counterevidence.

An OMCR mediates between these dimensions and the model-derived explanatory content. Its normative relevance does not arise intrinsically from the rule itself, nor is it produced by the ontology. Rather, the OMCR functions as an onto-epistemically situated explanatory artifact in which independently established domain and normative constraints can be represented in relation to a model-derived conceptual structure.

This distinction is important because an OMCR should not be conflated with the final evaluative procedure. An OMCR may encode or activate conditions under which an explanation should be challenged, qualified, or subjected to additional evidential scrutiny, but Justificatory Assessment remains responsible for assigning the justificatory status of the resulting explanatory claim**.**

For example, an OMCR may represent a conflict between the assumptions underlying a model-derived explanation and relevant domain knowledge; it may identify unresolved contextual conditions; or it may indicate that additional evidence is required. These mediated constraints then provide grounds for Justificatory Assessment to determine whether the explanatory claim **is** Epistemically Admissible, Inadmissible, or Epistemically Unstable**.**

This division of labor prevents the framework from collapsing ontological coherence into normative authority**.** A model-derived explanation may be ontologically coherent and yet fail under relevant evidential, scientific, institutional, ethical, or professional standards. Conversely, the mere fact that an explanation can be consistently represented within an ontology does not make it epistemically admissible.

Normative authority in the framework is also revisable rather than absolute. Scientific knowledge changes, institutional standards evolve, ethical expectations may be reformulated, new evidence may challenge previous assumptions, and domain ontologies themselves may require revision. Accordingly, the justificatory status of an explanatory claim may change over time even if the underlying model output remains unchanged.

Intersubjective establishment therefore contributes to public assessability and shared standards, but it does not guarantee correctness. The framework adopts a broadly fallibilist stance: normative and epistemic criteria may be well-grounded and authoritative within a domain while remaining open to criticism, revision, and replacement.

This also clarifies the dual determination of OMCRs. Their normative and epistemic content originates in the NEC, while their vocabulary and domain commitments are ontologically grounded. The former determines which standards apply; the latter determines what kinds of entities, properties, relations, measurements, and conditions those standards concern.

The ontological grounding of an OMCR does not require that the entire normative apparatus be encoded in a single domain ontology. Existing ontologies may need to be complemented, aligned, or extended, and additional ontological resources may be introduced when the relevant concepts or relations are not represented in the original ontology.

In the present case study, this relationship is operationalized through the Semantic Data Dictionary (SDD)**,** which functions as a semantic mediation workbench. The SDD records mappings among empirical variables, ontology terms, and OMCR specifications and supports their transformation into computational representations such as SWRL rules, RDF triples, and Knowledge Graph structures. These representations provide an implementation layer through which the mediated relations can be operationalized.

Accordingly, existing domain ontologies do not need to encode the complete normative apparatus of the framework. They provide the ontological grounding of the entities and relations involved, while normative-epistemic criteria are supplied independently by the relevant NEC and subsequently represented over that grounded vocabulary.

The central distinction can therefore be summarized as follows:

> Ontology provides ontological grounding.
>
> The Normative-Epistemic Context provides epistemic and normative criteria.
>
> The OMCR represents their mediated application to model-derived explanatory content.
>
> Justificatory Assessment evaluates the resulting explanatory claim.

<a id="q5-7"></a>

### 5.7. Why is an OMCR not simply an ontology axiom?

An Ontologically Mediated Concept Rule (OMCR) should not be confused with an ontology axiom, even though the two may interact closely and may sometimes be represented within the same ontology-based computational infrastructure.

The central distinction is functional and epistemic. An ontology axiom formalizes a commitment concerning the represented domain. An OMCR mediates a model-derived explanatory relation under explicit ontological, empirical, contextual, and epistemic-normative conditions.

Ontology axioms may express subsumption, disjointness, dependence, participation, existential restrictions, cardinality constraints, domain and range restrictions, equivalence relations, or other formal commitments concerning the entities and relations represented in an ontology. Their role is to articulate and constrain a domain conceptualization and, depending on the adopted formalism, to support logical inference, consistency checking, and other forms of reasoning.

An OMCR has a different epistemic role. It starts from explanatory content linked to a model-derived conceptual relation and situates that content relative to explicit domain commitments, empirical conditions, contextual restrictions, and epistemic-normative criteria so that the resulting explanatory claim can subsequently become an object of Justificatory Assessment.

The distinction can therefore be represented as follows:

1.  Ontology axiom: formalizes a commitment concerning the represented domain.

2.  Conceptual Rule: expresses or reconstructs a concept-level relation relevant to model behavior.

3.  OMCR: mediates that model-derived relation through explicit ontological, empirical, contextual, and epistemic-normative conditions for subsequent critical assessment.

These objects may interact without becoming interchangeable. An OMCR may invoke, depend on, or be constrained by ontology axioms. Domain axioms may, for example, specify which kinds of entities can instantiate particular properties, which relations are admissible, which dependencies must hold, or which configurations are ontologically inconsistent. Such commitments can become relevant when a model-derived explanatory relation is subjected to Ontological Mediation. The crucial point is that incorporating an OMCR into an ontology-based representational or computational environment does not make it conceptually identical to an ontology axiom.

An OMCR may be operationalized within an ontology-oriented computational environment. Its conditions and relations may be represented through SWRL rules, RDF structures, Knowledge Graph elements, SHACL constraints, or other semantic technologies. However, the particular implementation formalism does not by itself determine the conceptual or epistemic type of the represented artifact.

For example, an OMCR represented operationally as a SWRL rule does not thereby become identical to a domain-ontology axiom merely because both participate in the same semantic infrastructure. Similarly, RDF triples or Knowledge Graph structures may encode the entities, relations, mappings, provenance, and contextual information involved in an OMCR without thereby collapsing the mediated explanatory artifact into the ontology itself.

The distinction is therefore between formal representation and architectural role. A domain-ontology axiom contributes to the formal characterization of the domain. An OMCR, by contrast, uses ontologically grounded vocabulary and may rely on ontology axioms while performing a different function: it situates a model-derived explanatory relation within the additional empirical, contextual, and normative-epistemic conditions required for subsequent assessment. This distinction is especially important because Ontological Grounding is not equivalent to Justification.

Ontology axioms can make domain commitments explicit and constrain which interpretations are ontologically coherent. They do not, by themselves, determine whether a model-derived explanatory claim should be accepted, qualified, challenged, or regarded as epistemically unstable.

Those judgments require resources that are not reducible to the ontology alone, including empirical evidence, contextual applicability conditions, scientific or professional knowledge, institutional or regulatory constraints, known defeaters, and the relevant Normative-Epistemic Context. Their integration and application belong to Ontological Mediation and, ultimately, to Justificatory Assessment.

Accordingly, an OMCR should not be understood as an ontology axiom transferred into the explanatory layer. It is an onto-epistemically situated explanatory artifact that may rely on ontology axioms for the grounding and structural constraint of its domain vocabulary while performing a distinct mediating role between model-derived conceptual relations and subsequent justificatory evaluation.

This also explains why the same semantic technology may participate in both layers without eliminating their conceptual distinction. A formalism such as SWRL may be used to express a domain rule, a constraint, or an operational representation of an OMCR. What distinguishes these artifacts is therefore not merely their surface syntax or implementation language, but the kind of commitment they express, the provenance of their content, and the epistemic role they perform within the architecture.

The distinction can therefore be summarized as follows: an ontology axiom formalizes a commitment about the represented domain, whereas an OMCR provides an ontologically grounded and epistemically situated mediation of a model-derived explanatory relation for subsequent Justificatory Assessment.

Thus, an OMCR may be implemented within an ontology-based environment without being reducible to a domain-ontology axiom. Its identity is determined not simply by where or how it is encoded, but by the explanatory and mediating role it performs within the architecture.

<a id="q5-8"></a>

### 5.8. Why can’t an OMCR simply be replaced by an IF-THEN production rule? Could ordinary IF-THEN production rules perform the same function, making ontology unnecessary?

At the purely operational level, an Ontologically Mediated Concept Rule (OMCR) may indeed be represented in an IF-THEN form, and a conventional rule engine may be fully capable of executing the same extensional condition.

For example, *eTIV \< 1300 AND nWBV \> 0.72 → NonDemented* can be evaluated computationally without any explicit ontological machinery. A production-rule system can test the conditions and return the corresponding conclusion. Therefore, the framework does not claim that ontology is required for rule execution. The issue arises at a different level: execution is not the same as interpretation, grounding, or justificatory assessment.

A bare production rule does not, by virtue of its syntax alone, make explicit the ontological commitments under which its terms are interpreted. It does not necessarily specify what kind of entity bears nWBV, whether nWBV represents a biological quality, a measured quantity, or a measurement result; what kind of entity or status NonDemented denotes; or how the patient, biological structure, measurement process, and diagnostic classification are related.

These are not questions about whether the rule can be executed. They concern the semantic and ontological commitments presupposed by the explanatory content. This is where Ontological Unpacking and Ontological Mediation become relevant. Ontological Unpacking exposes the commitments implicit in the reconstructed conceptual relation, while Ontological Mediation situates that relation relative to explicit domain structures, empirical conditions, contextual restrictions, and epistemic-normative criteria.

Accordingly, the operational surface of an OMCR may resemble an ordinary IF-THEN rule, but its explanatory role is not exhausted by that syntax. The distinction can be stated as follows, rule execution does not entail Ontological Grounding. And, more generally, operational equivalence does not imply semantic, ontological, or epistemic equivalence.

Two systems may execute exactly the same threshold condition and produce the same output while differing substantially in what they make explicit about the meaning, domain commitments, contextual conditions, and epistemic standing of the relation being evaluated.

An OMCR should therefore not be understood as merely a conventional rule decorated with ontology terms. Its role is to situate a model-derived conceptual relation within an explicit onto-epistemic structure that makes the corresponding explanatory content inspectable and suitable for subsequent critical assessment.

A useful distinction is:

1.  Conceptual Rule: expresses or reconstructs a concept-level relation relevant to model behavior.

2.  Production rule: provides an operational mechanism for evaluating conditions and producing consequences.

3.  Ontology represents explicit domain commitments concerning entities, properties, relations, dependencies, and constraints;

4.  OMCR mediates model-derived conceptual content through those explicit commitments so that the resulting explanatory claim can be critically examined.

This distinction should not be defended by claiming that ordinary rule engines lack mechanisms such as inheritance, prioritization, consistency checking, constraint handling, or links to external knowledge. Modern rule systems, logic-programming environments, knowledge graphs, and constraint systems may support many such capabilities. The relevant claim is narrower, a production rule considered only as an executable condition does not by itself provide the ontological and justificatory structure required by the type of explanation pursued in the framework.

Ontology may also provide computational benefits such as taxonomic inference, consistency checking under appropriate formal semantics, interoperability, and reuse through explicit mappings. These benefits are relevant, but they are secondary to the central explanatory role: making the domain commitments of model-derived conceptual relations explicit and inspectable.

A further distinction must also be preserved, Ontological Grounding is not equivalent to Justification. Ontology can clarify what kinds of entities and relations are being assumed and constrain their coherent interpretation, but it does not by itself determine whether the resulting explanatory claim should be accepted. That requires additional empirical, contextual, and normative-epistemic criteria and remains the role of Justificatory Assessment.

The framework therefore does not claim that ontology enables rule execution. It claims instead: bare rule execution does not, by itself, provide the ontological grounding and epistemic structure required to make a model-derived explanatory claim justificatorily assessable.

For this reason, an OMCR may be operationally implemented as an IF-THEN rule while remaining conceptually distinct from an ordinary production rule. Its distinctive role lies not in computational exclusivity, but in the explicit mediation of model-derived explanatory content through domain and epistemic commitments.

<a id="q5-9"></a>

### 5.9. What does it mean to say that an OMCR functions as a Weak Truthbearer, and why does this not mean that the OMCR determines whether the underlying classification is true or false?

The notion of Weak Truthbearer is intended to characterize the epistemic status of the explanatory claim articulated through an Ontologically Mediated Concept Rule (OMCR)**.**

The central distinction is simple, truth-bearing is not truth-determining. A truthbearer is something that can meaningfully be assessed as true or false; it is not an artifact that automatically determines whether its content is true.

The term is useful because an OMCR does more than preserve a statistical or model-derived relation. It situates that relation within explicit ontological commitments, empirical conditions, contextual restrictions, and epistemic-normative criteria. In doing so, it supports the articulation of an explanatory claim that is sufficiently explicit to become an object of critical assessment.

This is the sense in which the explanatory claim articulated through an OMCR is truth-apt. It can be supported, challenged, defeated, revised, or rejected. The term *truthbearer* therefore marks a transition from a merely predictive or insufficiently articulated relation to a claim whose commitments are explicit enough to participate in epistemic evaluation.

The adjective weak**,** however, is essential. It does not mean that the claim is only “partially true,” nor that truth itself comes in weaker and stronger degrees. Rather, weakness qualifies the claim’s justificatory standing, not its capacity to bear truth.

A Weak Truthbearer remains defeasible because its admissibility depends on conditions that may change, remain incomplete, or be contested. These conditions may include the ontological interpretation of the concepts involved, the empirical configuration of the case, available scientific evidence, contextual applicability conditions, domain constraints, institutional or professional standards, and the relevant Normative-Epistemic Context.

An OMCR may therefore provide the structured basis for assessing an explanatory claim as Epistemically Admissible, Inadmissible, or Epistemically Unstable without thereby determining whether the model’s underlying classification is true or false. This distinction is fundamental because classification truth and explanatory admissibility are different objects of evaluation**.**

Suppose, for example, that a model classifies a patient as *NonDemented*. The OMCR-based mediation and subsequent Justificatory Assessment may indicate that the explanation offered for that classification is epistemically unstable because some of its supporting relations conflict with relevant domain evidence or because important contextual conditions remain unresolved.

From this it does not follow that NonDemented is false. What follows is only that the available grounds do not justify stable acceptance of the explanation currently offered for that classification.

Conversely, an explanation may be judged Epistemically Admissible without this amounting to a guarantee that the underlying classification is true. Admissibility indicates that the explanatory claim satisfies the relevant justificatory criteria under the specified conditions; it does not transform justificatory support into infallible truth.

The distinction can therefore be represented as follows:

1.  A classification claim asks whether the predicted state or category is actually the case.

2.  An explanatory claim mediated through an OMCR asks whether the proposed explanation of that classification is ontologically coherent, evidentially supported, contextually appropriate, and epistemically admissible.

3.  Justificatory Assessment evaluates the standing of that explanatory claim under the relevant conditions.

An OMCR therefore does not determine the truth of the model’s classification. It provides an onto-epistemically structured basis for assessing whether the explanation offered for that classification is currently defensible. This is why Epistemically Unstable cannot be equated with false, and Admissible cannot be equated with **true**. The framework evaluates the justificatory status of explanatory claims, not the binary truth-value of the underlying classification itself.

<a id="q5-10"></a>

### 5.10. How does the Cognitive Reserve OMCR illustrate the role of Ontological Mediation in exposing epistemic limitations, evidential tensions, and potential sources of bias in high-stakes predictive models?

The Cognitive Reserve OMCR illustrates how Ontological Mediation can reveal situations in which a model-derived explanation appears predictively plausible while remaining epistemically incomplete or potentially misleading when interpreted within the relevant clinical context.

The central lesson of the example is that predictive importance is not equivalent to evidential authority**.**

Consider the rule:

*IF (YearsEducation \> 16) AND (nWBV \> 0.72 AND eTIV \< 1300 AND ASF \< 1.1) AND (MMSE \>= 27)*

*THEN Status = PotentialCognitiveReserveMaskingCondition*

At the level of the predictive model, variables such as YearsEducation, MMSE, nWBV, eTIV, and ASF may participate in learned statistical relations associated with a classification such as *NonDemented*. A concept-based explanation can make these relations visible, but it does not by itself determine whether their joint interpretation is clinically or epistemically adequate.

The potential problem arises because these variables do not necessarily carry the same kind of evidential significance. High educational attainment and preserved performance on a cognitive screening instrument may support an apparently favorable functional interpretation, while structural neuroanatomical indicators may contribute a different and potentially conflicting evidential perspective.

Ontological Mediation helps make this heterogeneity explicit. YearsEducation is not treated merely as a numerical feature, MMSE merely as another scalar input, and neuroanatomical measurements merely as interchangeable predictors. Their domain meanings, measurement roles, ontological categories, and relations to the explanatory problem become explicit.

Within the case-study conceptualization, cognitive reserve provides a domain-level hypothesis that may help explain how relatively preserved cognitive performance can coexist with structural changes. Importantly, this hypothesis is not generated or validated by the OMCR itself. Its epistemic relevance depends on independently established domain knowledge, evidence, and applicability conditions represented within the relevant Normative-Epistemic Context.

The OMCR therefore does not establish that cognitive reserve is causally responsible for the observed pattern. Rather, it makes explicit a possible mediating condition whose relevance can be assessed against the available evidence. This creates the possibility of representing an epistemic tension among heterogeneous forms of evidence that the predictive relation alone may not adequately capture.

Suppose that the model predicts *NonDemented* and that its concept-level explanation relies substantially on high educational attainment and a high MMSE score. Without further mediation, this explanation may appear coherent with the model’s learned structure.

The OMCR introduces a further question: *Could the apparently reassuring functional indicators remain compatible with an independently supported masking condition under which preserved performance does not exclude underlying impairment?*

If that possibility is supported by relevant domain knowledge and is applicable to the individual case, the framework need not conclude that the classification is false or that the model is wrong. Instead, it may identify grounds for questioning the justificatory stability of the explanation currently offered.

The appropriate conclusion is therefore not “The patient has dementia.” Nor does it imply “The model is wrong.” Rather, the conclusion is closer to “The present explanation should not be accepted uncritically because a relevant and independently supported domain-level masking condition may reduce the justificatory force of some of its apparently favorable indicators.”

This is where the distinction between OMCRs and Justificatory Assessment becomes important. The OMCR provides an onto-epistemically structured representation of the potential conflict, while Justificatory Assessment determines the standing of the resulting explanatory claim under the relevant Normative-Epistemic Context.

Depending on the available evidence, the explanatory claim may therefore be regarded as:

1.  Epistemically Admissible, if the apparent conflict is adequately resolved;

2.  Inadmissible, if relevant domain or evidential constraints decisively undermine the explanation;

3.  Epistemically Unstable, if the available evidence is insufficient to resolve the tension among the relevant indicators and interpretations.

The third outcome is particularly important. A possible cognitive-reserve effect does not establish that the classification *NonDemented* is false. It indicates that some of the evidence supporting the explanation may be less justificatorily decisive than its predictive role suggests.

This is also the limited sense in which Ontological Mediation may contribute to the analysis of potential model bias or systematic epistemic distortion. It does not automatically detect or remove bias. Rather, it can expose domain distinctions, contextual dependencies, heterogeneous evidential roles, and conflicts that a purely statistical representation may obscure.

Accordingly, the Cognitive Reserve OMCR should not be understood as an automatic diagnostic correction mechanism. It functions as a mediating structure through which the justificatory sufficiency of a model-derived explanation can be challenged when independently grounded domain knowledge provides relevant reasons for caution.

In a nutshell, the example illustrates that Ontological Mediation does not guarantee that the model reaches the correct clinical conclusion. It makes it possible to identify situations in which a predictively plausible explanation may still require qualification, additional evidence, or further expert assessment before being regarded as epistemically adequate.

<a id="q6"></a>

## 6. Important aspects of the OU, considering its integration into our framework

<a id="q6-1"></a>

### 6.1. What is Ontological Unpacking in the proposed architecture, what does it do to model-derived Conceptual Rules, and how does it differ from merely translating a predictive rule into an ontology?

Ontological Unpacking (OU), inspired by [Guizzardi and Guarino (2023)](https://arxiv.org/abs/2304.11124), is the analytical process through which the framework makes explicit the ontological commitments presupposed by a particular interpretation of a model-derived Conceptual Rule. Its immediate purpose is not to determine whether the rule is scientifically correct, causally valid, normatively acceptable, clinically appropriate, or epistemically admissible. Those questions belong to later stages of the architecture, especially Ontological Mediation, OMCR construction or activation, and Justificatory Assessment.

Ontological Unpacking asks a prior question: *What kinds of entities, properties, relations, dependencies, identity conditions, and states of affairs must be made explicit for this Conceptual Rule to be coherently interpreted as being about the domain?*

A rule reconstructed from a concept-based model may be intelligible at the feature or concept level while remaining ontologically underspecified. Terms such as *Age***,** *Sex***,** *YearsEducatio***n,** *nWBV***,** *eTIV***, or** *Dementia* may appear straightforward as model variables, but their ontological status is not determined merely by their presence in the rule.

Ontological Unpacking therefore examines what these terms are taken to represent in the relevant domain interpretation. It may expose distinctions such as: an individual versus a quality inhering in that individual; a quality versus its measured value; a biological condition versus a diagnostic classification; an intrinsic property versus a relational or socially dependent characteristic; an enduring entity versus a temporally dependent state or phase; the bearer of a property versus the observation or measurement through which that property is represented.

Its purpose is to reveal distinctions that may have been compressed into a single variable or label by the machine-learning representation. For example, what appears in a predictive model as a single numerical feature may presuppose a richer structure such as mapping *measured value* to *measurement result* to *quality* to *bearer of the quality.*

Making these distinctions explicit matters because later explanatory mediation should not operate over labels whose ontological interpretation remains ambiguous.

Ontological Unpacking should also be distinguished from general ontology engineering. Ontology engineering asks how a domain should be formally conceptualized or represented; Ontological Unpacking asks what a particular explanatory representation already commits us to, or must make explicit, when it is interpreted as being about that domain.

The immediate output of OU is therefore not necessarily a new ontology, but a more explicit account of the ontological commitments required for interpreting the Conceptual Rule. An important boundary must be preserved: *Ontological Unpacking increases explicitness, not certainty.*

OU does not establish that YearsEducation causally contributes to dementia, that cognitive reserve explains a particular diagnostic pattern, that reduced *nWBV* should override an apparently favorable cognitive score, or that a specific combination of evidence is clinically admissible.

Those questions involve empirical, causal, contextual, epistemic, and normative considerations that go beyond ontological analysis. They belong principally to Ontological Mediation, OMCRs, and Justificatory Assessment.

The division of labor can therefore be represented as follows:

1.  Ontological Unpacking: What ontological commitments are presupposed by the interpretation of this Conceptual Rule?

2.  Ontological Mediation / OMCR: How should this model-derived relation be situated when those commitments are confronted with domain, empirical, contextual, and epistemic-normative knowledge?

3.  Justificatory Assessment: Given that mediated interpretation, what justificatory standing should the resulting explanatory claim receive?

Finally, Ontological Unpacking must not be confused with simply translating a predictive rule into OWL, RDF, OntoUML, or another representational formalism. A mechanical translation may preserve the original rule while leaving its ontological assumptions implicit. Encoding a rule in ontology-oriented syntax may merely re-express the same content in a different formal representation. Ontological Unpacking, by contrast, changes the explicitness of the ontological interpretation under which that rule is understood.

Accordingly, OU is not an all-purpose explanatory mechanism and does not itself determine whether a model-derived explanation should be accepted. Its contribution is more specific and prior: to make explicit what the explanatory representation ontologically commits us to so that later mediation and justificatory assessment can operate on a better-defined object of analysis.

<a id="q6-2"></a>

### 6.2. Why is Ontological Unpacking not simply a translation into OWL, RDF, OntoUML, or another formalism?

Ontological Unpacking (OU) must be distinguished from a purely representational conversion. Changing the language of a rule is not the same as making its ontological commitments explicit.

A predictive or conceptual rule may be represented in OWL, RDF, a Knowledge Graph, OntoUML, or another formalism while the assumptions implicit in that rule remain largely unanalyzed. Consider, for example: *nWBV AND YearsEducation → NonDemented*

A mechanical transformation could represent *nWBV*, *YearsEducation*, and *NonDemented* as classes, properties, nodes, predicates, or other formal elements while preserving essentially the same conceptual structure.

Such a transformation may be technically useful, but it does not necessarily clarify what *nWBV* ontologically represents, what entity bears the relevant biological quality, how that quality relates to a measurement process and measurement result, what kind of entity or status NonDemented denotes, or which identity and dependence conditions are presupposed by the interpretation. If these commitments remain implicit, the rule has been re-encoded, but not ontologically unpacked.

A useful diagnostic question is therefore, did the procedure merely reproduce the vocabulary and relations already explicit in the rule in another representational language, or did it expose ontological distinctions and commitments that were previously implicit?

The first is primarily a representational transformation. The second constitutes Ontological Unpacking in the sense adopted by the framework. This distinction also requires some care regarding the technologies involved. OWL, RDF, and OntoUML do not play identical roles. RDF primarily provides a graph-based representational framework; OWL provides formal ontology constructs and semantics; OntoUML is an ontologically well-founded conceptual modeling language specifically designed to support explicit ontological distinctions.

For this reason, OntoUML can be particularly useful for representing the results of Ontological Unpacking. However, the mere use of OntoUML does not guarantee that OU has been performed. Accordingly, OntoUML may serve as an instrument or representational output of Ontological Unpacking, but its use is neither necessary nor sufficient for OU.

The same general principle applies to other representational technologies. No notation or formalism performs Ontological Unpacking merely by being used. Ontological Unpacking is an analytical operation whose purpose is to expose the ontological commitments presupposed by an explanatory representation. Formal languages and modeling technologies provide possible means for representing, communicating, or operationalizing the results of that analysis.

Thus, the central distinction is translation changes the representation of the rule; Ontological Unpacking changes the explicitness of the ontological commitments under which the rule is interpreted.

<a id="q6-3"></a>

### 6.3. What does Ontological Unpacking contribute to the architecture?

The principal contribution of Ontological Unpacking (OU) is to provide the subsequent stages of the architecture with a better-defined and more inspectable explanatory object.

Its immediate product is not a verdict about whether a Conceptual Rule is true, causally valid, scientifically adequate, normatively acceptable, or epistemically admissible. Rather, OU makes explicit the ontological commitments presupposed by the interpretation of that rule.

Before Ontological Unpacking, a model-derived Conceptual Rule may contain variables and relations that appear understandable while remaining ontologically underspecified. Subsequent mediation would then risk confronting empirical, scientific, contextual, or normative knowledge with feature labels whose domain meaning remains ambiguous.

Ontological Unpacking reduces this ambiguity by exposing distinctions that may otherwise remain compressed in the model representation, such as entities and their bearers; qualities and measured values; measurement processes and measurement results; roles and states; dependence relations; identity conditions, and other domain-relevant ontological distinctions.

The result is not a “truer” rule, but a rule whose commitments are more explicit and therefore more available for inspection and criticism. This contribution can be summarized as follows, Ontological Unpacking increases assessability by increasing ontological explicitness. At the same time, Ontological Unpacking increases explicitness, not certainty.

OU does not by itself establish that the resulting interpretation is scientifically correct or justificatorily acceptable. Its role is to make explicit what the explanatory representation commits us to so that those commitments can subsequently be confronted with independent domain knowledge, empirical evidence, contextual constraints, and epistemic-normative criteria.

The architectural sequence is therefore:

1.  Conceptual Rule — provides model-derived explanatory content.

2.  Ontological Unpacking — makes the ontological commitments of that content explicit.

3.  Ontological Mediation / OMCR — situates those commitments relative to domain, empirical, contextual, and epistemic-normative resources.

4.  Justificatory Assessment — evaluates the standing of the resulting explanatory claim.

Accordingly, Ontological Unpacking does not decide whether a Conceptual Rule should be accepted. It makes explicit what the rule commits us to under the adopted domain interpretation, thereby providing Ontological Mediation and Justificatory Assessment with a more ontologically determinate object of analysis.

Its architectural contribution can therefore be stated succinctly: OU does not justify the explanation; it makes the explanation sufficiently explicit to be meaningfully mediated and critically assessed.

<a id="q7"></a>

## 7. What role does the Concept-Rule Base (CRB) concept play in determining the broader applicability of the framework beyond CEMs?

The proposed framework was initially developed and illustrated using Concept Embedding Models (CEMs), from which Conceptual Rules can be reconstructed at a human-interpretable concept level. However, the use of CEMs as the motivating case should not be interpreted as restricting the framework to that particular model family. The later notion of a Concept-Rule Base (CRB) was introduced precisely to generalize this point.

A CRB is not an additional processing stage within the Ontological Mediation framework. Rather, it provides a conceptual and methodological reference for determining whether other AI or computational artifacts expose, generate, or permit the faithful reconstruction of the kind of explicit concept-level structure required for the framework to be applicable.

The CEM case therefore serves as a motivating instance of a broader representational possibility. What matters for framework applicability is not whether the source system is specifically a CEM, but whether the relevant conceptual structure satisfies appropriate conditions such as:

- explicit and human-interpretable concepts;

- identifiable relations or compositions among those concepts;

- a sufficiently explicit connection between those conceptual relations and the relevant computational conclusion or output;

- derivational fidelity to the source model, decision process, or inference process;

- sufficient provenance and traceability to establish how the conceptual structure was obtained.

The CRB conceptualization abstracts from the particular mechanisms by which such structures are produced. A concept-level structure may originate from a CEM, another concept-based architecture, a rule-based system, a statistical model, a Knowledge Graph, a neuro-symbolic system, or another computational process, provided that the relevant CRB admissibility criteria are satisfied.

CRB therefore answers a question of *framework applicability, does this computational artifact provide, or permit the faithful reconstruction of, the kind of concept-level explanatory structure that the Ontological Mediation framework requires as its starting material***?**

If the answer is positive, the artifact may potentially be treated within the framework in a manner analogous to the Conceptual Rules reconstructed from the motivating CEM case.

If the answer is negative, the framework is not directly applicable to that artifact in the same way, because the required concept-level explanatory structure is absent or cannot be sufficiently reconstructed.

The distinction is important because the CRB should not be inserted into the framework’s internal processing sequence. Instead, two different analytical levels should be distinguished.

- At the level of the original framework application, as an case stydy: CEM → Conceptual Rules → Ontological Unpacking → Ontological Mediation / OMCR → Justificatory Assessment.

- At the level of scope and applicability: Candidate computational artifact → CRB admissibility criteria → determination of whether the required concept-level structure is available.

Thus, CRB provides a diagnostic and classificatory framework for generalizing the scope of applicability of the proposed approach. It does not transform the explanatory artifact, mediate it ontologically, or participate as a necessary intermediate layer in the justificatory process.

The broader implication is that the framework is not conceptually tied to CEMs. CEMs constitute one important and motivating instance of a more general class of computational systems capable of supplying suitable concept-level explanatory structures.

The role of CRB can therefore be summarized as follows, CRB characterizes the kind of concept-level structure that makes a computational artifact potentially compatible with the framework; it does not constitute a processing stage within that framework.

<a id="q8"></a>

## 8. Why do terms such as ~Age in a Conceptual Rule have a different meaning from simply omitting Age from the rule, and how should this distinction be interpreted ontologically?

The distinction between *~Age* and the omission of *Age* from a Conceptual Rule is important because it separates explicit model-level representation from the absence of an explicit statement, and both from ontological existence in the represented domain.

Consider the Conceptual Rule: *~eTIV AND YearsEducation AND ~Age AND ~Sex AND nWBV AND ASF → NonDemented*

Within the reconstructed conceptual representation, *~Age* indicates that *Age* is explicitly present in the rule with a formally defined non-positive or negative polarity. The exact interpretation of the symbol ~ depends on the semantics of the rule-extraction or reconstruction method being used. It may, for example, represent negative polarity, negated activation, or another formally specified non-supporting contribution. The framework should therefore not assign a stronger meaning to *~* than the source method warrants.

By contrast, if *Age* is omitted from the reconstructed rule, the rule contains no explicit proposition concerning A*ge* in that conceptual relation. Omission does not itself imply negative relevance, irrelevance to the model as a whole, or any particular reason for its absence from the extracted rule.

The distinction can therefore be stated succinctly, *~Age* expresses an explicit model-level statement within the reconstructed rule; omission of *Age* makes no explicit statement about *Age* within that rule.

This distinction becomes especially important when the rule is interpreted ontologically. *~Age* must not be read as saying that the patient “has no age,” that age does not exist as a property or quality of the patient, or that *Age* is ontologically irrelevant to the domain. Depending on the adopted domain ontology, *Age* may still correspond to an instantiated age-related quality or attribute of the patient independently of its polarity or presence in a particular model-derived rule.

Accordingly, the framework distinguishes three different levels:

1.  Positive conceptual relevance: *Age* is explicitly represented as contributing positively within the reconstructed rule.

2.  Negative or non-positive conceptual relevance: *~Age* explicitly represents Age with the polarity defined by the extraction method.

3.  Ontological instantiation: the patient may still instantiate the relevant age-related property or quality in the domain, regardless of how Age is represented in that particular rule.

Ontological Unpacking is important precisely because it prevents these levels from being conflated. A Conceptual Rule expresses how concepts are represented within a model-derived explanatory structure. Ontological Unpacking asks a different question: what kinds of entities, properties, relations, and dependencies are presupposed in the domain by the concepts appearing in that structure?

The central distinction is therefore, conceptual polarity or omission is not equivalent to ontological existence or non-existence. A concept may appear positively, appear with a negative or non-positive polarity, or be omitted from a reconstructed rule while the corresponding domain property remains ontologically instantiated and relevant.

For this reason, *~Age* should be interpreted as a statement about the organization of the reconstructed conceptual explanation, according to the semantics of the source method, and not as a literal ontological negation of the patient’s age.