# Alphington Landing Page Maintenance Guide

This guide will help you maintain and customize the Alphington accounting services landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- FAQ Section
- CTA Section
- Footer

### Updating Text Content

#### Hero Section
```html
<!-- Original Hero Text -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    We transform numbers into opportunities
</h1>
```
To update the hero text, simply modify the content between the opening and closing tags. For example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Your New Hero Message Here
</h1>
```

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Dedicated Manager</h3>
    <p class="text-gray-600">Your personal financial expert...</p>
</div>
```
To update a feature:
1. Locate the feature card you want to change
2. Modify the `<h3>` text for the title
3. Update the `<p>` text for the description

### Understanding Tailwind CSS Classes

#### Common Class Patterns
- Text Sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-gray-600`, `bg-blue-600`, etc.
- Spacing: `p-8` (padding), `mb-4` (margin-bottom), etc.
- Responsive Design: `md:text-5xl` (applies at medium screens)

#### Example: Modifying Button Styles
Original button:
```html
<a href="#" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">
```
To change button color to green:
```html
<a href="#" class="inline-block px-8 py-4 bg-green-600 text-white rounded-full">
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://theaccountants.com">Get Started</a>
```

### Updating Links
1. Internal Links (Same Page):
   - Use `#section-id` format
   - Example: `<a href="#features">Services</a>`

2. External Links:
   - Replace `https://theaccountants.com` with your actual URL
   - Example: `<a href="https://your-domain.com/signup">Get Started</a>`

### Link Verification Steps
1. Check all navigation menu links point to correct sections
2. Verify CTA buttons link to proper landing pages
3. Test all footer links work as expected
4. Ensure external links open in new tabs (add `target="_blank"` if needed)

## Linking Privacy and Terms Pages

### Adding Policy Links
Locate the footer section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Verify section IDs match href attributes
   - Check for typos in IDs
   - Ensure no duplicate IDs exist

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify media query classes (e.g., `md:`, `lg:`)
   - Test different screen sizes

3. **Style Inconsistencies**
   - Compare Tailwind classes with existing elements
   - Maintain consistent color codes (e.g., `blue-600`)
   - Keep padding/margin patterns consistent

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all changes across different devices and browsers

Remember to always backup your files before making significant changes, and test thoroughly on a development environment before pushing to production.