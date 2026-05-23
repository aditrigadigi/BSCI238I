# Visual Site Map - Single-Page Layout

Below is a visual representation of your new single-page website structure with anchor link IDs.

---

## Homepage Structure

```
HOMEPAGE (README.md)
│
├─── #home (Section 1)
│    ├─ Full-width banner image
│    ├─ Course title: "BSCI 238I: Machine Learning for the Life Sciences"
│    └─ Course description text
│
├─── #schedule (Section 2)
│    ├─ "Weekly Schedule" heading
│    ├─ Interactive calendar grid
│    │  ├─ Monday: Lecture, Section, Office Hours
│    │  ├─ Tuesday: (empty or events)
│    │  ├─ Wednesday: Lecture, Section, Office Hours
│    │  └─ ... (continues for week)
│    └─ Pull from: _schedules/weekly.md
│
├─── #syllabus (Section 3)
│    ├─ "Course Syllabus" heading
│    ├─ Course overview text
│    ├─ Learning objectives list
│    ├─ Course format (lectures, labs, projects)
│    ├─ Grading breakdown (30% homework, 15% labs, etc.)
│    └─ [Download Full Syllabus PDF] button
│
├─── #instructors (Section 4)
│    ├─ "Course Instructors & Staff" heading
│    └─ Staff grid (auto-loops from _staffers/):
│        ├─ Card 1: kevin.md
│        ├─ Card 2: evil-kevin.md
│        ├─ Card 3: more-evil-kevin.md
│        └─ Card 4: really-evil-kevin.md
│        │
│        └─ Each card contains:
│           ├─ Staff photo (150x150)
│           ├─ Name (linked to website if available)
│           ├─ Role (Instructor/TA)
│           ├─ Email (mailto link)
│           ├─ Office hours info
│           └─ Website link button
│
└─── #projects (Section 5)
     ├─ "Student Projects Gallery" heading
     ├─ Intro text
     └─ Projects grid (3-column responsive):
         ├─ Project Card 1: Protein Structure Prediction
         ├─ Project Card 2: Gene Expression Classification
         ├─ Project Card 3: Drug Discovery Pipeline
         ├─ Project Card 4: Metagenomic Binning
         ├─ Project Card 5: ECG Anomaly Detection
         └─ Project Card 6: Imaging Segmentation
         │
         └─ Each card contains:
            ├─ Thumbnail image (300x200)
            ├─ Project title
            ├─ 2-3 sentence description
            └─ [View Project →] button
```

---

## Navigation Reference

### Anchor Links (Use in URLs or nav buttons)

| Anchor | Target | Display Text |
|--------|--------|--------------|
| `/#home` | Home banner section | Home |
| `/#schedule` | Schedule section | Schedule |
| `/#syllabus` | Syllabus section | Syllabus |
| `/#instructors` | Instructors section | Instructors |
| `/#projects` | Projects section | Projects |

### Examples

```
Direct URL: https://aditrigadigi.github.io/BSCI238I/#schedule
HTML Link:  <a href="#schedule">Go to Schedule</a>
Markdown:   [Schedule](#schedule)
Button:     [Schedule](#schedule){: .btn .btn-outline }
```

---

## Data Sources

Each section automatically pulls data from:

| Section | Data Source | File Location |
|---------|------------|---------------|
| Home Banner | Manual | README.md (lines 11-18) |
| Schedule | YAML data | `_schedules/weekly.md` |
| Syllabus | Manual | README.md (lines 35-55) |
| Instructors | Collection | `_staffers/*.md` (4 files) |
| Projects | Manual | README.md (lines 78-165) |

---

## Directory Structure

