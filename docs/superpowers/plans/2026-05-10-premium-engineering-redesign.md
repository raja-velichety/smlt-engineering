# Premium Engineering Redesign Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Redesign the `index.html` page to achieve a "Premium Engineering" aesthetic for non-technical business users, focusing on trust, reliability, and clear contact options.

**Architecture:** The redesign will be implemented directly within the existing `index.html` file by updating the `<style>` block and minor structural changes to the HTML. We will use CSS variables for the new theme and the Intersection Observer API for scroll animations.

**Tech Stack:** Vanilla HTML/CSS/JS, Google Fonts (Playfair Display, Outfit).

---

### Task 1: Typography and Global Styles

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Update Google Fonts imports**
Replace existing font imports with Playfair Display and Outfit.
```html
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet"/>
```

- [ ] **Step 2: Update CSS Variables and Global Reset**
Update `:root` variables with the new palette and set the global fonts.
```css
:root {
  --navy: #0D1B2A;
  --navy-mid: #1A2F46;
  --navy-light: #243d57;
  --accent: #E8650A;
  --accent-light: #F97316;
  --accent-pale: #fff3e8;
  --steel: #607D8B;
  --steel-light: #B0BEC5;
  --offwhite: #F8F6F1;
  --white: #FFFFFF;
  --text: #1A2332;
  --text-mid: #445566;
  --text-muted: #7A8FA0;
  --border: rgba(13, 27, 42, 0.1);
  --success: #166534;
  --success-bg: #DCFCE7;
  --radius: 8px;
  --radius-lg: 16px;
  --shadow: 0 4px 20px rgba(13,27,42,0.06);
  --shadow-lg: 0 10px 40px rgba(13,27,42,0.12);
  --font-main: 'Outfit', sans-serif;
  --font-heading: 'Playfair Display', serif;
}

body {
  font-family: var(--font-main);
  background: var(--offwhite);
  color: var(--text);
  position: relative;
}

/* Noise Texture Overlay */
body::before {
  content: "";
  position: fixed;
  inset: 0;
  opacity: 0.03;
  pointer-events: none;
  z-index: 9999;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
}

h1, h2, h3, h4 {
  font-family: var(--font-heading);
}
```

- [ ] **Step 3: Commit**
```bash
git add index.html
git commit -m "style: update typography and global theme variables"
```

### Task 2: Premium Navigation Bar

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Update Navbar Styles**
Implement the frosted glass effect and amber CTA button.
```css
#navbar {
  background: rgba(13, 27, 42, 0.8);
  backdrop-filter: blur(15px);
  -webkit-backdrop-filter: blur(15px);
  height: 72px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
}

.nav-logo-mark {
  background: var(--accent);
  font-family: var(--font-main);
  border-radius: 6px;
}

.nav-links a {
  font-family: var(--font-main);
  letter-spacing: 0.5px;
  font-weight: 500;
}

.nav-cta {
  background: var(--accent) !important;
  box-shadow: 0 4px 15px rgba(232, 101, 10, 0.3);
}
```

- [ ] **Step 2: Commit**
```bash
git add index.html
git commit -m "style: redesign navigation bar with premium styling"
```

### Task 3: Hero Section Redesign

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Update Hero Typography and Layout**
Apply `Playfair Display` to the headline and improve spacing.
```css
.hero-title {
  font-family: var(--font-heading);
  letter-spacing: -1px;
}

.hero-subtitle {
  font-family: var(--font-main);
  font-weight: 400;
  color: rgba(255, 255, 255, 0.7);
}

.btn-primary {
  font-family: var(--font-main);
  text-transform: none;
  font-weight: 600;
}

.hero-stat-num {
  font-family: var(--font-heading);
}

/* Ken Burns Effect */
.hero-bg-pattern {
  animation: ken-burns 20s infinite alternate;
}

@keyframes ken-burns {
  0% { transform: scale(1); }
  100% { transform: scale(1.1); }
}
```

- [ ] **Step 2: Commit**
```bash
git add index.html
git commit -m "style: redesign hero section with animations and premium typography"
```

### Task 4: Service and Product Cards

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Update Card Styles**
Apply multi-layered shadows and hover lifting effects.
```css
.service-card, .product-card, .why-card {
  background: white;
  border: 1px solid rgba(13, 27, 42, 0.05);
  box-shadow: var(--shadow);
  transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
}

.service-card:hover, .product-card:hover, .why-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-lg);
  border-color: var(--accent);
}

.product-card-category {
  font-family: var(--font-main);
  font-weight: 600;
}

.product-card-body h3 {
  font-family: var(--font-heading);
  font-size: 18px;
}
```

- [ ] **Step 2: Commit**
```bash
git add index.html
git commit -m "style: enhance product and service cards with lift effects and shadows"
```

### Task 5: Enquiry Section and Floating WhatsApp

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Update Enquiry Form and Contact Info**
Improve the "business-first" visibility of contact options.
```css
.enquiry-info-item h4 {
  font-family: var(--font-heading);
  font-size: 18px;
}

.enquiry-icon {
  background: white;
  box-shadow: var(--shadow);
  color: var(--accent);
}

.form-submit {
  font-family: var(--font-main);
  background: var(--navy);
  box-shadow: 0 4px 20px rgba(13, 27, 42, 0.2);
}

.form-submit:hover {
  background: var(--navy-mid);
}

/* Pulsing WhatsApp Button */
.wa-float {
  animation: pulse-wa 2s infinite;
}

@keyframes pulse-wa {
  0% { transform: scale(1); box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.4); }
  70% { transform: scale(1.05); box-shadow: 0 0 0 15px rgba(37, 211, 102, 0); }
  100% { transform: scale(1); box-shadow: 0 0 0 0 rgba(37, 211, 102, 0); }
}
```

- [ ] **Step 2: Commit**
```bash
git add index.html
git commit -m "style: enhance enquiry section and add pulsing WhatsApp button"
```

### Task 6: Scroll Reveal Animations

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Update Reveal Logic**
Ensure smooth fade-in and slide-up effects.
```css
.fade-in {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}

.fade-in.visible {
  opacity: 1;
  transform: translateY(0);
}
```

- [ ] **Step 2: Commit**
```bash
git add index.html
git commit -m "style: finalize scroll reveal animations"
```
