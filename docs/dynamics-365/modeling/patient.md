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

## Patient
{: .d-inline-block }

Contact
{: .label .label-green }

| Field | Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='green' %} | INT (pk) | Patient ID |
| {% include colortext.md field='First Name' color='green' %} | VARCHAR | Patient first name |
| {% include colortext.md field='Last Name' color='green' %} | VARCHAR | Patient last name |
| {% include colortext.md field='Gender' color='green' %} | VARCHAR | Patient gender |
| {% include colortext.md field='Birth Date' color='green' %} | VARCHAR | Patient birth date |
| {% include colortext.md field='Address' color='green' %} | VARCHAR | Patient address |
| {% include colortext.md field='Email' color='green' %} | VARCHAR | Patient email address |
| {% include colortext.md field='Insurance Plan ID' color='purple-100' %} | INT (fk) | Insurance plan foreign key |

---

## List of Ailments
{: .d-inline-block }

Custom
{: .label .label-blue }

| Field | Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='Disease Classification ID' color='purple-100' %} | INT (fk) | Disease classification foreign key |
| {% include colortext.md field='Patient ID' color='purple-100' %} | INT (fk) | Patient foreign key |
| {% include colortext.md field='Date of Onset' color='blue-100' %} | VARCHAR | When the disease began |
| {% include colortext.md field='Current Medication' color='blue-100' %} | VARCHAR | Name of current medication |
| {% include colortext.md field='Medication Dosage' color='blue-100' %} | VARCHAR | Dosage of medication |

---

## Disease Classification
{: .d-inline-block }

Custom
{: .label .label-blue }

| Field | Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='blue-100' %} | INT (pk) | Disease Classification ID |
| {% include colortext.md field='ICD-10 Code' color='blue-100' %} | VARCHAR | Standardized code for disease classification |
| {% include colortext.md field='Short Name' color='blue-100' %} | VARCHAR | Short, common name for the disease |
| {% include colortext.md field='Long Name' color='blue-100' %} | VARCHAR | Long, descriptive name for the disease |
| {% include colortext.md field='Affected System' color='blue-100' %} | VARCHAR | Immune system, cardiovascular system, etc. |
