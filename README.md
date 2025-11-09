# The Shift Oakland Chiropractor - Landing Page Maintenance & Customization Guide

## Table of Contents
1. [Overview](#overview)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing Broken Links](#fixing-broken-links)
5. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
6. [Troubleshooting](#troubleshooting)
7. [Best Practices](#best-practices)

---

## Overview

This landing page uses **Tailwind CSS** for styling and **vanilla JavaScript** for interactivity. All content is contained in a single `index.html` file. The page is organized into distinct sections:

- **Header & Navigation** - Fixed navigation bar with mobile menu
- **Hero Section** - Large banner with call-to-action
- **Features Section** - Three service cards
- **Video Section** - Embedded YouTube video
- **Benefits Section** - Three benefit cards with alternating layouts
- **About Section** - Company story
- **Testimonials Section** - Customer reviews
- **FAQ Section** - Accordion-style questions
- **CTA Section** - Call-to-action banner
- **Contact Section** - Contact information cards
- **Footer** - Navigation links and legal pages

---

## Updating Text Content

### What is Text Content?
Text content includes all the words visible on your website: headlines, descriptions, testimonials, and any written information.

### Where to Find Text Content

#### 1. **Header/Navigation Section** (Lines 85-130)
This is the top bar that appears on every page.

**Location in HTML:**
```html
<!-- Logo Text - Line ~93 -->
<span class="text-xl font-bold text-gray-900 hidden sm:inline">The Shift</span>

<!-- Navigation Menu Items - Lines 97-104 -->
<a href="#home" class="text-gray-700 hover:text-blue-600...">Home</a>
<a href="#features" class="text-gray-700 hover:text-blue-600...">Features</a>
<!-- etc. -->
```

**How to Update:**
1. Open your `index.html` file in a text editor (like Notepad, VS Code, or Sublime Text)
2. Use `Ctrl+F` (Windows/Linux) or `Cmd+F` (Mac) to search for the text you want to change
3. For example, search for "The Shift" to find the logo text
4. Replace the text between the tags
5. Save the file using `Ctrl+S` or `Cmd+S`

**Example - Changing the Logo:**
```html
<!-- BEFORE -->
<span class="text-xl font-bold text-gray-900 hidden sm:inline">The Shift</span>

<!-- AFTER -->
<span class="text-xl font-bold text-gray-900 hidden sm:inline">Your Chiropractic Name</span>
```

---

#### 2. **Hero Section** (Lines 135-160)
The large banner at the top with the main headline.

**Location in HTML:**
```html
<!-- Main Headline - Line ~145 -->
<h1 class="text-4xl sm:text-5xl md:text-6xl font-bold text-white...">
    Oakland Chiropractor for Seniors Balance, Fall Prevention and Wellbeing
</h1>

<!-- Subheading - Line ~149 -->
<p class="text-xl md:text-2xl text-gray-100 mb-8...">
    The Shift Oakland Chiropractor high quality Senior Care
</p>
```

**How to Update:**
1. Search for "Oakland Chiropractor for Seniors Balance"
2. Replace the entire heading with your own text
3. Keep the HTML tags (`<h1>` and `</h1>`) - only change the text inside
4. Update the subheading paragraph similarly

**Example:**
```html
<!-- BEFORE -->
<h1 class="text-4xl sm:text-5xl md:text-6xl font-bold text-white leading-tight tracking-tight mb-6">
    Oakland Chiropractor for Seniors Balance, Fall Prevention and Wellbeing
</h1>

<!-- AFTER -->
<h1 class="text-4xl sm:text-5xl md:text-6xl font-bold text-white leading-tight tracking-tight mb-6">
    Expert Chiropractic Care for Active Seniors in Oakland
</h1>
```

---

#### 3. **Features Section** (Lines 168-220)
The three service cards below the hero.

**Location in HTML:**
```html
<!-- Section Title - Line ~172 -->
<h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4...">
    Our Specialized Services
</h2>

<!-- Feature Card 1 Heading - Line ~191 -->
<h3 class="text-xl font-bold text-gray-900 mb-3">
    Chiropractic Senior Care
</h3>

<!-- Feature Card 1 Description - Line ~194 -->
<p class="text-gray-600 leading-relaxed">
    Specialized chiropractic treatments tailored for the unique needs of seniors...
</p>
```

**How to Update:**
1. There are three feature cards - each has a heading (`<h3>`) and description (`<p>`)
2. Search for each feature title to find its location
3. Update the heading and description text while keeping the HTML structure intact
4. You can also change the icons (see the [Modifying Icons](#modifying-icons) section below)

**Example - Updating Feature 1:**
```html
<!-- BEFORE -->
<h3 class="text-xl font-bold text-gray-900 mb-3">
    Chiropractic Senior Care
</h3>
<p class="text-gray-600 leading-relaxed">
    Specialized chiropractic treatments tailored for the unique needs of seniors...
</p>

<!-- AFTER -->
<h3 class="text-xl font-bold text-gray-900 mb-3">
    Personalized Senior Adjustments
</h3>
<p class="text-gray-600 leading-relaxed">
    Custom chiropractic care designed specifically for the aging body with gentle techniques...
</p>
```

---

#### 4. **Video Section** (Lines 225-245)
The section with the embedded YouTube video.

**Location in HTML:**
```html
<!-- Section Title - Line ~229 -->
<h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4...">
    Learn More About Our Services
</h2>

<!-- Description - Line ~233 -->
<p class="text-lg text-gray-600 max-w-2xl mx-auto">
    Watch our video to discover how The Shift Oakland Chiropractor...
</p>
```

**How to Update:**
- Update the title and description text using the same method as above
- To change the YouTube video, see the [Linking Video Content](#linking-video-content) section below

---

#### 5. **Benefits Section** (Lines 250-380)
The three benefit cards with alternating layouts.

**Location in HTML:**
```html
<!-- Section Title - Line ~254 -->
<h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4...">
    Why Choose The Shift Oakland Chiropractor
</h2>

<!-- Benefit 1 Heading - Line ~270 -->
<h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-4">
    Effective Results
</h3>

<!-- Benefit 1 Description - Line ~273 -->
<p class="text-gray-600 leading-relaxed mb-4">
    Our proven chiropractic techniques deliver measurable results...
</p>

<!-- Benefit Bullet Points - Lines ~280-288 -->
<li class="flex items-start gap-3">
    <i class="fas fa-check text-green-500 mt-1 flex-shrink-0"></i>
    <span class="text-gray-700">Reduced chronic pain and discomfort</span>
</li>
```

**How to Update:**
1. Search for each benefit title ("Effective Results", "Efficient Care", "Safe Practices")
2. Update the main heading and description text
3. Update the bullet points by changing the text inside the `<span>` tags
4. Keep the `<i class="fas fa-check..."></i>` icon code - it displays the checkmark

**Example - Updating a Benefit:**
```html
<!-- BEFORE -->
<h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-4">
    Effective Results
</h3>

<!-- AFTER -->
<h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-4">
    Proven Pain Relief
</h3>
```

---

#### 6. **About Section** (Lines 385-420)
The company story section.

**Location in HTML:**
```html
<!-- Section Title - Line ~389 -->
<h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4...">
    About The Shift Oakland Chiropractor
</h2>

<!-- Subsection Heading - Line ~409 -->
<h3 class="text-2xl font-bold text-gray-900 mb-4">Our Story</h3>

<!-- Story Paragraphs - Lines ~410-420 -->
<p class="text-gray-600 leading-relaxed mb-6">
    The Shift Oakland Chiropractor was founded on the belief that seniors deserve...
</p>
```

**How to Update:**
1. Search for "Our Story" to find this section
2. Update the section title, subsection heading, and paragraph text
3. You can add or remove paragraphs by copying the `<p>` tag structure

**Example - Updating the Story:**
```html
<!-- BEFORE -->
<p class="text-gray-600 leading-relaxed mb-6">
    The Shift Oakland Chiropractor was founded on the belief that seniors deserve specialized...
</p>

<!-- AFTER -->
<p class="text-gray-600 leading-relaxed mb-6">
    Founded in 2020, our clinic has served over 1,000 seniors in the Oakland area...
</p>
```

---

#### 7. **Testimonials Section** (Lines 425-500)
Customer reviews section.

**Location in HTML:**
```html
<!-- Section Title - Line ~429 -->
<h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4...">
    What Our Patients Say
</h2>

<!-- Testimonial 1 Quote - Line ~445 -->
<p class="text-gray-600 leading-relaxed mb-6 italic">
    "I came to The Shift with chronic lower back pain..."
</p>

<!-- Testimonial 1 Name - Line ~450 -->
<p class="font-bold text-gray-900">Margaret Chen</p>

<!-- Testimonial 1 Title - Line ~451 -->
<p class="text-gray-600 text-sm">Retired Teacher, Oakland</p>
```

**How to Update:**
1. Each testimonial has a quote, customer name, and customer title
2. Search for a customer name to find their testimonial
3. Update the quote text, name, and title
4. The star rating (5 stars) is displayed automatically - don't modify the `<i class="fas fa-star..."></i>` code

**Example - Updating a Testimonial:**
```html
<!-- BEFORE -->
<p class="text-gray-600 leading-relaxed mb-6 italic">
    "I came to The Shift with chronic lower back pain that was affecting my daily activities..."
</p>
<div class="border-t border-gray-200 pt-4">
    <p class="font-bold text-gray-900">Margaret Chen</p>
    <p class="text-gray-600 text-sm">Retired Teacher, Oakland</p>
</div>

<!-- AFTER -->
<p class="text-gray-600 leading-relaxed mb-6 italic">
    "The best chiropractic care I've ever received. Highly recommended!"
</p>
<div class="border-t border-gray-200 pt-4">
    <p class="font-bold text-gray-900">John Smith</p>
    <p class="text-gray-600 text-sm">Retired Accountant, Oakland</p>
</div>
```

---

#### 8. **FAQ Section** (Lines 505-570)
Frequently Asked Questions with accordion.

**Location in HTML:**
```html
<!-- Section Title - Line ~509 -->
<h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4...">
    Frequently Asked Questions
</h2>

<!-- FAQ Item 1 Question - Line ~523 -->
<span class="text-lg font-semibold text-gray-900 text-left">
    Is chiropractic care safe for seniors?
</span>

<!-- FAQ Item 1 Answer - Line ~529 -->
<p>
    Yes, chiropractic care is very safe for seniors when provided by qualified practitioners...
</p>
```

**How to Update:**
1. Search for the FAQ question you want to change
2. Update the question text inside the `<span>` tag
3. Update the answer text inside the `<p>` tag
4. To add a new FAQ item, copy an entire FAQ block and modify it

**Example - Updating an FAQ:**
```html
<!-- BEFORE -->
<span class="text-lg font-semibold text-gray-900 text-left">
    Is chiropractic care safe for seniors?
</span>
<!-- ... -->
<p>
    Yes, chiropractic care is very safe for seniors when provided by qualified practitioners...
</p>

<!-- AFTER -->
<span class="text-lg font-semibold text-gray-900 text-left">
    What is your cancellation policy?
</span>
<!-- ... -->
<p>
    We require 24 hours notice for cancellations. Cancellations made less than 24 hours in advance...
</p>
```

---

#### 9. **Contact Section** (Lines 580-620)
Contact information cards.

**Location in HTML:**
```html
<!-- Contact Card 1 Title - Line ~595 -->
<h3 class="text-xl font-bold text-gray-900 mb-2">Email</h3>

<!-- Contact Card 1 Email - Line ~596 -->
<a href="mailto:Theshiftchiropractic@gmail.com" class="text-blue-600...">
    Theshiftchiropractic@gmail.com
</a>

<!-- Contact Card 3 Location - Line ~617 -->
<p class="text-gray-600">
    Oakland, California
</p>
```

**How to Update:**
- Update the email address (see [Fixing Broken Links](#fixing-broken-links) for email links)
- Update the location text
- Keep the contact card structure intact

---

#### 10. **Footer Section** (Lines 625-710)
The bottom of the page with company info and links.

**Location in HTML:**
```html
<!-- Footer Logo Text - Line ~632 -->
<span class="text-lg font-bold text-white">The Shift</span>

<!-- Footer Description - Line ~634 -->
<p class="text-sm leading-relaxed mb-4">
    Specialized chiropractic care for seniors in Oakland...
</p>

<!-- Footer Column Headings - Lines ~648, ~659, ~670 -->
<h4 class="text-white font-bold mb-4">Quick Links</h4>
```

**How to Update:**
1. Update the footer logo text to match your business name
2. Update the company description
3. Update column headings if needed
4. All links in the footer are covered in the [Fixing Broken Links](#fixing-broken-links) section

---

### Quick Reference: Text Content Locations

| Section | Search Term | Line Range |
|---------|------------|-----------|
| Header Logo | "The Shift" | ~93 |
| Hero Headline | "Oakland Chiropractor for Seniors" | ~145 |
| Features Titles | "Chiropractic Senior Care" | ~191-210 |
| Benefits Titles | "Effective Results" | ~270-340 |
| About Section | "Our Story" | ~409 |
| Testimonials | Customer names | ~445-490 |
| FAQ Questions | "Is chiropractic care safe" | ~523-560 |
| Contact Email | "Theshiftchiropractic@gmail.com" | ~596 |
| Footer | "The Shift" | ~632 |

---

## Modifying Tailwind CSS Classes

### What are Tailwind CSS Classes?
Tailwind CSS is a system of pre-made styling instructions. Instead of writing custom CSS code, you use class names to style elements. For example:
- `text-white` = white text
- `bg-blue-600` = blue background
- `p-8` = padding (space inside)
- `rounded-lg` = rounded corners

### Understanding the Class Structure

Every HTML element on this page has classes that look like this:
```html
<button class="text-white bg-blue-600 px-8 py-4 rounded-lg hover:bg-blue-700 transition-colors duration-300">
    Click Me
</button>
```

**Breaking it down:**
- `text-white` = white text color
- `bg-blue-600` = blue background
- `px-8` = horizontal padding (left and right)
- `py-4` = vertical padding (top and bottom)
- `rounded-lg` = rounded corners
- `hover:bg-blue-700` = darker blue on hover
- `transition-colors` = smooth color change
- `duration-300` = animation takes 300 milliseconds

---

### Common Tailwind Classes Used in This Page

#### Text Styling
```html
<!-- Text Color -->
<p class="text-gray-900">Dark gray text (main text)</p>
<p class="text-gray-600">Medium gray text (descriptions)</p>
<p class="text-white">White text (on dark backgrounds)</p>
<p class="text-blue-600">Blue text (links, accents)</p>

<!-- Text Size -->
<h1 class="text-6xl">Extra large (headlines)</h1>
<h2 class="text-4xl">Large (section titles)</h2>
<h3 class="text-2xl">Medium (subheadings)</h3>
<p class="text-lg">Large paragraph</p>
<p class="text-base">Normal paragraph</p>
<p class="text-sm">Small text (captions)</p>

<!-- Text Weight (boldness) -->
<p class="font-bold">Bold text</p>
<p class="font-semibold">Semi-bold text</p>
<p class="font-medium">Medium weight</p>
<p class="font-light">Light text</p>
```

#### Spacing (Padding and Margins)
```html
<!-- Padding (space inside) -->
<div class="p-8">Padding all sides (8 units)</div>
<div class="px-4">Padding left and right only</div>
<div class="py-4">Padding top and bottom only</div>

<!-- Margins (space outside) -->
<div class="mb-6">Margin bottom (6 units)</div>
<div class="mt-4">Margin top (4 units)</div>
<div class="mx-auto">Centered horizontally</div>
```

#### Background Colors
```html
<!-- Background Colors -->
<div class="bg-white">White background</div>
<div class="bg-gray-50">Very light gray background</div>
<div class="bg-gray-900">Dark gray/black background</div>
<div class="bg-blue-600">Blue background</div>
<div class="bg-green-100">Light green background</div>
```

#### Sizing
```html
<!-- Width -->
<div class="w-full">Full width (100%)</div>
<div class="w-1/2">Half width (50%)</div>
<div class="max-w-7xl">Maximum width container</div>

<!-- Height -->
<div class="h-64">Fixed height</div>
<div class="h-screen">Full screen height</div>
```

#### Responsive Design Classes
Tailwind uses prefixes to make elements responsive:
```html
<!-- These classes apply at different screen sizes -->
<div class="text-4xl md:text-5xl lg:text-6xl">
    <!-- text-4xl on small screens -->
    <!-- text-5xl on medium screens (md:) -->
    <!-- text-6xl on large screens (lg:) -->
</div>

<div class="hidden md:flex">
    <!-- hidden on small screens -->
    <!-- flex (visible) on medium screens -->
</div>
```

**Common breakpoints:**
- `sm:` = small screens (640px)
- `md:` = medium screens (768px)
- `lg:` = large screens (1024px)

---

### How to Modify Colors

#### Changing Primary Button Color

**Location:** Lines 153-155 (Hero CTA button)
```html
<!-- BEFORE - Blue button -->
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" 
   class="inline-block btn-primary bg-blue-600 hover:bg-blue-700 text-white font-bold py-4 px-8 rounded-lg shadow-lg">
    Schedule Your Appointment Today
</a>

<!-- AFTER - Green button -->
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" 
   class="inline-block btn-primary bg-green-600 hover:bg-green-700 text-white font-bold py-4 px-8 rounded-lg shadow-lg">
    Schedule Your Appointment Today
</a>
```

**What changed:**
- `bg-blue-600` → `bg-green-600` (background color)
- `hover:bg-blue-700` → `hover:bg-green-700` (hover color)

---

#### Changing Feature Card Colors

**Location:** Lines 184-220 (Feature cards)
```html
<!-- BEFORE - Blue border top -->
<div class="feature-card bg-white rounded-lg shadow-md p-8 border-t-4 border-blue-600">
    <div class="flex items-center justify-center w-16 h-16 bg-blue-100 rounded-full mb-6">
        <i class="fas fa-spine text-2xl text-blue-600"></i>
    </div>
    ...
</div>

<!-- AFTER - Purple border top -->
<div class="feature-card bg-white rounded-lg shadow-md p-8 border-t-4 border-purple-600">
    <div class="flex items-center justify-center w-16 h-16 bg-purple-100 rounded-full mb-6">
        <i class="fas fa-spine text-2xl text-purple-600"></i>
    </div>
    ...
</div>
```

**What changed:**
- `border-blue-600` → `border-purple-600` (border color)
- `bg-blue-100` → `bg-purple-100` (background color)
- `text-blue-600` → `text-purple-600` (icon color)

---

#### Changing Section Background Colors

**Location:** Lines 168 (Features section)
```html
<!-- BEFORE - Light gray background -->
<section id="features" class="py-16 md:py-24 bg-gray-50">
    ...
</section>

<!-- AFTER - White background -->
<section id="features" class="py-16 md:py-24 bg-white">
    ...
</section>
```

---

### How to Modify Spacing

#### Increasing Padding on Cards

**Location:** Lines 191-196 (Feature card example)
```html
<!-- BEFORE - 8 units padding -->
<div class="feature-card bg-white rounded-lg shadow-md p-8 border-t-4 border-blue-600">
    ...
</div>

<!-- AFTER - 12 units padding -->
<div class="feature-card bg-white rounded-lg shadow-md p-12 border-t-4 border-blue-600">
    ...
</div>
```

**Available padding values:** `p-4`, `p-6`, `p-8`, `p-10`, `p-12`, `p-16`

---

#### Adjusting Section Spacing

**Location:** Lines 168, 250, etc. (Section padding)
```html
<!-- BEFORE - 16 units top/bottom, 24 on medium screens -->
<section class="py-16 md:py-24 bg-gray-50">
    ...
</section>

<!-- AFTER - 20 units top/bottom, 32 on medium screens -->
<section class="py-20 md:py-32 bg-gray-50">
    ...
</section>
```

**Available spacing values:** `py-8`, `py-12`, `py-16`, `py-20`, `py-24`, `py-32`

---

#### Adjusting Gap Between Grid Items

**Location:** Lines 187-189 (Feature cards grid)
```html
<!-- BEFORE - 8 units gap -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    ...
</div>

<!-- AFTER - 12 units gap -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-12">
    ...
</div>
```

---

### How to Modify Typography

#### Changing Headline Size

**Location:** Lines 145-147 (Hero headline)
```html
<!-- BEFORE - Responsive sizing -->
<h1 class="text-4xl sm:text-5xl md:text-6xl font-bold text-white...">
    Oakland Chiropractor for Seniors Balance, Fall Prevention and Wellbeing
</h1>

<!-- AFTER - Larger on all screens -->
<h1 class="text-5xl sm:text-6xl md:text-7xl font-bold text-white...">
    Oakland Chiropractor for Seniors Balance, Fall Prevention and Wellbeing
</h1>
```

**Text size options:** `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, `text-3xl`, `text-4xl`, `text-5xl`, `text-6xl`, `text-7xl`

---

#### Changing Font Weight

**Location:** Lines 145-147 (Hero headline)
```html
<!-- BEFORE - Bold -->
<h1 class="text-4xl sm:text-5xl md:text-6xl font-bold text-white...">
    ...
</h1>

<!-- AFTER - Extra bold (if available) or keep bold -->
<h1 class="text-4xl sm:text-5xl md:text-6xl font-black text-white...">
    ...
</h1>
```

**Font weight options:** `font-light`, `font-normal`, `font-medium`, `font-semibold`, `font-bold`, `font-black`

---

### How to Modify Shadows

#### Adding More Shadow to Cards

**Location:** Lines 191-196 (Feature card)
```html
<!-- BEFORE - Medium shadow -->
<div class="feature-card bg-white rounded-lg shadow-md p-8...">
    ...
</div>

<!-- AFTER - Large shadow -->
<div class="feature-card bg-white rounded-lg shadow-lg p-8...">
    ...
</div>
```

**Shadow options:** `shadow-sm`, `shadow`, `shadow-md`, `shadow-lg`, `shadow-xl`, `shadow-2xl`

---

### How to Modify Border Radius (Rounded Corners)

#### Making Corners More Rounded

**Location:** Lines 191-196 (Feature card)
```html
<!-- BEFORE - Large rounded corners -->
<div class="feature-card bg-white rounded-lg shadow-md p-8...">
    ...
</div>

<!-- AFTER - Extra large rounded corners -->
<div class="feature-card bg-white rounded-2xl shadow-md p-8...">
    ...
</div>
```

**Border radius options:** `rounded-none`, `rounded-sm`, `rounded`, `rounded-md`, `rounded-lg`, `rounded-xl`, `rounded-2xl`, `rounded-full`

---

### Color Palette Reference

**Available colors in Tailwind:**
- `gray-50` to `gray-900` (grays)
- `blue-50` to `blue-900` (blues)
- `green-50` to `green-900` (greens)
- `red-50` to `red-900` (reds)
- `purple-50` to `purple-900` (purples)
- `yellow-50` to `yellow-900` (yellows)
- `white` and `black`

**Color intensity:**
- Lower numbers (50, 100) = lighter
- Middle numbers (500, 600) = standard
- Higher numbers (800, 900) = darker

---

### Responsive Design Tips

#### Making Something Hidden on Mobile

```html
<!-- This will be hidden on small screens, visible on medium+ -->
<div class="hidden md:block">
    Content only visible on medium screens and larger
</div>
```

#### Making Text Larger on Desktop

```html
<!-- Small on mobile, larger on desktop -->
<p class="text-lg md:text-2xl lg:text-3xl">
    This text grows on larger screens
</p>
```

#### Changing Grid Columns Responsively

```html
<!-- 1 column on mobile, 2 on medium, 3 on large -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    ...
</div>
```

---

## Fixing Broken Links

### What are Links?
Links are clickable elements that take you to different pages or sections. In HTML, they look like:
```html
<a href="destination">Click Here</a>
```

The `href` attribute tells the browser where to go when clicked.

---

### Types of Links in This Page

#### 1. **Internal Links** (Within the same page)
These use `#` followed by a section ID:
```html
<a href="#home">Home</a>          <!-- Goes to section with id="home" -->
<a href="#features">Features</a>  <!-- Goes to section with id="features" -->
```

#### 2. **External Links** (Different websites)
These use full URLs:
```html
<a href="https://example.com">External Site</a>
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735">Schedule</a>
```

#### 3. **Email Links**
These use `mailto:`:
```html
<a href="mailto:email@example.com">Send Email</a>
```

---

### Navigation Menu Links

**Location:** Lines 97-104 (Desktop menu) and Lines 118-127 (Mobile menu)

These links should point to sections on the same page using the `#` symbol.

**Current structure:**
```html
<!-- Desktop Menu - Line ~97 -->
<a href="#home" class="text-gray-700...">Home</a>
<a href="#features" class="text-gray-700...">Features</a>
<a href="#benefits" class="text-gray-700...">Benefits</a>
<a href="#about" class="text-gray-700...">About</a>
<a href="#testimonials" class="text-gray-700...">Testimonials</a>
<a href="#faq" class="text-gray-700...">FAQ</a>
<a href="#contact" class="text-gray-700...">Contact</a>

<!-- Mobile Menu - Line ~118 -->
<!-- Same links repeated -->
```

**Verify these sections exist on the page:**
```html
<section id="home" ...>        <!-- Line ~135 ✓ -->
<section id="features" ...>    <!-- Line ~168 ✓ -->
<section id="benefits" ...>    <!-- Line ~250 ✓ -->
<section id="about" ...>       <!-- Line ~385 ✓ -->
<section id="testimonials" ... > <!-- Line ~425 ✓ -->
<section id="faq" ...>         <!-- Line ~505 ✓ -->
<section id="contact" ...>     <!-- Line ~580 ✓ -->
```

**If a navigation link is broken:**
1. Check that the section ID exists
2. Make sure the `href` matches the section `id` exactly (case-sensitive)
3. Both must use the `#` symbol

**Example - Adding a new section to navigation:**
```html
<!-- Step 1: Add link to menu -->
<a href="#blog" class="text-gray-700...">Blog</a>

<!-- Step 2: Create the section with matching ID -->
<section id="blog" class="py-16 md:py-24 bg-white">
    <!-- Blog content here -->
</section>
```

---

### Scheduling/CTA Links

**Locations:**
- Line ~153 (Hero button)
- Line ~577 (CTA section button)
- Line ~608 (Contact section)

These currently point to an Acuity Scheduling link:
```html
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" target="_blank" rel="noopener noreferrer">
    Schedule Your Appointment Today
</a>
```

**How to update this link:**

1. **Find all instances** - Use `Ctrl+F` to search for `app.acuityscheduling.com`
2. **Replace the URL** - Change the entire URL to your scheduling system
3. **Keep the attributes:**
   - `target="_blank"` - Opens in new tab
   - `rel="noopener noreferrer"` - Security measure

**Example - Changing to a different scheduling system:**
```html
<!-- BEFORE - Acuity Scheduling -->
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" target="_blank" rel="noopener noreferrer">
    Schedule Your Appointment Today
</a>

<!-- AFTER - Calendly -->
<a href="https://calendly.com/yourname" target="_blank" rel="noopener noreferrer">
    Schedule Your Appointment Today
</a>

<!-- AFTER - Your own website -->
<a href="https://yourwebsite.com/schedule" target="_blank" rel="noopener noreferrer">
    Schedule Your Appointment Today
</a>
```

---

### Email Links

**Locations:**
- Line ~596 (Contact section)
- Line ~705 (Footer)

Current email link:
```html
<a href="mailto:Theshiftchiropractic@gmail.com">
    Theshiftchiropractic@gmail.com
</a>
```

**How to update:**

1. **Find the email** - Search for `mailto:`
2. **Replace with your email:**

```html
<!-- BEFORE -->
<a href="mailto:Theshiftchiropractic@gmail.com">
    Theshiftchiropractic@gmail.com
</a>

<!-- AFTER -->
<a href="mailto:youremail@yourcompany.com">
    youremail@yourcompany.com
</a>
```

**Important:** Update the email address in TWO places:
1. In the `href` attribute (after `mailto:`)
2. In the visible text (between the tags)

---

### Social Media Links

**Location:** Lines 643-650 (Footer social icons)

Current placeholder links:
```html
<a href="#" class="text-gray-400 hover:text-blue-400...">
    <i class="fab fa-facebook..."></i>
</a>
```

**How to update:**

1. Find the social media section in the footer
2. Replace `href="#"` with your actual social media URLs

```html
<!-- BEFORE - Placeholder links -->
<a href="#" class="text-gray-400 hover:text-blue-400...">
    <i class="fab fa-facebook..."></i>
</a>
<a href="#" class="text-gray-400 hover:text-blue-400...">
    <i class="fab fa-twitter..."></i>
</a>
<a href="#" class="text-gray-400 hover:text-blue-400...">
    <i class="fab fa-instagram..."></i>
</a>
<a href="#" class="text-gray-400 hover:text-blue-400...">
    <i class="fab fa-youtube..."></i>
</a>

<!-- AFTER - Real social media links -->
<a href="https://www.facebook.com/yourpage" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-blue-400...">
    <i class="fab fa-facebook..."></i>
</a>
<a href="https://www.twitter.com/yourhandle" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-blue-400...">
    <i class="fab fa-twitter..."></i>
</a>
<a href="https://www.instagram.com/yourhandle" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-blue-400...">
    <i class="fab fa-instagram..."></i>
</a>
<a href="https://www.youtube.com/yourchannel" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-blue-400...">
    <i class="fab fa-youtube..."></i>
</a>
```

---

### Footer Link Updates

**Location:** Lines 652-680 (Footer navigation links)

The footer has several sections with links:
- Quick Links
- Services
- Contact
- Legal

**Quick Links section - Line ~654:**
```html
<li><a href="#home" class="text-gray-400...">Home</a></li>
<li><a href="#features" class="text-gray-400...">Features</a></li>
<!-- etc. -->
```

These should match your navigation menu links (all use `#` for internal sections).

**Services section - Line ~665:**
```html
<li><a href="#features" class="text-gray-400...">Chiropractic Senior Care</a></li>
<li><a href="#features" class="text-gray-400...">Fall Prevention</a></li>
<li><a href="#features" class="text-gray-400...">Adjusting</a></li>
<li><a href="blog.html" class="text-gray-400...">Blog</a></li>
```

**Note:** The blog link points to `blog.html` - see below for creating this page.

**Legal section - Line ~686:**
```html
<li><a href="privacy.html" class="text-gray-400...">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400...">Terms of Service</a></li>
```

These are covered in detail in the next section.

---

### Video Link

**Location:** Line ~240 (Video section)

Current embedded YouTube video:
```html
<iframe src="https://www.youtube.com/embed/iGSD988Rypg?si=s9MSvYmcdcO5rvsY" 
        allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
```

**How to change the video:**

1. Go to YouTube and find your video
2. Click "Share" → "Embed"
3. Copy the embed code
4. Replace the `src` URL in the iframe

```html
<!-- BEFORE - Old video -->
<iframe src="https://www.youtube.com/embed/iGSD988Rypg?si=s9MSvYmcdcO5rvsY" 
        allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>

<!-- AFTER - New video -->
<iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID" 
        allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
```

Replace `YOUR_VIDEO_ID` with the ID from your YouTube URL.

---

### Link Verification Checklist

Use this checklist to verify all links work:

- [ ] Navigation menu links (7 links) - go to correct sections
- [ ] Mobile menu links (7 links) - go to correct sections
- [ ] Hero CTA button - opens scheduling system
- [ ] CTA section button - opens scheduling system
- [ ] Contact section email - opens email client
- [ ] Contact section "Book an Appointment" - opens scheduling system
- [ ] Footer "Quick Links" - all go to correct sections
- [ ] Footer "Services" - all go to correct sections
- [ ] Footer social media - open correct profiles
- [ ] Footer legal links - link to privacy.html and terms.html
- [ ] Video embed - shows correct video

---

## Linking Privacy and Terms Pages

### Understanding the Structure

Your website currently has three files:
1. **index.html** - Main landing page (what we've been editing)
2. **privacy.html** - Privacy policy page (needs to be created)
3. **terms.html** - Terms of service page (needs to be created)

All three files should be in the same folder.

---

### Step 1: Create the Privacy Policy Page

#### Create a new file named `privacy.html`

**Steps:**
1. Open your text editor (Notepad, VS Code, Sublime Text)
2. Create a new file
3. Save it as `privacy.html` in the same folder as `index.html`

#### Add basic HTML structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - The Shift Oakland Chiropractor">
    <meta name="keywords" content="Privacy Policy, Oakland Chiropractor">
    <meta name="author" content="The Shift Oakland Chiropractor">
    <title>Privacy Policy | The Shift Oakland Chiropractor</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Navigation Header (copy from index.html) -->
    <header class="fixed top-0 left-0 right-0 bg-white shadow-md z-50">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <i class="fas fa-heartbeat text-2xl text-blue-600"></i>
                <a href="index.html" class="text-xl font-bold text-gray-900 hidden sm:inline">The Shift</a>
            </div>
            
            <div class="hidden md:flex items-center gap-8">
                <a href="index.html#home" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#benefits" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Benefits</a>
                <a href="index.html#about" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">About</a>
                <a href="index.html#contact" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Contact</a>
            </div>
            
            <button class="mobile-menu-button md:hidden text-gray-700 hover:text-blue-600 transition-colors duration-300" onclick="toggleMobileMenu()">
                <i class="fas fa-bars text-2xl"></i>
            </button>
        </nav>
        
        <div class="mobile-menu hidden md:hidden bg-white border-t border-gray-200 max-h-0 overflow-hidden transition-all duration-300">
            <div class="px-4 py-4 space-y-2">
                <a href="index.html#home" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#benefits" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Benefits</a>
                <a href="index.html#about" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">About</a>
                <a href="index.html#contact" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Contact</a>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="pt-24">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-600 space-y-6">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Introduction</h2>
                    <p>
                        The Shift Oakland Chiropractor ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Information We Collect</h2>
                    <p>
                        We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                    </p>
                    <ul class="list-disc pl-6 space-y-2">
                        <li>Personal Data: Personally identifiable information, such as your name, shipping address, email address, and telephone number, that you voluntarily give to us when you choose to participate in various activities related to the Site.</li>
                        <li>Financial Data: Financial information, such as data related to your payment method (e.g., valid credit card number, card brand, expiration date) that we may collect when you purchase, order, return, exchange, or request information about our services from the Site.</li>
                        <li>Data From Social Networks: User information from social networks, including your name, your social network username, location, gender, birth date, email address, profile picture, and public data for contacts, if you connect your account to such social networks.</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Use of Your Information</h2>
                    <p>
                        Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:
                    </p>
                    <ul class="list-disc pl-6 space-y-2">
                        <li>Process your transactions and send related information.</li>
                        <li>Email regarding your account or order.</li>
                        <li>Fulfill and manage purchases, orders, payments, and other transactions related to the Site.</li>
                        <li>Generate a personal profile about you so that future visits to the Site will be personalized as possible.</li>
                        <li>Increase the efficiency and operation of the Site.</li>
                        <li>Monitor and analyze usage and trends to improve your experience with the Site.</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Disclosure of Your Information</h2>
                    <p>
                        We may share information we have collected about you in certain situations:
                    </p>
                    <ul class="list-disc pl-6 space-y-2">
                        <li><strong>By Law or to Protect Rights:</strong> If we believe the release of information about you is necessary to comply with the law.</li>
                        <li><strong>Third-Party Service Providers:</strong> We may share your information with parties who perform services for us, including payment processing, data analysis, email delivery, hosting services, customer service, and marketing assistance.</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Security of Your Information</h2>
                    <p>
                        We use administrative, technical, and physical security measures to protect your personal information. However, perfect security does not exist online.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Contact Us</h2>
                    <p>
                        If you have questions or comments about this Privacy Policy, please contact us at:
                    </p>
                    <p>
                        <strong>The Shift Oakland Chiropractor</strong><br>
                        Email: <a href="mailto:Theshiftchiropractic@gmail.com" class="text-blue-600 hover:text-blue-700">Theshiftchiropractic@gmail.com</a><br>
                        Location: Oakland, California
                    </p>
                </section>

                <section>
                    <p class="text-sm text-gray-500">
                        Last updated: <span id="lastUpdated"></span>
                    </p>
                </section>
            </div>
        </div>
    </main>

    <!-- Footer (copy from index.html and update links) -->
    <footer class="bg-gray-900 text-gray-300 py-12 md:py-16 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8 mb-8">
                <div>
                    <div class="flex items-center gap-2 mb-4">
                        <i class="fas fa-heartbeat text-2xl text-blue-400"></i>
                        <span class="text-lg font-bold text-white">The Shift</span>
                    </div>
                    <p class="text-sm leading-relaxed mb-4">
                        Specialized chiropractic care for seniors in Oakland, focusing on balance, fall prevention, and overall wellness.
                    </p>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-4">Quick Links</h4>
                    <ul class="space-y-2 text-sm">
                        <li><a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Home</a></li>
                        <li><a href="index.html#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Benefits</a></li>
                        <li><a href="index.html#about" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">About Us</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-4">Legal</h4>
                    <ul class="space-y-2 text-sm">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-4">Contact</h4>
                    <ul class="space-y-2 text-sm">
                        <li class="flex items-start gap-2">
                            <i class="fas fa-envelope text-blue-400 mt-1 flex-shrink-0"></i>
                            <a href="mailto:Theshiftchiropractic@gmail.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Theshiftchiropractic@gmail.com</a>
                        </li>
                        <li class="flex items-start gap-2">
                            <i class="fas fa-map-marker-alt text-blue-400 mt-1 flex-shrink-0"></i>
                            <span class="text-gray-400">Oakland, California</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 pt-8">
                <div class="flex flex-col md:flex-row items-center justify-between">
                    <p class="text-sm text-gray-400 mb-4 md:mb-0">
                        &copy; <span id="year"></span> The Shift Oakland Chiropractor. All rights reserved.
                    </p>
                    <p class="text-sm text-gray-400">
                        Providing quality senior chiropractic care in Oakland, California.
                    </p>
                </div>
            </div>
        </div>
    </footer>

    <script>
        function toggleMobileMenu() {
            const menu = document.querySelector('.mobile-menu');
            const button = document.querySelector('.mobile-menu-button');
            
            menu.classList.toggle('active');
            if (menu.classList.contains('active')) {
                menu.style.maxHeight = '500px';
            } else {
                menu.style.maxHeight = '0';
            }
        }
        
        document.querySelectorAll('.mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                const menu = document.querySelector('.mobile-menu');
                menu.classList.remove('active');
                menu.style.maxHeight = '0';
            });
        });
        
        document.getElementById('year').textContent = new Date().getFullYear();
        document.getElementById('lastUpdated').textContent = new Date().toLocaleDateString();
    </script>
</body>
</html>
```

---

### Step 2: Create the Terms of Service Page

#### Create a new file named `terms.html`

Follow the same process as above, but save it as `terms.html`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - The Shift Oakland Chiropractor">
    <meta name="keywords" content="Terms of Service, Oakland Chiropractor">
    <meta name="author" content="The Shift Oakland Chiropractor">
    <title>Terms of Service | The Shift Oakland Chiropractor</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Navigation Header -->
    <header class="fixed top-0 left-0 right-0 bg-white shadow-md z-50">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <i class="fas fa-heartbeat text-2xl text-blue-600"></i>
                <a href="index.html" class="text-xl font-bold text-gray-900 hidden sm:inline">The Shift</a>
            </div>
            
            <div class="hidden md:flex items-center gap-8">
                <a href="index.html#home" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#benefits" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Benefits</a>
                <a href="index.html#about" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">About</a>
                <a href="index.html#contact" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Contact</a>
            </div>
            
            <button class="mobile-menu-button md:hidden text-gray-700 hover:text-blue-600 transition-colors duration-300" onclick="toggleMobileMenu()">
                <i class="fas fa-bars text-2xl"></i>
            </button>
        </nav>
        
        <div class="mobile-menu hidden md:hidden bg-white border-t border-gray-200 max-h-0 overflow-hidden transition-all duration-300">
            <div class="px-4 py-4 space-y-2">
                <a href="index.html#home" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#benefits" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Benefits</a>
                <a href="index.html#about" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">About</a>
                <a href="index.html#contact" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Contact</a>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="pt-24">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none text-gray-600 space-y-6">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Agreement to Terms</h2>
                    <p>
                        These Terms of Service constitute a legally binding agreement made between you, whether personally or on behalf of an entity ("you") and The Shift Oakland Chiropractor ("we," "us," "our," or "Company"), concerning your access to and use of the website as well as any other media form, media channel, mobile website, or mobile application relating, linked, or otherwise connected thereto (collectively, the "Site").
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Intellectual Property Rights</h2>
                    <p>
                        Unless otherwise indicated, the Site is our proprietary property and all source code, databases, functionality, software, website designs, audio, video, text, photographs, and graphics on the Site (collectively, the "Content") and the trademarks, service marks, and logos contained therein (the "Marks") are owned or controlled by us or licensed to us, and are protected by copyright and trademark laws.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">User Representations</h2>
                    <p>
                        By using the Site, you represent and warrant that:
                    </p>
                    <ul class="list-disc pl-6 space-y-2">
                        <li>All registration information you submit is true, accurate, current, and complete.</li>
                        <li>You will maintain the accuracy of such information and promptly update such registration information as necessary.</li>
                        <li>You have the legal capacity and you agree to comply with these Terms of Service.</li>
                        <li>You are not a minor in the jurisdiction in which you reside, or if a minor, you have received parental permission to use the Site.</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">User Prohibited Behavior</h2>
                    <p>
                        You may not access or use the Site for any purpose other than that for which we make the Site available. The Site may not be used in connection with any commercial endeavors except those specifically endorsed or approved by us.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Disclaimer of Warranties</h2>
                    <p>
                        The Site is provided on an "as-is" and "as-available" basis. We make no warranties, expressed or implied, regarding the Site. To the fullest extent permissible pursuant to applicable law, we disclaim all warranties, express or implied, including, but not limited to, implied warranties of merchantability and fitness for a particular purpose.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Limitation of Liability</h2>
                    <p>
                        In no event shall the Company or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on the Site.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Governing Law</h2>
                    <p>
                        These Terms of Service and your use of the Site are governed by and construed in accordance with the laws of the State of California, United States, without regard to its conflict of law principles, and any disputes related to the Site will be resolved in the state and federal courts located in California.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">Contact Information</h2>
                    <p>
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p>
                        <strong>The Shift Oakland Chiropractor</strong><br>
                        Email: <a href="mailto:Theshiftchiropractic@gmail.com" class="text-blue-600 hover:text-blue-700">Theshiftchiropractic@gmail.com</a><br>
                        Location: Oakland, California
                    </p>
                </section>

                <section>
                    <p class="text-sm text-gray-500">
                        Last updated: <span id="lastUpdated"></span>
                    </p>
                </section>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12 md:py-16 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8 mb-8">
                <div>
                    <div class="flex items-center gap-2 mb-4">
                        <i class="fas fa-heartbeat text-2xl text-blue-400"></i>
                        <span class="text-lg font-bold text-white">The Shift</span>
                    </div>
                    <p class="text-sm leading-relaxed mb-4">
                        Specialized chiropractic care for seniors in Oakland, focusing on balance, fall prevention, and overall wellness.
                    </p>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-4">Quick Links</h4>
                    <ul class="space-y-2 text-sm">
                        <li><a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Home</a></li>
                        <li><a href="index.html#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Benefits</a></li>
                        <li><a href="index.html#about" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">About Us</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-4">Legal</h4>
                    <ul class="space-y-2 text-sm">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-4">Contact</h4>
                    <ul class="space-y-2 text-sm">
                        <li class="flex items-start gap-2">
                            <i class="fas fa-envelope text-blue-400 mt-1 flex-shrink-0"></i>
                            <a href="mailto:Theshiftchiropractic@gmail.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Theshiftchiropractic@gmail.com</a>
                        </li>
                        <li class="flex items-start gap-2">
                            <i class="fas fa-map-marker-alt text-blue-400 mt-1 flex-shrink-0"></i>
                            <span class="text-gray-400">Oakland, California</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 pt-8">
                <div class="flex flex-col md:flex-row items-center justify-between">
                    <p class="text-sm text-gray-400 mb-4 md:mb-0">
                        &copy; <span id="year"></span> The Shift Oakland Chiropractor. All rights reserved.
                    </p>
                    <p class="text-sm text-gray-400">
                        Providing quality senior chiropractic care in Oakland, California.
                    </p>
                </div>
            </div>
        </div>
    </footer>

    <script>
        function toggleMobileMenu() {
            const menu = document.querySelector('.mobile-menu');
            const button = document.querySelector('.mobile-menu-button');
            
            menu.classList.toggle('active');
            if (menu.classList.contains('active')) {
                menu.style.maxHeight = '500px';
            } else {
                menu.style.maxHeight = '0';
            }
        }
        
        document.querySelectorAll('.mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                const menu = document.querySelector('.mobile-menu');
                menu.classList.remove('active');
                menu.style.maxHeight = '0';
            });
        });
        
        document.getElementById('year').textContent = new Date().getFullYear();
        document.getElementById('lastUpdated').textContent = new Date().toLocaleDateString();
    </script>
</body>
</html>
```

---

### Step 3: Update Links in index.html

Now that you've created the privacy and terms pages, you need to make sure the links in `index.html` point to them correctly.

#### Verify Footer Links (Lines 694-695)

```html
<!-- Line ~694 in index.html -->
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

**These should already be correct in the provided HTML!** ✓

No changes needed - the links are already set up to point to `privacy.html` and `terms.html`.

---

### File Structure After Setup

Your website folder should now contain:

```
your-website-folder/
├── index.html          (main landing page)
├── privacy.html        (privacy policy)
├── terms.html          (terms of service)
└── (optional) blog.html (if you want to create a blog page)
```

---

### Testing the Links

After creating the new files:

1. **Test from index.html:**
   - Scroll to the footer
   - Click "Privacy Policy" - should open privacy.html
   - Click "Terms of Service" - should open terms.html

2. **Test from privacy.html:**
   - Click the logo or navigation links - should return to index.html
   - Click "Terms of Service" - should open terms.html

3. **Test from terms.html:**
   - Click the logo or navigation links - should return to index.html
   - Click "Privacy Policy" - should open privacy.html

---

### Optional: Create a Blog Page

If you want to add a blog page (referenced in the footer), create a file named `blog.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Blog - The Shift Oakland Chiropractor">
    <meta name="keywords" content="Blog, Chiropractic Tips, Oakland">
    <meta name="author" content="The Shift Oakland Chiropractor">
    <title>Blog | The Shift Oakland Chiropractor</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Navigation Header (same as privacy.html) -->
    <header class="fixed top-0 left-0 right-0 bg-white shadow-md z-50">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <i class="fas fa-heartbeat text-2xl text-blue-600"></i>
                <a href="index.html" class="text-xl font-bold text-gray-900 hidden sm:inline">The Shift</a>
            </div>
            
            <div class="hidden md:flex items-center gap-8">
                <a href="index.html#home" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#benefits" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Benefits</a>
                <a href="index.html#about" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">About</a>
                <a href="blog.html" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Blog</a>
                <a href="index.html#contact" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Contact</a>
            </div>
            
            <button class="mobile-menu-button md:hidden text-gray-700 hover:text-blue-600 transition-colors duration-300" onclick="toggleMobileMenu()">
                <i class="fas fa-bars text-2xl"></i>
            </button>
        </nav>
        
        <div class="mobile-menu hidden md:hidden bg-white border-t border-gray-200 max-h-0 overflow-hidden transition-all duration-300">
            <div class="px-4 py-4 space-y-2">
                <a href="index.html#home" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#benefits" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Benefits</a>
                <a href="index.html#about" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">About</a>
                <a href="blog.html" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Blog</a>
                <a href="index.html#contact" class="block px-4 py-2 text-gray-700 hover:bg-blue-50 hover:text-blue-600 rounded-md transition-colors duration-300 font-medium">Contact</a>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="pt-24">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">Blog</h1>
            <p class="text-xl text-gray-600 mb-12">Tips, insights, and information for senior wellness</p>
            
            <div class="space-y-12">
                <!-- Blog Post 1 -->
                <article class="border-b border-gray-200 pb-12">
                    <h2 class="text-3xl font-bold text-gray-900 mb-2">
                        <a href="#" class="hover:text-blue-600 transition-colors duration-300">5 Fall Prevention Tips for Active Seniors</a>
                    </h2>
                    <p class="text-gray-600 mb-4">
                        <i class="fas fa-calendar mr-2"></i>
                        <span id="date1"></span>
                    </p>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Falls are a serious concern for seniors, but they're often preventable. In this post, we share five practical tips that can help you maintain your independence and reduce your fall risk. From improving your home environment to strengthening your core muscles, these strategies can make a real difference in your daily life...
                    </p>
                    <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold">Read More →</a>
                </article>

                <!-- Blog Post 2 -->
                <article class="border-b border-gray-200 pb-12">
                    <h2 class="text-3xl font-bold text-gray-900 mb-2">
                        <a href="#" class="hover:text-blue-600 transition-colors duration-300">The Benefits of Regular Chiropractic Care for Arthritis</a>
                    </h2>
                    <p class="text-gray-600 mb-4">
                        <i class="fas fa-calendar mr-2"></i>
                        <span id="date2"></span>
                    </p>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Arthritis affects millions of seniors, causing pain and limiting mobility. Discover how regular chiropractic adjustments can help reduce arthritis symptoms and improve your quality of life. Our specialists explain the science behind spinal alignment and its impact on joint health...
                    </p>
                    <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold">Read More →</a>
                </article>

                <!-- Blog Post 3 -->
                <article class="pb-12">
                    <h2 class="text-3xl font-bold text-gray-900 mb-2">
                        <a href="#" class="hover:text-blue-600 transition-colors duration-300">Balance Exercises You Can Do at Home</a>
                    </h2>
                    <p class="text-gray-600 mb-4">
                        <i class="fas fa-calendar mr-2"></i>
                        <span id="date3"></span>
                    </p>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Improving your balance doesn't require expensive equipment or a gym membership. Learn simple, effective exercises that you can do in the comfort of your own home. These exercises are designed specifically for seniors and can be modified to match your current fitness level...
                    </p>
                    <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold">Read More →</a>
                </article>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12 md:py-16 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8 mb-8">
                <div>
                    <div class="flex items-center gap-2 mb-4">
                        <i class="fas fa-heartbeat text-2xl text-blue-400"></i>
                        <span class="text-lg font-bold text-white">The Shift</span>
                    </div>
                    <p class="text-sm leading-relaxed mb-4">
                        Specialized chiropractic care for seniors in Oakland, focusing on balance, fall prevention, and overall wellness.
                    </p>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-4">Quick Links</h4>
                    <ul class="space-y-2 text-sm">
                        <li><a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Home</a></li>
                        <li><a href="index.html#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Benefits</a></li>
                        <li><a href="blog.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Blog</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-4">Legal</h4>
                    <ul class="space-y-2 text-sm">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-4">Contact</h4>
                    <ul class="space-y-2 text-sm">
                        <li class="flex items-start gap-2">
                            <i class="fas fa-envelope text-blue-400 mt-1 flex-shrink-0"></i>
                            <a href="mailto:Theshiftchiropractic@gmail.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Theshiftchiropractic@gmail.com</a>
                        </li>
                        <li class="flex items-start gap-2">
                            <i class="fas fa-map-marker-alt text-blue-400 mt-1 flex-shrink-0"></i>
                            <span class="text-gray-400">Oakland, California</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 pt-8">
                <div class="flex flex-col md:flex-row items-center justify-between">
                    <p class="text-sm text-gray-400 mb-4 md:mb-0">
                        &copy; <span id="year"></span> The Shift Oakland Chiropractor. All rights reserved.
                    </p>
                    <p class="text-sm text-gray-400">
                        Providing quality senior chiropractic care in Oakland, California.
                    </p>
                </div>
            </div>
        </div>
    </footer>

    <script>
        function toggleMobileMenu() {
            const menu = document.querySelector('.mobile-menu');
            const button = document.querySelector('.mobile-menu-button');
            
            menu.classList.toggle('active');
            if (menu.classList.contains('active')) {
                menu.style.maxHeight = '500px';
            } else {
                menu.style.maxHeight = '0';
            }
        }
        
        document.querySelectorAll('.mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                const menu = document.querySelector('.mobile-menu');
                menu.classList.remove('active');
                menu.style.maxHeight = '0';
            });
        });
        
        document.getElementById('year').textContent = new Date().getFullYear();
        
        // Set blog post dates (adjust as needed)
        const today = new Date();
        const date1 = new Date(today.getTime() - 7 * 24 * 60 * 60 * 1000); // 7 days ago
        const date2 = new Date(today.getTime() - 14 * 24 * 60 * 60 * 1000); // 14 days ago
        const date3 = new Date(today.getTime() - 21 * 24 * 60 * 60 * 1000); // 21 days ago
        
        document.getElementById('date1').textContent = date1.toLocaleDateString();
        document.getElementById('date2').textContent = date2.toLocaleDateString();
        document.getElementById('date3').textContent = date3.toLocaleDateString();
    </script>
</body>
</html>
```

---

## Troubleshooting

### Common Issues and Solutions

#### Issue 1: Links Not Working

**Problem:** Clicking a link does nothing or shows a 404 error.

**Solutions:**
1. **Check file names** - Make sure file names match exactly (case-sensitive on some servers):
   - `privacy.html` (not `Privacy.html`)
   - `terms.html` (not `Terms.html`)

2. **Check href attributes** - Make sure the `href` value matches the file name:
   ```html
   <!-- Correct -->
   <a href="privacy.html">Privacy</a>
   
   <!-- Incorrect -->
   <a href="Privacy.html">Privacy</a>  <!-- Wrong capitalization -->
   <a href="privacy">Privacy</a>        <!-- Missing .html extension -->
   <a href="./privacy.html">Privacy</a> <!-- Unnecessary ./ prefix -->
   ```

3. **Check file location** - All files must be in the same folder:
   ```
   ✓ Correct structure:
   your-website/
   ├── index.html
   ├── privacy.html
   └── terms.html
   
   ✗ Incorrect structure:
   your-website/
   ├── index.html
   └── pages/
       ├── privacy.html
       └── terms.html
   ```

4. **Clear browser cache** - Sometimes browsers cache old versions:
   - Press `Ctrl+Shift+Delete` (Windows) or `Cmd+Shift+Delete` (Mac)
   - Select "All time"
   - Click "Clear data"

---

#### Issue 2: Styling Not Applied to New Pages

**Problem:** New pages (privacy.html, terms.html) don't have the same styling as index.html.

**Solution:**
Make sure you included the Tailwind CSS link in the `<head>` section:
```html
<head>
    <!-- ... other meta tags ... -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
```

Both CDN links must be present for styling and icons to work.

---

#### Issue 3: Mobile Menu Not Working on New Pages

**Problem:** Mobile menu doesn't toggle on new pages.

**Solution:**
Make sure the JavaScript function is included in the `<script>` section at the bottom:
```html
<script>
    function toggleMobileMenu() {
        const menu = document.querySelector('.mobile-menu');
        const button = document.querySelector('.mobile-menu-button');
        
        menu.classList.toggle('active');
        if (menu.classList.contains('active')) {
            menu.style.maxHeight = '500px';
        } else {
            menu.style.maxHeight = '0';
        }
    }
    
    document.querySelectorAll('.mobile-menu a').forEach(link => {
        link.addEventListener('click', () => {
            const menu = document.querySelector('.mobile-menu');
            menu.classList.remove('active');
            menu.style.maxHeight = '0';
        });
    });
</script>
```

---

#### Issue 4: Text Not Updating

**Problem:** You changed text in the HTML file, but it doesn't appear on the website.

**Solutions:**
1. **Save the file** - Make sure you saved after making changes (`Ctrl+S` or `Cmd+S`)
2. **Clear browser cache** - Browser may be showing old version
3. **Check file location** - Make sure you edited the right file
4. **Reload the page** - Press `F5` or `Ctrl+R` to refresh

---

#### Issue 5: Colors Not Changing

**Problem:** You changed Tailwind CSS classes, but colors didn't update.

**Solution:**
Make sure you're using valid Tailwind colors:
```html
<!-- Valid -->
<div class="bg-blue-600">Blue background</div>
<div class="text-gray-900">Dark gray text</div>

<!-- Invalid -->
<div class="bg-blue">This color doesn't exist</div>
<div class="text-dark-gray">This class doesn't exist</div>
```

Valid color options: `50`, `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900`

---

#### Issue 6: Navigation Links Not Scrolling to Sections

**Problem:** Clicking navigation links doesn't scroll to the correct section.

**Solution:**
Make sure the section ID matches the link href:
```html
<!-- Navigation link -->
<a href="#benefits">Benefits</a>

<!-- Corresponding section - must have matching id -->
<section id="benefits" ...>
    Content here
</section>

<!-- This won't work - mismatched names -->
<a href="#benefits">Benefits</a>
<section id="benefit" ...>  <!-- Wrong ID name -->
```

---

#### Issue 7: Responsive Design Not Working

**Problem:** Page doesn't look right on mobile or tablet.

**Solution:**
Check that the viewport meta tag is in the `<head>`:
```html
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Other meta tags -->
</head>
```

This tells browsers how to handle different screen sizes.

---

## Best Practices

### 1. **Always Backup Your Files**
Before making major changes, create a backup:
- Copy your files to a safe location
- Use version control (Git) if possible
- Name backups with dates: `index_backup_2024-01-15.html`

---

### 2. **Make One Change at a Time**
When modifying the website:
1. Make one small change
2. Save the file
3. Test the change in your browser
4. If it works, move to the next change
5. If it breaks, undo and try a different approach

This makes it easier to find and fix problems.

---

### 3. **Use Comments for Important Notes**
Add HTML comments to mark important sections:
```html
<!-- UPDATE: Contact information - Last updated Jan 2024 -->
<a href="mailto:Theshiftchiropractic@gmail.com">Email</a>

<!-- TODO: Add new testimonial from John Smith -->
<!-- <div class="testimonial-card">...</div> -->
```

---

### 4. **Test All Links Regularly**
Create a checklist and test links monthly:
- [ ] All navigation links work
- [ ] CTA buttons open scheduling system
- [ ] Email links work
- [ ] Social media links are correct
- [ ] Privacy and terms pages are accessible

---

### 5. **Keep Consistent Styling**
When adding new content, match existing styles:
- Use the same color scheme
- Match heading sizes
- Keep spacing consistent
- Use the same card styling

**Example:**
```html
<!-- Matches existing feature cards -->
<div class="feature-card bg-white rounded-lg shadow-md p-8 border-t-4 border-blue-600">
    <div class="flex items-center justify-center w-16 h-16 bg-blue-100 rounded-full mb-6">
        <i class="fas fa-icon text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-3">Title</h3>
    <p class="text-gray-600 leading-relaxed">Description</p>
</div>
```

---

### 6. **Update Content Seasonally**
Keep your website fresh:
- Update testimonials quarterly
- Refresh blog posts monthly
- Update seasonal promotions
- Keep contact information current
- Review and update service descriptions

---

### 7. **Monitor Performance**
Regularly check website performance:
- Test on different browsers (Chrome, Firefox, Safari, Edge)
- Test on different devices (mobile, tablet, desktop)
- Check page load speed
- Verify all images load correctly

---

### 8. **Use Descriptive File Names**
When creating new pages, use clear names:
```
✓ Good names:
- privacy.html
- terms.html
- blog.html
- services.html

✗ Poor names:
- page1.html
- new.html
- temp.html
- test123.html
```

---

### 9. **Document Your Changes**
Keep a changelog of updates:
```
=== Website Updates ===

2024-01-15:
- Updated email address to newemail@company.com
- Added new testimonial from Sarah Johnson
- Changed CTA button color to green

2024-01-08:
- Created privacy.html and terms.html pages
- Updated social media links in footer
```

---

### 10. **Security Tips**
Protect your website:
- Don't share sensitive information in code comments
- Use strong passwords for any admin panels
- Keep backups in a secure location
- Be careful with email addresses (consider using contact forms instead)
- Regularly update any plugins or extensions

---

## Quick Reference Guide

### File Locations for Common Updates

| Item | File | Line Range | Search Term |
|------|------|-----------|------------|
| Business Name | All files | Various | "The Shift" |
| Email Address | index.html, privacy.html, terms.html | Multiple | "Theshiftchiropractic@gmail.com" |
| Scheduling Link | index.html | 153, 577, 608 | "app.acuityscheduling.com" |
| Navigation Menu | index.html | 97-127 | "href=#" |
| Hero Headline | index.html | 145 | "Oakland Chiropractor" |
| Features Section | index.html | 184-220 | "Specialized Services" |
| Contact Section | index.html | 580-620 | "Get in Touch" |
| Footer Links | index.html | 652-710 | "Quick Links" |

---

### Tailwind CSS Quick Reference

```html
<!-- Text Colors -->
text-white, text-gray-900, text-gray-600, text-blue-600, text-green-500

<!-- Background Colors -->
bg-white, bg-gray-50, bg-gray-900, bg-blue-600, bg-green-100

<!-- Spacing (padding) -->
p-4, p-6, p-8, p-12  (all sides)
px-4, px-8           (left & right)
py-4, py-8           (top & bottom)

<!-- Spacing (margin) -->
mb-4, mb-6, mb-8     (margin bottom)
mt-4, mt-8           (margin top)
mx-auto              (center horizontally)

<!-- Text Size -->
text-sm, text-base, text-lg, text-xl, text-2xl, text-3xl, text-4xl, text-5xl, text-6xl

<!-- Font Weight -->
font-light, font-normal, font-medium, font-semibold, font-bold

<!-- Borders & Shadows -->
rounded-lg, rounded-xl, rounded-2xl    (rounded corners)
shadow-md, shadow-lg, shadow-xl        (shadows)
border-t-4 border-blue-600             (top border)

<!-- Responsive -->
hidden, md:flex      (hidden on small, visible on medium+)
text-lg md:text-2xl  (text size changes on medium screens)
grid-cols-1 md:grid-cols-2 lg:grid-cols-3  (columns change per screen size)
```

---

## Conclusion

You now have a comprehensive guide for maintaining and customizing your landing page. Remember:

1. **Update text content** by finding and replacing text between HTML tags
2. **Modify styles** by changing Tailwind CSS class names
3. **Fix broken links** by ensuring href attributes match file names and section IDs
4. **Create additional pages** like privacy.html and terms.html using the provided templates
5. **Always test changes** before considering them final
6. **Keep backups** of your files
7. **Document updates** for future reference

If you have questions about specific changes, refer back to the relevant sections in this guide. Happy maintaining! 🎉