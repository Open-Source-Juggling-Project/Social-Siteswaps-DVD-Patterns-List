---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

# Social Siteswaps DVD Patterns List

Testing _data files: https://jekyllrb.com/docs/datafiles/


## Attempting: Patterns.csv

### Using a Table

<table>
  <tr>
    <tr>
    <th>Section</th>
    <th>Pattern</th>
    <th>Sum</th>
    <th>Period</th>
    <th>Average</th>
    <th>Jugglers</th>
    <th>Objects</th>
    <th>Passes</th>
    <th>Link</th>
  </tr>
  </tr>
  {% for pattern in site.data.patterns %}
    {% if pattern.Section %}
  <tr>
    <td colspan="9" class="dvd-section">{{ pattern.Section }}</td>
  </tr>
    {% else %}
    <tr>
    <td></td>
    <td colspan="8" class="prechac-pattern">{{ pattern.Pattern }}</td>
    </tr>
  <tr>
    <td colspan="2" ></td>
    <td class="pattern-details pattern-sum">{{ pattern.Sum }}</td>
    <td class="pattern-details pattern-period">{{ pattern.Period }}</td>
    <td class="pattern-details pattern-average">{{ pattern.Average }}</td>
    <td class="pattern-details pattern-jugglers">{{ pattern.Jugglers }}</td>
    <td class="pattern-details pattern-objects">{{ pattern.Objects }}</td>
    <td class="pattern-details pattern-passes">{{ pattern.Passes }}</td>
    <td class="pattern-details pattern-link">{{ pattern.Link }}</td>
  </tr>
      {% endif %}
{% endfor %}
<tr>
    <th>Section</th>
    <th>Pattern</th>
    <th>Sum</th>
    <th>Period</th>
    <th>Average</th>
    <th>Jugglers</th>
    <th>Objects</th>
    <th>Passes</th>
    <th>Link</th>
  </tr>
</table>


### Using a List

Section,Pattern,Sum,Period,Average,Jugglers,Objects,Passes,Link

<ul>
{% for pattern in site.data.patterns %}
    {% if pattern.Section %}
        <li>
            {{ pattern.Section }}
        </li>
    {% else %}
        <li>
            {{ pattern.Pattern }} <br />
            {{ pattern.Sum }} <br />
            {{ pattern.Period }} <br />
            {{ pattern.Average }} <br />
            {{ pattern.Jugglers }} <br />
            {{ pattern.Objects }} <br />
            {{ pattern.Passes }} <br />
            {{ pattern.Link }}
        </li>
    {% endif %}
{% endfor %}
</ul>