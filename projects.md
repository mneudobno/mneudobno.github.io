---
layout: page
title: Projects
subtitle: A collection of my work and side projects
permalink: /projects/
redirect_from:
  - /portfolio/
  - /work/
---

Here are some projects I've worked on. Each one taught me something new and helped me grow as a developer. :rocket:

<div class="projects-grid projects-page-grid">
{% for project in site.projects %}
{% include project-card.html project=project %}
{% endfor %}
</div>

---

## :bulb: Want to collaborate?

I'm always interested in working on interesting projects. If you have an idea or need help with development, let's talk!

<div class="projects-cta">
  <a href="{{ '/contact/' | relative_url }}" class="btn btn-primary">Start a Conversation</a>
</div>
