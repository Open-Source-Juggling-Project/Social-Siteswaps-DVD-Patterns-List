---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

# Social Siteswaps DVD Patterns List

A companion site for those who own the Social Siteswaps DVD from Gandini Juggling.

Don't own it?

[Buy Social Siteswaps DVD](http://www.gandinipress.com/product/social-siteswaps-dvd-ntscall/)

<table class="table-center">
  <thead>
  <tr>
    <th>Pattern</th>
    <th>Period</th>
    <th>Jugglers</th>
    <th>Objects</th>
    <th>Passes</th>
  </tr>
  </thead>
  <tbody>
  {% for pattern in site.data.patterns %}
    {% if pattern.Section %}
  <tr>
    <td colspan="5" class="dvd-section">{{ pattern.Section }}</td>
  </tr>
    {% else %}
  {% if pattern.Link %}
  <tr>
    <td colspan="5">
        <div class="prechac-pattern">{{ pattern.Pattern }}</div>
        <div class="prechac-this-link"><a href="{{ pattern.Link }}">Link to Prechach This</a></div>
    </td>
  </tr>  
  {% else %}
  <tr>
    <td colspan="5">
        <div class="prechac-pattern-solo">{{ pattern.Pattern }}</div>
    </td>
  </tr> 
  {% endif %}
  <tr>
    <td></td>
    <td class="pattern-details pattern-period">{{ pattern.Period }}</td>
    <td class="pattern-details pattern-jugglers">{{ pattern.Jugglers }}</td>
    <td class="pattern-details pattern-objects">{{ pattern.Objects }}</td>
    <td class="pattern-details pattern-passes">{{ pattern.Passes }}</td>
  </tr>
      {% endif %}
{% endfor %}
</tbody>
<tfoot>
<tr>
    <th>Pattern</th>
    <th>Period</th>
    <th>Jugglers</th>
    <th>Objects</th>
    <th>Passes</th>
  </tr>
  </tfoot>
</table>