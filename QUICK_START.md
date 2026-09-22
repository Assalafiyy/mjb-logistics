# MJB Logistics - Quick Start Guide

Get your MJB Logistics website live in 5 steps!

---

## 📁 Project Files Overview

```
mjb-logistics/
├── index.html              # Homepage (Hero + Services + Features)
├── about.html             # About Us (Story + Mission + Team)
├── services.html          # Services Details (Land, Air, Sea, Customs)
├── portfolio.html         # Projects Showcase (With filtering)
├── contact.html           # Contact + FAQ + Service Areas
├── styles.css             # All styling (Responsive design)
├── script.js              # JavaScript functionality
├── README.md              # Main documentation
├── DEPLOYMENT_GUIDE.md    # Detailed deployment instructions
├── QUICK_START.md         # This file
└── .gitignore             # Git ignore rules
```

**Total Files**: 11 (5 HTML + 1 CSS + 1 JS + 4 Docs)

---

## ⚡ 5-Minute Quick Start

### 1️⃣ Test Locally (1 minute)

```bash
# Navigate to project folder
cd mjb-logistics

# Option A: Double-click index.html
# Option B: Use Python server
python -m http.server 8000

# Then visit: http://localhost:8000
```

### 2️⃣ Initialize Git (1 minute)

```bash
git init
git add .
git commit -m "Initial commit: MJB Logistics website"
```

### 3️⃣ Create GitHub Repository (1 minute)

