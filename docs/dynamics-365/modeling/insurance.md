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
{: .label .label-insurance }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='insurance-purple' %} | Primary key | Insurance plan ID (member ID) |
| {% include colortext.md field='Policy Number' color='insurance-purple' %} | Single line of text | Patient's insurance policy number |
| {% include colortext.md field='Group Number' color='insurance-purple' %} | Single line of text | Patient's insurance group number |
| {% include colortext.md field='Plan Type' color='insurance-purple' %} | Option set | PPO, HMO, POS |
| {% include colortext.md field='Deductable' color='insurance-purple' %} | Currency | Insurance plan deductible, expressed in Currency |
| {% include colortext.md field='Insurance Company ID' color='aurora-orange' %} | Lookup | Insurance company foreign key |

---

## Lab Invoice
{: .d-inline-block }

Invoices
{: .label .label-default-entity }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='aurora-green' %} | Primary key | Lab invoice ID |
| {% include colortext.md field='Invoice Date' color='aurora-green' %} | Date | Date invoice produced |
| {% include colortext.md field='Customer' color='aurora-green' %} | Customer | Account, Contact |
| {% include colortext.md field='Total Price' color='aurora-green' %} | Currency | Total invoice price, including all itemized Lab Products, expressed in Currency |
| {% include colortext.md field='Status' color='aurora-green' %} | Status | Active or Inactive |
| {% include colortext.md field='Status Reason' color='aurora-green' %} | Status Reason | _(Active)_ Unpaid, Partially paid;      _(Inactive)_ Paid in full, Waived |

---

## Insurance Company
{: .d-inline-block }

Account
{: .label .label-default-entity }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='aurora-green' %} | Primary key | Insurance Carrier ID |
| {% include colortext.md field='Account Type' color='aurora-green' %} | Option set | Insurance company, service provider |
| {% include colortext.md field='Carrier Type' color='aurora-green' %} | Option set | Private or Government sponsored |
| {% include colortext.md field='Name' color='aurora-green' %} | Single line of text | Insurance company's name |
| {% include colortext.md field='Address' color='aurora-green' %} | Single line of text | Carrier address |
| {% include colortext.md field='Phone' color='aurora-green' %} | Phone | Carrier phone number |
| {% include colortext.md field='Website' color='aurora-green' %} | URL | Carrier website |

---

## Insurance Agent
{: .d-inline-block }

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
