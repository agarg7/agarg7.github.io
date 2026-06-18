<h2 id="publications" style="margin: 2px 0px -15px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for pub in site.data.publications.main %}

<li>
<div class="pub-row" style="display: flex; align-items: stretch; gap: 20px;">
  <div class="abbr" style="flex: 0 0 auto; position: relative; display: flex; align-items: flex-start;">
    {% if pub.image %} 
      <img src="{{ pub.image }}"
           class="teaser img-fluid z-depth-1"
           style="height: 100%; width: auto; max-height: 100%; object-fit: contain;">


  {% if pub.conference_short %} 
    <abbr class="badge"
          style="position: absolute; left: 6px; top: 6px; z-index: 2;">
      {{ pub.conference_short }}
    </abbr>
  {% endif %}
{% endif %}


  </div>

  <div class="pub-info" style="flex: 1; min-width: 0;">
    <div class="title">
      {% if pub.pdf %}
        <a href="{{ pub.pdf }}">{{ pub.title }}</a>
      {% else %}
        {{ pub.title }}
      {% endif %}
    </div>

<div class="author">{{ pub.authors }}</div>

<div class="periodical">
  <em>{{ pub.conference }}</em>
</div>

<div class="links">
  {% for item in pub.links %}
    {% if item.url %}
      <a href="{{ item.url }}"
         class="btn btn-sm z-depth-0"
         role="button"
         target="_blank"
         style="font-size:12px; margin-right:6px; margin-bottom:4px;">
        {{ item.label }}
      </a>
    {% endif %}
  {% endfor %}

  {% if pub.notes %} 
    <strong><i style="color:#e74d3c">{{ pub.notes }}</i></strong>
  {% endif %}

  {% if pub.others %} 
    {{ pub.others }}
  {% endif %}
</div>

  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
