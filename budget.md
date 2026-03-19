---
layout: default
title: Budget
description: Season budgets for Bennington Area Robotics FTC teams — Cookie Clickers (18650) and Bolts and Biscuits (32473).
---

Bennington Area Robotics runs two FTC teams on a combined regular-season cash budget of roughly $6,900, funded by local businesses, community organizations, and foundations, plus about $2,100 in in-kind support (equipment, food, and discounts). 

We are now hoping to raise an additional $23,500 for post-season advancement. Cookie Clickers won the Vermont Championship and is now advancing to "Worlds", the FIRST Championship in Houston TX from April 29-May 2. First-year team Bolts and Biscuits placed 7th overall and is advancing to the New England Premier Event from April 17-18.

Their success has created entirely new budget needs 3-4x the size of our regular season spending. Cookie Clickers alone went from a $3,100 regular season to an estimated $20,000 post-season budget. Aside from travel and lodging, post-season registration fees alone ($4,000) could easily fund a third team for next year. Event registration fees in Vermont are often waived in exchange for outreach and participation; out-of-state registration fees are not!

Thus we see that FTC Robotics in Vermont is normally quite affordable, until the teams do well enough to advance out of state, where budgets are larger, teams are more competitive, and everyone travels further to more events. Despite the cost, advancement is a good experience for the students, to see their same activity pursued at higher levels of accomplishment, and understand themselves as peers on the national and international level.

## Post-Season Advancement, 2026

### Cookie Clickers → Houston

