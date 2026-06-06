# boss-battle-level-1-project-frontend-
## FINAL PROJECT ASSIGNMENT
### Complete Website Build – HTML + CSS (Box Model → Display → Flexbox → Grid → Media Queries)

---

## PROJECT OVERVIEW

You are going to build a **complete, fully responsive business website** for a fictional company called **"TechNova Solutions"** – a modern technology consulting firm.

This project will test **EVERYTHING** you have learned:

| Lesson | Topic | How it's tested |
|--------|-------|-----------------|
| HTML Basics | Structure, tags, lists, links, images, forms | All present in the site |
| Box Model | Padding, margin, border, box-sizing | Cards, buttons, spacing |
| Display | Block, inline, inline-block | Navigation, buttons, layout |
| Flexbox | justify-content, align-items, flex-wrap, gap | Navigation, cards, footer sections |
| Grid | grid-template-columns, grid-area, auto-fit, minmax | Main page layout, gallery |
| Media Queries | Mobile-first responsive design | Entire site adapts to all screen sizes |

---

## PROJECT REQUIREMENTS

### Page Structure (Minimum 5 Sections)

Your website must include the following sections in order:

1. **Navigation Bar** (sticky at top)
2. **Hero Section** (welcome banner with call-to-action button)
3. **Services Section** (3-4 cards showing company services)
4. **About Section** (company information with image)
5. **Gallery/Portfolio Section** (grid of images/projects)
6. **Testimonials Section** (customer reviews in a flexbox layout)
7. **Contact Form** (with name, email, message fields)
8. **Footer** (copyright, social links, contact info)

---

### Detailed Requirements by Section

#### 1. Navigation Bar (Flexbox)
- Logo on the left, navigation links on the right
- On mobile screens, navigation should stack vertically
- Sticky position (stays at top when scrolling)
- Hover effects on links

#### 2. Hero Section (Flexbox for centering)
- Large heading welcoming visitors
- Short tagline describing the company
- Call-to-action button (styled with padding, border-radius, hover effect)
- Background color or subtle background image

#### 3. Services Section (Grid or Flexbox with wrap)
- Minimum 3 cards
- Each card must have: icon/title, description, learn more button
- Cards must be responsive: 3 columns on desktop, 2 on tablet, 1 on mobile
- Use proper padding, margin, border, border-radius, box-shadow

#### 4. About Section (Grid – 2 columns)
- Left column: text description about the company
- Right column: placeholder image (use a solid color with text or an emoji)
- On mobile: stacks vertically (1 column)

#### 5. Gallery Section (CSS Grid with auto-fit/minmax)
- Minimum 6 items
- Use `grid-template-columns: repeat(auto-fit, minmax(200px, 1fr))`
- Each gallery item: image placeholder (solid color with text), title
- One featured item that is larger (span 2 columns on desktop)

#### 6. Testimonials Section (Flexbox)
- Minimum 3 testimonials
- Each testimonial: quote, customer name, role
- Use flexbox with wrap, gap, and proper alignment
- Different background color or border to distinguish

#### 7. Contact Form
- Fields: Name (text), Email (email), Message (textarea)
- Submit button
- Proper form styling: padding, border, border-radius, focus effects
- On mobile: form takes full width

#### 8. Footer (Grid – 3 or 4 columns)
- Columns: Company info, Quick links, Services, Social media
- On mobile: stack vertically

---

### CSS Requirements (Must Use ALL)

| Concept | Where to use it |
|---------|-----------------|
| `box-sizing: border-box` | Universal reset |
| `margin`, `padding`, `border` | Cards, buttons, sections, form inputs |
| `border-radius` | Cards, buttons, images |
| `box-shadow` | Cards, hero section |
| `display: flex` | Navigation bar, testimonials, footer sections, hero centering |
| `display: grid` | Services (optional), About section, Gallery, Footer |
| `flex-direction` | Mobile navigation |
| `justify-content` | Navigation bar, hero button |
| `align-items` | Navigation bar, hero section |
| `flex-wrap` | Testimonials, services on small screens |
| `gap` | Grid and flex containers |
| `grid-template-columns` | About section, footer, gallery |
| `grid-template-areas` | (Bonus) Main layout |
| `repeat(auto-fit, minmax())` | Gallery section |
| `grid-column: span` | Featured gallery item |
| `position: sticky` | Navigation bar |
| **Media Queries** | Minimum 3 breakpoints |
| Hover effects | Links, buttons, cards |

