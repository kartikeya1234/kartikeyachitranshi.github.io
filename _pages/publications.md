<style>
.bibtex.noshow {
  display: none;
}
.bibtex {
  margin-top: 10px;
  padding: 10px;
  background-color: #f5f5f5;
  border-radius: 4px;
}
</style>

<script>
function toggleBibtex(label) {
  var elem = document.getElementById('bib_' + label);
  if (elem.style.display === 'block') {
    elem.style.display = 'none';
  } else {
    elem.style.display = 'block';
  }
}
</script>

---
title: "Publications"
permalink: /publications/
layout: single
author_profile: true
---
You can also find my publications on [Google Scholar](https://scholar.google.com/citations?user=Cb6W6tgAAAAJ&hl=en).

<h4 style="margin-bottom:0px;padding-top:10px;">Preprints</h4>
<ul class="preprint_list">

{% assign number_printed = 0 %}
{% for publi in site.data.publication_list %}
{% if publi.type == "preprint" %}

<li ><p>
<b>{{ publi.title }}</b> ({{ publi.year }})
<br>{{ publi.authors }}<br>
<a href="javascript:toggleBibtex('{{ publi.label }}')">[BibTeX]</a>
<a href="{{ publi.link_pre.url }}" target="_blank">[PDF]</a> 
</p>
<div id="bib_{{ publi.label }}" class="bibtex noshow">
<pre>
{{ publi.bibtex }}
</pre>
</div>
</li>

{% endif %}
{% endfor %}

</ul>

