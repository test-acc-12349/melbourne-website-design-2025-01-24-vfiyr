# Melbourne Website Design - Landing Page Maintenance Guide

This guide will help you maintain and customize the Melbourne Website Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text (MWD)**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">MWD</a>
```
- Replace "MWD" with your desired text
- The gradient effect is created by `from-purple-500 to-pink-500`

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Other menu items -->
</div>
```
- Update text between `>` and `</a>`
- `hidden md:flex` means menu is hidden on mobile, visible on medium screens
- `space-x-8` controls spacing between items

### Hero Section
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-6 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">Melbourne Website Design</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">Best Websites In Melbourne</p>
```
- Update heading and subheading text
- Text sizes increase at different breakpoints (`text-4xl` on mobile, `text-6xl` on medium screens)

### Features Section
To add a new feature card:
1. Copy an existing feature div
2. Paste within the grid container
3. Update icon, title, and description
```html
<div class="bg-gray-900 p-8 rounded-2xl hover:scale-105 transition-transform duration-300">
    <div class="w-12 h-12 bg-purple-600 rounded-lg mb-6 flex items-center justify-center">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Your New Feature</h3>
    <p class="text-gray-400">Your feature description</p>
</div>
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://mwd.com" class="...">Get Started</a>
```
- Replace `https://mwd.com` with your actual website URL

3. Contact Link:
```html
<a href="mailto:admin@mwd.com">admin@mwd.com</a>
```
- Update with your actual email address

### Updating Links
1. Internal Links (sections on same page):
- Keep the `#` symbol
- Ensure the ID matches the section you're linking to
```html
<!-- Navigation link -->
<a href="#features">Features</a>

<!-- Corresponding section -->
<section id="features" class="py-24 bg-gray-800">
```

2. External Links:
- Use complete URLs including `https://`
- Test links after updating

## Adding Privacy and Terms Pages

### Footer Modification
Add these links to the Quick Links section:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

Common Issues:
1. **Broken Gradients**
   - Ensure all gradient classes include both `from-` and `to-` components
   - Example: `bg-gradient-to-r from-purple-500 to-pink-500`

2. **Mobile Menu Issues**
   - Check that `hidden md:flex` is present on the navigation menu
   - This hides menu on mobile and shows it on medium screens

3. **Misaligned Features Grid**
   - Verify the grid classes: `grid grid-cols-1 md:grid-cols-2 gap-8`
   - This creates a single column on mobile, two columns on medium screens

4. **Link Not Working**
   - For section links (#features, etc.), ensure the section ID matches exactly
   - For external links, verify the complete URL including `https://`

Remember to:
- Test all changes on multiple screen sizes
- Validate links after updating
- Keep consistent spacing and formatting
- Back up your code before making changes

For additional help or advanced customization, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs).