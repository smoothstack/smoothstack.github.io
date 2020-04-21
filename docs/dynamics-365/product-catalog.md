---
layout: default
title: Product Catalog
parent: Dynamics 365
description: "Knowledge Base for the Clinical Lab CRM Project"
nav_order: 3
---

# Product Catalog
{: .no_toc .fs-9 }

#### Catalog Contents
{: .no_toc .mb-4 }

| Item #  | Product Type | Package Type |
|:-|:-|:-|
| {% include color_link2.md title='1-11' link_color='aurora-green' link='#products' %} | Lab Test | Individual |
| {% include color_link2.md title='12-14' link_color='aurora-purple' link='#bundles' %} | Lab Test | Bundle |
| {% include color_link2.md title='15-17' link_color='aurora-yellow' link='#events' %} | Collection Service | Individual |

---

{% include bundle.md field='Product' color='aurora-green' %}

<ul id='products'>
{% include product.md field='Complete Genome Sequence' number='1' price='$2,000' color='aurora-green' unit='Test' %}
</ul>

<ul>
{% include product.md field='Nasal Mucosal Assay' number='2' price='$10' color='aurora-green' unit='Test' %}
</ul>

<ul>
{% include product.md field='Coronavirus Antibody Test' number='3' price='$15' color='aurora-green' unit='Test' %}
</ul>

<ul>
{% include product.md field='Complete Blood Count' number='4' price='$30' color='aurora-green' unit='Test' %}
</ul>

<ul>
{% include product.md field='Prothrombin Time' number='5' price='$55' color='aurora-green' unit='Test' %}
</ul>

<ul>
{% include product.md field='Basic Metabolic Panel' number='6' price='$65' color='aurora-green' unit='Test' %}
</ul>

<ul>
{% include product.md field='Lipid Panel' number='7' price='$30' color='aurora-green' unit='Test' %}
</ul>

<ul>
{% include product.md field='Liver Panel' number='8' price='$35' color='aurora-green' unit='Test' %}
</ul>

<ul>
{% include product.md field='Thyroid Stimulating Hormone' number='9' price='$15' color='aurora-green' unit='Test' %}
</ul>

<ul>
{% include product.md field='Hemoglobin A1C' number='10' price='$35' color='aurora-green' unit='Test' %}
</ul>

<ul>
{% include product.md field='Urinalysis' number='11' price='$45' color='aurora-green' unit='Test' %}
</ul>

{% include hidetext.md field='.' %}

---

{% include bundle.md field='Bundle' color='aurora-purple' %}
<ul id='bundles' class="bundles">
{% include bundle-head.md field='Comprehensive Diabetes Monitoring' number='12' price='$75' color='aurora-purple' unit='Bundle' %}
{% include bundle-child.md field='Hemoglobin A1C' %}
{% include bundle-child.md field='Urinalysis' %}
</tbody></table></li>
</ul>

<ul class="bundles">
{% include bundle-head.md field='Comprehensive Metabolic Panel' number='13' price='$105' color='aurora-purple' unit='Bundle' %}
{% include bundle-child.md field='Basic Metabolic Panel' %}
{% include bundle-child.md field='Liver Panel' %}
{% include bundle-child.md field='Thyroid Stimulating Hormone' %}
</tbody></table></li>
</ul>

<ul class="bundles">
{% include bundle-head.md field='Comprehensive COVID-19 Assesment' number='14' price='$75' color='aurora-purple' unit='Bundle' %}
{% include bundle-child.md field='Nasal Mucosal Assay' %}
{% include bundle-child.md field='Coronavirus Antibody Test' %}
</tbody></table></li>
</ul>

{% include hidetext.md field='.' %}

---

{% include bundle.md field='Event' color='aurora-yellow' %}

<ul id='events'>
{% include product.md field='Specimen Pickup Service' number='15' price='50' color='aurora-yellow' unit='Event' %}
</ul>

<ul>
{% include product.md field='On-Site Specimen Collection' number='16' price='$350' color='aurora-yellow' unit='Event' %}
</ul>

<ul>
{% include product.md field='Mobile Collection Event' number='17' price='$500' color='aurora-yellow' unit='Event' %}
</ul>

{% include hidetext.md field='.' %}
