---
title: Equipe
layout: splash
permalink: /members/
entries_layout: grid
# header:
#   overlay_color: "#114c24"
---
<h2>Membres</h2>
{%- for member in site.data.authors -%}
  <div class="grid__item">
    <article class="archive__item" itemscope itemtype="https://schema.org/CreativeWork">
        <div class="archive__item-teaser">
          <img src="{{ member[1].avatar | relative_url }}" alt="" style="width: 120px" center >
        </div>
      <h3 class="archive__item-title no_toc" itemprop="headline">
          {{ member[1].name }}
      </h3>
      <p class="archive__item-excerpt" itemprop="description">{{ member[1].bio | truncate: 160 }}</p>
    {% include page__meta.html type="grid" %}
    </article>
  </div>
{%- endfor -%}