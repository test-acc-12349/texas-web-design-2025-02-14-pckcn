# Texas Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this line in the header -->
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
- Replace "TWD" with your desired logo text
- Adjust size using text-2xl (can be text-xl for smaller or text-3xl for larger)

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Replace text between `>` and `</a>` for each menu item
- Keep the `href` attributes matching section IDs

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```
- Update heading and subheading text as needed
- Maintain responsive classes (md: and lg: prefixes)

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <!-- Icon container -->
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included with every website package...</p>
</div>
```
To modify:
1. Update heading text between `<h3>` tags
2. Change description text between `<p>` tags
3. Keep all Tailwind classes for consistent styling

## Managing Links

### External Links
Current placeholder links to update:
```html
<!-- Main CTA button -->
<a href="https://twd.com" class="px-6 py-2 bg-blue-600 text-white rounded-full">Get Started</a>

<!-- Contact email -->
<a href="mailto:admin@twd.com" class="px-8 py-4 bg-white text-blue-600 rounded-full">Contact Us</a>
```
To update:
1. Replace `https://twd.com` with your actual website URL
2. Update `admin@twd.com` with your contact email

### Internal Navigation
```html
<!-- Navigation menu links -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
These links correspond to section IDs. When updating:
1. Ensure section IDs match exactly (case-sensitive)
2. Keep the `#` prefix for smooth scrolling
3. Update both the link text and href attribute if changing section names

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Add these new lines -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Use the same header and footer as index.html
3. Add your policy content between `<main>` tags
4. Maintain consistent styling using Tailwind classes

## Troubleshooting

Common Issues:
1. **Broken Internal Links**
   - Check that section IDs exactly match href attributes
   - IDs must be unique across the page
   - Remove any spaces in IDs

2. **Responsive Design Issues**
   - Don't remove md: or lg: prefixes from classes
   - Test on multiple screen sizes
   - Keep the viewport meta tag in header

3. **Styling Inconsistencies**
   - Copy exact class strings when duplicating elements
   - Maintain the same color schemes (blue-600, gray-400, etc.)
   - Keep hover states (hover:) for interactive elements

Need help? Contact support at [support email]

---
Remember to:
- Test all changes in multiple browsers
- Validate links before deploying
- Keep backups of working versions
- Maintain consistent branding throughout