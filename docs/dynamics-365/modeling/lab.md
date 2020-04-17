---
layout: default
title: Diagnostic Service Performed
parent: Modeling the Entities
grand_parent: Dynamics 365
nav_order: 3
---

# Diagnostic Service Performed
{: .no_toc }

See [Product Catalog]({{ site.baseurl }}{% link docs/dynamics-365/product-catalog.md %}/#external-references) to see the list of products.
{: .fs-3 .mb-6 }

<div class="code-example" markdown="1">

#### Table of Contents
{: .no_toc }

1. TOC
{:toc}

</div>

---

<img src='/assets/images/lab.png' />

---

<div class="code-example" markdown="1">

#### Entity Types
{: .no_toc }

{% include color_label.md entity_type='**Custom Entity**' label_color="lab" %}
{% include color_label.md entity_type='**Extended Entity**' label_color="default-entity" %}

---

#### Field Types
{: .no_toc }

{% include color_field.md field='**Custom Field,**' color="lab-orange" %}
{% include color_field.md field='**Default Field,**' color="aurora-green" %}
{% include color_field.md field='**Foreign Key (Lookup)**' color="aurora-purple" %}

</div>

---

## Lab Order
{: .d-inline-block .label-not-really-title }

Custom
{: .label .label-lab }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='lab-orange' %} | Primary key | Lab order ID |
| {% include colortext.md field='Order Date' color='lab-orange' %} | Date | Date test was ordered |
| {% include colortext.md field='Status Reason' color='lab-orange' %} | Status Reason | _(Active)_ Preparation, In-Progress;      _(Inactive)_ Completed, Canceled |
| {% include colortext.md field='Status' color='aurora-green' %} | Status | Active or Inactive |
| {% include colortext.md field='Service Event ID' color='aurora-purple' %} | Lookup | Service event that produced this order |
| {% include colortext.md field='Lab Product ID' color='aurora-purple' %} | Lookup | Medical procedure being ordered |

---

## Lab Result
{: .d-inline-block .label-not-really-title }

Custom
{: .label .label-lab }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='lab-orange' %} | Primary key | Lab result ID |
| {% include colortext.md field='Result Date' color='lab-orange' %} | Date | Date the test result is produced |
| {% include colortext.md field='Numeric Value' color='lab-orange' %} | Decimal number | Numeric value of the tested metric |
| {% include colortext.md field='Unit of Measurement' color='lab-orange' %} | Single line of text | Unit of measure for the tested metric |
| {% include colortext.md field='Remarks' color='lab-orange' %} | Multiple lines of text | Notable comments regarding the test results |
| {% include colortext.md field='Lab Cost' color='lab-orange' %} | Currency | The price charged by the lab company for the lab test, expressed in Currency |
| {% include colortext.md field='Lab Order ID' color='aurora-purple' %} | Lookup | Which lab order these results correspond to |

---

## Lab Product
{: .d-inline-block .label-not-really-title }

Product Catalog
{: .label .label-default-entity }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='aurora-green' %} | Primary key | Medical procedure ID |
| {% include colortext.md field='Name' color='aurora-green' %} | Single line of text | Descriptive name of the medical procedure |
| {% include colortext.md field='Product Type' color='lab-orange' %} | Option set | Standard Medical Procedure, Derived Product |
| {% include colortext.md field='CPT Code' color='lab-orange' %} | Single line of text | Standardized code for billing a medical procedure |

---

## Lab Price List
{: .d-inline-block .label-not-really-title }

Price List
{: .label .label-default-entity }

| Field | Dynamics Datatype | Description |
|:------|:------------|:-|
| {% include colortext.md field='ID' color='aurora-green' %} | Primary key | Medical procedure ID |
| {% include colortext.md field='Unit Price' color='aurora-green' %} | Currency | The price per unit of Lab Product, expressed in Currency |
| {% include colortext.md field='Insurance Network' color='lab-orange' %} | Option set | Aetna, Anthem, CareFirst, Cigna Health, Humana, Kaiser Permanente, UnitedHealth |
| {% include colortext.md field='Lab Product ID' color='aurora-purple' %} | Lookup | Lab product this price applies to |