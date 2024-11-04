---
layout: default
title: Method
---
<hr class="thin">
# VB schema

<style>
    hr.thin {
        border: 0;
        height: 1px;
        background: #ccc;
    }
    
    .spaced {
        margin-top: 20px; /* 위쪽 여백 */
        margin-bottom: 20px; /* 아래쪽 여백 */
    }
</style>

The relationship between data and virtual models, as well as the classes for data and virtual models are defined.


<p align="center">
    <img src="/assets/images/Fig_2.png" alt="Project Overview" width="500">
</p>

<hr class="thin">

# The integration of the VB schema and Brick schema

To implement the VB schema for building digital twinning, it is essential to use sensor data collected from actual buildings to achieve various applications. Therefore, the Brick schema, which describes the actual building system, was integrated with the VB schema.

<p align="center">
    <img src="/assets/images/Fig_3.png" alt="Project Overview" width="700">
</p>

<hr class="thin">

# Data Classification

The development of wireless communication technologies, such as the Internet of Things (IoT), and building management systems (BMS) resulted in significant improvements in the field of data collection. As tremendous amounts of data have accumulated in recent years, the integration of data from various sources and effective data management are now available. Therefore, in this context, three data subclasses were defined according to the data sources in the VB schema.

| [On-site data](#on-site-data)   | [Off-site data](#off-site-data)  | [Virtual data](#virtual-data)   |

<hr class="thin">

# Virtual Model Classification

Modeling an accurate behavior model is challenging because of the continuous changes in the systems being built over time. To address this issue, it is crucial to model the behavior of a virtual building, detect anomalies, and calibrate the target virtual behavior model during the building operation phase. Therefore, based on the perspectives of VIM and VIC, three subclasses of virtual models–the (1) behavior model, (2) correction model, and (3) distance model–are defined.

| [Behavior model](#behavior-model) | [Correction model](#correction-model) | [Distance model](#distance-model) |

<hr class="thin">

# Relationships

Relationships depict interactions and associations between entities. There are four types of relationships: (1) model-model relationships, (2) model–data relationships, (3) model–physical entity relationship, and (4) model–application entity relationship. Model–model relationships represent interactions within the virtual model, while model–data relationships capture interactions between the virtual model and data. Model–physical entity relationships describe a unidirectional connection, where the model represents the behavior of the target physical entity. Lastly, model–application relationships describe how the model is used for the execution of an application.

| [isAssembledWith](#isassembledwith) | [isLinkedWith](#islinkedwith) | [calibrates](#calibrates) | [estimates](#estimates) | [isInputOf](#isinputof) | [hasVirtualData](#hasvirtualdata) | [isUsedFor](#isusedfor) | [isVirtualModelOf](#isvirtualmodelof) |


<p class="spaced">
</p>
<p class="spaced">
</p>
<p class="spaced">
</p>
<p class="spaced">
</p>
<p class="spaced">
</p>
<p class="spaced">
</p>
<p class="spaced">
</p>
<p class="spaced">
</p>

## <a id="on-site-data"></a>On-site Data

On-site data are a subclass of operational data collected by physical sensing networks within target building operations. They are further divided into two categories: (1) nonintrusive data, collected through a built-in sensor network within the building system, and (2) intrusive data, gathered through additional measurements using temporary sensing devices with extra effort.

<hr class="thin">

## <a id="off-site-data"></a>Off-site Data

Off-site data are a subclass of data obtained from sources outside an existing sensing network in a physical building (e.g., simulated or open data). They can be utilized as auxiliary data in a physical building through a fine-tuning process. This is crucial because the sensing network in a real building system often faces limitations owing to financial issues regarding sensor installation, sensor degradation, and unmeasurable variables with conventional sensors.

<hr class="thin">

## <a id="virtual-data"></a>Virtual Data

Virtual data are a subclass of data calculated using virtual models. They have the potential to expand the sensing range and validate and calibrate both physical and virtual data by leveraging virtual models and other DT elements.

<hr class="thin">

## <a id="behavior-model"></a>Behavior Model

The behavior model is a subclass of the virtual model that describes the physical-mathematical behavior of the target building operation. Depending on the modeling environment, the behavior model can be subdivided into two subclasses: (1) the observed model and (2) the unobserved model. The observed model is a behavior model constructed when a physical sensor measures the output variable of the subject model, whereas the unobserved model is built when the measurement of a physical counterpart of the subject model's output is impossible or unreliable.

<hr class="thin">

## <a id="correction-model"></a>Correction Model

The correction model is a subclass of the virtual model that explains the gap between the ground truth values and the output variable of the behavior model. Since the main objective of the correction model is to calibrate the behavior model, when the behavior model turns out to be no longer valid, the correction model calibrates in the behavior model for model calibration.

<hr class="thin">

## <a id="distance-model"></a>Distance Model

The distance model is a subclass of virtual models used for the verification and validation of behavior or correction models. The distance model, which serves as an objective function to estimate the parameters of the virtual model, represents the difference between the output virtual data of the virtual model and its physically measured counterpart data. Consequently, the output virtual data generated by the distance model serve as a trigger for calibrating the behavior model and simultaneously aid in determining the parameters of the models associated with the distance function, accounting for both vertical and horizontal structures.

<hr class="thin">

## <a id="isassembledwith"></a>isAssembledWith

The output variable of the subject behavior model is utilized as the input variable in the object virtual models through the model assembly technique [42]. The output variable of the subject behavior model is utilized as the input variable in the object virtual models through the model assembly technique.

<hr class="thin">

## <a id="islinkedwith"></a>isLinkedWith

The output variable of the subject behavior model is utilized as the input variable in the object distance models to serve as an object function. 

<hr class="thin">

## <a id="calibrates"></a>calibrates

The subject correction model enhances the performance of the object behavior model.

<hr class="thin">

## <a id="estimates"></a>estimates

The subject distance model is used to estimate the model parameter of the object correction model or behavior model.

<hr class="thin">

## <a id="isinputof"></a>isInputOf

The subject data is used as an input variable in the object virtual model.

<hr class="thin">

## <a id="hasvirtualdata"></a>hasVirtualData

The subject virtual model serves as a function to derive the object virtual data as an output variable.

<hr class="thin">

## <a id="isusedfor"></a>isUsedFor

The subject virtual model is utilized to conduct object application.

<hr class="thin">

## <a id="isvirtualmodelof"></a>isVirtualModelOf

The subject virtual model represents the behavior of the object physical entity.

<hr class="thin">
