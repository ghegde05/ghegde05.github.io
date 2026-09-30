## research interests

<div class="theme-grid">
{% for theme in site.data.research_themes %}
  <div class="theme-card">
    <h3>{% if theme.icon %}<i class="{{ theme.icon }}" aria-hidden="true"></i> {% endif %}{{ theme.title }}</h3>
    <p>{{ theme.summary }}</p>
    {% if theme.links %}
    <ul>
      {% for link in theme.links %}
      {% assign first_char = link.url | slice: 0 %}
      <li><a href="{{ link.url }}"{% if first_char != '#' %} target="_blank" rel="noopener"{% endif %}>{{ link.label }}</a></li>
      {% endfor %}
    </ul>
    {% endif %}
  </div>
{% endfor %}
</div>
