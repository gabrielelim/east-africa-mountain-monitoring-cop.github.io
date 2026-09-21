---
layout: default
title: Symposium registration
permalink: /symposium/registration/
---

<div class="page-header page-header--symposium">
  <div class="container">
    <p class="eyebrow">GEOMountain Symposium</p>
    <h1>Registration</h1>
  </div>
</div>

<div class="container prose" markdown="1">

### Registration overview

Welcome! Use this page to register for the upcoming **GEOMountain Symposium**.

**Eligibility:**  
Open to academics, field researchers, policy stakeholders, local practitioners and students working on East African mountain environments.

**Registration:**  
<!-- Standard Delegate **$1050 USD** | Student Rate **$275 USD** *(Institutional ID required)*. -->

**Financial support:**  
A limited number of travel grants and registration fee waivers may be available.

**Important deadlines:**

- **Early Bird Registration Closes:** December 1, 2026
- **Final Registration Deadline:** January 20, 2027

**Data protection:**  
All submitted details will be handled securely and used only for purposes related to symposium registration, organization and communication.

## Complete the registration form

{% if site.symposium_registration_url and site.symposium_registration_url != '' %}
<div class="cta-block">
  <p>Ready to join us? Use the link below to complete your symposium registration.</p>
  <a class="button" href="{{ site.symposium_registration_url }}" target="_blank" rel="noopener">Open registration form</a>
  {% if site.symposium_abstract_url and site.symposium_abstract_url != '' %}
  <a class="button button--secondary" href="{{ site.symposium_abstract_url }}" target="_blank" rel="noopener">Submit an abstract</a>
  {% endif %}
</div>
{% else %}
<div class="empty-state">
  <strong>Registration is not open yet.</strong>
  <p>When the form is ready, add its URL to <code>symposium_registration_url</code> in <code>_config.yml</code>.</p>
</div>
{% endif %}

<p>If you also wish to submit an abstract, please use the <a href="{{ '/symposium/abstracts/' | relative_url }}">abstract submission page</a>.</p>

</div>
