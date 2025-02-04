# EarwigFacts Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the EarwigFacts landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the site logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header section -->
<a href="#" class="text-xl font-bold text-white hover:text-blue-400 transition duration-300">
    EarwigFacts
</a>
```
Simply replace "EarwigFacts" with your desired text.

### Hero Section
The main headline and subheading can be modified here:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-6 bg-gradient-to-r from-blue-400 to-teal-400 bg-clip-text text-transparent">
    How to Get Rid of Earwigs
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    No More Earwigs – Take Control of Your Home Today
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout the page:
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-[size]`: Adds margin bottom (4, 6, 8, etc.)
- `bg-[color]-[shade]`: Sets background color (gray-900, blue-500, etc.)
- `hover:`: Prefix for hover effects
- `md:`: Prefix for medium screen sizes
- `lg:`: Prefix for large screen sizes

Example of modifying a feature card:
```html
<!-- Original -->
<div class="bg-gray-700 rounded-xl p-8 hover:bg-gray-600">
<!-- To change colors -->
<div class="bg-blue-700 rounded-xl p-8 hover:bg-blue-600">
```

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the link text

Example:
```html
<!-- From -->
<a href="#features">Features</a>
<!-- To -->
<a href="/new-page.html">New Page</a>
```

### Call-to-Action (CTA) Links
The main CTA buttons currently point to "https://earwigfacts.com":
```html
<a href="https://earwigfacts.com" class="inline-block bg-blue-500 hover:bg-blue-600...">
```

To update:
1. Locate the CTA button in the hero and CTA sections
2. Replace the href value with your desired URL
3. Update the button text if needed

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the legal section in the footer:
```html
<div class="space-y-4">
    <h4 class="text-lg font-semibold">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create privacy.html and terms.html files in your project directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in href attributes
   - Ensure linked files exist in the correct directory
   - Verify file names match exactly (case-sensitive)

2. **Styling Problems**
   - Confirm Tailwind CSS is properly loaded
   - Check for missing or mistyped class names
   - Verify responsive classes (md:, lg:) are working

3. **Layout Issues**
   - Inspect container widths and padding
   - Check for proper nesting of elements
   - Verify responsive breakpoints are working

### Need Help?
If you encounter issues:
1. Use browser developer tools (F12) to inspect elements
2. Check the console for error messages
3. Verify all CDN links are accessible
4. Test the page across different devices and browsers

Remember to always backup your files before making changes, and test modifications in a development environment first.