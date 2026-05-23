# 🎓 Single-Page Website Transformation - Complete Implementation Guide

Your BSCI238I course website has been transformed into a modern single-page layout where all content lives on the homepage with smooth anchor-based navigation. This guide walks you through everything that's been done and what you need to do next.

---

## ✅ What's Been Completed

### 1. **Homepage Redesigned (README.md)**
Your new homepage now features:
- **Section 1: Home Banner** - Full-width header with course title and description
- **Section 2: Weekly Schedule** - Interactive calendar using your existing schedule data
- **Section 3: Course Syllabus** - Course overview with learning objectives and grading
- **Section 4: Instructors** - Staff card grid automatically pulling from `_staffers/` collection
- **Section 5: Student Projects** - Responsive 6-project gallery showcase (easily expandable)

**File:** `README.md`

### 2. **Enhanced Styling**
Added modern CSS enhancements to `_sass/custom/custom.scss`:
- Smooth scroll behavior for anchor links
- Hover effects on staff and project cards
- Responsive grid layouts
- Section spacing and visual hierarchy

**File:** `_sass/custom/custom.scss`

### 3. **Configuration Documentation**
Created three new documentation files to guide you:

| File | Purpose |
|------|---------|
| `SINGLE_PAGE_SETUP.md` | Complete setup guide with all configuration steps |
| `CONFIG_CHANGES.md` | Specific `_config.yml` changes required |
| `IMPLEMENTATION_GUIDE.md` | This file - overview and next steps |

---

## 🔧 Next Steps: What You Need to Do

### **Step 1: Hide Old Pages from Navigation** (Takes 5 minutes)

Your old pages (schedule.md, staff.md, etc.) need to be marked as `nav_exclude: true` so they don't show in the sidebar. Update each file's front matter:

**Edit `schedule.md`:**
```yaml
---
layout: schedule
title: Schedule
nav_exclude: true
---
```

**Edit `staff.md`:**
```yaml
---
layout: default
title: Staff
nav_exclude: true
---
```

**Edit `announcements.md`:**
```yaml
---
layout: default
title: Announcements
nav_exclude: true
---
```

**Edit `calendar.md`:**
```yaml
---
layout: default
title: Calendar
nav_exclude: true
---
```

**Edit `about.md`:**
```yaml
---
layout: default
title: About
nav_exclude: true
---
```

### **Step 2: Update Navigation Links in _config.yml** (Takes 3 minutes)

Update the `aux_links` section in `_config.yml`:

```yaml
aux_links:
  Aditri Gadigi:
    - 'https://www.aditrigadigi.com'
  Anushka Poddar:
    - 'https://www.example.com'
  Canvas:
    - 'https://canvas.umd.edu/'
```

*See `CONFIG_CHANGES.md` for the complete updated file.*

### **Step 3: Add Banner Image** (Takes 5 minutes)

1. Prepare an image file (JPG, PNG, or WebP)
2. Place it at: `/assets/images/banner.jpg`
3. Or edit line in README.md to use a solid color gradient instead

**Current line in README.md:**
```markdown
![Course Banner](/assets/images/banner.jpg){: style="width: 100%; display: block;" }
```

### **Step 4: Customize Project Gallery** (Takes 10 minutes)

Edit the 6 project cards in the Projects section to showcase real student work:

**For each project card, update:**
- `href="/assets/images/placeholder-project-N.jpg"` → Add real project thumbnail
- `<strong>Protein Structure Prediction</strong>` → Your project title
- `Developed a deep learning model...` → Your project description
- `href="#"` → Link to project subpage or GitHub repo

**Example update:**
```html
<a href="https://github.com/student-username/protein-prediction" class="btn btn-outline" target="_blank">View Project →</a>
```

### **Step 5: Update Instructor Information** (Takes 5 minutes)

Your instructor cards automatically pull from `_staffers/*.md`. Verify:

1. Staff photos are in `/assets/images/` with correct filenames (referenced in .md files)
2. Email addresses and websites are correct
3. Office hours information is up to date

**Check files:**
- `/workspaces/BSCI238I/_staffers/kevin.md`
- `/workspaces/BSCI238I/_staffers/evil-kevin.md`
- `/workspaces/BSCI238I/_staffers/more-evil-kevin.md`
- `/workspaces/BSCI238I/_staffers/really-evil-kevin.md`

### **Step 6: Add Syllabus PDF** (Takes 5 minutes)

1. Place your PDF in `/assets/syllabus.pdf`
2. Update the button link in README.md (find "Download Full Syllabus"):
   ```markdown
   [Download Full Syllabus (PDF)](#){: .btn .btn-purple }
   ```
   Change to:
   ```markdown
   [Download Full Syllabus (PDF)](/assets/syllabus.pdf){: .btn .btn-purple }
   ```

### **Step 7: Update Schedule Data** (Takes 10 minutes)

Edit `_schedules/weekly.md` to match your actual course schedule:

**Current file has Monday, Tuesday, Wednesday example events. Update to include:**
- Your actual class times
- Office hours times
- Lab/section times
- Correct room locations

