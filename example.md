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

<p class="spaced">
</p>
<p class="spaced">
</p>
<p class="spaced">
</p>
<p class="spaced">
</p>

# Example RDF Content

<p>아래의 상자에서 `.rdf` 파일 내용을 복사할 수 있습니다. 내용이 길기 때문에 스크롤을 통해 필요한 부분만 볼 수 있습니다.</p>

<div style="border: 1px solid #ddd; padding: 10px; background-color: #f9f9f9; overflow: auto; max-height: 400px; white-space: pre;">
<?xml version="1.0" encoding="utf-8"?>
<rdf:RDF
   xmlns:brick1="https://brickschema.org/schema/1.2/Brick#"
   xmlns:VB="https://skku-bist.github.io/method#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
>
  <rdf:Description rdf:about="https://skku-bist.github.io/method#BehaviorModel_DT">
    <VB:hasVirtualdataOf rdf:resource="https://skku-bist.github.io/method#VirtualData_DT"/>
    <VB:isAssembledWith rdf:resource="https://skku-bist.github.io/method#CorrectionModel_SP"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://skku-bist.github.io/method#VirtualData_DT">
    <VB:isInputOf rdf:resource="https://skku-bist.github.io/method#CorrectionModel_SP"/>
    <brick1:hasTag rdf:resource="https://brickschema.org/schema/1.2/Brick#Water_Differential_Temperature_Sensor"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://brickschema.org/schema/1.2/Brick#Supply_Pressure_Sensor">
    <brick1:isPointOf rdf:resource="https://brickschema.org/schema/1.2/Brick#Heat_Exchanger"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://skku-bist.github.io/method#IntrusiveData_SP">
    <VB:isInputOf rdf:resource="https://skku-bist.github.io/method#DistanceModel_SP"/>
    <brick1:hasTag rdf:resource="https://brickschema.org/schema/1.2/Brick#Supply_Pressure_Sensor"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://skku-bist.github.io/method#BehaviorModel_SP">
    <VB:hasVirtualdataOf rdf:resource="https://skku-bist.github.io/method#VirtualData_SP"/>
    <VB:isLinkedWith rdf:resource="https://skku-bist.github.io/method#DistanceModel_SP"/>
    <brick1:hasTag rdf:resource="https://brickschema.org/schema/1.2/Brick#Supply_Pressure_Sensor"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://brickschema.org/schema/1.2/Brick#Pump">
    <brick1:hasPoint rdf:resource="https://brickschema.org/schema/1.2/Brick#Pump_Frequency_Sensor"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://skku-bist.github.io/method#NonintrusiveData_2ST">
    <VB:isInputOf rdf:resource="https://skku-bist.github.io/method#BehaviorModel_DT"/>
    <brick1:hasTag rdf:resource="https://brickschema.org/schema/1.2/Brick#Heat_Exchanger_Supply_Water_Temperature_Sensor"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://brickschema.org/schema/1.2/Brick#Primary_Supply_Temperature_Sensor">
    <brick1:isPointOf rdf:resource="https://brickschema.org/schema/1.2/Brick#Heat_Exchanger"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://skku-bist.github.io/method#NonintrusiveData_RP">
    <VB:isInputOf rdf:resource="https://skku-bist.github.io/method#BehaviorModel_SP"/>
    <brick1:hasTag rdf:resource="https://brickschema.org/schema/1.2/Brick#Return_Pressure_Sensor"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://brickschema.org/schema/1.2/Brick#Differential_Pressure_Control_Valve">
    <brick1:hasPoint rdf:resource="https://brickschema.org/schema/1.2/Brick#Differential_Pressure_Sensor"/>
    <brick1:hasPoint rdf:resource="https://brickschema.org/schema/1.2/Brick#DPV_Valve_Opening"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://brickschema.org/schema/1.2/Brick#District_Heating_System">
    <brick1:hasPart rdf:resource="https://brickschema.org/schema/1.2/Brick#Pump"/>
    <brick1:hasPart rdf:resource="https://brickschema.org/schema/1.2/Brick#Temperature_Control_Valve"/>
    <brick1:hasPart rdf:resource="https://brickschema.org/schema/1.2/Brick#Differential_Pressure_Control_Valve"/>
    <brick1:hasPart rdf:resource="https://brickschema.org/schema/1.2/Brick#Heat_Exchanger"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://brickschema.org/schema/1.2/Brick#Return_Pressure_Sensor">
    <brick1:isPointOf rdf:resource="https://brickschema.org/schema/1.2/Brick#Heat_Exchanger"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://skku-bist.github.io/method#VirtualData_SP">
    <VB:isInputOf rdf:resource="https://skku-bist.github.io/method#DistanceModel_SP"/>
    <brick1:hasTag rdf:resource="https://brickschema.org/schema/1.2/Brick#Supply_Pressure_Sensor"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://skku-bist.github.io/method#CorrectionModel_SP">
    <VB:calibrates rdf:resource="https://skku-bist.github.io/method#BehaviorModel_SP"/>
    <brick1:hasTag rdf:resource="https://brickschema.org/schema/1.2/Brick#Supply_Pressure_Sensor"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://skku-bist.github.io/method#ontology">
  </rdf:Description>
  
  <rdf:Description rdf:about="https://brickschema.org/schema/1.2/Brick#Temperature_Control_Valve">
    <brick1:hasPoint rdf:resource="https://brickschema.org/schema/1.2/Brick#TCV_Valve_Opening"/>
    <brick1:controls rdf:resource="https://brickschema.org/schema/1.2/Brick#Supply_Setpoint_Temperature"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://skku-bist.github.io/method#NonintrusiveData_2RT">
    <VB:isInputOf rdf:resource="https://skku-bist.github.io/method#BehaviorModel_DT"/>
    <brick1:hasTag rdf:resource="https://brickschema.org/schema/1.2/Brick#Return_Water_Temperature_Sensor"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://brickschema.org/schema/1.2/Brick#Heat_Exchanger_Supply_Water_Temperature_Sensor">
    <brick1:isPointOf rdf:resource="https://brickschema.org/schema/1.2/Brick#Heat_Exchanger"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://brickschema.org/schema/1.2/Brick#Return_Water_Temperature_Sensor">
    <brick1:isPointOf rdf:resource="https://brickschema.org/schema/1.2/Brick#Heat_Exchanger"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://brickschema.org/schema/1.2/Brick#Primary_Return_Temperature_Sensor">
    <brick1:isPointOf rdf:resource="https://brickschema.org/schema/1.2/Brick#Heat_Exchanger"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://skku-bist.github.io/method#NonintrusiveData_PF">
    <VB:isInputOf rdf:resource="https://skku-bist.github.io/method#BehaviorModel_SP"/>
    <brick1:hasTag rdf:resource="https://brickschema.org/schema/1.2/Brick#Pump_Frequency_Sensor"/>
  </rdf:Description>
  
  <rdf:Description rdf:about="https://skku-bist.github.io/method#DistanceModel_SP">
    <VB:estimates rdf:resource="https://skku-bist.github.io/method#CorrectionModel_SP"/>
    <brick1:hasTag rdf:resource="https://brickschema.org/schema/1.2/Brick#Supply_Pressure_Sensor"/>
  </rdf:Description>
</rdf:RDF>
</div>

<style>
    div {
    }
</style>


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
