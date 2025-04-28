# Landing Page Maintenance Guide
## For 101Headshots Corporate Photography Website

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. The documentation is structured for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<a href="/" class="text-2xl font-bold">101Headshots</a>
```
To update the company name:
1. Locate this line in the `<header>` section
2. Replace "101Headshots" with your desired text
3. Maintain the surrounding HTML tags

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    Olathe, Kansas Corporate Headshot Photography Services
</h1>
```
To update the main headline:
1. Find this `<h1>` tag in the first `<section>`
2. Replace the text while keeping the HTML structure intact
3. Maintain proper spacing and formatting

### Tailwind CSS Classes Explained

#### Responsive Design Classes
Common patterns in the code:
- `md:text-5xl`: Applies at medium screens (768px+)
- `lg:text-6xl`: Applies at large screens (1024px+)
- `text-4xl`: Default size for all screens

Example modification:
```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">

<!-- Making text smaller -->
<h1 class="text-3xl md:text-4xl lg:text-5xl">
```

#### Color Classes
The site uses a purple/pink gradient theme:
```html
class="bg-gradient-to-r from-purple-500 to-pink-500"
```
To change colors:
1. Replace `purple-500` with alternatives like `blue-500`
2. Replace `pink-500` with alternatives like `indigo-500`

## Fixing Broken Links

### Current Link Structure
The page contains these main link types:

#### Navigation Links
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```
To update:
1. The `#` symbol indicates an internal page section
2. Replace with full URLs for external links
3. Example: `<a href="https://www.yoursite.com/services">Services</a>`

#### Call-to-Action Links
```html
<a href="https://www.101headshots.com">Book Your Session</a>
```
To update:
1. Locate the booking link in the hero section
2. Replace the URL with your booking system
3. Test the link after updating

#### Email Links
```html
<a href="mailto:bryan@101headshots.com">Email Us Today</a>
```
To update:
1. Find all `mailto:` links
2. Replace the email address
3. Format: `mailto:your.email@domain.com`

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the footer's Quick Links section:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Styling Consistency
- Copy the existing link classes: `text-gray-400 hover:text-white transition-colors duration-300`
- Maintain the `<li>` structure for consistent spacing
- Keep the same hover effects

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in ID names
   - Verify that sections have the correct ID attribute

2. **Responsive Design Problems**
   - Test at different screen sizes
   - Verify media query classes (md:, lg:) are correct
   - Check for missing responsive classes

3. **Gradient Issues**
   - Confirm proper class order in gradient definitions
   - Verify color classes exist in Tailwind
   - Check for typos in color names

### Getting Help
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all changes in multiple browsers

Remember to:
- Back up files before making changes
- Test all modifications in a development environment
- Validate HTML using [W3C Validator](https://validator.w3.org/)
- Check all links after updates