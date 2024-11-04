---
layout: default
title: Example
---

<hr class="thin">

## Ontological representation of the virtual supply pressure sensor

<p class="spaced">
The example ontology represents the virtual supply pressure sensor, expressed using both the VB schema and the Brick schema. This ontology illustrates the relationships between various virtual models used to develop the virtual supply pressure sensor, as well as the physical entities corresponding to the real-world equipment and data applied to the system. 
</p>

<script type="text/javascript" id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

<hr class="thin">

## The Scenario for VB Schema-Based Developed Virtual Supply Pressure Model through VIM and VIC

<p class="spaced">
To monitor, an in-situ pressure behavior model was developed. During the modeling phase, it was assumed that the supply pressure was unobserved, resulting in the implementation of a white-box modeling approach to develop the initial supply pressure model using <a href="#eq1">(Eq. 1)</a>. To calibrate the developed behavior model, an intrusive measurement was conducted from December 16, 2019, to December 20, 2019. This measurement aimed to determine the correction parameters in <a href="#eq2">(Eq. 2)</a> using the Markov chain Monte Carlo (MCMC) method and the Metropolis–Hastings algorithm.
</p>

<p id="eq1"><strong>Eq. 1:</strong></p>
<p>$$ P_{sup} = H_{ref} \left( \frac{f_{pu}}{f_{ref}} \right)^2 + P_{ret} $$</p>

<p id="eq2"><strong>Eq. 2:</strong></p>
<p>$$ f_c(X_c, \theta_c) = \theta_{c,1} + \theta_{c,2} \times (T_{sup} - T_{ret}) $$</p>

<hr class="thin">

# Example RDF Content

<p>아래의 상자에서 `.rdf` 파일 내용을 복사할 수 있습니다. 내용이 길기 때문에 스크롤을 통해 필요한 부분만 볼 수 있습니다.</p>

<div style="border: 1px solid #ddd; padding: 10px; background-color: #f9f9f9; overflow: auto; max-height: 400px; white-space: pre; font-family: monospace;">
&lt;?xml version="1.0" encoding="utf-8"?&gt;
&lt;rdf:RDF
   xmlns:brick1="https://brickschema.org/schema/1.2/Brick#"
   xmlns:VB="https://skku-bist.github.io/method#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
&gt;
  &lt;rdf:Description rdf:about="https://skku-bist.github.io/method#BehaviorModel_DT"&gt;
    &lt;VB:hasVirtualdataOf rdf:resource="https://skku-bist.github.io/method#VirtualData_DT"/&gt;
    &lt;VB:isAssembledWith rdf:resource="https://skku-bist.github.io/method#CorrectionModel_SP"/&gt;
  &lt;/rdf:Description&gt;
  
  &lt;rdf:Description rdf:about="https://skku-bist.github.io/method#VirtualData_DT"&gt;
    &lt;VB:isInputOf rdf:resource="https://skku-bist.github.io/method#CorrectionModel_SP"/&gt;
    &lt;brick1:hasTag rdf:resource="https://brickschema.org/schema/1.2/Brick#Water_Differential_Temperature_Sensor"/&gt;
  &lt;/rdf:Description&gt;
  
  &lt;rdf:Description rdf:about="https://brickschema.org/schema/1.2/Brick#Supply_Pressure_Sensor"&gt;
    &lt;brick1:isPointOf rdf:resource="https://brickschema.org/schema/1.2/Brick#Heat_Exchanger"/&gt;
  &lt;/rdf:Description&gt;
  
  <!-- 중략 -->

  &lt;rdf:Description rdf:about="https://skku-bist.github.io/method#DistanceModel_SP"&gt;
    &lt;VB:estimates rdf:resource="https://skku-bist.github.io/method#CorrectionModel_SP"/&gt;
    &lt;brick1:hasTag rdf:resource="https://brickschema.org/schema/1.2/Brick#Supply_Pressure_Sensor"/&gt;
  &lt;/rdf:Description&gt;
&lt;/rdf:RDF&gt;
</div>

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