---

### Responsive Breakpoints (Mobile-First Approach)

You must implement these breakpoints:

| Breakpoint | Target | Changes |
|------------|--------|---------|
| Base (mobile: < 576px) | Phones | All sections stacked, 1 column layout |
| 576px to 768px | Small tablets | 2 columns where appropriate |
| 768px to 992px | Tablets | 2-3 columns, adjust padding |
| 992px and above | Desktops | Full 3-4 column layout |

---

### Color Scheme Suggestions (or choose your own)

```
Primary Blue:     #2c3e50
Secondary Blue:   #3498db
Accent Orange:    #e67e22
Success Green:    #2ecc71
Dark Text:        #333333
Light Text:       #7f8c8d
Background Light: #f8f9fa
White:            #ffffff
```

---

## STARTING CODE (Scaffold – Complete This)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TechNova Solutions | Technology Consulting</title>
    <style>
        /* ============================================ */
        /* UNIVERSAL RESET & BOX MODEL */
        /* ============================================ */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        /* ============================================ */
        /* BASE STYLES (Mobile First) */
        /* ============================================ */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }
        
        /* Container for consistent width */
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Section spacing */
        section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 40px;
            color: #2c3e50;
        }
        
        /* ============================================ */
        /* TYPOGRAPHY */
        /* ============================================ */
        h1, h2, h3 {
            margin-bottom: 15px;
        }
        
        /* ============================================ */
        /* BUTTONS */
        /* ============================================ */
        .btn {
            display: inline-block;
            padding: 12px 24px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
        }
        
        .btn-primary {
            background-color: #3498db;
            color: white;
            border: none;
        }
        
        .btn-primary:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }
        
        /* ============================================ */
        /* NAVIGATION BAR (Flexbox + Sticky) */
        /* ============================================ */
        /* TO DO: Add sticky positioning, flexbox layout */
        
        
        /* ============================================ */
        /* HERO SECTION (Flexbox Centering) */
        /* ============================================ */
        /* TO DO: Add flexbox centering, background, padding */
        
        
        /* ============================================ */
        /* SERVICES SECTION (Grid or Flexbox with wrap) */
        /* ============================================ */
        /* TO DO: Create responsive cards */
        
        
        /* ============================================ */
        /* ABOUT SECTION (2-column Grid) */
        /* ============================================ */
        /* TO DO: Grid layout, responsive to 1 column on mobile */
        
        
        /* ============================================ */
        /* GALLERY SECTION (CSS Grid with auto-fit) */
        /* ============================================ */
        /* TO DO: repeat(auto-fit, minmax(250px, 1fr)) + featured item */
        
        
        /* ============================================ */
        /* TESTIMONIALS SECTION (Flexbox) */
        /* ============================================ */
        /* TO DO: Flexbox with wrap, cards, styling */
        
        
        /* ============================================ */
        /* CONTACT FORM */
        /* ============================================ */
        /* TO DO: Form styling, focus effects */
        
        
        /* ============================================ */
        /* FOOTER (Grid Layout) */
        /* ============================================ */
        /* TO DO: Grid columns, responsive to 1 column on mobile */
        
        
        /* ============================================ */
        /* MEDIA QUERIES (Responsive Design) */
        /* ============================================ */
        /* Tablet: 768px and up */
        @media (min-width: 768px) {
            /* TO DO: Tablet-specific styles */
        }
        
        /* Desktop: 992px and up */
        @media (min-width: 992px) {
            /* TO DO: Desktop-specific styles */
        }
        
        /* Large Desktop: 1200px and up */
        @media (min-width: 1200px) {
            /* TO DO: Large desktop styles */
        }
    </style>
