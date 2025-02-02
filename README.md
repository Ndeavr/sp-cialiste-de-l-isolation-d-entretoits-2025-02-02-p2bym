# IS Royal Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the IS Royal landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<div class="text-2xl font-bold text-blue-500">IS Royal</div>
```
To update the company name, modify the text between the `<div>` tags.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 leading-tight">
    Spécialiste de l'isolation d'entretoits
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Entreprise spécialisée en gestion énergétique
</p>
```
- To update the main heading, modify the text within the `<h1>` tags
- For the subheading, update the text within the `<p>` tags

### Tailwind CSS Classes Explained

#### Responsive Design Classes
- `md:` prefix: Applies styles on medium screens (768px and up)
- `lg:` prefix: Applies styles on large screens (1024px and up)

Example:
```html
text-4xl md:text-5xl lg:text-6xl
```
This means:
- Mobile: text size is 4xl
- Tablet: text size is 5xl
- Desktop: text size is 6xl

#### Common Class Modifications

1. Text Colors:
```html
text-gray-100  /* Light gray text */
text-blue-500  /* Blue text */
text-gray-300  /* Medium gray text */
```

2. Background Colors:
```html
bg-gray-900    /* Dark background */
bg-blue-600    /* Blue button background */
```

3. Spacing:
```html
px-6           /* Horizontal padding */
py-4           /* Vertical padding */
mb-6           /* Bottom margin */
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:
```html
<a href="#services">Services</a>
<a href="#avantages">Avantages</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update these links:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#` followed by the section ID
3. Example: `<a href="#new-section">New Section</a>`

### External Links
Current external link example:
```html
<a href="https://isroyal.ca/inspection">Inspection Gratuite</a>
```

To update external links:
1. Replace the URL in the `href` attribute
2. Ensure the new URL includes `https://` or `http://`
3. Test the link to verify it works

### Social Media Links
```html
<a href="#" class="text-gray-400 hover:text-blue-400">
    <i class="fab fa-facebook"></i>
</a>
```

To update social media links:
1. Replace the `#` with your social media profile URL
2. Update the icon class if needed (e.g., `fa-facebook` to `fa-twitter`)

## Adding Privacy and Terms Pages

### Footer Modification
Add these links to the footer's "Liens Rapides" section:

```html
<ul class="space-y-2">
    <!-- Existing links -->
    <li>
        <a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">
            Politique de confidentialité
        </a>
    </li>
    <li>
        <a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">
            Conditions d'utilisation
        </a>
    </li>
</ul>
```

### Creating New Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your privacy policy and terms content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Verify that section IDs match exactly with href attributes
   - Section IDs are case-sensitive
   - Example: `href="#Services"` won't link to `id="services"`

2. **Responsive Design Issues**
   - Check mobile view using browser developer tools
   - Verify all `md:` and `lg:` classes are properly set
   - Test at different screen sizes

3. **Missing Icons**
   - Ensure Font Awesome CSS is properly loaded
   - Check for correct icon class names
   - Verify internet connection for CDN access

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12 key)
2. Verify all CDN links are accessible
3. Compare your changes against this original file
4. Test the page in multiple browsers

Remember to always backup your files before making changes, and test all modifications in a development environment first.