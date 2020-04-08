---
layout: default
title: Patient Health Data
parent: Modeling the Entities
grand_parent: Dynamics 365
nav_order: 1
---

# Patient Health Data
{: .no_toc .fs-9 }

<div class="code-example" markdown="1">

#### Patient Entities
{: .no_toc }

1. TOC
{:toc}

</div>

---

<img src="/assets/images/patient.png" />

---

<div class="code-example" markdown="1">

#### Entity Types
{: .no_toc }

{% include color_label.md entity_type='**Custom Entity**' label_color="patient" %}
{% include color_label.md entity_type='**Extended Entity**' label_color="default-entity" %}

---

#### Field Types
{: .no_toc }

{% include color_field.md field='**Custom Field,**' color="patient-yellow" %}
{% include color_field.md field='**Default Field,**' color="aurora-green" %}
{% include color_field.md field='**Foreign Key (Lookup)**' color="aurora-purple" %}

</div>

---

## List of Ailments
{: .d-inline-block .label-not-really-title }

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
{: .d-inline-block .label-not-really-title }

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
{: .d-inline-block .label-not-really-title }

Contact
{: .label .label-default-entity }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='aurora-green' %} | Primary key | Patient ID |
| {% include colortext.md field='First Name' color='aurora-green' %} | Single line of text | Patient first name |
| {% include colortext.md field='Last Name' color='aurora-green' %} | Single line of text | Patient last name |
| {% include colortext.md field='Gender' color='aurora-green' %} | Option set | Patient gender |
| {% include colortext.md field='Address' color='aurora-green' %} | Single line of text | Patient address |
| {% include colortext.md field='Email' color='aurora-green' %} | Email | Patient email address |
| {% include colortext.md field='Phone' color='aurora-green' %} | Phone | Patient phone number |
| {% include colortext.md field='Birth Date' color='patient-yellow' %} | Date Only | Patient birth date |
| {% include colortext.md field='Contact Type' color='patient-yellow' %} | Option set | Patient & optionally, insurance agent |
| {% include colortext.md field='Age' color='patient-yellow' %} | Calculated field (cur date - birth date) | Patient age |
| {% include colortext.md field='Height' color='patient-yellow' %} | Whole number | Patient height (cm) |
| {% include colortext.md field='Weight' color='patient-yellow' %} | Float | Patient weight (kg) |
| {% include colortext.md field='Body Mass Index' color='patient-yellow' %} | Calculated field ((weight / height^2)*10,000) | Patient BMI (unitless) |
| {% include colortext.md field='Insurance Plan ID' color='aurora-purple' %} | Lookup | Insurance plan foreign key |