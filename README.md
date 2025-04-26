# Tape In Lashes Landing Page - Maintenance Guide

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Privacy and Terms Pages](#privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and brand name. To update:

1. **Brand Name**
```html
<!-- Located at the start of the nav section -->
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Tape In Lashes  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Voordelen</a>  <!-- Change these text labels -->
    <a href="#benefits">Waarom Kiezen</a>
    <a href="#faq">FAQ</a>
</div>
```

### Hero Section
The main banner section contains:
```html
<h1 class="text-4xl md:text-6xl font-bold mb-6 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Koop Tape In Lashes Met Korting  <!-- Main headline -->
</h1>
<p class="text-xl text-gray-300 mb-10">
    Transformeer je look met onze premium tape in lashes.  <!-- Subheadline -->
</p>
```

### Tailwind CSS Tips
- Font sizes use classes like `text-4xl` (larger) or `text-xl` (smaller)
- Colors follow pattern: `text-purple-400` or `bg-gray-800`
- Spacing uses `m` (margin) or `p` (padding) with numbers: `mb-6` (margin-bottom)
- Responsive classes start with screen sizes: `md:text-6xl`

## Managing Links

### Navigation Links
Current internal links:
```html
<a href="#features">Voordelen</a>
<a href="#benefits">Waarom Kiezen</a>
<a href="#faq">FAQ</a>
```
To update:
1. Replace `#features` with your new section ID
2. Ensure corresponding section has matching ID: `<section id="features">`

### Call-to-Action Buttons
```html
<a href="https://amzn.to/3Er049t" class="bg-gradient-to-r from-purple-600 to-pink-600...">
    Bestel Nu
</a>
```
To update:
1. Replace `https://amzn.to/3Er049t` with your product link
2. Keep the existing classes for consistent styling

### Social Media Links
Located in footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-purple-400">Instagram</a>
    <a href="#" class="text-gray-400 hover:text-purple-400">Facebook</a>
</div>
```
Replace `#` with actual social media URLs.

## Privacy and Terms Pages

### Adding Policy Links
Current footer placeholder:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Terms & Conditions</a></li>
</ul>
```

To link to policy pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update links:
```html
<li><a href="privacy.html" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-purple-400 transition-colors duration-300">Terms & Conditions</a></li>
```

### Contact Information
Update email in footer:
```html
<p class="text-gray-400">support@example.com</p>  <!-- Replace with actual email -->
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Check that section IDs match exactly with href values
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
- Check screen size classes:
  - `md:` for medium screens (768px+)
  - `lg:` for large screens (1024px+)
- Test on multiple devices

3. **Gradient Text Not Showing**
- Ensure these classes are present together:
  - `bg-gradient-to-r`
  - `from-[color]`
  - `to-[color]`
  - `bg-clip-text`
  - `text-transparent`

### Need Help?
- Check Tailwind CSS documentation for class references
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test all links before deploying
- Maintain backup copies before making major changes

Remember to always test changes in a development environment before pushing to production.