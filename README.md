# BrightSmile Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the BrightSmile dental services landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">BrightSmile</a>
```
- Replace "BrightSmile" with your business name
- Adjust text size by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600">Services</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `<a>` tags
- Maintain the `hidden md:flex` class for proper mobile responsiveness

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">Professional Teeth Whitening in Dallas, TX</h1>
<p class="text-xl md:text-2xl text-gray-600">Get expert teeth whitening in Dallas, TX at Dallas</p>
```
- Update location and service information
- Keep the responsive text sizing (`text-4xl md:text-5xl lg:text-6xl`)

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-blue-600`, `bg-white`, `text-gray-900`
- Spacing: `px-4`, `py-6`, `mb-8`, `mt-4`
- Flex layout: `flex`, `items-center`, `justify-between`

## Managing Links

### Navigation Links
Current links in the navigation:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="tel:8776490020">(877) 649-0020</a>
```

To update:
1. Internal links (starting with #):
   - Ensure the href matches the `id` of the target section
   - Example: `href="#services"` should match `id="services"` in the target section

2. Phone numbers:
   - Update the `href="tel:8776490020"` with your phone number
   - Update the displayed number between the tags

### Call-to-Action Buttons
Located in hero and footer sections:
```html
<a href="tel:8776490020" class="inline-flex items-center justify-center px-8 py-4">
    Call Now
</a>
```
- Update both the `href` and button text
- Maintain the styling classes for consistent appearance

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

1. Locate the Quick Links section:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
```

2. Add new links with matching styles:
```html
<li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Style Consistency
- Copy existing link classes: `text-gray-400 hover:text-white transition-colors duration-300`
- Maintain the `space-y-2` spacing between list items

## Troubleshooting

### Common Issues

1. **Broken Internal Links:**
- Verify that section IDs match their corresponding href attributes
- Example: `href="#services"` needs a matching `<section id="services">`

2. **Responsive Design Problems:**
- Check that you've maintained the responsive classes (md:, lg:)
- Example: `text-4xl md:text-5xl lg:text-6xl`

3. **Styling Inconsistencies:**
- Copy existing classes for new elements
- Use browser inspection tools to compare styles

### Best Practices

1. Always test changes across different screen sizes
2. Maintain the existing class structure for consistency
3. Back up the file before making changes
4. Validate phone numbers and email addresses
5. Check all links after updating

Need additional help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).