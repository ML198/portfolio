# Biostat Portfolio - R Markdown Website

A professional personal website built with R Markdown and deployed on GitHub Pages. Showcasing biostatistics expertise, research projects, and technical skills.

## Repository Information

- **GitHub Username:** ML198
- **Repository Name:** biostat-portfolio
- **Website URL:** `https://ML198.github.io/biostat-portfolio`

## Features

✨ **Modern, Minimal Design**
- Custom CSS styling with responsive layout
- Mobile-friendly design with professional typography
- Color scheme optimized for readability and visual hierarchy

📄 **Key Pages**
- **Home Page** - Professional introduction with skills overview
- **Projects Page** - Detailed showcase of featured graduate-level projects
- **CV Page** - Comprehensive curriculum vitae with embedded PDF resume

🔧 **Technical Implementation**
- Built with R Markdown website framework
- Navigation bar with links to portfolio pages and social media
- Custom CSS for advanced styling beyond basic Markdown
- Fully responsive design for desktop, tablet, and mobile

## Project Structure

```
biostat-portfolio/
├── _site.yml                    # Website configuration (navigation, title, metadata)
├── index.Rmd                    # Home page
├── projects.Rmd                 # Projects showcase page
├── cv.Rmd                       # Curriculum vitae page
├── styles.css                   # Custom CSS styling
├── Mingrui_Li_Resume.pdf        # Resume PDF
├── README.md                    # This file
├── .gitignore                   # Git ignore patterns
└── _site/                       # Generated website (created after rendering)
```

## Setup Instructions

### Prerequisites

You'll need:
- **R** (version 3.6+)
- **RStudio** (recommended)
- **Git** (for version control)
- **GitHub account** (for hosting)

### 1. Install Required R Packages

Open R or RStudio and run:

```r
install.packages("rmarkdown")
```

Verify installation:
```r
library(rmarkdown)
rmarkdown::render_site()
```

### 2. Build the Website Locally

Navigate to the project directory and render the site:

```r
setwd("path/to/biostat-portfolio")
rmarkdown::render_site()
```

This will generate a `_site/` directory containing the rendered HTML files.

### 3. Preview Locally

After rendering, you can open `_site/index.html` in your browser to preview the website.

Alternatively, in RStudio, click the "Build Website" button or use:
```r
servr::httd("_site")
```

## Deployment to GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com/new)
2. Create a new repository named `biostat-portfolio`
3. Make it **public** so GitHub Pages can host it
4. Do **NOT** initialize with README (we already have one)

### Step 2: Initialize Git in Your Project

```bash
cd biostat-portfolio
git init
git add -A
git commit -m "Initial commit: R Markdown website"
```

### Step 3: Connect to GitHub and Push

