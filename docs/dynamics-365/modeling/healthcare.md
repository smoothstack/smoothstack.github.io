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

<div class="code-example" markdown="1">

#### Entity Types
{: .no_toc }

{% include color_label.md entity_type='**Custom Entity**' label_color="healthcare" %}
{% include color_label.md entity_type='**Extended Entity**' label_color="default-entity" %}

---

#### Field Types
{: .no_toc }

{% include color_field.md field='**Custom Field,**' color="healthcare-blue" %}
{% include color_field.md field='**Default Field,**' color="aurora-green" %}
{% include color_field.md field='**Foreign Key (Lookup)**' color="aurora-purple" %}

</div>

---

## Healthcare Professional
{: .d-inline-block .label-not-really-title }

Custom
{: .label .label-healthcare }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='healthcare-blue' %} | Primary key | Healthcare professional ID |
| {% include colortext.md field='License Type' color='healthcare-blue' %} | Option set | Medical Doctor, Psychiatrist, Physician's Assistant, Veterinarian, Dentist |
| {% include colortext.md field='Specialization' color='healthcare-blue' %} | Option set | Internal Medicine, Gynecology, Cardiology, Nephrology, Neurology, Geriatrics, Pediatrics |
| {% include colortext.md field='First Name' color='aurora-green' %} | Single line of text | Healthcare professional first name |
| {% include colortext.md field='Last Name' color='aurora-green' %} | Single line of text | Healthcare professional last name |
| {% include colortext.md field='Email' color='aurora-green' %} | Email | Healthcare professional email address |
| {% include colortext.md field='Address' color='aurora-green' %} | Single line of text | Healthcare professional address |
| {% include colortext.md field='Phone' color='aurora-green' %} | Phone | Healthcare professional phone number |
| {% include colortext.md field='Service Provider ID' color='aurora-purple' %} | Lookup | Service provider foreign key |

---

## Service Event
{: .d-inline-block .label-not-really-title }

Custom
{: .label .label-healthcare }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='healthcare-blue' %} | Primary key | Service event ID |
| {% include colortext.md field='Event Date' color='healthcare-blue' %} | Date | Date of service |
| {% include colortext.md field='Reason' color='healthcare-blue' %} | Multiple lines of text | Reason for test |
| {% include colortext.md field='Patient ID' color='aurora-purple' %} | Lookup | Patient foreign key |
| {% include colortext.md field='Healthcare Professional ID' color='aurora-purple' %} | Lookup | Healthcare professional foreign key |

---

## Service Provider
{: .d-inline-block .label-not-really-title }

Account
{: .label .label-default-entity }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='aurora-green' %} | Primary key | Provider ID |
| {% include colortext.md field='Name' color='aurora-green' %} | Single line of text | Provider name |
| {% include colortext.md field='Address' color='aurora-green' %} | Single line of text | Provider address |
| {% include colortext.md field='Phone' color='aurora-green' %} | Phone | Provider phone number |
| {% include colortext.md field='Website' color='aurora-green' %} | URL | Provider website |
| {% include colortext.md field='Insurance Participation' color='healthcare-blue' %} | Multi-Select Option Set | Aetna, Anthem, CareFirst, Cigna Health, Humana, Kaiser Permanente, UnitedHealth |
| {% include colortext.md field='Account Type' color='healthcare-blue' %} | Option set | Insurance company, service provider |
| {% include colortext.md field='Provider Type' color='healthcare-blue' %} | Option set | Private Practice, Nursing Home, Urgent Care Clinic, Free-Standing Facility, Hospital |