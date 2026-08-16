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

<div class="instructor-grid">

  <div class="instructor-card">
    <h3 class="instructor-card-title">Aditri Gadigi</h3>
    <p class="instructor-card-role">Course Facilitator</p>
    <p class="instructor-card-email"><a href="mailto:agadigi@terpmail.umd.edu">agadigi@terpmail.umd.edu</a></p>
  </div>

  <div class="instructor-card">
    <h3 class="instructor-card-title">Anushka Poddar</h3>
    <p class="instructor-card-role">Course Facilitator</p>
    <p class="instructor-card-email"><a href="mailto:apoddar2@terpmail.umd.edu">apoddar2@terpmail.umd.edu</a></p>
  </div>

  <div class="instructor-card">
    <h3 class="instructor-card-title">Dr. Najib M. El-Sayed</h3>
    <p class="instructor-card-role">Faculty Advisor</p>
    <p class="instructor-card-email"><a href="mailto:elsayed@umd.edu">elsayed@umd.edu</a></p>
  </div>

</div>

</section>

---

<section id="projects" markdown="1">

## Student Projects

View final projects made by past students!

<!-- Semester Filter Toggle Buttons (Active Gold by Default) -->
<div class="semester-filter-controls">
  <button type="button" class="sem-toggle-btn active-sem" data-sem="fall-2025">
    Fall 2025
  </button>
  <button type="button" class="sem-toggle-btn active-sem" data-sem="spring-2026">
    Spring 2026
  </button>
</div>

<!-- Project Cards Grid -->
<div class="projects-grid">
  {% for project in site.data.projects %}
  <div class="animated-project-card" data-semester="{{ project.semester }}">
    
    <div>
      <div class="project-card-title">
        {{ project.title }}
      </div>
      <p class="project-card-desc">
        {{ project.description }}
      </p>
    </div>

    <div>
      {% if project.type == "paper" %}
        <a href="{{ project.link }}" target="_blank" rel="noopener noreferrer" class="btn-card-action btn-card-paper">
          View Paper &rarr;
        </a>
      {% else %}
        <a href="{{ project.link }}" target="_blank" rel="noopener noreferrer" class="btn-card-action btn-card-project">
          View Project &rarr;
        </a>
      {% endif %}
    </div>

  </div>
  {% endfor %}
</div>

</section>

<script>
  (function() {
    function setupSemesterFilter() {
      const buttons = document.querySelectorAll('.sem-toggle-btn');
      const cards = document.querySelectorAll('.animated-project-card');
      const activeSemesters = new Set(['fall-2025', 'spring-2026']);

      function updateVisibility() {
        cards.forEach(card => {
          const cardSem = card.getAttribute('data-semester');
          if (activeSemesters.has(cardSem)) {
            card.style.setProperty('display', 'flex', 'important');
          } else {
            card.style.setProperty('display', 'none', 'important');
          }
        });
      }

      buttons.forEach(btn => {
        btn.addEventListener('click', function(e) {
          e.preventDefault();
          const sem = this.getAttribute('data-sem');

          if (activeSemesters.has(sem)) {
            activeSemesters.delete(sem);
            this.classList.remove('active-sem');
          } else {
            activeSemesters.add(sem);
            this.classList.add('active-sem');
          }
          updateVisibility();
        });
      });

      updateVisibility();
    }

    if (document.readyState === 'loading') {
      document.addEventListener('DOMContentLoaded', setupSemesterFilter);
    } else {
      setupSemesterFilter();
    }
  })();
</script>