---
layout: home
title: BSCI 238I | Machine Learning for the Life Sciences
nav_exclude: true
permalink: /:path/
seo:
  type: Course
  name: BSCI 238I
---

<!-- ============================================
     1. HOME SECTION - TOP IMAGE BANNER & HEADER
     ============================================ -->
<section id="home" markdown="1">

![Course Banner](/assets/images/banner.jpg){: style="width: 100%; display: block;" }

# BSCI 238I: Machine Learning for the Life Sciences

Welcome to BSCI 238I! This course provides an introduction to machine learning fundamentals with applications in the life sciences. You will learn essential ML concepts, from supervised and unsupervised learning to neural networks, and apply them to real-world biological datasets. By the end of the course, you'll be able to implement machine learning solutions for genomics, protein structure prediction, drug discovery, and other biomedical applications.

</section>

---

<!-- ============================================
     2. SCHEDULE SECTION - COURSE CALENDAR
     ============================================ -->
<section id="schedule" markdown="1">

## Course Calendar

{% for module in site.modules %}
{{ module }}
{% endfor %}

</section>

---

<!-- ============================================
     3. SYLLABUS SECTION
     ============================================ -->
<section id="syllabus" markdown="1">

## Course Syllabus

### Course Overview
BSCI 238I combines practical machine learning skills with biological applications. Students will work with real-world datasets from genomics, proteomics, and biomedical research to gain hands-on experience implementing and evaluating machine learning models.

### Learning Objectives
- Understand fundamental machine learning algorithms (regression, classification, clustering)
- Preprocess and explore biological datasets
- Build and evaluate predictive models
- Apply deep learning to biomedical data
- Interpret and communicate machine learning results in a biological context

### Course Format
- **Lectures**: Interactive sessions covering ML theory and life sciences applications
- **Lab Sessions**: Hands-on coding in Python with scikit-learn, TensorFlow, and PyTorch
- **Projects**: Real-world capstone projects using actual biological datasets
- **Office Hours**: Weekly instructor availability for questions and project guidance

### Grading
- Homework Assignments: 30%
- Lab Participation: 15%
- Midterm Project: 20%
- Final Capstone Project: 35%

