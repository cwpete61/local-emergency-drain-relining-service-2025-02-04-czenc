# Emergency Plumbing Landing Page - Maintenance Guide

This guide will help you maintain and customize the emergency plumbing landing page. It's written for beginners with no prior coding experience.

## 1. Updating Text and Tailwind CSS Classes

### Header Section
```html
<header class="fixed w-full z-50 bg-gray-900/95 backdrop-blur-sm border-b border-gray-800">
```
The header contains:
- Company name ("DrainPro")
- Navigation menu
- Emergency Call button

To update the company name:
1. Locate: `<a href="#" class="text-2xl font-bold text-blue-500">DrainPro</a>`
2. Replace "DrainPro" with your company name
3. Adjust text size using `text-2xl` class (options: `text-xl`, `text-3xl`, etc.)

### Hero Section Text
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 text-white leading-tight">
    Local Emergency Drain Relining Service
</h1>
```
To modify:
1. Replace text between `<h1>` tags
2. Keep responsive text sizes:
   - Mobile: `text-4xl`
   - Tablet: `md:text-5xl`
   - Desktop: `lg:text-6xl`

### Tailwind CSS Color Classes
Common color classes used:
- Background: `bg-gray-900`, `bg-blue-600`
- Text: `text-white`, `text-gray-300`, `text-blue-500`
- Hover: `hover:bg-blue-700`, `hover:text-white`

To change colors:
1. Replace color names (e.g., `blue` to `red`)
2. Adjust shade numbers (50-900)
Example: `bg-blue-600` → `bg-red-600`

## 2. Fixing Broken Links

### Navigation Menu Links
Current internal links:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Internal links (same page):
   - Keep the `#` prefix
   - Match the `id` of the target section
   Example: `<a href="#services">` links to `<section id="services">`

2. External links:
   - Replace placeholder URLs:
   ```html
   <a href="https://plumbers.com" class="bg-blue-600">
   ```
   Change to your actual URL:
   ```html
   <a href="https://your-website.com" class="bg-blue-600">
   ```

### Emergency Call Button
Located in header and hero section:
```html
<a href="https://plumbers.com" class="bg-blue-600 hover:bg-blue-700">
```
Replace with:
- Phone number link: `href="tel:+1234567890"`
- Contact page: `href="/contact.html"`

## 3. Linking Privacy and Terms Pages

### Footer Links Section
Current placeholder links:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2 text-gray-400">
        <li>Privacy Policy</li>
        <li>Terms of Service</li>
        <li>Cookie Policy</li>
    </ul>
</div>
```

To add proper links:
1. Update the list items with anchor tags:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    <li><a href="/cookies.html" class="hover:text-white transition-colors duration-300">Cookie Policy</a></li>
</ul>
```

## Troubleshooting Tips

1. If links aren't working:
   - Check for typos in `href` attributes
   - Verify file names match exactly
   - Ensure files are in the correct directory

2. If styles aren't applying:
   - Check for missing classes
   - Verify Tailwind CSS CDN link is working
   - Test responsive designs using browser developer tools

3. If sections aren't aligned:
   - Check container classes: `container mx-auto px-4`
   - Verify padding classes: `py-24`, `px-8`
   - Review responsive classes (md:, lg: prefixes)

## Important Notes

- Always test changes across different screen sizes
- Maintain the responsive design by keeping `md:` and `lg:` prefixed classes
- Back up your code before making significant changes
- Keep the consistent color scheme throughout the page
- Preserve accessibility features like proper heading hierarchy and text contrast

Need more help? Refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)