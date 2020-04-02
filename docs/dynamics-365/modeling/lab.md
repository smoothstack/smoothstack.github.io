---
layout: default
title: Diagnostic Service Performed
parent: Modeling the Entities
grand_parent: Dynamics 365
nav_order: 3
---

# Diagnostic Service Performed
{: .no_toc }

<div class="code-example" markdown="1">

#### Table of Contents
{: .no_toc }

1. TOC
{:toc}

</div>

---

<img src='/assets/images/lab.png' />

---

## Lab Order
{: .d-inline-block }

Custom
{: .label .label-blue }

| Field | Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='blue-100' %} | INT (pk) | Lab order ID |
| {% include colortext.md field='Order Date' color='blue-100' %} | VARCHAR | Date test was ordered |
| {% include colortext.md field='Service Event ID' color='purple-100' %} | INT (fk) | Service event that produced this order |
| {% include colortext.md field='Medical procedure ID' color='purple-100' %} | INT (fk) | Medical procedure being ordered |

---

## Medical Procedure
{: .d-inline-block }

Custom
{: .label .label-blue }

| Field | Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='blue-100' %} | INT (pk) | Medical procedure ID |
| {% include colortext.md field='CPT Code' color='blue-100' %} | VARCHAR | Standardized code for billing a medical procedure |
| {% include colortext.md field='Name' color='blue-100' %} | VARCHAR | Descriptive name of the medical procedure |

---

## Lab Result
{: .d-inline-block }

Custom
{: .label .label-blue }

| Field | Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='blue-100' %} | INT (pk) | Lab result ID |
| {% include colortext.md field='Result Date' color='blue-100' %} | VARCHAR | Date the test result is produced |
| {% include colortext.md field='Numeric Value' color='blue-100' %} | VARCHAR | Numeric value of the tested metric |
| {% include colortext.md field='Unit of Measurement' color='blue-100' %} | VARCHAR | Unit of measure for the tested metric |
| {% include colortext.md field='Remarks' color='blue-100' %} | VARCHAR | Notable comments regarding the test results |
| {% include colortext.md field='Lab Order ID' color='purple-100' %} | INT (fk) | Which lab order these results correspond to |

