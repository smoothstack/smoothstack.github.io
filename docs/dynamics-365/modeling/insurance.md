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

<div class="code-example" markdown="1">

#### Entity Types
{: .no_toc }

{% include color_label.md entity_type='**Custom Entity**' label_color="custom-entity-patient" %}
{% include color_label.md entity_type='**Extended Entity**' label_color="default-entity" %}

---

#### Field Types
{: .no_toc }

{% include color_field.md field='**Custom Field,**' color="aurora-yellow" %}
{% include color_field.md field='**Default Field,**' color="aurora-green" %}
{% include color_field.md field='**Foreign Key (Lookup)**' color="aurora-purple" %}

</div>

---

## Insurance Plan
{: .d-inline-block .label-not-really-title }

Custom
{: .label .label-custom-entity-patient }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='aurora-yellow' %} | Primary key | Insurance plan ID (member ID) |
| {% include colortext.md field='Policy Number' color='aurora-yellow' %} | Single line of text | Patient's insurance policy number |
| {% include colortext.md field='Group Number' color='aurora-yellow' %} | Single line of text | Patient's insurance group number |
| {% include colortext.md field='Plan Type' color='aurora-yellow' %} | Option set | PPO, HMO, POS |
| {% include colortext.md field='Deductible' color='aurora-yellow' %} | Currency | Insurance plan deductible, expressed in Currency |
| {% include colortext.md field='Insurance Company ID' color='aurora-purple' %} | Lookup | Insurance company foreign key |

---

## Lab Invoice
{: .d-inline-block .label-not-really-title }

Invoices
{: .label .label-default-entity }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='aurora-green' %} | Primary key | Lab invoice ID |
| {% include colortext.md field='Customer' color='aurora-green' %} | Customer | Account, Contact |
| {% include colortext.md field='Total Price' color='aurora-green' %} | Currency | Total invoice price, including all itemized Lab Products, expressed in Currency |
| {% include colortext.md field='Invoice Date (Created on)' color='aurora-green' %} | Date | Date invoice produced |
| {% include colortext.md field='Status' color='aurora-green' %} | Status | Active or Inactive |
| {% include colortext.md field='Status Reason' color='aurora-yellow' %} | Status Reason | _(Active)_ Unpaid, Partially paid;      _(Inactive)_ Paid in full, Waived |

---

## Insurance Company
{: .d-inline-block .label-not-really-title }

Account
{: .label .label-default-entity }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='aurora-green' %} | Primary key | Insurance Carrier ID |
| {% include colortext.md field='Name' color='aurora-green' %} | Single line of text | Insurance company's name |
| {% include colortext.md field='Address' color='aurora-green' %} | Single line of text | Carrier address |
| {% include colortext.md field='Phone' color='aurora-green' %} | Phone | Carrier phone number |
| {% include colortext.md field='Website' color='aurora-green' %} | URL | Carrier website |
| {% include colortext.md field='Account Type' color='aurora-yellow' %} | Option set | Insurance company, service provider |
| {% include colortext.md field='Carrier Type' color='aurora-yellow' %} | Option set | Private or Government sponsored |

---

## Insurance Agent
{: .d-inline-block .label-not-really-title }

Contact
{: .label .label-default-entity }

_*Not currently included in our CRM solution_

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='aurora-green' %} | Primary key | Agent ID |
| {% include colortext.md field='First Name' color='aurora-green' %} | Single line of text | Agent's first name |
| {% include colortext.md field='Last Name' color='aurora-green' %} | Single line of text | Agent's last name |
| {% include colortext.md field='Phone' color='aurora-green' %} | Phone | Agent's phone number |
| {% include colortext.md field='Email' color='aurora-green' %} | Email | Agent's email address |
| {% include colortext.md field='Fax' color='aurora-green' %} | Phone | Agent's fax number |
| {% include colortext.md field='Insurance Carrier ID' color='aurora-purple' %} | Lookup | Insurance carrier foreign key |
