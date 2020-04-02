---
layout: default
title: Insurance Billing Data
parent: Modeling the Entities
grand_parent: Dynamics 365
nav_order: 4
---

# Insurance Billing Data
{: .no_toc }

<div class="code-example" markdown="1">

#### Table of Contents
{: .no_toc }

1. TOC
{:toc}

</div>

---

<img src='/assets/images/insurance.png' />

---

## Insurance Plan
{: .d-inline-block }

Custom
{: .label .label-blue }

| Field | Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='blue-100' %} | INT (pk) | Insurance plan ID (member ID) |
| {% include colortext.md field='Policy Number' color='blue-100' %} | VARCHAR | Patient's insurance policy number |
| {% include colortext.md field='Group Number' color='blue-100' %} | VARCHAR | Patient's insurance group number |
| {% include colortext.md field='Plan Type' color='blue-100' %} | VARCHAR | PPO, HMO, Medicare, Medicaid, etc. |
| {% include colortext.md field='Insurance Carrier ID' color='purple-100' %} | INT (fk) | Insurance carrier foreign key |

---

## Insurance Carrier
{: .d-inline-block }

Account
{: .label .label-green }

| Field | Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='green' %} | INT (pk) | Insurance Carrier ID |
| {% include colortext.md field='Carrier Type' color='green' %} | VARCHAR | Private or Public |
| {% include colortext.md field='Name' color='green' %} | VARCHAR | Insurance company's name |
| {% include colortext.md field='Address' color='green' %} | VARCHAR | Carrier address |
| {% include colortext.md field='Phone' color='green' %} | VARCHAR | Carrier phone number |
| {% include colortext.md field='Fax' color='green' %} | VARCHAR | Carrier fax number |


---

## Insurance Agent
{: .d-inline-block }

Contact
{: .label .label-green }

| Field | Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='green' %} | INT (pk) | Agent ID |
| {% include colortext.md field='First Name' color='green' %} | VARCHAR | Agent's first name |
| {% include colortext.md field='Last Name' color='green' %} | VARCHAR | Agent's last name |
| {% include colortext.md field='Phone' color='green' %} | VARCHAR | Agent's phone number |
| {% include colortext.md field='Email' color='green' %} | VARCHAR | Agent's email address |
| {% include colortext.md field='Fax' color='green' %} | VARCHAR | Agent's fax number |
| {% include colortext.md field='Insurance Carrier ID' color='purple-100' %} | INT (fk) | Insurance carrier foreign key |

---