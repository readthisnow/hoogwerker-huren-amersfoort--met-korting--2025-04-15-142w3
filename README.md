# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page for Hoogwerker Huren Amersfoort. Follow these detailed instructions to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-gray-900">Hoogwerker</a>
```
- Replace "Hoogwerker" with your desired text
- The `text-2xl` class controls size
- `text-gray-900` controls color

2. **Navigation Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Features</a>
    <!-- Other navigation items -->
</div>
```
- Update text between `>` and `</a>`
- Keep the `href` attributes matching your section IDs
- `space-x-8` controls spacing between items

### Hero Section
To modify the main banner:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight">
    Hoogwerker Huren Amersfoort<br>(Met Korting)
</h1>
```
- Replace text while keeping the `<br>` tag for line breaks
- `text-4xl` sets mobile size, `md:text-6xl` sets desktop size

2. **Background Image:**
```html
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" 
    alt="Hoogwerker" class="w-full h-full object-cover">
```
- Replace the `src` URL with your image
- Update the `alt` text
- Keep `object-cover` for proper scaling

### Tailwind CSS Tips for Beginners
- `text-{size}`: Controls text size (xs, sm, base, lg, xl, 2xl, etc.)
- `font-{weight}`: Controls text thickness (normal, medium, bold, etc.)
- `bg-{color}-{shade}`: Sets background color (bg-blue-600, bg-gray-900, etc.)
- `p-{number}`: Sets padding (p-4, p-8, etc.)
- `m-{number}`: Sets margin (m-4, m-8, etc.)

## Managing Links

### Internal Navigation Links
Current internal links use section IDs:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Identify the section ID you want to link to
2. Add a matching ID to the section:
```html
<section id="your-section-name">
```
3. Update the href attribute:
```html
<a href="#your-section-name">Your Link Text</a>
```

### External Links
The main call-to-action buttons link to:
```html
<a href="https://hoogwerkerhurenamersfoort.nl">
```

To update:
1. Replace all instances of this URL with your actual website
2. Check these locations:
   - Header "Nu Huren" button
   - Hero section "Direct Huren" button
   - Contact section button

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

1. Locate the footer section:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
    <div>
        <h3 class="text-lg font-semibold mb-4">Over Ons</h3>
```

2. Add new links:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li>
            <a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors">
                Privacy Policy
            </a>
        </li>
        <li>
            <a href="/terms.html" class="text-gray-400 hover:text-white transition-colors">
                Terms of Service
            </a>
        </li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Text Not Visible:**
   - Check text color classes (text-{color})
   - Ensure background colors don't match text colors

2. **Links Not Working:**
   - Verify section IDs match href attributes exactly
   - Check for typos in URLs
   - Ensure external URLs include "https://"

3. **Responsive Issues:**
   - Look for `md:` classes that control desktop appearance
   - Test at different screen sizes
   - Don't remove `responsive` classes

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always test changes across different devices and browsers before publishing updates.