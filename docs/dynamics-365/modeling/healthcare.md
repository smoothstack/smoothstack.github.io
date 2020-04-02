---
layout: default
title: Healthcare System Data
parent: Modeling the Entities
grand_parent: Dynamics 365
nav_order: 2
---

# Healthcare System Data
{: .no_toc }

<div class="code-example" markdown="1">

#### Table of Contents
{: .no_toc }

1. TOC
{:toc}

</div>

---

<img src='/assets/images/healthcare.png' /> 

---

## Service Provider
{: .d-inline-block }

Custom
{: .label .label-blue }

| Field | Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='blue-100' %} | INT (pk) | Provider ID |
| {% include colortext.md field='Type' color='blue-100' %} | VARCHAR | Hospital, urgent care, private practice, etc. |
| {% include colortext.md field='Name' color='blue-100' %} | VARCHAR | Provider name |
| {% include colortext.md field='Address' color='blue-100' %} | VARCHAR | Provider address |
| {% include colortext.md field='Phone' color='blue-100' %} | VARCHAR | Provider phone number |
| {% include colortext.md field='Fax' color='blue-100' %} | VARCHAR | Provider fax number |

---

## Healthcare Professional
{: .d-inline-block }

Custom
{: .label .label-blue }

| Field | Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='blue-100' %} | INT (pk) | Healthcare professional ID |
| {% include colortext.md field='License Type' color='blue-100' %} | VARCHAR | Nurse, MD, Physician's Assistant, etc. |
| {% include colortext.md field='Specialization' color='blue-100' %} | VARCHAR | Internal medicine, cardiology, etc. |
| {% include colortext.md field='First Name' color='blue-100' %} | VARCHAR | Healthcare professional first name |
| {% include colortext.md field='Last Name' color='blue-100' %} | VARCHAR | Healthcare professional last name |
| {% include colortext.md field='Email' color='green' %} | VARCHAR | Healthcare professional email address |
| {% include colortext.md field='Address' color='blue-100' %} | VARCHAR | Healthcare professional address |
| {% include colortext.md field='Phone' color='blue-100' %} | VARCHAR | Healthcare professional phone number |
| {% include colortext.md field='Fax' color='blue-100' %} | VARCHAR | Healthcare professional fax number |
| {% include colortext.md field='Service Provider ID' color='purple-100' %} | INT (fk) | Service provider foreign key |

---

## Service Event
{: .d-inline-block }

Custom
{: .label .label-blue }

| Field | Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='blue-100' %} | INT (pk) | Service event ID |
| {% include colortext.md field='Event Date' color='blue-100' %} | VARCHAR | Date of service |
| {% include colortext.md field='Reason' color='blue-100' %} | VARCHAR | Reason for test |
| {% include colortext.md field='Event Date' color='blue-100' %} | VARCHAR | Date of service |
| {% include colortext.md field='Patient ID' color='purple-100' %} | INT (fk) | Patient foreign key |
| {% include colortext.md field='Healthcare Professional ID' color='purple-100' %} | INT (fk) | Healthcare professional foreign key |
