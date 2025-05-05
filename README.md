# Roofing Newcastle Landing Page - Maintenance Guide

This guide will help you maintain and customize the Roofing Newcastle landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company name and navigation menu:

```html
<header class="fixed w-full bg-white/95 backdrop-blur-sm z-50 shadow-md">
    <nav class="container mx-auto px-4 py-4 flex justify-between items-center">
        <a href="/" class="text-2xl font-bold text-gray-800">Roofing Newcastle</a>
        <!-- Navigation items -->
    </nav>
</header>
```

To update:
1. Change company name: Replace "Roofing Newcastle" with your business name
2. Adjust text size: Modify `text-2xl` to `text-3xl` for larger text
3. Change color: Replace `text-gray-800` with colors like `text-blue-600`

### Hero Section
The main banner section contains your primary headline:

```html
<div class="max-w-4xl">
    <h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight">
        Roofing Newcastle: Say Goodbye To Leaky Roofs
    </h1>
    <p class="text-xl md:text-2xl text-gray-200 mb-8">
        Prevent Costly Water Damage & Increase Your Home's Value
    </p>
</div>
```

To update:
1. Change headline: Replace the h1 text
2. Modify subheading: Update the p tag content
3. Adjust spacing: Change `mb-6` to `mb-8` for more space
4. Background image: Update the URL in `style="background-image: url('...')">`

### Common Tailwind Classes Explained
- `container`: Centers content and sets max-width
- `mx-auto`: Centers element horizontally
- `px-4`: Adds horizontal padding
- `py-4`: Adds vertical padding
- `text-2xl`: Sets font size
- `font-bold`: Makes text bold
- `bg-white`: Sets white background
- `hover:scale-105`: Enlarges element on hover

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Internal links: Ensure section IDs match (e.g., `href="#services"` should match `id="services"`)
2. External links: Replace `#` with full URLs
3. Email links: Update format `mailto:quote@roofingnewcastle.com.au`

### Call-to-Action Links
Update the main CTA button:

```html
<a href="https://roofingnewcastle.com.au" class="inline-block bg-blue-600 hover:bg-blue-700 text-white font-semibold px-8 py-4 rounded-lg">
    Get Your Free Quote
</a>
```

Replace the URL with your actual website or contact form link.

## Linking Privacy and Terms Pages

### Footer Links Section
Current footer links:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files:
   ```
   privacy.html
   terms.html
   ```

2. Update footer links:
   ```html
   <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
   <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
   ```

3. Ensure consistent styling by copying the header and footer to new pages

## Troubleshooting

Common issues and solutions:

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CSS is loading
   - Ensure proper class names

2. **Non-Working Links**
   - Confirm file paths are correct
   - Check for typos in URLs
   - Verify section IDs exist

3. **Responsive Issues**
   - Test on multiple devices
   - Check responsive classes (md:, lg:)
   - Verify menu toggle works on mobile

Need help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).