Advancing to the [FIRST Championship](https://www.firstchampionship.org/){:target="_blank"} in Houston, TX, as the first team from southwestern Vermont to reach Worlds. Sending 6 students and 3-4 mentors.

{% assign cc_total = 0 %}{% assign cc_individual = 0 %}{% assign cc_firstinvt = 0 %}
{% for d in site.data.donations.donations %}
  {% if d.recipient == "Cookie Clickers" %}
    {% assign cc_total = cc_total | plus: d.amount %}
    {% if d.donor == "FIRSTinVT" %}{% assign cc_firstinvt = cc_firstinvt | plus: d.amount %}
    {% else %}{% assign cc_individual = cc_individual | plus: d.amount %}{% endif %}
  {% endif %}
{% endfor %}
<table>
<thead><tr><th>Income</th><th style="text-align:right">Amount</th></tr></thead>
<tbody>
{% if cc_firstinvt > 0 %}<tr><td>FIRSTinVT</td><td style="text-align:right">${{ cc_firstinvt | replace: '.0', '' }}</td></tr>{% endif %}
{% if cc_individual > 0 %}<tr><td>Individual donations</td><td style="text-align:right">${{ cc_individual | replace: '.0', '' }}</td></tr>{% endif %}
<tr><td><strong>Total Income</strong></td><td style="text-align:right"><strong>${{ cc_total | replace: '.0', '' }}</strong></td></tr>
</tbody>
</table>

| Expense | Estimated Cost |
|----------|---------------:|
| Event Registration | $2,500.00 |
| Flights | TBD |
| Lodging | TBD |
| Meals | TBD |
| Robot improvements | $1,500.00 |
| Travel equipment (robot & tool cases) | $800.00 |
| **Estimated Total** | **~$20,000** |

### Bolts and Biscuits → New England

Advancing to the [New England Premier Event](https://www.nefirst.org/ftc-premier){:target="_blank"} at the Big E in West Springfield, MA. Sending 5 students and 2 mentors.

{% assign bb_total = 0 %}{% assign bb_individual = 0 %}{% assign bb_firstinvt = 0 %}
{% for d in site.data.donations.donations %}
  {% if d.recipient == "Bolts and Biscuits" %}
    {% assign bb_total = bb_total | plus: d.amount %}
    {% if d.donor == "FIRSTinVT" %}{% assign bb_firstinvt = bb_firstinvt | plus: d.amount %}
    {% else %}{% assign bb_individual = bb_individual | plus: d.amount %}{% endif %}
  {% endif %}
{% endfor %}
<table>
<thead><tr><th>Income Source</th><th style="text-align:right">Amount</th></tr></thead>
<tbody>
{% if bb_firstinvt > 0 %}<tr><td>FIRSTinVT</td><td style="text-align:right">${{ bb_firstinvt | replace: '.0', '' }}</td></tr>{% endif %}
{% if bb_individual > 0 %}<tr><td>Individual donations</td><td style="text-align:right">${{ bb_individual | replace: '.0', '' }}</td></tr>{% endif %}
<tr><td><strong>Total Income</strong></td><td style="text-align:right"><strong>${{ bb_total | replace: '.0', '' }}</strong></td></tr>
</tbody>
</table>

| Expense | Estimated Cost |
|----------|---------------:|
| Event Registration | $1,500.00 |
| Lodging | TBD |
| Meals | TBD |
| Robot improvements | $1,000.00 |
| **Estimated Total** | **~$3,500** |

### Shared (Post-Season)

{% assign sh_total = 0 %}{% assign sh_individual = 0 %}{% assign sh_firstinvt = 0 %}
{% for d in site.data.donations.donations %}
  {% if d.recipient == "Robotics General Fund" %}
    {% assign sh_total = sh_total | plus: d.amount %}
    {% if d.donor == "FIRSTinVT" %}{% assign sh_firstinvt = sh_firstinvt | plus: d.amount %}
    {% else %}{% assign sh_individual = sh_individual | plus: d.amount %}{% endif %}
  {% endif %}
{% endfor %}
<table>
<thead><tr><th>Income Source</th><th style="text-align:right">Amount</th></tr></thead>
<tbody>
{% if sh_firstinvt > 0 %}<tr><td>FIRSTinVT</td><td style="text-align:right">${{ sh_firstinvt | replace: '.0', '' }}</td></tr>{% endif %}
{% if sh_individual > 0 %}<tr><td>Individual donations</td><td style="text-align:right">${{ sh_individual | replace: '.0', '' }}</td></tr>{% endif %}
<tr><td><strong>Total Income</strong></td><td style="text-align:right"><strong>${{ sh_total | replace: '.0', '' }}</strong></td></tr>
</tbody>
</table>

<p style="text-align:center; margin-top:2rem;">
  <a href="/donate" class="btn-donate">Support Our Teams</a>
</p>

## Regular Season, 2025-26

### Cookie Clickers (18650)

Estimated robot replacement cost: $3,100

| Income | Amount |
|--------|-------:|
| Community organizations | $350.00 |
| Local businesses | $1,700.00 |
| National foundations | $200.00 |
| **Total Income** | **$2,250.00** |

| Expense | Amount |
|----------|-------:|
| Season Registration | $325.00 |
| Building Supplies | $316.60 |
| Cameras | $398.12 |
| Major Parts | $1,327.20 |
| Uniforms | $700.81 |
| **Total Expenses** | **$3,067.73** |
| **Net** | <strong style="color:var(--accent)">-$817.73</strong> |

### Bolts and Biscuits (32473)

| Income | Amount |
|--------|-------:|
| FIRSTinVT | $2,000.00 |
| UVM Ext Ag Eng | $2,107.31 |
| **Total Income** | **$4,107.31** |

| Expense | Amount |
|----------|-------:|
| Season Registration | $325.00 |
| Building Supplies | $470.73 |
| Controls | $895.00 |
| StarterBot | $777.31 |
| Uniforms | $550.43 |
| **Total Expenses** | **$3,018.47** |
| **Net** | <strong style="color:#2a9d8f">+$1,088.84</strong> |


### Shared (Bennington Area Robotics)

| Cash Income | Amount |
|--------|-------:|
| Community organizations | $500.00 |
| **Total Cash Income** | **$500.00** |

| Expense | Amount |
|----------|-------:|
| 3D Printing | $360.37 |
| DECODE game pieces | $72.47 |
| **Total Expenses** | **$432.84** |
| **Net** | <strong style="color:#2a9d8f">+$67.16</strong> |

| In-Kind Support | Value |
|--------|-------:|
| Family donations (food) | $1,300.00 |
| FIRSTinVT (field set) | $300.00 |
| Local businesses (food, computers) | $542.24 |
| **Total In-Kind** | **$2,142.24** |
