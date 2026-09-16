<h2 id="publications">Selected Publications <span class="pub-scholar-note">(for the complete list, see my <a href="{{ site.google_scholar }}" target="_blank">Google Scholar profile</a>)</span></h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-entry{% if link.badge_image %} has-badge{% endif %}">
    <div class="pub-text">
    <div class="title">{{ link.title }}{% if link.pdf %} <a href="{{ link.pdf }}" class="paper-link" target="_blank">[Paper]</a>{% endif %}</div>
    <div class="author">{{ link.authors }}{% if link.author_note %} <span class="author-note">{{ link.author_note }}</span>{% endif %}</div>
    <div class="periodical"><span class="venue-name">{{ link.venue }}</span><span class="venue-year">, {{ link.year }}{% if link.notes %} ({{ link.notes }}){% endif %}.</span>{% if link.accept_stat %} <span class="accept-stat">{{ link.accept_stat }}</span>{% endif %}</div>
    {% if link.badges %}
    <div class="ae-badges">
      {% for badge in link.badges %}
      <span class="ae-badge">{{ badge }}</span>
      {% endfor %}
    </div>
    {% endif %}
    </div>
    {% if link.badge_image %}<img src="{{ link.badge_image }}" alt="{{ link.badge_image_alt | default: 'award badge' }}" class="ae-badge-image" />{% endif %}
</div>
</li>

{% endfor %}

</ol>
</div>