</head>
<body>

    <!-- ============================================ -->
    <!-- NAVIGATION BAR -->
    <!-- ============================================ -->
    <!-- TO DO: Create navbar with logo and links -->
    
    
    <!-- ============================================ -->
    <!-- HERO SECTION -->
    <!-- ============================================ -->
    <!-- TO DO: Hero content with heading, paragraph, button -->
    
    
    <!-- ============================================ -->
    <!-- SERVICES SECTION -->
    <!-- ============================================ -->
    <!-- TO DO: 3-4 service cards -->
    
    
    <!-- ============================================ -->
    <!-- ABOUT SECTION -->
    <!-- ============================================ -->
    <!-- TO DO: 2-column grid with text and image placeholder -->
    
    
    <!-- ============================================ -->
    <!-- GALLERY SECTION -->
    <!-- ============================================ -->
    <!-- TO DO: Gallery grid with auto-fit and featured item -->
    
    
    <!-- ============================================ -->
    <!-- TESTIMONIALS SECTION -->
    <!-- ============================================ -->
    <!-- TO DO: Testimonial cards in flexbox -->
    
    
    <!-- ============================================ -->
    <!-- CONTACT FORM -->
    <!-- ============================================ -->
    <!-- TO DO: Contact form with name, email, message -->
    
    
    <!-- ============================================ -->
    <!-- FOOTER -->
    <!-- ============================================ -->
    <!-- TO DO: Multi-column footer -->
    

</body>
</html>
```

---

## YOUR TASKS (Complete the Code)

### Task 1: Navigation Bar (10 points)
- Make the navbar `position: sticky; top: 0;`
- Use flexbox: logo on left, links on right
- Links: Home, Services, About, Gallery, Contact
- Add hover effects on links
- On mobile (< 768px): navigation links stack vertically

### Task 2: Hero Section (10 points)
- Set min-height: 400px
- Use flexbox to centre content vertically and horizontally
- Add background color `#2c3e50` with text white
- Heading: "TechNova Solutions"
- Paragraph: "Innovative technology solutions for modern businesses"
- Button: "Get Started" (use .btn-primary class)

### Task 3: Services Section (15 points)
- Create 3 service cards (or 4)
- Each card must have: title, description, "Learn More" button
- Use `display: grid` with `gap: 20px`
- On desktop: 3 columns
- On tablet: 2 columns
- On mobile: 1 column
- Cards must have: `border-radius`, `box-shadow`, `padding`, `background: white`

### Task 4: About Section (10 points)
- Use 2-column grid
- Left column: heading and paragraph about the company
- Right column: placeholder (grey box with text "Company Image")
- On mobile: 1 column (stacks vertically)

### Task 5: Gallery Section (15 points)
- Use `grid-template-columns: repeat(auto-fit, minmax(200px, 1fr))`
- Minimum 6 gallery items
- One featured item that spans 2 columns on desktop using `grid-column: span 2`
- Each gallery item: coloured box (use different shades of blue) with text "Project X"

### Task 6: Testimonials Section (10 points)
- Use `display: flex` with `flex-wrap: wrap` and `gap`
- Minimum 3 testimonial cards
- Each card: "⭐⭐⭐⭐⭐", quote text, customer name, role
- Cards should have border, border-radius, padding, background white

### Task 7: Contact Form (10 points)
- Fields: Name (text), Email (email), Message (textarea)
- Submit button styled as `.btn-primary`
- Inputs must have: padding, border, border-radius, margin-bottom
- Add focus effect: `outline: none; border-color: #3498db;`

### Task 8: Footer (10 points)
- Use `display: grid` with 4 columns on desktop
- Columns: Company Info, Quick Links, Services, Social Media
- On mobile: 1 column
- Background color: `#2c3e50`, text white

### Task 9: Media Queries (10 points)
- Implement responsive breakpoints at 576px, 768px, 992px, 1200px
- Ensure all sections adapt correctly at each breakpoint
- Navigation must collapse on mobile (stack vertically)

### Task 10: Polish & Creativity (Bonus 10 points)
- Add smooth scrolling to anchor links
- Add active/focus states for all interactive elements
- Consistent spacing and alignment
- Clean, readable code with proper indentation and comments

---

## SUBMISSION CHECKLIST

Before submitting, verify you have:

