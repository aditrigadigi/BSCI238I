# 📖 Documentation Guide - Start Here!

Your BSCI238I website has been transformed into a single-page layout. This folder contains comprehensive guides to help you complete the setup and customize everything.

---

## 🚀 Start Here - Read in This Order

### 1. **QUICK_START.md** ⭐ START HERE
**Read this first!** (5 min read)
- Overview of what was done
- 3 quick tasks to complete immediately  
- Customization priorities
- Quick reference checklist

### 2. **SITE_MAP.md** (5 min read)
Visual representation of your new site structure
- Homepage section breakdown
- Navigation reference
- Directory structure
- Customization points

### 3. **IMPLEMENTATION_GUIDE.md** (15 min read)
Complete step-by-step guide for next steps
- Detailed instructions for each section
- Customization walkthrough
- Pro tips and tricks
- Troubleshooting guide

---

## 🔧 Reference Guides - Use as Needed

### **CONFIG_CHANGES.md**
When you need to update `_config.yml`:
- Specific changes required
- Full updated config template
- Testing and verification steps

### **SINGLE_PAGE_SETUP.md**
Comprehensive setup instructions:
- Step-by-step configuration
- Detailed explanations
- Navigation options
- CSS customization

### **PAGE_UPDATES.md**
How to hide old pages from navigation:
- Templates for each page
- What adding `nav_exclude: true` does
- Verification checklist

---

## 📋 Quick Reference

### Files That Changed
✅ `README.md` - Complete redesign with 5 sections  
✅ `_sass/custom/custom.scss` - Enhanced styling  
⚠️ `_config.yml` - YOU need to update `aux_links`  
⚠️ 5 old pages - YOU need to add `nav_exclude: true`

### What You Need to Do
1. Hide old pages (5 min)
2. Update _config.yml (3 min)
3. Customize with your content (30-60 min)
4. Test locally and deploy

### Files You'll Need to Create/Upload
- `/assets/images/banner.jpg` - Your course banner
- `/assets/images/placeholder-project-1.jpg` through `6.jpg` - Project images
- Staff photos referenced in `_staffers/*.md` files
- `/assets/syllabus.pdf` - Your course syllabus (optional)

---

## 🎯 Your Tasks

### Immediate (Do First)
- [ ] Read QUICK_START.md
- [ ] Read SITE_MAP.md
- [ ] Hide old pages (see PAGE_UPDATES.md)
- [ ] Update _config.yml (see CONFIG_CHANGES.md)
- [ ] Run `jekyll serve` locally and test

### Soon (Do Next)
- [ ] Add banner image
- [ ] Update instructor info
- [ ] Update schedule times
- [ ] Add project images and descriptions
- [ ] Test all anchor links

### Eventually (Polish)
- [ ] Add more project cards
- [ ] Customize colors/fonts
- [ ] Deploy to GitHub
- [ ] Share with students

---

## 📚 Documentation File Index

| File | Purpose | Read When |
|------|---------|-----------|
| **QUICK_START.md** | Overview & quick tasks | First! (5 min) |
| **SITE_MAP.md** | Visual site structure | Second (5 min) |
| **IMPLEMENTATION_GUIDE.md** | Complete guide to all steps | Third (15 min) |
| **CONFIG_CHANGES.md** | _config.yml details | When updating config |
| **SINGLE_PAGE_SETUP.md** | Detailed setup instructions | When setting up |
| **PAGE_UPDATES.md** | How to hide old pages | When updating pages |
| **README.md** | YOUR NEW HOMEPAGE | For editing content |
| **This file** | Navigation guide | You're reading it! |

---

## 🔗 Your Homepage Sections

Your README.md now has these sections with anchor links:

| Anchor | Section | Purpose |
|--------|---------|---------|
| `#home` | Home Banner | Course title & description |
| `#schedule` | Schedule | Weekly calendar |
| `#syllabus` | Syllabus | Course policies & grading |
| `#instructors` | Instructors | Staff cards |
| `#projects` | Projects | Student project gallery |

Access any section:
- Direct URL: `https://aditrigadigi.github.io/BSCI238I/#schedule`
- Markdown link: `[Go to Schedule](#schedule)`
- Button: `[Schedule](#schedule){: .btn .btn-outline }`

---

## 🎨 What's New

✨ **Single-page layout** - Everything on one page  
✨ **Anchor navigation** - Jump to sections with smooth scroll  
✨ **Auto-populated staff** - Cards pull from `_staffers/` collection  
✨ **Interactive schedule** - Calendar grid from schedule data  
✨ **Projects gallery** - Responsive 2-3 column layout  
✨ **Mobile friendly** - Works on all devices  
✨ **Enhanced styling** - Modern card designs with hover effects  

---

## 🆘 Quick Troubleshooting

**Old pages still showing in sidebar?**  
→ Add `nav_exclude: true` to front matter and restart Jekyll

**Anchor links not working?**  
→ Check section IDs match (e.g., `id="schedule"` matches `href="#schedule"`)

**Schedule not displaying?**  
→ Verify `_schedules/weekly.md` exists with timeline and schedule arrays

**Staff photos not showing?**  
→ Check photo files exist in `/assets/images/` with correct filenames

**CSS not updating?**  
→ Run `bundle exec jekyll clean` then `bundle exec jekyll serve`

**More issues?**  
→ See "Troubleshooting" section in IMPLEMENTATION_GUIDE.md

---

## 🚀 Get Started Now

1. **Open** QUICK_START.md ← Start here!
2. **Read** SITE_MAP.md to understand structure
3. **Follow** IMPLEMENTATION_GUIDE.md for next steps
4. **Reference** other docs as needed

---

## 📞 Support Resources

- **Just the Docs Theme:** https://just-the-docs.github.io/
- **Jekyll Documentation:** https://jekyllrb.com/docs/
- **GitHub Pages:** https://pages.github.com/
- **Markdown Guide:** https://www.markdownguide.org/

---

## ✅ Success Criteria

Your transformation is complete when:
- ✓ README.md displays all 5 sections correctly
- ✓ Old pages are hidden from sidebar
- ✓ Anchor links (#schedule, #instructors, etc.) work
- ✓ Schedule displays with your actual times
- ✓ Instructor cards show with photos
- ✓ Project gallery displays
- ✓ Site looks good on mobile devices
- ✓ Ready to deploy and share!

---

## 📅 Timeline

- **Now:** Read QUICK_START.md (5 min)
- **5 min:** Hide old pages + update config (8 min)
- **13 min:** Test locally with jekyll serve (5 min)
- **18 min:** Start customizing with real content (30-60 min)
- **1 hour:** Deploy to GitHub and launch! 🎉

---

**Status:** ✅ Documentation Complete  
**Your Next Step:** Open → QUICK_START.md  
**Estimated Time to Launch:** ~1 hour  

Good luck! 🚀

