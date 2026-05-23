# Single-Page Website Configuration Guide

## Overview
Your README.md is now a single-page website with all content in one place. This guide explains how to configure your Jekyll setup to use anchor-based navigation and hide the old multi-page layout.

---

## Step 1: Update `_config.yml` Navigation Links

Replace your current navigation links with anchor-based navigation pointing to sections on the homepage.

**Find this section in `_config.yml`:**
```yaml
aux_links:
  Aditri Gadigi:
    - 'www.google.com'
  Anushka Poddar:
    - 'www.google.com'
  Canvas:
    - 'https://github.com/kevinlin1/just-the-class'
```

**Replace with:**
```yaml
aux_links:
  Aditri Gadigi:
    - 'www.google.com'
  Anushka Poddar:
    - 'www.google.com'
  Canvas:
    - 'https://canvas.umd.edu/'
```

---

## Step 2: Hide Old Standalone Pages from Navigation

To keep the old pages (schedule.md, staff.md, announcements.md, calendar.md) in your repo but hide them from navigation, add `nav_exclude: true` to each page's front matter.

### Update `schedule.md`:
```yaml
---
layout: schedule
title: Schedule
nav_exclude: true
---
```

### Update `staff.md`:
```yaml
---
layout: default
title: Staff
nav_exclude: true
---
```

### Update `announcements.md`:
```yaml
---
layout: default
title: Announcements
nav_exclude: true
---
```

### Update `calendar.md`:
```yaml
---
layout: default
title: Calendar
nav_exclude: true
---
```

### Update `about.md`:
```yaml
---
layout: default
title: About
nav_exclude: true
---
```

---

## Step 3: Create Navigation Menu with Anchor Links

The Just the Docs theme doesn't have built-in anchor navigation in the sidebar by default. To add anchor navigation that jumps to sections on the homepage, you have two options:

### Option A: Update the Home Layout (Recommended)

Create a custom navigation menu in your site theme by modifying the navbar to include anchor links to homepage sections.

**Create or update `_includes/custom_nav.html`:**
```html
<nav class="site-nav">
  <button class="site-nav-toggle" type="button" onclick="toggleNav()">
    <svg viewBox="0 0 24 24"><path d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z"/></svg>
  </button>
  <div class="site-nav-scroll">
    <div class="site-nav-child-list">
      <a href="/#home" class="nav-list-link">Home</a>
      <a href="/#schedule" class="nav-list-link">Schedule</a>
      <a href="/#syllabus" class="nav-list-link">Syllabus</a>
      <a href="/#instructors" class="nav-list-link">Instructors</a>
      <a href="/#projects" class="nav-list-link">Projects</a>
    </div>
  </div>
</nav>
```

### Option B: Add Navigation Buttons in README

Alternatively, add a navigation menu directly at the top of your README.md (before the Home section):

```markdown
<div style="display: flex; gap: 1rem; margin-bottom: 2rem; flex-wrap: wrap;">
  <a href="#home" class="btn btn-outline">Home</a>
  <a href="#schedule" class="btn btn-outline">Schedule</a>
  <a href="#syllabus" class="btn btn-outline">Syllabus</a>
  <a href="#instructors" class="btn btn-outline">Instructors</a>
  <a href="#projects" class="btn btn-outline">Projects</a>
</div>
```

---

## Step 4: Keep Your Repository Organized

**Recommended structure:**
- Keep all old pages (schedule.md, staff.md, etc.) for archival purposes
- Mark them all with `nav_exclude: true`
- All content now flows through README.md as the primary entry point
- Old pages remain accessible via direct URLs if needed

---

## Step 5: Add Smooth Scrolling (Optional Enhancement)

Add this to your custom CSS (or in a `<style>` block in README.md) for smooth anchor scrolling:

```css
html {
  scroll-behavior: smooth;
}
```

Add this to `_sass/custom/custom.scss`:
```scss
html {
  scroll-behavior: smooth;
}
```

---

## Step 6: Update Project Links

In the Projects Gallery section, update the placeholder links (`href="#"`) to point to actual project pages or external URLs:

```markdown
<a href="/path/to/project-page.html" class="btn btn-outline">View Project →</a>
```

Or for external links:
```markdown
<a href="https://github.com/yourusername/project-repo" class="btn btn-outline" target="_blank">View Project →</a>
```

---

## Step 7: Banner Image Setup

Add your banner image to `/assets/images/banner.jpg`. You can:

1. **Replace the placeholder**: If you have a banner image, rename it to `banner.jpg` and place it in `/assets/images/`
2. **Use a solid color background instead**: Replace the image line with:
   ```markdown
   <div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); height: 300px; display: flex; align-items: center; justify-content: center; color: white; font-size: 2rem; font-weight: bold; border-radius: 8px; margin-bottom: 2rem;">BSCI 238I</div>
   ```

---

## Step 8: Test Your Setup Locally

Run your Jekyll site locally to test the anchor navigation:

```bash
bundle exec jekyll serve
```

Then navigate to `http://localhost:4000` and test:
- Click on navigation links to verify smooth scrolling
- Verify all sections are properly visible
- Check that old pages are hidden from sidebar navigation

---

## Troubleshooting

### Issue: Anchor links not working
**Solution:** Ensure your section IDs match your links:
- Link: `<a href="#schedule">` must match `<section id="schedule">`
- Check browser console for any JavaScript errors

### Issue: Sidebar still shows old pages
**Solution:** Verify you've added `nav_exclude: true` to each old page's front matter and rerun Jekyll

### Issue: Content not rendering in sections
**Solution:** Ensure each section block has `markdown="1"` attribute:
```html
<section id="schedule" markdown="1">
  Your markdown content here
</section>
```

### Issue: Schedule not displaying
**Solution:** Verify that `_schedules/weekly.md` exists and has proper front matter with timeline and schedule data

---

## Next Steps

1. **Customize project cards**: Edit the projects gallery to show real student projects
2. **Add syllabus PDF**: Upload PDF to `/assets/` and update the download link
3. **Configure instructors**: Ensure staff photos are in `/assets/images/` with proper filenames
4. **Deploy**: Push your changes to GitHub and your site will auto-update

---

## Quick Reference: Anchor IDs

Keep these section IDs consistent for navigation:
- `#home` → Top banner and course title
- `#schedule` → Weekly calendar grid
- `#syllabus` → Course syllabus and policies
- `#instructors` → Staff cards and faculty information
- `#projects` → Student projects gallery