---

## 📋 Verification Checklist

Before pushing to GitHub, verify everything is working:

- [ ] Run `bundle exec jekyll serve` locally
- [ ] Visit `http://localhost:4000`
- [ ] Check that **old pages are hidden** from sidebar navigation
- [ ] Click each anchor link (#home, #schedule, #syllabus, #instructors, #projects) and verify smooth scrolling
- [ ] Verify schedule grid displays correctly with your data
- [ ] Verify instructor cards display with photos and information
- [ ] Test that any buttons/links work correctly
- [ ] Check mobile responsiveness by resizing browser
- [ ] Verify that search still works (searches README.md content)

---

## 🚀 Deployment

When everything looks good locally:

```bash
# Add all changes
git add README.md _config.yml schedule.md staff.md announcements.md calendar.md about.md _sass/custom/custom.scss

# Commit with descriptive message
git commit -m "Transform to single-page layout with anchor navigation

- Redesigned homepage with 5 main sections
- Added smooth anchor-based navigation
- Hid old standalone pages from navigation
- Enhanced styling for projects gallery and staff cards
- Maintained all existing content and functionality"

# Push to GitHub
git push origin main
```

Your site will automatically rebuild on GitHub Pages. Visit your live site to verify the changes are live!

---

## 📚 Section IDs Reference

These are the anchor IDs for each section. Use these in links:

```
/#home           → Top banner and course title
/#schedule       → Weekly schedule calendar
/#syllabus       → Course syllabus and policies
/#instructors    → Staff and instructors
/#projects       → Student projects gallery
```

**Example navigation link:**
```markdown
[Jump to Schedule](#schedule)
```

---

## 💡 Pro Tips

### Add a Navigation Menu (Optional)

For even better navigation, add this at the top of README.md (right after the `---` front matter):

```html
<div style="display: flex; gap: 1rem; margin-bottom: 2rem; flex-wrap: wrap; sticky; top: 0; background: white; padding: 1rem 0; z-index: 100;">
  <a href="#home" class="btn btn-outline">Home</a>
  <a href="#schedule" class="btn btn-outline">Schedule</a>
  <a href="#syllabus" class="btn btn-outline">Syllabus</a>
  <a href="#instructors" class="btn btn-outline">Instructors</a>
  <a href="#projects" class="btn btn-outline">Projects</a>
</div>
```

### Add More Project Cards

The project gallery is easily expandable. Copy this template for each new project:

```html
<!-- Project Card Template -->
<div style="border: 1px solid #e0e0e0; border-radius: 8px; overflow: hidden; background: white; box-shadow: 0 2px 4px rgba(0,0,0,0.1);">
  <img src="/assets/images/placeholder-project-X.jpg" alt="Project Name" style="width: 100%; height: 200px; object-fit: cover; background-color: #e8e8e8;">
  <div style="padding: 1.5rem;">
    <h4 style="margin: 0 0 0.5rem 0;"><strong>Your Project Title</strong></h4>
    <p style="margin: 0 0 1rem 0; color: #555; font-size: 0.95rem;">2-3 sentence project description here.</p>
    <a href="#" class="btn btn-outline" style="display: inline-block; padding: 0.4rem 1rem; font-size: 0.9rem;">View Project →</a>
  </div>
</div>
```

### Add More Sections

To add new sections (e.g., Resources, FAQ, Contact):

```html
<section id="section-name" markdown="1">

## Section Title

Your markdown content here...

</section>
```

Then add a navigation link:
```markdown
<a href="#section-name" class="btn btn-outline">Section Name</a>
```

---

## 🆘 Common Issues & Solutions

| Problem | Solution |
|---------|----------|
| Old pages still in sidebar | Restart Jekyll after adding `nav_exclude: true` |
| Anchor links not working | Check IDs match (e.g., `id="schedule"` matches `href="#schedule"`) |
| Schedule not showing | Ensure `_schedules/weekly.md` has `timeline` and `schedule` arrays |
| Staff photos not loading | Verify photo filenames match in `_staffers/*.md` and files exist in `/assets/images/` |
| CSS not updating | Run `bundle exec jekyll clean` then `bundle exec jekyll serve` |
| Mobile layout broken | Test in browser DevTools mobile view (F12 → toggle device toolbar) |

---

## 📞 Support Resources

- **Just the Docs Theme:** https://just-the-docs.github.io/
- **Jekyll Documentation:** https://jekyllrb.com/docs/
- **GitHub Pages:** https://pages.github.com/
- **Markdown Guide:** https://www.markdownguide.org/

---

## ✨ What's Next?

Now that your single-page layout is ready:

1. **Customize** the content to match your course
2. **Add real data** - projects, instructors, schedule
3. **Deploy** to GitHub Pages
4. **Share** the link with your students
5. **Maintain** by updating content in-place on README.md

All edits are made in one file (README.md), making it easy to manage your course website going forward!

---

**Last Updated:** May 23, 2026  
**Status:** Ready for customization and deployment

