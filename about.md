---
layout: page
title: About Me
subtitle: My journey, experience, and what drives me
permalink: /about/
---

## Hello!

I'm Anna Bushueva, a passionate junior full-stack developer based in Berlin, Germany. I recently graduated from the Technical University of Berlin with a degree in Computer Science, and I'm excited to build my career in software development.

I love turning ideas into reality through code. Whether it's crafting intuitive user interfaces or designing robust backend systems, I find joy in solving problems and creating software that makes a difference.

When I'm not coding, you'll find me exploring Berlin's tech meetups, contributing to open-source projects, or learning about the latest web technologies.

---

## Work Experience

<div class="timeline">
{% for job in site.data.experience %}
<div class="timeline-item">
  <div class="timeline-marker"></div>
  <div class="timeline-content">
    <div class="timeline-header">
      <h3>{{ job.title }}</h3>
      <span class="timeline-period">{{ job.period }}</span>
    </div>
    <p class="timeline-company">{{ job.company }} &middot; {{ job.location }}</p>
    <p class="timeline-description">{{ job.description }}</p>
    <ul class="timeline-highlights">
      {% for highlight in job.highlights %}
      <li>{{ highlight }}</li>
      {% endfor %}
    </ul>
  </div>
</div>
{% endfor %}
</div>

---

## Education

<div class="education-list">
{% for edu in site.data.education.degrees %}
<div class="education-item">
  <div class="education-header">
    <h3>{{ edu.degree }}</h3>
    <span class="education-period">{{ edu.period }}</span>
  </div>
  <p class="education-institution">{{ edu.institution }} &middot; {{ edu.location }}</p>
  <p class="education-description">{{ edu.description }}</p>
  <ul class="education-highlights">
    {% for highlight in edu.highlights %}
    <li>{{ highlight }}</li>
    {% endfor %}
  </ul>
</div>
{% endfor %}
</div>

---

## Certifications

<div class="certifications-grid">
{% for cert in site.data.education.certifications %}
<div class="certification-item">
  <span class="certification-name">{{ cert.name }}</span>
  <span class="certification-meta">{{ cert.issuer }} &middot; {{ cert.date }}</span>
</div>
{% endfor %}
</div>

---

## Technical Skills

<div class="skills-detailed">
{% for category in site.data.skills %}
{% unless category[0] == 'soft_skills' %}
<div class="skill-category-detailed">
  <h3>{{ category[1].title }}</h3>
  <div class="skill-tags">
    {% for skill in category[1].items %}
    <span class="skill-tag-detailed">{{ skill.name }}</span>
    {% endfor %}
  </div>
</div>
{% endunless %}
{% endfor %}

<div class="skill-category-detailed">
  <h3>{{ site.data.skills.soft_skills.title }}</h3>
  <div class="skill-tags">
    {% for skill in site.data.skills.soft_skills.items %}
    <span class="skill-tag-detailed soft">{{ skill }}</span>
    {% endfor %}
  </div>
</div>
</div>

---

## Let's Connect

I'm always open to discussing new opportunities, interesting projects, or just having a chat about technology. Feel free to reach out!

<div class="about-cta">
  <a href="{{ '/contact/' | relative_url }}" class="btn btn-primary">Get in Touch</a>
  <a href="https://github.com/{{ site.author.github }}" target="_blank" rel="noopener" class="btn btn-outline">View GitHub</a>
</div>