- Go to [github.com/new](https://github.com/new)
- Name: `mjb-logistics`
- Make it **Public**
- Click "Create repository"

### 4️⃣ Push to GitHub (1 minute)

```bash
git remote add origin https://github.com/USERNAME/mjb-logistics.git
git branch -M main
git push -u origin main
```

### 5️⃣ Deploy to Vercel (1 minute)

- Go to [vercel.com](https://vercel.com)
- Click "Import Git Repository"
- Select your `mjb-logistics` repository
- Click "Deploy"
- **Done!** Your site is live! 🎉

---

## 📋 What's Included

### ✅ HTML Pages (5 pages - Requirement: 5+)
- **Home** - Landing page with hero section
- **About** - Company information, team, values
- **Services** - Detailed service offerings
- **Portfolio** - Case studies and projects
- **Contact** - Forms, FAQ, information

### ✅ Features
- Responsive design (mobile, tablet, desktop)
- Navigation bar with mobile menu
- Forms with validation
- Smooth animations and scrolling
- Professional styling
- Dark/light theme ready
- SEO-friendly structure

### ✅ Technology
- Pure HTML5, CSS3, JavaScript (No frameworks!)
- 100% Responsive
- No dependencies
- Fast loading
- Modern browser support

---

## 🎨 Customization Quick Guide

### Change Company Name
Replace `MJB Logistics` in:
- All HTML files
- README.md
- Commit messages

### Change Colors
Edit `:root` variables in `styles.css`:
```css
:root {
    --primary-color: #003d82;      /* Change this */
    --secondary-color: #ff6b35;    /* Or this */
    --accent-color: #f7931e;       /* Or this */
}
```

### Update Images
All images use Unsplash URLs. To change:
1. Visit [unsplash.com](https://unsplash.com)
2. Search for desired image
3. Copy the image URL
4. Replace in HTML: `<img src="NEW_URL" alt="description">`

### Modify Services
Edit service cards in `index.html` and full details in `services.html`:
```html
<div class="service-card">
    <div class="service-icon">📦</div>
    <h3>Your Service</h3>
    <p>Your description</p>
</div>
```

### Update Contact Info
Edit in `index.html`, `contact.html`, and `footer` sections:
- Email: `info@mjblogistics.com`
- Phone: `+1 (800) 123-4567`
- Address: Update in footer

---

## 📝 Making Updates

### Small Changes (CSS, Content)
```bash
# Make your changes in any file
git add .
git commit -m "style: Update button colors"
git push origin main
# Vercel auto-deploys within seconds!
```

### Major Updates (New Page)
```bash
# Create new branch
git checkout -b feature/new-page

# Create new HTML file
# Make changes
git add .
git commit -m "feat: Add new services page"
git push origin feature/new-page

# Create Pull Request on GitHub, then merge
```

---

## 🔍 File Descriptions

| File | Purpose | Lines |
|------|---------|-------|
| `index.html` | Homepage landing page | 150+ |
| `about.html` | Company story & team | 180+ |
| `services.html` | Service details & comparison | 200+ |
| `portfolio.html` | Projects showcase | 220+ |
| `contact.html` | Contact form & FAQ | 280+ |
| `styles.css` | Complete styling | 1100+ |
| `script.js` | Interactivity & validation | 300+ |
| `README.md` | Main documentation | 400+ |
| `DEPLOYMENT_GUIDE.md` | Detailed deployment help | 500+ |
| `QUICK_START.md` | This quick reference | 250+ |

**Total Code**: ~3,700 lines of quality, documented code

---

## 🚀 Deployment Status Checklist

- [ ] Files created locally
- [ ] Tested in browser
- [ ] Git initialized
- [ ] GitHub repository created
- [ ] Code pushed to GitHub
- [ ] Vercel deployment complete
- [ ] Live URL working
- [ ] README updated with URLs
- [ ] Custom domain configured (optional)

---

## 🐛 Quick Troubleshooting

| Problem | Solution |
|---------|----------|
| Links not working | Check filenames match exactly |
| Styles not loading | Restart server, clear cache |
| Mobile menu broken | Open console (F12), check errors |
| Form not working | Clear cache, refresh page |
| Vercel not deploying | Check build logs, verify files |
| Git push fails | Check internet, verify credentials |

---

## 📱 Testing Checklist

### Desktop (1920px+)
- [ ] Navigation works
- [ ] All sections visible
- [ ] Buttons clickable
- [ ] Hover effects work

### Tablet (768px)
- [ ] Responsive layout
- [ ] Touch-friendly buttons
- [ ] Images scale properly
- [ ] Text readable

### Mobile (480px)
- [ ] Mobile menu works
- [ ] Single column layout
- [ ] Touch-friendly spacing
- [ ] Fast loading

### All Devices
- [ ] No horizontal scroll
- [ ] Forms functional
- [ ] Links working
- [ ] Images loading

---

## 💡 Pro Tips

1. **Regular Commits**: Commit after each feature (not at the end)
2. **Meaningful Messages**: "Add contact form" not "update stuff"
3. **Feature Branches**: Use branches for new features
4. **Preview URLs**: Test Vercel preview before merging
5. **Browser DevTools**: Use F12 to debug and test responsiveness

---

## 🎓 Learning Path

1. **Start Here**: This Quick Start
2. **Then Read**: README.md for full overview
3. **For Deployment**: DEPLOYMENT_GUIDE.md
4. **For Code**: Open files in VS Code and explore

---

## 🔗 Important Links

- **GitHub**: https://github.com
- **Vercel**: https://vercel.com
- **Unsplash Images**: https://unsplash.com
- **Git Docs**: https://git-scm.com
- **Web Standards**: https://developer.mozilla.org

---

## ✨ Next Steps

1. **Review the code** - Open files in VS Code
2. **Customize content** - Update company info
3. **Test locally** - Open in browser
4. **Deploy** - Follow the 5-minute quick start
5. **Share** - Tell others about your site!

---

## 📞 Need Help?

- Read **DEPLOYMENT_GUIDE.md** for detailed instructions
- Check **README.md** for full documentation
- Review code comments in HTML/CSS/JS files
- Google any error messages you encounter

---

**Ready? Let's deploy!** 🚀

```bash
# One-command deployment checklist:
cd mjb-logistics
git add .
git commit -m "Initial commit: MJB Logistics website setup"
git remote add origin https://github.com/USERNAME/mjb-logistics.git
git push -u origin main
# Then deploy on Vercel!
```

---

**Project Status**: ✅ Complete and Ready to Deploy  
**Last Updated**: December 2024  
**Version**: 1.0.0
