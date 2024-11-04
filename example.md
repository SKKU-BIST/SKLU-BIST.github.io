---
layout: default
title: Example
---

<hr class="thin">

# Ontological representation of the virtual supply pressure sensor

<p class="spaced">
The example ontology represents the virtual supply pressure sensor, expressed using both the VB schema and the Brick schema. This ontology illustrates the relationships between various virtual models used to develop the virtual supply pressure sensor, as well as the physical entities corresponding to the real-world equipment and data applied to the system. The figure shows the interactions between entities, with a particular emphasis on the interactions between the virtual supply pressure model, correction model, and distance model. The labeled nodes and edges within the ontology contribute to a comprehensive understanding of the structure and logic of the represented system.
</p>

<script type="text/javascript" id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

<h1>The Scenario for VB Schema-Based Developed Virtual Supply Pressure Model through VIM and VIC</h1>

<p class="spaced">
To monitor, an in-situ pressure behavior model was developed. During the modeling phase, it was assumed that the supply pressure was unobserved, resulting in the implementation of a white-box modeling approach to develop the initial supply pressure model using <a href="#eq1">(Eq. 1)</a>. To calibrate the developed behavior model, an intrusive measurement was conducted from December 16, 2019, to December 20, 2019. This measurement aimed to determine the correction parameters in <a href="#eq2">(Eq. 2)</a> using the Markov chain Monte Carlo (MCMC) method and the Metropolis–Hastings algorithm.
</p>

<p id="eq1"><strong>Eq. 1:</strong></p>
<p>$$ P_{sup} = H_{ref} \left( \frac{f_{pu}}{f_{ref}} \right)^2 + P_{ret} $$</p>

<p id="eq2"><strong>Eq. 2:</strong></p>
<p>$$ f_c(X_c, \theta_c) = \theta_{c,1} + \theta_{c,2} \times (T_{sup} - T_{ret}) $$</p>

<p align="center">
    <a href="assets/example_ontology.rdf" download>
        <button style="padding: 10px 20px; font-size: 16px; background-color: #4CAF50; color: white; border: none; border-radius: 5px;">
            Download example_ontology.rdf
        </button>
    </a>
</p>

<hr class="thin">

<style>
    .spaced {
        margin-top: 20px;
        margin-bottom: 20px;
    }
    
    hr.thin {
        border: 0;
        height: 1px;
        background: #ccc;
    }
</style>
