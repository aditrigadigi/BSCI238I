---
layout: home
title: BSCI238I | Machine Learning for the Life Sciences
nav_exclude: true
permalink: /:path/
seo:
  type: Course
  name: BSCI238I
---

<section id="home" markdown="1">

![Course Banner](/assets/images/banner.jpg){: style="width: 100%; display: block;" }

# BSCI238I: Machine Learning for the Life Sciences

Machine learning is transforming the life sciences, enabling breakthroughs in fields such as genomics, medical imaging, and drug discovery. This course introduces students to the fundamental principles of machine learning and its applications in biology and medicine. Students will learn about key machine learning techniques, including classification, regression, clustering, and deep learning, with a focus on practical applications like cancer diagnosis, gene expression analysis, and protein structure prediction. Through lectures and guided projects, students will gain an understanding of how to apply machine learning models to biological datasets, evaluate their performance, and interpret results. No prior programming or machine learning experience is required—this course is designed to bridge the gap between computational techniques and life science research, preparing biology students to understand and leverage machine learning as a tool as they encounter real-world challenges in their fields of study.

<span style="color: #543290;"><strong>Th 3:30-4:20 @ ESJ B0322</strong></span>
</section>

---

<section id="syllabus" markdown="1">

## Syllabus

{% for module in site.modules %}
{{ module }}
{% endfor %}
 <br> 

### Office Hours
* TBD

 <br> 

[View the Full Syllabus (PDF)](https://docs.google.com/document/d/16saZJkMiUvnaw4p9VcXmwhjTT6Aip9h54B6hkIj-rv4/edit?usp=sharing){: .btn .btn-blueprint }

</section>

---

<section id="instructors" markdown="1">

## Instructors

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 2rem; margin-top: 2rem;">

  <div style="border: 1px solid #d0d0d0; border-radius: 8px; padding: 1.5rem; text-align: center; background-color: #fafafa;">
    <h3 style="margin: 0.5rem 0;">Aditri Gadigi</h3>
    <p style="color: #666; margin: 0.25rem 0; font-size: 0.95rem;"><strong>Course Facilitator</strong></p>
    <p style="margin: 0.5rem 0;"><a href="mailto:agadigi@terpmail.umd.edu">agadigi@terpmail.umd.edu</a></p>
  </div>

  <div style="border: 1px solid #d0d0d0; border-radius: 8px; padding: 1.5rem; text-align: center; background-color: #fafafa;">
    <h3 style="margin: 0.5rem 0;">Anushka Poddar</h3>
    <p style="color: #666; margin: 0.25rem 0; font-size: 0.95rem;"><strong>Course Facilitator</strong></p>
    <p style="margin: 0.5rem 0;"><a href="mailto:apoddar2@terpmail.umd.edu">apoddar2@terpmail.umd.edu</a></p>
  </div>

  <div style="border: 1px solid #d0d0d0; border-radius: 8px; padding: 1.5rem; text-align: center; background-color: #fafafa;">
    <h3 style="margin: 0.5rem 0;">Dr. Najib M. El-Sayed</h3>
    <p style="color: #666; margin: 0.25rem 0; font-size: 0.95rem;"><strong>Faculty Advisor</strong></p>
    <p style="margin: 0.5rem 0;"><a href="mailto:elsayed@umd.edu">elsayed@umd.edu</a></p>
  </div>

</div>

</section>

---

<section id="projects" markdown="1">

## Student Projects

View final projects made by past students!

<style>
  .animated-project-card {
    cursor: pointer;
    border: 1px solid #e0e0e0;
    border-radius: 12px;
    overflow: hidden;
    background: white;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
    transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
    height: 100%;
  }

  .animated-project-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 24px rgba(0, 0, 0, 0.12);
  }

  .project-card-button {
    display: inline-block;
    padding: 0.5rem 1rem;
    font-size: 0.9rem;
    cursor: pointer;
  }
</style>

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; margin-top: 2rem;">
{% for project in site.data.projects %}
  <div class="animated-project-card" style="display: flex; flex-direction: column; justify-content: space-between; padding: 1.5rem;" onclick="window.open('{{ project.link | relative_url }}', '_blank')">
    <div>
      <div style="font-family: inherit !important; font-size: 1.00rem !important; font-weight: 600 !important; line-height: 1.3 !important; color: #2f2f2f !important; margin: 0 0 0.6rem 0 !important; text-transform: none !important; letter-spacing: normal !important;">
        {{ project.title }}
      </div>
      
      {% if project.authors != "" and project.authors != nil %}
      <div style="margin: 0 0 0.15rem 0; color: #333; font-size: 0.95rem; font-weight: 400;">{{ project.authors }}</div>
      {% endif %}

      <p style="margin: 0 0 1.25rem 0; color: #666; font-size: 0.9rem;">{{ project.description }}</p>
    </div>

    <div style="margin-top: auto;">
      <button class="btn btn-outline project-card-button" type="button" onclick="event.stopPropagation(); window.open('{{ project.link | relative_url }}', '_blank')">View Project →</button>
    </div>
  </div>
{% endfor %}
</div>

</section>