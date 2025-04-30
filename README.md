# Dream AI Art Landing Page - Maintenance Guide

This guide will help you maintain and customize the Dream AI Art landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Navigation Links](#managing-navigation-links)
- [Adding Legal Pages](#adding-legal-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Header Text
The site's main title "Dream AI Art" appears in two locations:

1. Navigation bar (top of page):
```html
<div class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Dream AI Art
</div>
```

2. Hero section:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Dream AI Art
</h1>
```

To update the text, simply replace "Dream AI Art" with your desired text in both locations.

### Modifying Colors
The page uses a purple-based color scheme. Common color classes include:
- `bg-purple-600`: Primary button background
- `text-purple-400`: Link hover color
- `from-purple-500 to-pink-500`: Gradient text

To change colors, replace these classes with Tailwind's color utilities:
```html
<!-- Original button -->
<button class="bg-purple-600 hover:bg-purple-700">

<!-- Example change to blue -->
<button class="bg-blue-600 hover:bg-blue-700">
```

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-gray-900 p-8 rounded-2xl hover:transform hover:scale-105 transition-all duration-300">
    <div class="h-16 w-16 bg-purple-600 rounded-xl mb-6 flex items-center justify-center">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Art</h3>
    <p class="text-gray-400">Create stunning digital artwork with our advanced AI tools.</p>
</div>
```

To add a new feature card:
1. Copy the entire `<div>` block
2. Paste it within the `grid` container
3. Update the heading and description text
4. Replace the SVG icon as needed

## Managing Navigation Links

### Current Navigation Structure
The main navigation is in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-purple-400 transition-colors duration-300">Features</a>
    <a href="#benefits" class="hover:text-purple-400 transition-colors duration-300">Benefits</a>
    <a href="#gallery" class="hover:text-purple-400 transition-colors duration-300">Gallery</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the link text between the tags

Example adding a new link:
```html
<a href="#pricing" class="hover:text-purple-400 transition-colors duration-300">Pricing</a>
```

### Footer Links
Footer links are organized in columns:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">About</a></li>
    <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Features</a></li>
    <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Gallery</a></li>
</ul>
```

Replace `#` with actual page URLs when adding real links.

## Adding Legal Pages

### Adding Privacy and Terms Links
Add these links to the footer section:

```html
<div>
    <h4 class="text-xl font-bold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Insert this code block in the footer's grid system, alongside existing columns.

### Creating Legal Pages
1. Create new files named `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your legal content between them
4. Ensure consistent styling by using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check that all `href` attributes point to valid pages or sections
   - Ensure section IDs match their corresponding links
   - Example: `href="#features"` should match `id="features"`

2. **Responsive Design Issues**
   - Look for classes starting with `md:` or `lg:`
   - These control how elements appear on different screen sizes
   - Example: `text-5xl md:text-6xl lg:text-7xl` increases text size on larger screens

3. **Missing Styles**
   - Verify the Tailwind CSS CDN link is working
   - Check for typos in class names
   - Use the browser's inspector tool to debug style issues

### Best Practices

- Always test changes across different screen sizes
- Maintain consistent spacing using Tailwind's spacing classes
- Keep the gradient color scheme consistent throughout
- Back up files before making significant changes

Need more help? Refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact your development team.