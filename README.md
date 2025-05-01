# Landing Page Maintenance Guide

This guide will help you maintain and customize the WebAgency landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Modifying Text Content

#### Hero Section
The main headline and subtext are located in the hero section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Best Web Agency In Sydney  <!-- Edit this text -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Grow your business with clicks  <!-- Edit this text -->
</p>
```

#### Features Section
Each feature card contains a title and description:
```html
<h3 class="text-xl font-semibold mb-4">Easy to Use</h3>  <!-- Edit title -->
<p class="text-gray-400">Intuitive interfaces and...</p>  <!-- Edit description -->
```

### Understanding Tailwind Classes

Key class patterns used throughout the page:

1. Text Sizing:
   - `text-4xl`: Large text
   - `md:text-5xl`: Larger text on medium screens
   - `lg:text-6xl`: Largest text on large screens

2. Spacing:
   - `mb-8`: Bottom margin
   - `py-24`: Vertical padding
   - `px-6`: Horizontal padding

3. Colors:
   - `bg-gray-900`: Dark background
   - `text-gray-100`: Light text
   - `text-blue-500`: Blue accent color

To modify a style, locate the relevant class and replace it with another Tailwind class. For example:
```html
<!-- Original -->
<div class="bg-gray-900">

<!-- Modified to lighter gray -->
<div class="bg-gray-800">
```

## Fixing Broken Links

### Navigation Menu Links
The main navigation is in the header section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace `#section-name` with your desired link
3. For external links, use complete URLs (e.g., `https://example.com`)
4. For internal links, use `#section-id` matching the section's ID attribute

### Call-to-Action Links
Current CTA buttons point to "https://fixrr.online". Update these links:
```html
<!-- Example CTA button -->
<a href="https://fixrr.online" class="inline-block px-8 py-4 bg-blue-600...">
    Start Growing Today
</a>
```

## Linking Privacy and Terms Pages

### Footer Legal Links
Located in the footer section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   - Verify that sections have unique IDs

2. **Responsive Design Issues**
   - Check media query classes (md:, lg:)
   - Test on different screen sizes
   - Verify Tailwind CDN is loading

3. **Animation Problems**
   - Confirm AOS script is loaded
   - Check data-aos attributes
   - Verify AOS initialization in script section

### Best Practices

1. Always test changes in multiple browsers
2. Maintain consistent spacing using Tailwind classes
3. Keep brand colors consistent throughout
4. Ensure all links are working before deploying
5. Back up files before making significant changes

Need additional help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).