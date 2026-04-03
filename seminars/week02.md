---
layout: default
title: Week 2
instructor_slides: ""
---

# Week 2

<div class="card">
  <h3>👤 Presenter</h3>
  <p>Student Name</p>
</div>

<div class="card">
  <h3>📖 Readings</h3>
  <p>Author (Year)</p>
</div>

{% if page.instructor_slides %}
<div class="card">
  <h3>🎓 Instructor Slides</h3>
  <a class="button" href="{{ page.instructor_slides }}" target="_blank">
    Open slides →
  </a>
</div>
{% endif %}

<div class="card">
  <h3>📊 Student Slides</h3>
  <p>Available via Dropbox (restricted access)</p>
</div>
