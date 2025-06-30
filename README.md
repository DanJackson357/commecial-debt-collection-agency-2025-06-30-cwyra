# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the DebtCollect Pro landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**
```html
<!-- Located in header section -->
<h1 class="text-2xl font-bold text-blue-600">DebtCollect Pro</h1>
```
Simply replace "DebtCollect Pro" with your company name.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
The main headline and subheading are in the hero section:

```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    If we don't collect your business debt, there is no fee
</h2>
<p class="text-xl text-gray-600 mb-12">Professional commercial debt collection services with over 50 years of experience</p>
```

Tailwind CSS Class Guide:
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `mb-8`: Margin bottom spacing
- `text-gray-900`: Dark gray text color

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h4 class="text-xl font-semibold mb-4">No Risk</h4>
    <p class="text-gray-600">Only pay when we successfully collect your debt.</p>
</div>
```

To update:
1. Change the heading text in the `<h4>` tag
2. Modify the description in the `<p>` tag
3. Keep the existing classes for consistent styling

## Managing Links

### Navigation Links
Current internal links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. For internal sections, keep the `#` prefix
2. For external links, use the full URL:
```html
<a href="https://your-website.com/page">Page Name</a>
```

### Call-to-Action Buttons
There are two main CTA buttons:
```html
<!-- Hero section button -->
<a href="https://jo.my/debt-collection-agency" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started Now
</a>

<!-- Bottom section button -->
<a href="https://jo.my/debt-collection-agency" class="inline-block bg-white text-blue-600 px-8 py-4 rounded-lg">
    Get Started Now
</a>
```

Update the `href` attribute with your desired URL.

## Adding Privacy and Terms Pages

### Footer Legal Links
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
- Ensure section IDs match the href attributes
- Check for typos in IDs
- Verify that sections have the correct ID attribute:
```html
<section id="features"> <!-- This ID must match the href="#features" -->
```

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- Keep the existing responsive class structure:
```html
class="text-4xl md:text-5xl lg:text-6xl"
```

3. **Styling Inconsistencies**
- Copy existing classes when adding new elements
- Use the same color classes (e.g., `text-blue-600`, `bg-white`)
- Maintain spacing classes (`mb-4`, `py-24`, etc.)

Remember to:
- Test all changes on multiple screen sizes
- Validate external links before publishing
- Keep a backup of the original code
- Test the page after each significant change

For additional help, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact your web development team.