[Download Full Syllabus (PDF)](#){: .btn .btn-purple }

</section>

---

<!-- ============================================
     4. INSTRUCTORS SECTION - STAFF GRID
     ============================================ -->
<section id="instructors" markdown="1">

## Course Instructors & Staff

Meet the instructors and teaching assistants leading this course:

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 2rem; margin-top: 2rem;">
{% for staffer in site.staffers %}
  <div style="border: 1px solid #d0d0d0; border-radius: 8px; padding: 1.5rem; text-align: center; background-color: #fafafa;">
    {% if staffer.photo %}
    <img src="{{ site.baseurl }}/assets/images/{{ staffer.photo }}" alt="{{ staffer.name }}" style="width: 150px; height: 150px; border-radius: 50%; object-fit: cover; margin-bottom: 1rem;">
    {% endif %}
    <h3 style="margin: 0.5rem 0;">{{ staffer.name }}</h3>
    <p style="color: #666; margin: 0.25rem 0; font-size: 0.95rem;"><strong>{{ staffer.role }}</strong></p>
    {% if staffer.email %}
    <p style="margin: 0.5rem 0;"><a href="mailto:{{ staffer.email }}">{{ staffer.email }}</a></p>
    {% endif %}
    {% if staffer.website %}
    <p style="margin: 0.5rem 0;"><a href="{{ staffer.website }}" class="btn btn-outline" style="display: inline-block; padding: 0.25rem 0.75rem; font-size: 0.85rem;">Visit Website</a></p>
    {% endif %}
    {% if staffer.meta %}
    <div style="text-align: left; margin-top: 1rem; font-size: 0.9rem;">
      {% for meta_item in staffer.meta %}
        <p style="margin: 0.25rem 0;"><strong>{{ meta_item[0]}}:</strong> {{ meta_item[1] }}</p>
      {% endfor %}
    </div>
    {% endif %}
  </div>
{% endfor %}
</div>

</section>

---

<!-- ============================================
     5. STUDENT PROJECTS GALLERY
     ============================================ -->
<section id="projects" markdown="1">

## Student Projects Gallery

Below are featured projects from students in this course. These projects showcase real-world applications of machine learning in the life sciences:

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; margin-top: 2rem;">

<!-- Project Card 1 -->
<div style="border: 1px solid #e0e0e0; border-radius: 8px; overflow: hidden; background: white; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
  <img src="/assets/images/placeholder-project-1.jpg" alt="Project 1" style="width: 100%; height: 200px; object-fit: cover; background-color: #e8e8e8;">
  <div style="padding: 1.5rem;">
    <h4 style="margin: 0 0 0.5rem 0;"><strong>Protein Structure Prediction</strong></h4>
    <p style="margin: 0 0 1rem 0; color: #555; font-size: 0.95rem;">Developed a deep learning model to predict secondary protein structures from amino acid sequences. Achieved 89% accuracy on test dataset using CNN architecture.</p>
    <a href="#" class="btn btn-outline" style="display: inline-block; padding: 0.4rem 1rem; font-size: 0.9rem;">View Project →</a>
  </div>
</div>

<!-- Project Card 2 -->
<div style="border: 1px solid #e0e0e0; border-radius: 8px; overflow: hidden; background: white; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
  <img src="/assets/images/placeholder-project-2.jpg" alt="Project 2" style="width: 100%; height: 200px; object-fit: cover; background-color: #e8e8e8;">
  <div style="padding: 1.5rem;">
    <h4 style="margin: 0 0 0.5rem 0;"><strong>Gene Expression Classification</strong></h4>
    <p style="margin: 0 0 1rem 0; color: #555; font-size: 0.95rem;">Built a random forest classifier to identify disease subtypes from gene expression data. Performed feature selection on 20,000+ genes to improve model interpretability.</p>
    <a href="#" class="btn btn-outline" style="display: inline-block; padding: 0.4rem 1rem; font-size: 0.9rem;">View Project →</a>
  </div>
</div>

<!-- Project Card 3 -->
<div style="border: 1px solid #e0e0e0; border-radius: 8px; overflow: hidden; background: white; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
  <img src="/assets/images/placeholder-project-3.jpg" alt="Project 3" style="width: 100%; height: 200px; object-fit: cover; background-color: #e8e8e8;">
  <div style="padding: 1.5rem;">
    <h4 style="margin: 0 0 0.5rem 0;"><strong>Drug Discovery Pipeline</strong></h4>
    <p style="margin: 0 0 1rem 0; color: #555; font-size: 0.95rem;">Created an automated ML pipeline for predicting drug-protein binding affinities. Implemented hyperparameter tuning and cross-validation to optimize model performance.</p>
    <a href="#" class="btn btn-outline" style="display: inline-block; padding: 0.4rem 1rem; font-size: 0.9rem;">View Project →</a>
  </div>
</div>

<!-- Project Card 4 -->
<div style="border: 1px solid #e0e0e0; border-radius: 8px; overflow: hidden; background: white; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
  <img src="/assets/images/placeholder-project-4.jpg" alt="Project 4" style="width: 100%; height: 200px; object-fit: cover; background-color: #e8e8e8;">
  <div style="padding: 1.5rem;">
    <h4 style="margin: 0 0 0.5rem 0;"><strong>Metagenomic Binning</strong></h4>
    <p style="margin: 0 0 1rem 0; color: #555; font-size: 0.95rem;">Clustered microbial DNA sequences into species using unsupervised learning. Compared k-means, hierarchical clustering, and DBSCAN for optimal taxonomic resolution.</p>
    <a href="#" class="btn btn-outline" style="display: inline-block; padding: 0.4rem 1rem; font-size: 0.9rem;">View Project →</a>
  </div>
</div>

<!-- Project Card 5 -->
<div style="border: 1px solid #e0e0e0; border-radius: 8px; overflow: hidden; background: white; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
  <img src="/assets/images/placeholder-project-5.jpg" alt="Project 5" style="width: 100%; height: 200px; object-fit: cover; background-color: #e8e8e8;">
  <div style="padding: 1.5rem;">
    <h4 style="margin: 0 0 0.5rem 0;"><strong>ECG Anomaly Detection</strong></h4>
    <p style="margin: 0 0 1rem 0; color: #555; font-size: 0.95rem;">Trained autoencoders to detect abnormal cardiac rhythms from ECG time series data. Achieved 94% sensitivity in identifying arrhythmias with minimal false positives.</p>
    <a href="#" class="btn btn-outline" style="display: inline-block; padding: 0.4rem 1rem; font-size: 0.9rem;">View Project →</a>
  </div>
</div>

<!-- Project Card 6 -->
<div style="border: 1px solid #e0e0e0; border-radius: 8px; overflow: hidden; background: white; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
  <img src="/assets/images/placeholder-project-6.jpg" alt="Project 6" style="width: 100%; height: 200px; object-fit: cover; background-color: #e8e8e8;">
  <div style="padding: 1.5rem;">
    <h4 style="margin: 0 0 0.5rem 0;"><strong>Imaging Segmentation</strong></h4>
    <p style="margin: 0 0 1rem 0; color: #555; font-size: 0.95rem;">Built a U-Net deep learning model for automated cell segmentation in microscopy images. Achieved Dice coefficient of 0.92 on validation set.</p>
    <a href="#" class="btn btn-outline" style="display: inline-block; padding: 0.4rem 1rem; font-size: 0.9rem;">View Project →</a>
  </div>
</div>

</div>

</section>
