# WebTX Landing Page Maintenance Guide

This guide will help you maintain and customize the WebTX landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">WebTX</a>
```
- Replace "WebTX" with your brand name
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

### Hero Section
Located at the top of the page with main heading and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Best Websites In Texas</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Custom Websites For Your Business</p>
```
- Update heading text between `<h1>` tags
- Modify subheading text between `<p>` tags
- Size classes explained:
  - `text-4xl`: Base size for mobile
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-600 leading-relaxed">Intuitive interface designed for seamless navigation and management.</p>
</div>
```
- Update feature title between `<h3>` tags
- Modify description between `<p>` tags
- Common Tailwind classes used:
  - `rounded-xl`: Rounded corners
  - `p-8`: Padding
  - `shadow-lg`: Shadow effect
  - `hover:shadow-xl`: Shadow effect on hover

## Fixing Broken Links

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
To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Example: `<a href="#new-section">New Section</a>`

### External Links
The site contains these external links:
```html
<a href="https://sigmaseo.io" class="inline-block px-6 py-3">Get Started</a>
```
To update:
1. Replace `https://sigmaseo.io` with your desired URL
2. Test the link to ensure it opens correctly
3. Consider adding `target="_blank"` for external links

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Check that section IDs match exactly with href attributes
- Section IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
- Check mobile-first classes (without prefix)
- Then check responsive classes (with md: or lg: prefix)
- Example: `text-xl md:text-2xl lg:text-3xl`

3. **Styling Inconsistencies**
- Copy existing Tailwind classes for similar elements
- Keep hover effects consistent:
  ```html
  class="hover:text-white transition-colors duration-300"
  ```

### Need Help?
- Verify your changes in multiple browsers
- Test on different screen sizes
- Use browser developer tools (F12) to inspect elements
- Reference [Tailwind CSS documentation](https://tailwindcss.com/docs) for class options

Remember to always backup your files before making changes, and test thoroughly on a development environment before pushing to production.