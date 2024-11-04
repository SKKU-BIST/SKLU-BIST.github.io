---
layout: default
title: Example
---

<hr class="thin">

## Example RDF Content
<textarea style="width: 100%; height: 400px; border: 1px solid #ddd; padding: 10px; background-color: #f9f9f9; font-family: monospace;">
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

</textarea>
