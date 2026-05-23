# Page Update Templates

Below are templates for updating your existing pages to hide them from the sidebar navigation. Simply add `nav_exclude: true` to each file's front matter.

---

## schedule.md (Updated)

Replace the front matter in `schedule.md` with this:

```yaml
---
layout: schedule
title: Schedule
nav_exclude: true
---
```

**Note:** Keep the rest of the file's content as-is. The page becomes a standalone archive, but is hidden from navigation.

---

## staff.md (Updated)

Replace the front matter in `staff.md` with this:

```yaml
---
layout: default
title: Staff
nav_exclude: true
---
```

---

## announcements.md (Updated)

Replace the front matter in `announcements.md` with this:

```yaml
---
layout: default
title: Announcements
nav_exclude: true
---
```

---

## calendar.md (Updated)

Replace the front matter in `calendar.md` with this:

```yaml
---
layout: default
title: Calendar
nav_exclude: true
---
```

---

## about.md (Updated)

Replace the front matter in `about.md` with this:

```yaml
---
layout: default
title: About
nav_exclude: true
---
```

---

## What This Does

When you add `nav_exclude: true` to the front matter:

✅ The page is **NOT removed** from the repository  
✅ The page **remains accessible** at its URL (e.g., `/schedule/`)  
✅ The page is **hidden from the sidebar navigation**  
✅ The page is **hidden from search results**  
✅ Students can still access via direct link if they know the URL  

---

## After Making Changes

1. **Stop** your Jekyll server (Ctrl+C if running `jekyll serve`)
2. **Make the changes** to each file's front matter
3. **Clean** the build: `bundle exec jekyll clean`
4. **Rebuild**: `bundle exec jekyll serve`
5. **Verify** the pages are no longer in the sidebar

---

## Quick Command to Update All Files

If you want to use the command line, run this from your repo root:

```bash
# Update schedule.md
sed -i '3a nav_exclude: true' schedule.md

# Update staff.md  
sed -i '3a nav_exclude: true' staff.md

# Update announcements.md
sed -i '3a nav_exclude: true' announcements.md

# Update calendar.md
sed -i '3a nav_exclude: true' calendar.md

# Update about.md
sed -i '3a nav_exclude: true' about.md
```

**Note:** This assumes each file's front matter is at the top. If your files have a different structure, manually edit them instead.

---

## Verification

After updating all files and rebuilding Jekyll, check that:

- README.md is the only main page in the sidebar
- Old pages are completely hidden from navigation
- You can still access old pages at: `/schedule/`, `/staff/`, `/announcements/`, `/calendar/`, `/about/`
- The new single-page layout works with anchor navigation

