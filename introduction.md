---
layout: default
title: Introduction
---
Concept
---

Virtual building model metadata schema (named VB schema) is a metadata schema that describes VBMs representing physical behaviors in DT-enabled building operations. The VB schema was established based on an ontology that identifies the semantic relationships of virtual sub-models composing the VBM in a DT. The VB schema is used as a management means for accurately modeling VBMs by utilizing VIM and VIC. In order to incorporate VIM and VIC into the process of creating and calibrating virtual models that compose VBMs, the relationship between data and virtual models, as well as the classes for data and virtual models, are defined

<img src="/assets/images/Fig_1.png" alt="Project Overview" width="150">

Related concept and definitions
---
Virtual building model (VBM)
---
Virtual building models (VBMs) are mathematical representations describing the physical behavior of buildings across their lifecycle. By comparing virtual sub-models models, they depict the operational aspects of the target building, including physical variables, equipment, systems, indoor conditions, and structural and material behaviors. In VBM, the focus lies on the actual physical behaviors and environment during the operational phase, rather than the structural aspects of the physical building. Highly explanatory VBMs can be achieved through in-situ modeling and synchronized with in-situ calibration in a DT. Accurate construction of VBM throughout a building facilitates DT-enabled intelligent applications, offering multifaceted and reliable real-time data during building operations.

Building digital twinning: Virtual in-situ modeling (VIM)
---
In the construction and building industry, building digital twinning refers to a DT modeling process for the creation, expansion, and maintenance of a VBM by utilizing data, information, and virtual models (DIM) throughout its life cycle. From the perspective of building digital twinning, the virtual in-situ modeling (VIM) methodology refers to the modeling process of constructing virtual behavioral models in target building operations to produce more accurate models than those provided outside the target building operations (e.g., different buildings, modeling environments, and periods). The concept of building digital twinning based on an in-situ modeling perspective can contribute to achieving a full DT state, where a virtual building model can observe and represent all elements (e.g., building materials, equipment, and systems), their physical behaviors, and indoor environments in real building operations.

Virtual in-situ calibration (VIC)
---
Virtual in-situ calibration (VIC) is a methodology that calibrates physical sensors, virtual sensors, and virtual sub-models models on-site, in real time, and simultaneously for real building operations. In the context of building DTs, VIC can provide reliable virtual model environments through in-situ sensors and model calibration capabilities. This can be regarded as a novel methodology of DT synchronization in building operations. VIC is categorized into intrusive and nonintrusive in-situ calibration based on the type of data used for calibration. It is also classified into indirect and direct in-situ calibration, depending on the benchmark environment used for calibration. In a typical calibration environment for unobserved behavior models that are not measured by their physical sensor counterparts, intrusive calibration is considered a direct calibration approach that employs benchmarks for calibration through additional on-site measurements, whereas nonintrusive calibration indirectly calibrates the target unobserved behavior model without additional effort to measure physical targets. As an example of non-intrusive calibration, Choi et al. modeled the secondary return temperature in a district heating system using a physics-based model and indirectly calibrated it by reducing uncertainty in the valve opening rate model. Intrusive calibration generally establishes an accurate benchmark; however, it is expensive and time-consuming. Nonintrusive calibration, on the other hand, has the potential to overcome the practical limitations associated with intrusive calibration, such as the financial issue of additional sensor installation costs and the challenge of measuring variables that are not feasible with conventional sensors. Therefore, by appropriately employing both approaches depending on the situation, it is possible to accurately calibrate a virtual model for building operations.
