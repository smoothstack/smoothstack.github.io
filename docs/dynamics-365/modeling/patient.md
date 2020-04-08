---
layout: default
title: Patient Health Data
parent: Modeling the Entities
grand_parent: Dynamics 365
nav_order: 1
---

# Patient Health Data
{: .no_toc }

<div class="code-example" markdown="1">

#### Table of Contents
{: .no_toc }

1. TOC
{:toc}

</div>

---

<img src='/assets/images/patient.png' />

---

## List of Ailments
{: .d-inline-block }

Custom
{: .label .label-patient }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='Date of Onset' color='patient-yellow' %} | Date | When the disease began |
| {% include colortext.md field='Current Medication' color='patient-yellow' %} | Single line of text | Name of current medication |
| {% include colortext.md field='Medication Dosage' color='patient-yellow' %} | Whole number | Dosage of medication |
| {% include colortext.md field='Medication Unit of Measure' color='patient-yellow' %} | Single line of text | Unit the dosage is measured in |
| {% include colortext.md field='Medication Frequency' color='patient-yellow' %} | Single line of text | How frequently the medication is taken |
| {% include colortext.md field='Disease Classification ID' color='aurora-purple' %} | Lookup | Disease classification foreign key |
| {% include colortext.md field='Patient ID' color='aurora-purple' %} | Lookup | Patient foreign key |

---

## Disease Classification
{: .d-inline-block }

Custom
{: .label .label-patient }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='patient-yellow' %} | Primary key | Disease Classification ID |
| {% include colortext.md field='ICD-10 Code' color='patient-yellow' %} | Single line of text | Standardized code for disease classification |
| {% include colortext.md field='Short Name' color='patient-yellow' %} | Single line of text | Short, common name for the disease |
| {% include colortext.md field='Long Name' color='patient-yellow' %} | Single line of text | Long, descriptive name for the disease |
| {% include colortext.md field='Affected System' color='patient-yellow' %} | Option set | Immune system, cardiovascular system, etc. |

---

## Patient
{: .d-inline-block }

Contact
{: .label .label-default-entity }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='aurora-green' %} | Primary key | Patient ID |
| {% include colortext.md field='Contact Type' color='aurora-green' %} | Option set | Patient & optionally, insurance agent |
| {% include colortext.md field='First Name' color='aurora-green' %} | Single line of text | Patient first name |
| {% include colortext.md field='Last Name' color='aurora-green' %} | Single line of text | Patient last name |
| {% include colortext.md field='Gender' color='aurora-green' %} | Option set | Patient gender |
| {% include colortext.md field='Birth Date' color='aurora-green' %} | Date Only | Patient birth date |
| {% include colortext.md field='Address' color='aurora-green' %} | Single line of text | Patient address |
| {% include colortext.md field='Email' color='aurora-green' %} | Email | Patient email address |
| {% include colortext.md field='Phone' color='aurora-green' %} | Phone | Patient phone number |
| {% include colortext.md field='Age' color='aurora-green' %} | Calculated field (cur date - birth date) | Patient age |
| {% include colortext.md field='Height' color='aurora-green' %} | Whole number | Patient height (cm) |
| {% include colortext.md field='Weight' color='aurora-green' %} | Float | Patient weight (kg) |
| {% include colortext.md field='Body Mass Index' color='aurora-green' %} | Calculated field ((weight / height^2)*10,000) | Patient BMI (unitless) |
| {% include colortext.md field='Insurance Plan ID' color='aurora-purple' %} | Lookup | Insurance plan foreign key |