```
/workspaces/BSCI238I/
│
├── README.md                              ← MAIN HOMEPAGE
│   ├─ Front matter (layout, title, etc.)
│   ├─ Home section (ID: home)
│   ├─ Schedule section (ID: schedule)
│   ├─ Syllabus section (ID: syllabus)
│   ├─ Instructors section (ID: instructors)
│   └─ Projects section (ID: projects)
│
├── _config.yml                            ← Configuration
│   └─ aux_links (navigation)
│
├── _schedules/
│   └── weekly.md                          ← Schedule data
│       ├─ timeline: [9:00 AM, 9:30 AM, ...]
│       └─ schedule: [{name: Monday, events: [...]}, ...]
│
├── _staffers/                             ← Staff cards data
│   ├── kevin.md
│   ├── evil-kevin.md
│   ├── more-evil-kevin.md
│   └── really-evil-kevin.md
│
├── _sass/custom/
│   └── custom.scss                        ← Custom styling
│       └─ Smooth scroll, hover effects, responsive grids
│
├── assets/images/
│   ├── banner.jpg                         ← Course banner (add this)
│   ├── placeholder-project-1.jpg          ← Project images (6 needed)
│   ├── placeholder-project-2.jpg
│   ├── ... (etc)
│   ├── [staff-photo-1.jpg]                ← Staff photos (referenced in _staffers/)
│   ├── [staff-photo-2.jpg]
│   └── ... (etc)
│
├── Old Pages (Hidden from Nav)
│   ├── schedule.md (nav_exclude: true)
│   ├── staff.md (nav_exclude: true)
│   ├── announcements.md (nav_exclude: true)
│   ├── calendar.md (nav_exclude: true)
│   └── about.md (nav_exclude: true)
│
└── Documentation (You're reading this!)
    ├── QUICK_START.md
    ├── IMPLEMENTATION_GUIDE.md
    ├── CONFIG_CHANGES.md
    ├── SINGLE_PAGE_SETUP.md
    ├── PAGE_UPDATES.md
    └── SITE_MAP.md (this file)
```

---

## User Flow

### Current Multi-Page Structure (Before)
```
Homepage (README.md)
     ├─ Schedule page (schedule.md)
     ├─ Staff page (staff.md)
     ├─ Announcements (announcements.md)
     ├─ Calendar (calendar.md)
     └─ About (about.md)
```

### New Single-Page Structure (After)
```
Homepage (README.md)
├─ #home section (brand new)
├─ #schedule section (from schedule.md)
├─ #syllabus section (new comprehensive syllabus)
├─ #instructors section (from staff.md)
└─ #projects section (new project gallery)

Old pages: Hidden but archived at /schedule/, /staff/, etc.
```

---

## Responsive Grid Layouts

### Instructors Section
- Desktop (1200px+): 4 columns
- Tablet (768px): 2 columns
- Mobile (< 768px): 1 column

### Projects Section
- Desktop (1200px+): 3 columns
- Tablet (768px): 2 columns
- Mobile (< 768px): 1 column

---

## Color & Styling Reference

### Button Styles Used
```
.btn              ← Basic button
.btn-outline      ← Outlined button
.btn-purple       ← Purple filled button
```

### Custom Styling Applied
```css
html { scroll-behavior: smooth; }  ← Smooth anchor scrolling
section { scroll-margin-top: 120px; }  ← Offset for fixed nav
```

---

## Quick Customization Points

To customize different parts:

| Want to Change | Edit | Location |
|---|---|---|
| Course title/description | README.md | Line 12-18 |
| Schedule times | _schedules/weekly.md | Entire file |
| Instructor info/photos | _staffers/*.md | All 4 files |
| Syllabus content | README.md | Line 35-55 |
| Project cards | README.md | Line 78-165 |
| Colors/fonts | _sass/custom/custom.scss | Line 48+ |
| Banner image | /assets/images/banner.jpg | Add file here |

---

## Testing Checklist by Section

### Section: #home
- [ ] Banner image displays
- [ ] Course title is visible
- [ ] Description text is readable
- [ ] Width spans full container

### Section: #schedule
- [ ] Timeline (times) displays on left
- [ ] Days of week display (Mon, Tue, Wed)
- [ ] Events show up for each day
- [ ] Event details visible (name, time, location)

### Section: #syllabus
- [ ] Headings display correctly
- [ ] Course overview text visible
- [ ] Learning objectives listed
- [ ] Grading table displays
- [ ] PDF download button works

### Section: #instructors
- [ ] Grid displays with 2-4 columns (depending on screen size)
- [ ] Staff photos load correctly
- [ ] Names, roles, emails visible
- [ ] Office hours info displayed
- [ ] Website links work

### Section: #projects
- [ ] Grid displays with 2-3 columns
- [ ] Project images load
- [ ] Titles and descriptions readable
- [ ] View Project buttons work
- [ ] Hover effects visible on desktop

---

## Next Steps

1. **Understand Structure** ✓ (you're reading this)
2. **Hide Old Pages** → Add `nav_exclude: true` to 5 files
3. **Update Config** → Update `aux_links` in `_config.yml`
4. **Add Real Content** → Update schedule, staff, projects
5. **Add Images** → Banner, projects, staff photos
6. **Test Locally** → `jekyll serve` and verify
7. **Deploy** → `git push` to GitHub

---

**Version:** 1.0 | **Date:** May 23, 2026

