# Design Specification: Premium Engineering Redesign

**Date:** 2026-05-10  
**Topic:** Visual Redesign for SMLT Engineering Home Page  
**Status:** Draft (Pending User Review)

## 1. Project Overview
The goal is to redesign the `index.html` page of SMLT Engineering to create a "Premium Engineering" aesthetic. This redesign targets procurement managers and non-technical business owners, emphasizing trust, reliability, and ease of contact.

## 2. Visual Direction: Premium Engineering
The aesthetic will move away from a generic industrial look toward a high-end, bespoke engineering feel.

### 2.1 Typography
- **Primary Headings:** `Playfair Display` (Serif). Used for main section titles and hero headlines to convey authority and heritage.
- **Body & Secondary Text:** `Outfit` (Sans-Serif). A geometric, highly legible font for technical specs and descriptions.
- **Micro-copy:** `Outfit` (Uppercase, tracked 1px) for badges and labels.

### 2.2 Color Palette
- **Deep Navy (`#0D1B2A`):** Used for headers, footers, and primary text to establish "weight" and authority.
- **Industrial Amber (`#E8650A`):** Primary action color for buttons and high-importance highlights.
- **Brushed Steel (`#607D8B`):** Used for borders, icons, and secondary visual elements.
- **Soft Parchment (`#F8F6F1`):** A warm off-white background to reduce eye strain and feel more like a physical catalog.

### 2.3 Visual Details
- **Noise Texture:** A subtle `0.03` opacity noise overlay on the main background for a tactile, "premium" feel.
- **Elevated Shadows:** Multi-layered drop shadows on cards to create a sense of depth and quality.
- **Hygienic Accents:** Clean lines and generous whitespace to mimic the "cleanroom" standards of the pharma industry.

## 3. Layout & Components

### 3.1 Global Navigation
- **Behavior:** Sticky header with "frosted glass" (backdrop-filter) effect.
- **Contact Focus:** A high-contrast "Get Quote" button in the navigation bar.

### 3.2 Hero Section
- **Content:** Large headline in `Playfair Display`, followed by a brief, punchy subtitle.
- **Imagery:** High-quality background image with a subtle zoom animation (Ken Burns effect).
- **Primary CTA:** "Browse Products" (Amber) and "Request Quote" (Outline).

### 3.3 Product & Service Cards
- **Structure:** Image top, category badge, title, and a "Learn More" arrow.
- **Interaction:** Cards "lift" on hover; images scale slightly.
- **Filter Bar:** Redesigned search and category filters with sharper, premium styling.

### 3.4 Contact & Enquiry
- **Prominence:** Large icons for contact methods.
- **WhatsApp Action:** A floating, pulsing WhatsApp icon in the bottom-right corner for immediate access.

## 4. Animations & Interactivity
Animations are "mechanical and smooth," designed to guide rather than distract.

- **Load Reveal:** Headlines and hero content fade and slide up on page load.
- **Scroll Entrance:** Service and Product cards use a staggered fade-in effect as they enter the viewport.
- **Micro-interactions:** Buttons expand slightly on hover; form inputs highlight with an Amber border.

## 5. Success Criteria
- The site feels "expensive" and authoritative to a non-technical procurement manager.
- Contact options (Quote, WhatsApp) are impossible to miss.
- Product information is presented with high legibility and clear hierarchy.
