# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the IDO Consulting landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Name/Logo**
```html
<!-- Find this section near the top -->
<div class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    IDO Consulting  <!-- Replace this text -->
</div>
```

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update text here -->
    <a href="#benefits">Benefits</a>  <!-- And here -->
    <a href="#faq">FAQ</a>           <!-- And here -->
</div>
```

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Stop Wearing Too Many Hats.<br/>  <!-- Main headline -->
    <span class="bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
        Get Fractional C-Suite Expertise.  <!-- Gradient headline -->
    </span>
</h1>
```

### Understanding Tailwind Classes
Common classes used throughout:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-light`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-4`, `mb-8`)
- `py-[size]`: Adds padding top and bottom
- `px-[size]`: Adds padding left and right

Example of modifying a feature card:
```html
<!-- Original -->
<div class="p-8 rounded-2xl bg-gradient-to-br from-gray-50 to-white">

<!-- To make padding larger -->
<div class="p-12 rounded-2xl bg-gradient-to-br from-gray-50 to-white">

<!-- To change background color -->
<div class="p-8 rounded-2xl bg-gradient-to-br from-blue-50 to-white">
```

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact Us</a>
```

To update:
1. The `#` symbol indicates an internal page link
2. The text after `#` must match the `id` of the target section
3. For external links, replace with full URL:
```html
<a href="https://example.com">External Link</a>
```

### Email Links
Located in contact section and footer:
```html
<!-- Find and update this email address in both locations -->
<a href="mailto:jk@idoconsulting.ca">
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links:
```html
<!-- Original footer links -->
<div class="space-y-2">
    <a href="#" class="block text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
    <a href="#" class="block text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
</div>

<!-- Updated footer links -->
<div class="space-y-2">
    <a href="privacy.html" class="block text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
    <a href="terms.html" class="block text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section `id` attributes match link `href` values exactly
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Check for proper responsive classes (e.g., `md:`, `lg:` prefixes)
   - Test at different screen sizes using browser dev tools
   - Maintain existing responsive patterns when adding new content

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent
     ```

4. **Navigation Menu Hidden on Mobile**
   - The `hidden md:flex` class intentionally hides the menu on mobile
   - Keep this pattern for proper responsive behavior

### Need Help?
- Check the Tailwind CSS documentation for class references
- Use browser developer tools to inspect elements
- Test all changes across different devices and browsers
- Maintain backup copies before making significant changes

Remember to test all changes thoroughly before deploying to a live site. When in doubt, make one change at a time and verify its impact before proceeding.