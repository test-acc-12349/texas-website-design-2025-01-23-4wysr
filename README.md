# Texas Website Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Website Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this line and change "TWD":
```html
<a href="/" class="text-2xl font-bold text-gray-900">TWD</a>
```

2. **Navigation Menu Items**: Locate these lines to modify menu text:
```html
<a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
<a href="#benefits" class="text-gray-600 hover:text-gray-900">Benefits</a>
```

### Hero Section
Update your main headline and subtitle:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight mb-6">
    Texas Website Design  <!-- Change this text -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Best Websites In Texas  <!-- Change this text -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text thickness (e.g., `font-bold`, `font-semibold`)
- `mb-[size]`: Adds bottom margin (e.g., `mb-6`, `mb-10`)
- `py-[size]`: Adds vertical padding (e.g., `py-24`)
- `px-[size]`: Adds horizontal padding (e.g., `px-6`)

To modify spacing or sizing, adjust these numbers following Tailwind's scale:
- 4 = 1rem (16px)
- 6 = 1.5rem (24px)
- 8 = 2rem (32px)

## Managing Links

### Navigation Menu Links
Current internal links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update these:
1. Find the section ID you want to link to (e.g., `id="features"`)
2. Use that ID with a # in the href (e.g., `href="#features"`)

### Call-to-Action Buttons
Update the "Get Started" button link:
```html
<a href="https://twd.com" class="inline-flex items-center justify-center px-6 py-2...">
    Get Started
</a>
```
Replace `https://twd.com` with your actual URL.

### Footer Links
Update service links in the footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">Custom Design</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Development</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">SEO</a></li>
</ul>
```
Replace `#` with actual page URLs.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Find this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in href attributes
   - Ensure file names match exactly (case-sensitive)
   - Verify files are in the correct directory

2. **Styling Problems**
   - Make sure Tailwind CDN link is present in the head section
   - Check for missing or mistyped class names
   - Verify responsive classes (md:, lg:) are correctly formatted

3. **Layout Issues**
   - Check container classes are present
   - Verify grid column settings
   - Ensure padding and margin classes are correct

### Need Help?
- Double-check the Tailwind CSS documentation
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Keep backups before making significant changes

Remember to test all changes across different devices and screen sizes to ensure responsive design remains intact.