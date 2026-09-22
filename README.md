# MJB Logistics - Logistics Solutions

A professional, responsive website for MJB Logistics, a global logistics and freight management company. This project demonstrates modern web development practices with HTML5, CSS3, and vanilla JavaScript.

## 🌐 Live Demo

**Website**: [View Live Website](#) *(Add your Vercel deployment URL here)*

**GitHub Repository**: [GitHub Link](#) *(Add your GitHub repository URL here)*

## 📋 Project Overview

MJB Logistics is a complete frontend website showcasing:
- Global logistics and freight services
- Professional company branding
- Comprehensive service portfolio
- Customer contact and inquiry system
- Responsive design for all devices

## ✨ Features

### Pages Included
1. **Home Page** - Hero section with call-to-action, quick services overview, and key features
2. **About Page** - Company story, mission, vision, core values, team, and statistics
3. **Services Page** - Detailed service offerings (Land Transport, Air Freight, Sea Freight, Warehousing)
4. **Portfolio Page** - Showcase of completed projects and case studies with filtering
5. **Contact Page** - Contact form, business information, service areas, and FAQ section

### Key Components
- ✅ Responsive Navigation Bar with mobile menu
- ✅ Eye-catching Hero Section with CTA button
- ✅ Service Cards with hover effects
- ✅ Team Member Showcase
- ✅ Portfolio Grid with category filtering
- ✅ Contact Form with validation
- ✅ FAQ Accordion Section
- ✅ Statistics Counter Animation
- ✅ Testimonials Section
- ✅ Comprehensive Footer with links and social media
- ✅ Service Comparison Table
- ✅ Smooth Scroll Animations

### Responsive Design
- **Desktop**: Full layout with multi-column grids
- **Tablet** (768px and below): Optimized 2-column layouts
- **Mobile** (480px and below): Single-column responsive design
- **Extra Small** (360px and below): Ultra-compact layouts

## 🛠️ Technologies Used

- **HTML5**: Semantic markup and structure
- **CSS3**: 
  - Flexbox and CSS Grid for layouts
  - Media queries for responsive design
  - CSS custom properties (variables)
  - Animations and transitions
  - Gradient backgrounds
- **JavaScript (Vanilla)**:
  - DOM manipulation
  - Event handling
  - Form validation
  - Intersection Observer API for animations
  - Mobile menu toggle functionality

## 📁 Project Structure

```
mjb-logistics/
├── index.html           # Homepage
├── about.html          # About Us page
├── services.html       # Services page
├── portfolio.html      # Portfolio/Projects page
├── contact.html        # Contact page
├── styles.css          # Main stylesheet
├── script.js           # JavaScript functionality
└── README.md           # This file
```

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- Code editor (VS Code, Sublime Text, etc.)
- Git (for version control)

### Local Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/mjb-logistics.git
   cd mjb-logistics
   ```

2. **Open in Browser**
   - Option A: Double-click `index.html` to open in default browser
   - Option B: Use Live Server extension in VS Code
   - Option C: Use Python simple server
     ```bash
     python -m http.server 8000
     # Visit http://localhost:8000
     ```


### Customizing Colors

Modify CSS variables in `styles.css`:

```css
:root {
    --primary-color: #003d82;      /* Main blue */
    --secondary-color: #ff6b35;    /* Orange accent */
    --accent-color: #f7931e;       /* Yellow accent */
    /* ... more variables */
}
```

### Adding Portfolio Projects

Add new items to the portfolio grid in `portfolio.html`:

```html
<div class="portfolio-item" data-category="land">
    <div class="portfolio-image">
        <img src="image-url" alt="Project name">
        <div class="overlay">
            <a href="#" class="portfolio-link">View Project</a>
        </div>
    </div>
    <div class="portfolio-info">
        <h3>Project Title</h3>
        <p class="category-tag">Category</p>
        <p>Project description.</p>
    </div>
</div>
```

### Form Handling

The contact form includes frontend validation. To add backend functionality:

1. Uncomment/modify form submission handler in `script.js`
2. Add server endpoint for form processing
3. Implement email notification system

## 📱 Responsive Breakpoints

| Device | Breakpoint | Features |
|--------|-----------|----------|
| Desktop | > 768px | Full multi-column layouts |
| Tablet | 481px - 768px | 2-column grid, adjusted spacing |
| Mobile | 360px - 480px | Single-column, hamburger menu |
| Extra Small | < 360px | Compact layouts, minimal spacing |

## 🎨 Design System

### Color Palette
- **Primary Blue**: `#003d82` - Main branding color
- **Secondary Orange**: `#ff6b35` - Call-to-action and accents
- **Accent Yellow**: `#f7931e` - Highlights and emphasis
- **Dark Text**: `#333333` - Main text
- **Light Gray**: `#f5f5f5` - Backgrounds

### Typography
- **Font Family**: Segoe UI, Tahoma, Geneva, Verdana, sans-serif
- **Headings**: Bold, 700 weight
- **Body Text**: 400 weight, 1.6 line-height

### Spacing
- Base unit: 20px
- Padding: 20px - 80px (sections)
- Gap: 15px - 40px (grid items)

## 🔧 JavaScript Features

### Mobile Menu Toggle
```javascript
// Handled by mobileMenuBtn click listener
// Toggles active class on navLinks
```

### Form Validation
```javascript
// Validates: email format, phone format, required fields
// Shows success/error messages
```

### Portfolio Filtering
```javascript
// Filter portfolio items by category
// Smooth fade-in animation for filtered items
```

### FAQ Accordion
```javascript
// Click to expand/collapse FAQ items
// Only one item open at a time
```

### Scroll Animations
```javascript
// Elements fade in as they enter viewport
// Counter animation for statistics
```

## 📊 Performance Optimizations

- ✅ Lazy loading for images
- ✅ CSS minification ready
- ✅ Debounced resize events
- ✅ Intersection Observer for scroll animations
- ✅ Optimized animation performance
- ✅ Semantic HTML for better SEO

