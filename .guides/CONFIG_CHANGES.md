# _config.yml Configuration Changes

Below are the specific changes to make in your `_config.yml` file to support the single-page layout with anchor navigation.

## Current _config.yml

Here's your current configuration:

```yaml
# Site settings
title: "BSCI238I"
tagline: "Spring 2026 | University of Maryland, College Park"
description: "A modern, highly customizable, responsive Jekyll template for course websites"
author: "Aditri Gadigi and Anushka Poddar"
baseurl: "/BSCI238I"
url: "https://aditrigadigi.github.io"
exclude: ["Gemfile", "Gemfile.lock", "LICENSE"]

# Theme settings
remote_theme: just-the-docs/just-the-docs@v0.12.0
color_scheme: light
search_enabled: true
heading_anchors: true
permalink: pretty
aux_links:
  Aditri Gadigi:
    - 'www.google.com'
  Anushka Poddar:
    - 'www.google.com'
  Canvas:
    - 'https://github.com/kevinlin1/just-the-class'
footer_content:

# Collections for website data
collections:
  staffers:
  modules:
  schedules:
  announcements:
# ... rest of config
```

## Required Changes

### 1. Update aux_links (Navigation Links)

**CHANGE FROM:**
```yaml
aux_links:
  Aditri Gadigi:
    - 'www.google.com'
  Anushka Poddar:
    - 'www.google.com'
  Canvas:
    - 'https://github.com/kevinlin1/just-the-class'
```

**CHANGE TO:**
```yaml
aux_links:
  Aditri Gadigi:
    - 'https://www.aditrigadigi.com'
  Anushka Poddar:
    - 'https://www.example.com'
  Canvas:
    - 'https://canvas.umd.edu/'
```

### 2. Add Navigation Links Configuration (Optional but Recommended)

Add this new section to enable better sidebar navigation customization:

```yaml
# Navigation configuration for single-page layout
nav_order: 1
has_children: false
```

### 3. Hide Old Pages from Navigation

After running Jekyll with the updated `_config.yml`, update each of these files' front matter to include `nav_exclude: true`:

- `schedule.md` - Add `nav_exclude: true`
- `staff.md` - Add `nav_exclude: true`
- `announcements.md` - Add `nav_exclude: true`
- `calendar.md` - Add `nav_exclude: true`
- `about.md` - Add `nav_exclude: true`

**Example - schedule.md:**
```yaml
---
layout: schedule
title: Schedule
nav_exclude: true
---
```

### 4. Full Updated _config.yml Template

Here's what your complete `_config.yml` should look like:

```yaml
# Welcome to Jekyll!

# Site settings
title: "BSCI238I"
tagline: "Spring 2026 | University of Maryland, College Park"
description: "Machine Learning for the Life Sciences"
author: "Aditri Gadigi and Anushka Poddar"
baseurl: "/BSCI238I"
url: "https://aditrigadigi.github.io"
exclude: ["Gemfile", "Gemfile.lock", "LICENSE"]

# Theme settings
remote_theme: just-the-docs/just-the-docs@v0.12.0
color_scheme: light
search_enabled: true
heading_anchors: true
permalink: pretty

# Navigation - Anchor-based links for single-page layout
aux_links:
  Aditri Gadigi:
    - 'https://www.aditrigadigi.com'
  Anushka Poddar:
    - 'https://www.example.com'
  Canvas:
    - 'https://canvas.umd.edu/'

footer_content: "BSCI 238I © 2026. All rights reserved."

# Collections for website data
collections:
  staffers:
  modules:
  schedules:
  announcements:

# Default layouts for each collection type
defaults:
  - scope:
      path: ''
      type: staffers
    values:
      layout: staffer
      height: 300
      subpath: '/assets/images/'
      width: 300
  - scope:
      path: ''
      type: modules
    values:
      layout: module
  - scope:
      path: ''
      type: schedules
    values:
      layout: schedule
  - scope:
      path: ''
      type: announcements
    values:
      layout: announcement

compress_html:
  clippings: all
  comments: all
  endings: all
  startings: []
  blanklines: false
  profile: false

liquid:
  error_mode: strict
  strict_filters: true
```

## Optional Enhancements

### Add Custom Search Scope

To limit search to specific sections, add:

```yaml
search:
  heading_level: 2
  previews: 2
  preview_words_before: 5
  preview_words_after: 5
```

### Enable Specific Theme Features

For better mobile responsiveness:

```yaml
# Enable mobile-friendly features
enable_search_focus: true
back_to_top: true
```

## Testing Your Changes

After updating `_config.yml`:

1. **Stop your Jekyll server** (if running)
2. **Rebuild the site:**
   ```bash
   bundle exec jekyll clean
   bundle exec jekyll build
   ```
3. **Restart the local server:**
   ```bash
   bundle exec jekyll serve
   ```
4. **Visit:** `http://localhost:4000`
5. **Verify:**
   - Sidebar shows only README.md (or default page)
   - Old pages (schedule.md, staff.md, etc.) are hidden
   - Anchor links (#schedule, #instructors, etc.) work in URL bar
   - All sections are properly linked

## Deployment

When you push to GitHub:

```bash
git add _config.yml README.md _sass/custom/custom.scss
git commit -m "Transform to single-page layout with anchor navigation"
git push origin main
```

Your site will rebuild automatically on GitHub Pages within a few minutes.

## Quick Troubleshooting

| Issue | Solution |
|-------|----------|
| Pages still showing in sidebar | Ensure `nav_exclude: true` is in each page's front matter AND you've restarted Jekyll |
| Anchor links not smooth | Check that `scroll-behavior: smooth;` is in custom.scss (already added) |
| Schedule not displaying | Verify `_schedules/weekly.md` exists with proper timeline and schedule arrays |
| Staff cards not showing | Check that `_staffers/*.md` files exist and have proper photo filenames |
| CSS not applying | Run `jekyll clean` then `jekyll serve` to force CSS rebuild |