- [ ] Universal reset with `box-sizing: border-box`
- [ ] Sticky navigation bar with flexbox
- [ ] Hero section with flexbox centering
- [ ] Services section with responsive grid cards
- [ ] About section with 2-column grid
- [ ] Gallery with `auto-fit/minmax` and featured item spanning columns
- [ ] Testimonials with flexbox wrap
- [ ] Contact form with styled inputs
- [ ] Footer with grid layout
- [ ] Minimum 3 media queries
- [ ] All hover effects working
- [ ] No horizontal scroll on any screen size
- [ ] Code is clean and well-commented

---

## EXPECTED OUTPUT PREVIEW

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ [LOGO] TechNova                    Home Services About Gallery Contact      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│                      TechNova Solutions                                     │
│         Innovative technology solutions for modern businesses              │
│                        [Get Started]                                        │
│                                                                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                         Our Services                                        │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐                         │
│  │  Web Dev    │  │  Cloud      │  │  AI/ML      │                         │
│  │  Desc...    │  │  Desc...    │  │  Desc...    │                         │
│  │ [Learn]     │  │ [Learn]     │  │ [Learn]     │                         │
│  └─────────────┘  └─────────────┘  └─────────────┘                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                         About Us                                           │
│  ┌────────────────────────────┐  ┌────────────────────────┐                │
│  │ We are a team of experts   │  │    [Company Image]     │                │
│  │ delivering innovative...   │  │                        │                │
│  └────────────────────────────┘  └────────────────────────┘                │
├─────────────────────────────────────────────────────────────────────────────┤
│                         Our Work                                           │
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌─────┐ ┌─────┐ ┌─────────────┐                  │
│  │Proj1│ │Proj2│ │Proj3│ │Proj4│ │Proj5│ │  Featured   │                  │
│  │     │ │     │ │     │ │     │ │     │ │  Project    │                  │
│  └─────┘ └─────┘ └─────┘ └─────┘ └─────┘ └─────────────┘                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                       What Clients Say                                     │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐                         │
│  │ "Great job" │  │ "Excellent" │  │ "Amazing"   │                         │
│  │ - Client 1  │  │ - Client 2  │  │ - Client 3  │                         │
│  └─────────────┘  └─────────────┘  └─────────────┘                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                         Contact Us                                         │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ Name:  [____________________]                                       │   │
│  │ Email: [____________________]                                       │   │
│  │ Message: [____________________]                                     │   │
│  │                          [Send Message]                             │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
├─────────────────────────────────────────────────────────────────────────────┤
│ ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐                        │
│ │Company   │ │Quick     │ │Services  │ │Follow Us │                        │
│ │Info      │ │Links     │ │          │ │          │                        │
│ └──────────┘ └──────────┘ └──────────┘ └──────────┘                        │
│                         © 2025 TechNova Solutions                          │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## GRADING RUBRIC (100 points + 10 bonus)

| Task | Points | Completed? |
|------|--------|------------|
| Task 1: Navigation Bar (sticky + flexbox + responsive) | 10 | |
| Task 2: Hero Section (flex centering + button) | 10 | |
| Task 3: Services Section (responsive grid cards) | 15 | |
| Task 4: About Section (2-col grid) | 10 | |
| Task 5: Gallery Section (auto-fit/minmax + span) | 15 | |
| Task 6: Testimonials Section (flexbox wrap) | 10 | |
| Task 7: Contact Form (styling + focus effects) | 10 | |
| Task 8: Footer (grid responsive) | 10 | |
| Task 9: Media Queries (3+ breakpoints) | 10 | |
| Task 10: Polish & Creativity (bonus) | (10) | |
| **TOTAL** | **100** | |

---

## HELPFUL HINTS

1. **Start mobile-first** – Write styles for mobile, then use `min-width` media queries for larger screens
2. **Use the container class** – Wrap section content in `<div class="container">` for consistent width
3. **Test as you build** – Don't wait until the end. Test each section in the browser
4. **Use browser DevTools** – Inspect elements to debug layout issues
5. **Grid vs Flexbox** – Use Grid for 2D layouts (gallery, about), Flexbox for 1D layouts (navbar, testimonials)
6. **Color consistency** – Use CSS variables if you want (bonus), or stick to the suggested colors

---

**Good luck! Build something you are proud of. Submit your completed HTML/CSS file when done.**