```bash
git remote add origin https://github.com/ML198/biostat-portfolio.git
git branch -M main
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under "Source", select:
   - Branch: `main`
   - Folder: `/ (root)` or `/docs` (depending on your preference)
4. Click **Save**

**Important:** For this setup, ensure your `_site` folder is **committed and pushed to GitHub** (or rename it to `docs` if GitHub Pages is configured for `/docs`).

### Step 5: Access Your Website

Your website will be live at:
```
https://ML198.github.io/biostat-portfolio
```

*Note: It may take a few minutes for GitHub Pages to build and deploy.*

## Custom CSS Implementation

The website includes **custom CSS styling** that goes beyond basic Markdown formatting:

### Key CSS Features

**File:** `styles.css`

**Custom Implementations:**

1. **CSS Variables** - Professional color scheme with consistent theming
   - Primary colors, gradients, shadows, and transitions
   - Easy customization by editing root variables

2. **Advanced Layout Components**
   - Hero section with gradient background
   - Expertise grid with hover effects
   - Skills cards with left border accent
   - Project cards with shadow and hover animations

3. **Typography & Spacing**
   - Custom font stack using system fonts
   - Responsive line-height and sizing
   - Professional spacing and hierarchy

4. **Interactive Elements**
   - Button styling with hover effects
   - Link underlines on hover
   - Card elevation on hover
   - Smooth transitions throughout

5. **Responsive Design**
   - Mobile-first approach
   - Breakpoints at 768px and 480px
   - Flexible grid layouts with `grid-template-columns: repeat(auto-fit, ...)`

6. **Navigation Styling**
   - Sticky navbar with border
   - Active link indicators
   - Responsive flex layout

### View Custom CSS

The custom CSS implementation starts at line 1 in `styles.css`. Key sections include:

- **Lines 1-10:** Root CSS variables
- **Lines 20-80:** Global styles and typography
- **Lines 90-150:** Navigation bar styling
- **Lines 160-250:** Hero section and section containers
- **Lines 260-350:** Expertise and skills grids
- **Lines 360-430:** Button and CTA styling
- **Lines 440-550:** Projects page specific styling
- **Lines 560-750:** CV page specific styling
- **Lines 760-850:** Responsive design breakpoints

## Updating Content

### Modify Home Page
Edit `index.Rmd` to update:
- Professional introduction
- Expertise descriptions
- Skills sections

### Modify Projects
Edit `projects.Rmd` to update:
- Project titles and descriptions
- Technical stacks
- Project links

### Modify CV
Edit `cv.Rmd` to update:
- Education details
- Work experience
- Skills
- Publications

### After Making Changes

1. Render the site locally:
   ```r
   rmarkdown::render_site()
   ```

2. Preview in browser

3. Commit and push to GitHub:
   ```bash
   git add -A
   git commit -m "Update [page name]"
   git push
   ```

## Customization

### Change Colors

Edit `styles.css` and modify the root CSS variables:

```css
:root {
  --primary-color: #2c3e50;      /* Main color */
  --secondary-color: #3498db;    /* Accent color */
  --accent-color: #1abc9c;       /* Highlight color */
  /* ... other colors ... */
}
```

### Change Fonts

Edit the `font-family` in `styles.css` body rule:

```css
body {
  font-family: 'Your Font Name', fallback, sans-serif;
}
```

### Modify Logo/Title

Edit `_site.yml`:

```yaml
navbar:
  title: "Your Name"
  left:
    - text: "Home"
      href: index.html
```

## Troubleshooting

### Website not showing changes after pushing

- Ensure `_site/` folder is committed to GitHub
- GitHub Pages may take 1-2 minutes to rebuild
- Clear browser cache and do a hard refresh (Ctrl+Shift+R or Cmd+Shift+R)

### Local preview not working

- Make sure all required packages are installed:
  ```r
  install.packages(c("rmarkdown", "servr"))
  ```
- Check that you're in the correct directory

### Navigation links not working

- Verify all `.Rmd` files are in the root directory
- Check that file names in `_site.yml` match actual file names exactly

### CSS not loading

- Ensure `styles.css` is in the project root
- After changes, re-render the site: `rmarkdown::render_site()`
- Check browser console (F12) for CSS loading errors

## File-by-File Breakdown

### `_site.yml`
Configuration file that defines:
- Website title and description
- Navigation bar structure
- CSS output settings
- HTML output options

### `index.Rmd`
Home page featuring:
- Hero section with professional tagline
- About section with expertise overview
- Skills grid with technical capabilities
- Call-to-action buttons

### `projects.Rmd`
Projects showcase with:
- Two featured graduate-level projects with detailed descriptions
- Technical stacks and methodologies
- Links to GitHub repositories
- Additional project summaries in grid format

### `cv.Rmd`
Curriculum vitae including:
- Education (MPH Biostatistics, BS Bioinformatics)
- Professional experience (Research Assistant, Biotech Analyst, etc.)
- Technical skills
- Publications
- Link to downloadable PDF resume

### `styles.css`
Custom styling providing:
- 850+ lines of professional CSS
- Responsive design with mobile optimization
- Component-specific styling for all page elements
- Advanced features like gradients, shadows, and transitions

## Best Practices

✅ **DO:**
- Commit frequently with descriptive messages
- Test locally before pushing
- Keep CSS organized and commented
- Use semantic HTML in Rmd files
- Optimize images for web

❌ **DON'T:**
- Commit the `_site/` directory if using `/docs` deployment
- Push sensitive information (API keys, passwords)
- Make major CSS changes without testing
- Forget to rebuild before pushing

## Additional Resources

- [R Markdown Website Guide](https://rmarkdown.rstudio.com/websites.html)
- [GitHub Pages Documentation](https://pages.github.com/)
- [CSS Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [R Markdown Reference](https://rmarkdown.rstudio.com/authoring_quick_tour.html)

## License

This portfolio website is open source and available for personal and professional use.

---

**Created:** April 2026
**Author:** Mingrui Li
**Contact:** mingrui.li@emory.edu
# portfolio
