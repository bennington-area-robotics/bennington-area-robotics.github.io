---
layout: default
title: Sponsors
---

## Post-Season Donors

{% assign tiers = "5000,1000,500,200,100,0" | split: "," %}
{% assign tier_labels = "$5,000+|$1,000-$4,999|$500-$999|$200-$499|$100-$199|Under $100" | split: "|" %}
{% assign tier_caps = "999999,4999,999,499,199,99" | split: "," %}

{% for tier in tiers %}
{% assign tier_floor = tier | plus: 0 %}
{% assign tier_cap = tier_caps[forloop.index0] | plus: 0 %}
{% assign tier_label = tier_labels[forloop.index0] %}
{% assign names = "" %}
{% assign anon_count = 0 %}
{% assign seen = "" %}

{% for d in site.data.donations.donations %}
  {% if d.type == "family" %}{% continue %}{% endif %}
  {% if d.donor == "Anonymous" or d.donor contains "Anonymous gift" %}
    {% if d.amount >= tier_floor and d.amount <= tier_cap %}
      {% assign anon_count = anon_count | plus: 1 %}
    {% endif %}
    {% continue %}
  {% endif %}
  {% unless seen contains d.donor %}
    {% assign donor_total = 0 %}
    {% for d2 in site.data.donations.donations %}
      {% if d2.donor == d.donor %}
        {% assign donor_total = donor_total | plus: d2.amount %}
      {% endif %}
    {% endfor %}
    {% if donor_total >= tier_floor and donor_total <= tier_cap %}
      {% if names != "" %}{% assign names = names | append: "|" %}{% endif %}
      {% assign names = names | append: d.donor %}
    {% endif %}
    {% assign seen = seen | append: d.donor | append: "||" %}
  {% endunless %}
{% endfor %}

{% assign name_list = names | split: "|" %}
{% if name_list.size > 0 or anon_count > 0 %}
### {{ tier_label }}

{% for name in name_list %}{% assign url = nil %}{% for d in site.data.donations.donations %}{% if d.donor == name and d.url %}{% assign url = d.url %}{% endif %}{% endfor %}- {% if url %}[{{ name }}]({{ url }}){:target="_blank"}{% else %}{{ name }}{% endif %}
{% endfor %}{% if anon_count > 0 %}- *and {{ anon_count }} anonymous donation{% if anon_count > 1 %}s{% endif %}*
{% endif %}
{% endif %}
{% endfor %}

*Contact us to sponsor the first-ever southwestern Vermont team at Worlds!*

## Season Sponsors (2025-2026)

We are grateful to the following organizations for their support of youth robotics in the Bennington Vermont area.

### Financial support from:

- [FIRSTinVT](https://www.firstinvermont.org/){:target="_blank"}
- [Comprehensive Computing](https://www.comprehensive-computing.com/){:target="_blank"}
- [UVM Extension Ag Engineering](https://blog.uvm.edu/cwcallah/){:target="_blank"}
- [Gene Haas Foundation](https://www.ghaasfoundation.org/){:target="_blank"}
- [Bennington Rotary Club](https://www.benningtonrotary.org/){:target="_blank"}
- [Catamount Rotary Club](https://portal.clubrunner.ca/2912){:target="_blank"}
- [Abacus Automation](https://abacusautomation.com/){:target="_blank"}

### In-kind support from:

- [Bennington Ramunto's](https://ramuntos.com/bennington-vt/){:target="_blank"}

### Space provided by:

- [Southwest Vermont Supervisory Union (SVSU)](https://www.svsu.org/){:target="_blank"}

*We are also grateful to our [event sponsors](/events/bennington-qualifier-2026#event-sponsors) of the Bennington FTC Qualifier.*

---

### Become a Sponsor

Interested in supporting youth robotics in our community? Sponsor our teams' trips to Worlds and New England. See our [budget](/budget) to understand how funds are used. Contact us at [info@bamvt.com](mailto:info@bamvt.com?subject=Robotics%20Sponsorship).

*Want to make a personal donation? Visit our [donate page](/donate).*
