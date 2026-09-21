---
layout: default
title: Abstract submission
permalink: /symposium/abstracts/
---

<div class="page-header page-header--symposium">
  <div class="container">
    <p class="eyebrow">GEOMountain Symposium</p>
    <h1>Abstract submission</h1>
  </div>
</div>

<div class="container prose" markdown="1">
Use this page for the call for abstracts, themes, submission deadline, abstract length, oral/poster preference, review process and publication conditions.



{% if site.symposium_abstract_url and site.symposium_abstract_url != '' %}
<div class="cta-block">
  <p>Ready to share your work? Use the link below to submit your abstract.</p>
  <a class="button" href="{{ site.symposium_abstract_url }}" target="_blank" rel="noopener">Submit an abstract</a>
  {% if site.symposium_registration_url and site.symposium_registration_url != '' %}
  <a class="button button--secondary" href="{{ site.symposium_registration_url }}" target="_blank" rel="noopener">Register for the symposium</a>
  {% endif %}
</div>
{% else %}
<div class="empty-state">
  <strong>Abstract submission is not open yet.</strong>
  <p>When the form is ready, add its URL to <code>symposium_abstract_url</code> in <code>_config.yml</code>.</p>
</div>
{% endif %}
</div>
