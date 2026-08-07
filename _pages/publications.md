---
title: "Publications"
permalink: /publications/
subtitle: "Selected publications and manuscripts."
---

{% assign pubs = site.publications | sort: 'year' | reverse %}
{% if pubs.size > 0 %}
<div class="publication-list">
  {% for pub in pubs %}
  <article class="publication-item">
    <div class="publication-year">{{ pub.year }}</div>
    <div>
      <h3><a href="{{ pub.url | relative_url }}">{{ pub.title }}</a></h3>
      {% if pub.authors %}<p class="publication-authors">{{ pub.authors }}</p>{% endif %}
      {% if pub.venue %}<p class="publication-venue">{{ pub.venue }}</p>{% endif %}
      <div class="publication-links">
        {% if pub.paperurl %}<a href="{{ pub.paperurl }}">Paper</a>{% endif %}
        {% if pub.codeurl %}<a href="{{ pub.codeurl }}">Code</a>{% endif %}
        {% if pub.projecturl %}<a href="{{ pub.projecturl }}">Project</a>{% endif %}
      </div>
    </div>
  </article>
  {% endfor %}
</div>
{% else %}
<div class="empty-state">
  <h3>Publication list ready to populate</h3>
  <p>This page is connected to the <code>_publications/</code> collection. Add one Markdown file per paper and the list will be generated automatically.</p>
</div>
{% endif %}

## How to add a paper

Create a file such as <code>_publications/2026-paper-title.md</code>:

```yaml
---
title: "Paper Title"
year: 2026
authors: "Wentao Wu, ..."
venue: "Conference or Journal"
paperurl: ""
codeurl: ""
projecturl: ""
---

A short abstract, description, or project note can go here.
```
