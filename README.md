# image-slider
<!-- Jekyll Ideal Image Slider Include -->
<!-- https://github.com/jekylltools/jekyll-ideal-image-slider-include -->
<!-- v1.8 -->
{%- if include.selector != empty -%}
  {%- assign slider = site.data.sliders | where:"selector",include.selector | first -%}
  <div id="{{ slider.selector }}">
  {% for image in slider.images -%}
    {% if image.href -%}<a href="{{ image.href }}">{%- endif -%}<img data-src="{{ image.data-src | relative_url }}" data-src-2x="{{ image.data-src-2x | relative_url }}" src="{{ image.src | relative_url }}" title="{{ image.title }}" alt="{{ image.alt }}">{%- if image.href -%}</a>{% endif %}
  {% endfor -%}
  </div>
{%- endif -%}
