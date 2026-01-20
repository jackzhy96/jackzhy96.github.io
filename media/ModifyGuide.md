# Website Modification Guide

This guide explains how to add, remove, or modify content on your portfolio website. The website is built using Jekyll and hosted on GitHub Pages.

---

## Table of Contents

1. [Quick Start](#quick-start)
2. [Website Layout Overview](#website-layout-overview)
3. [File Structure Overview](#file-structure-overview)
4. [Sidebar and Profile](#sidebar-and-profile)
5. [Favicon](#favicon)
6. [Navigation Menu](#navigation-menu)
6. [About Me Page](#about-me-page)
   - [Summary Section](#summary-section)
   - [News Section](#news-section)
   - [Experience Timeline](#experience-timeline)
   - [Education Timeline](#education-timeline)
   - [Technical Skills](#technical-skills)
   - [Training Certificates](#training-certificates)
7. [Research Projects](#research-projects)
8. [Course/Personal Projects](#coursepersonal-projects)
9. [Build Projects](#build-projects)
10. [Publications](#publications)
11. [Blog Posts](#blog-posts)
12. [CV Page](#cv-page)
13. [Adding Images and Media](#adding-images-and-media)
14. [Styling and Colors](#styling-and-colors)
15. [Testing Locally](#testing-locally)
16. [Troubleshooting](#troubleshooting)

---

## Quick Start

### To Add New Content:
1. Create a new Markdown file (`.md`) in the appropriate folder
2. Add the required front matter (YAML header)
3. Write your content in Markdown
4. Commit and push to GitHub

### To Edit Existing Content:
1. Find the file in the appropriate folder
2. Edit the Markdown content
3. Save, commit, and push

### To Remove Content:
1. Delete the corresponding `.md` file
2. Commit and push

### Common Locations:
| Content Type | Location |
|-------------|----------|
| Site configuration | `_config.yml` |
| Navigation menu | `_data/navigation.yml` |
| About page | `_pages/about.md` |
| CV page | `_pages/cv.md` |
| Research items | `_research/` folder |
| Project items | `_projects/` folder |
| Build items | `_build/` folder |
| Publications | `_publications/` folder |
| Blog posts | `_posts/` folder |
| Images | `images/` folder |
| Resume PDF | `media/` folder |

---

## Website Layout Overview

The website uses a **two-column split layout**:

```
┌─────────────────────────────────────────────────────────┐
│                    Navigation Bar                        │
├──────────────┬──────────────────────────────────────────┤
│              │                                          │
│   SIDEBAR    │              MAIN CONTENT                │
│   (Left)     │              (Right)                     │
│              │                                          │
│  - Profile   │  - Page title                            │
│  - Photo     │  - Content sections                      │
│  - Name      │  - Projects, publications, etc.          │
│  - Bio       │                                          │
│  - Location  │                                          │
│  - Links     │                                          │
│              │                                          │
└──────────────┴──────────────────────────────────────────┘
```

**Desktop:** Side-by-side layout (sidebar 280px, content fills rest)
**Mobile/Tablet:** Stacked layout (sidebar on top, content below)

### Key Style Files

| File | Purpose |
|------|---------|
| `_sass/layout/_portfolio-custom.scss` | Main custom styles (layout, sidebar, cards) |
| `_sass/theme/_default_light.scss` | Light mode colors |
| `_sass/theme/_default_dark.scss` | Dark mode colors |

---

## File Structure Overview

```
jackzhy96.github.io/
├── _config.yml              # Main site configuration (profile info)
├── _data/
│   └── navigation.yml       # Navigation menu items
├── _pages/
│   ├── about.md             # Home/About Me page
│   ├── cv.md                # CV page
│   ├── research.html        # Research listing page
│   ├── projects.html        # Projects listing page
│   ├── build.html           # Build listing page
│   ├── publications.html    # Publications listing page
│   └── year-archive.html    # Blog archive page
├── _research/               # Research project entries
├── _projects/               # Course project entries
├── _build/                  # Build/infrastructure entries
├── _publications/           # Publication entries
├── _posts/                  # Blog post entries
├── _includes/               # Reusable HTML components
│   ├── project-card.html    # Project card layout
│   └── publication-item.html # Publication list item
├── images/                  # Image files
│   ├── cooking/             # Cooking blog images
│   ├── research/            # Research project images
│   ├── projects/            # Course project images
│   ├── build/               # Build project images
│   └── profile.png          # Your profile photo
├── media/                   # Media files (resume PDF, etc.)
└── _sass/                   # Style files
    ├── theme/               # Color theme files
    └── layout/
        └── _portfolio-custom.scss  # Custom styles
```

---

## Sidebar and Profile

The sidebar (left panel) displays your profile information and is controlled by `_config.yml`.

### Edit Profile Information

Open `_config.yml` and find the `author:` section:

```yaml
author:
  avatar           : "profile_photo.jpg"  # Profile photo in /images/
  name             : "Haoying (Jack) Zhou"
  name_chinese     : "周昊英"              # Chinese name (optional, displayed below English)
  pronouns         : "he/him"              # Optional
  bio_title        : "Surgical Robotics, Simulation"    # Bold line 1 (optional)
  bio_title2       : "Infrastructure and AI"            # Bold line 2 (optional)
  bio              : "Visiting Scholar at JHU"          # Regular line 1 (optional)
  bio2             : "PhD Candidate at WPI"             # Regular line 2 (optional)
  location         : "Baltimore, MD"
  employer         : "Johns Hopkins University"
  employer2        : "Worcester Polytechnic Institute"  # Second affiliation (optional)
  email            : "hzhou6@wpi.edu"

  # Social links (leave empty to hide)
  github           : "jackzhy96"
  linkedin         : "haoyingzhoujack"
  googlescholar    : "https://scholar.google.com/citations?user=YOUR_ID"
  orcid            : ""                 # Empty = hidden
  twitter          : ""                 # Empty = hidden
```

### Bio Title and Bio Lines

The sidebar supports up to **two bold lines** followed by up to **two regular lines**:

```yaml
bio_title:  "Surgical Robotics, Simulation"      # Bold line 1
bio_title2: "Infrastructure and AI"              # Bold line 2
bio:        "Visiting Graduate Scholar at JHU"   # Regular line 1
bio2:       "Robotics PhD Candidate at WPI"      # Regular line 2
```

**Result in sidebar:**
```
Surgical Robotics, Simulation          ← Bold
Infrastructure and AI                  ← Bold
Visiting Graduate Scholar at JHU       ← Regular
Robotics PhD Candidate at WPI          ← Regular
```

**All fields are optional.** Examples:

```yaml
# One bold + two regular lines
bio_title:  "Robotics Engineer"
bio_title2: ""
bio:        "Visiting Scholar at JHU"
bio2:       "PhD Candidate at WPI"

# Two bold + one regular line
bio_title:  "Surgical Robotics"
bio_title2: "Simulation & AI"
bio:        "PhD Candidate at WPI"
bio2:       ""

# Single bold line only
bio_title:  "Robotics Engineer"
bio_title2: ""
bio:        ""
bio2:       ""
```

### Update Profile Photo

1. Replace `/images/profile.png` with your new photo
2. Keep the same filename, or update `avatar:` in `_config.yml`
3. Recommended size: 300x300 pixels, square aspect ratio

### Add/Remove Social Links

**To add a link:** Fill in the username/URL
```yaml
github: "jackzhy96"
```

**To remove a link:** Leave it empty or delete the line
```yaml
twitter: ""  # Will not be displayed
```

**Available social link options:**
- `email`, `github`, `linkedin`, `googlescholar`
- `twitter`, `facebook`, `instagram`
- `orcid`, `researchgate`, `youtube`
- `uri` (personal website)

---

## Favicon

The favicon is the small icon that appears in browser tabs and bookmarks. The website uses PNG-based favicons.

### Favicon Files

All favicon files are located in `/images/`:

| File | Size | Purpose |
|------|------|---------|
| `favicon-32x32.png` | 32x32 | Browser tab icon |
| `favicon-192x192.png` | 192x192 | Android/PWA icon |
| `favicon-512x512.png` | 512x512 | Large PWA icon |
| `apple-touch-icon-180x180.png` | 180x180 | iOS home screen |
| `favicon.ico` | 48x48 | Legacy browser support |

### Update Favicon

**Option 1: Using an existing image**

1. Place your source image in `/images/` (e.g., `my-favicon.png`)
2. Use ImageMagick to generate all sizes:

```bash
cd images/

# Generate all favicon sizes from source image
convert my-favicon.png -resize 32x32 favicon-32x32.png
convert my-favicon.png -resize 192x192 favicon-192x192.png
convert my-favicon.png -resize 512x512 favicon-512x512.png
convert my-favicon.png -resize 180x180 apple-touch-icon-180x180.png
convert my-favicon.png -resize 48x48 favicon.ico
```

3. Restart Jekyll and clear browser cache

**Option 2: Using an online generator**

1. Go to [favicon.io](https://favicon.io/) or [realfavicongenerator.net](https://realfavicongenerator.net/)
2. Upload your image
3. Download the generated files
4. Replace files in `/images/` folder

### Favicon Configuration

The favicon is configured in `_includes/head/custom.html`:

```html
<link rel="apple-touch-icon" sizes="180x180" href="{{ base_path }}/images/apple-touch-icon-180x180.png"/>
<link rel="icon" type="image/png" href="{{ base_path }}/images/favicon-32x32.png" sizes="32x32"/>
<link rel="icon" type="image/png" href="{{ base_path }}/images/favicon-192x192.png" sizes="192x192"/>
<link rel="icon" type="image/png" href="{{ base_path }}/images/favicon-512x512.png" sizes="512x512"/>
<link rel="manifest" href="{{ base_path }}/images/manifest.json"/>
<link rel="icon" href="{{ base_path }}/images/favicon.ico"/>
```

### PWA Manifest

The `/images/manifest.json` file configures PWA settings:

```json
{
  "name": "Your Name - Title",
  "short_name": "Initials",
  "icons": [
    { "src": "/images/favicon-192x192.png", "sizes": "192x192", "type": "image/png" },
    { "src": "/images/favicon-512x512.png", "sizes": "512x512", "type": "image/png" }
  ],
  "theme_color": "#4a90d9",
  "background_color": "#ffffff",
  "display": "standalone"
}
```

### Troubleshooting Favicon

If favicon doesn't update:
1. **Clear browser cache**: `Ctrl+Shift+R` (Windows/Linux) or `Cmd+Shift+R` (Mac)
2. **Try incognito/private window**
3. **Clear Jekyll build cache**: Delete `_site/` folder and rebuild
4. **Check file paths**: Ensure all files are in `/images/` folder

---

## Navigation Menu

### Edit Navigation Items

Open `_data/navigation.yml`:

```yaml
main:
  - title: "About Me"
    url: /

  - title: "Research"
    url: /research/

  - title: "Projects"
    url: /projects/

  - title: "Build"
    url: /build/

  - title: "Publications"
    url: /publications/

  - title: "Blog"
    url: /year-archive/

  - title: "CV"
    url: /cv/
```

### Add New Navigation Item

Add a new entry:
```yaml
  - title: "New Page"
    url: /new-page/
```

Then create the corresponding page file in `_pages/`.

### Remove Navigation Item

Delete or comment out the entry:
```yaml
  # - title: "Hidden Page"
  #   url: /hidden/
```

---

## About Me Page

**File:** `_pages/about.md`

### Summary Section

Edit the text under `## Summary`:

```markdown
## Summary

Your summary paragraph here. You can use **bold**, *italic*,
and [links](https://example.com).
```

---

### News Section

Find the `<ul class="news-list">` section:

```html
<ul class="news-list">
  <li class="news-item">
    <span class="news-date">2026 Jan:</span>
    <a href="/publication/2026-surgsync">SurgSync</a> paper submitted!
  </li>
  <li class="news-item">
    <span class="news-date">2025 Oct:</span>
    Paper accepted to ICRA 2025!
    <span class="badge badge-highlight">ICRA 2025</span>
  </li>
</ul>
```

**Add new news item:**
```html
<li class="news-item">
  <span class="news-date">YYYY Mon:</span>
  Your news text here. <a href="/link">Link text</a>
  <span class="badge badge-highlight">Optional Badge</span>
</li>
```

**Badge classes:**
| Class | Use |
|-------|-----|
| `badge-highlight` | Conference acceptances |
| `badge-award` | Awards and honors |
| `badge-spotlight` | Spotlight papers |

---

### Experience Highlights (Compact Timeline)

The About Me page uses a compact timeline format with date/location on the left and a brief description on the right.

Find `<div class="experience-highlights">`:

```html
<div class="highlight-item">
  <div class="highlight-date">
    <span class="date">2023 - Present</span>
    <span class="location">Baltimore, MD</span>
  </div>
  <div class="highlight-content">
    Visiting Graduate Scholar at <a href="https://university.edu" target="_blank">University Name</a>,
    working on research topic with <a href="https://advisor.edu" target="_blank">Prof. Advisor Name</a>.
  </div>
</div>
```

**Add new highlight:** Copy the template above and modify. Add newest entries at the top.

**Tips:**
- Keep descriptions brief (1-2 sentences)
- Use links for organizations, advisors, and labs
- Include location for context
- Combine education and work experience in chronological order

**Detailed Experience (CV page):**

For detailed experience with bullet points, see the CV page (`_pages/cv.md`):

```markdown
### Job Title
**Organization** | Location | *Date Range*
<br>*Advisor: [Prof. Name](https://url)*

- Accomplishment 1
- Accomplishment 2
```

---

### CV Timeline (Education & Experience)

The CV page (`_pages/cv.md`) uses a timeline format for both Education and Professional Experience.

**Education entry with advisor:**
```html
<div class="cv-timeline-item">
  <div class="cv-timeline-date">
    <span class="date">Sept 2020 - May 2026</span>
    <span class="location">Worcester, MA</span>
  </div>
  <div class="cv-timeline-content">
    <h3>Ph.D. in Robotics Engineering</h3>
    <span class="organization">Worcester Polytechnic Institute</span>
    <div class="advisor">Advisor: <a href="https://url" target="_blank">Prof. Name</a></div>
    <div class="gpa">GPA: 3.95/4.0</div>
    <ul>
      <li>Research focus: Topic 1, Topic 2</li>
    </ul>
  </div>
</div>
```

**Professional Experience entry:**
```html
<div class="cv-timeline-item">
  <div class="cv-timeline-date">
    <span class="date">June 2023 - Present</span>
    <span class="location">Baltimore, MD</span>
  </div>
  <div class="cv-timeline-content">
    <h3>Job Title</h3>
    <span class="organization">Company/University</span>
    <div class="advisor">Advisor: <a href="https://url" target="_blank">Prof. Name</a></div>
    <ul>
      <li>Accomplishment 1</li>
      <li>Accomplishment 2</li>
    </ul>
  </div>
</div>
```

**Optional elements:**
- `<div class="advisor">` - Add advisor with optional link
- `<div class="gpa">` - Add GPA for education entries
- `<ul>` - Add bullet points for details

---

### Education Timeline (Legacy)

For the old timeline format (if still used), find `<div class="education-timeline">`:

```html
<div class="timeline-item">
  <div class="timeline-date">
    <span class="date">Sept 2020 - May 2026</span>
    <span class="location">Worcester, MA</span>
  </div>
  <div class="timeline-content">
    <div class="degree">Ph.D. in Robotics Engineering</div>
    <span class="school">Worcester Polytechnic Institute</span>
    <div class="gpa">GPA: 3.95/4.0</div>
    <ul>
      <li>Research focus: Surgical robotics</li>
    </ul>
  </div>
</div>
```

---

### Technical Skills

Find `<div class="skills-section">`:

```html
<div class="skills-category">
  <h3><i class="fas fa-code"></i> Programming Languages</h3>
  <div class="skills-tags">
    <span class="skill-tag" data-level="expert">Python</span>
    <span class="skill-tag">C/C++</span>
    <span class="skill-tag">ROS/ROS 2</span>
  </div>
</div>
```

**Add new skill:** Add `<span class="skill-tag">Skill Name</span>`

**Mark as expert:** Add `data-level="expert"` for gradient highlight

**Add icon:** `<span class="skill-tag"><i class="fab fa-python"></i>Python</span>`

**Add new category:**
```html
<div class="skills-category">
  <h3><i class="fas fa-icon-name"></i> Category Name</h3>
  <div class="skills-tags">
    <span class="skill-tag">Skill 1</span>
  </div>
</div>
```

**Common icons:** `fa-code`, `fa-robot`, `fa-brain`, `fa-server`, `fa-wrench`

---

### Training Certificates

Find `<ul class="certificates-list">`:

```html
<li class="certificate-item">
  <span class="cert-name">Certificate Name</span>
  <span class="cert-issuer"> - Issuing Organization</span>
</li>
```

---

## Research Projects

**Folder:** `_research/`

### Create New Research Project

Create: `_research/XX-project-name.md` (XX = order number, e.g., `01`, `02`)

```yaml
---
title: "Your Research Title"
excerpt: "Short description (1-2 sentences)"
collection: research
date: 2024-01-01
venue: "University/Lab Name"
location: "City, State"

# Thumbnail image/GIF for the project card (displayed on listing page)
# Path is relative to /images/ folder
teaser: "research/your-project-thumbnail.gif"

# Tags
tags:
  - Deep Learning
  - Robotics

# Publications list (RECOMMENDED)
publications:
  - title: "First Paper Title"
    authors: "Zhou, H., Author2, et al."
    venue: "IEEE ICRA"
    year: 2025
    paper_url: "https://link-to-paper.pdf"
    arxiv_url: "https://arxiv.org/abs/..."
    video_url: "https://youtube.com/..."
    code_url: "https://github.com/..."
    award: "Best Paper Award"

  - title: "Second Paper (Under Review)"
    authors: "Zhou, H.*, CoAuthor*, et al."
    venue: "IEEE RAL"
    year: 2026
    under_review: true
    code_url: "coming_soon"
---

## Overview

Project description here.

## Key Contributions

- Contribution 1
- Contribution 2

## Media

![Demo GIF](/images/research/demo.gif)
![Result Image](/images/research/result.png)
```

### Adding Images and GIFs to Research Projects

**Step 1: Prepare your image/GIF**
- Place the file in `/images/research/` folder
- Recommended formats: `.gif`, `.png`, `.jpg`, `.webp`
- Recommended sizes:
  - Teaser thumbnail: 400x250 px (for project card)
  - Content images: 800-1200 px width
  - GIFs: Keep under 5MB for fast loading

**Step 2: Add teaser (thumbnail) for project card**

In the front matter (YAML header), add:
```yaml
teaser: "research/your-project-demo.gif"
```

This image/GIF will appear on the left side of the project card on the Research listing page.

**Step 3: Add images/GIFs in project content**

In the markdown content (after the `---`), use standard markdown:
```markdown
## Demo

![Demo Animation](/images/research/demo.gif)

## Results

![Results Figure](/images/research/results.png)
```

**Step 4: Add multiple images with captions**
```html
<div class="project-media">
  <figure>
    <img src="/images/research/figure1.png" alt="Description">
    <figcaption>Figure 1: Your caption here</figcaption>
  </figure>

  <figure>
    <img src="/images/research/animation.gif" alt="Demo">
    <figcaption>Demo: System in action</figcaption>
  </figure>
</div>
```

**Example file structure:**
```
images/
└── research/
    ├── multimodal-contact-teaser.gif    # Teaser for project card
    ├── multimodal-contact-overview.png  # Overview figure
    ├── multimodal-contact-demo.gif      # Demo animation
    └── multimodal-contact-results.png   # Results figure
```

### Publication Fields

| Field | Description |
|-------|-------------|
| `title` | Paper title (required) |
| `authors` | Author string ("Zhou, H." auto-highlighted) |
| `venue` | Conference/journal |
| `year` | Year |
| `paper_url` | Direct PDF link |
| `arxiv_url` | arXiv link |
| `video_url` | Video link |
| `code_url` | Code link (or `"coming_soon"`) |
| `award` | Award badge text |
| `under_review` | Set `true` for pending |

### Delete Research Project

Delete the `.md` file from `_research/`.

---

## Course/Personal Projects

**Folder:** `_projects/`

Same format as Research Projects. Use `collection: projects`.

### Adding Images and GIFs to Course Projects

**Step 1:** Place images in `/images/projects/` folder

**Step 2:** Add teaser in front matter:
```yaml
teaser: "projects/your-project-thumbnail.gif"
```

**Step 3:** Add images in content:
```markdown
![Project Demo](/images/projects/demo.gif)
```

**Example:**
```yaml
---
title: "Robot Arm Control Project"
excerpt: "PID control implementation for 6-DOF robot arm"
collection: projects
date: 2023-05-01
teaser: "projects/robot-arm-demo.gif"
---

## Project Overview

Description here...

## Demo

![Control Demo](/images/projects/robot-arm-demo.gif)
```

---

## Build Projects

**Folder:** `_build/`

Same format as Research Projects. Use `collection: build`.

### Adding Images and GIFs to Build Projects

**Step 1:** Place images in `/images/build/` folder

**Step 2:** Add teaser in front matter:
```yaml
teaser: "build/your-build-thumbnail.jpg"
```

**Step 3:** Add images in content:
```markdown
![Build Process](/images/build/assembly.gif)
```

**Example:**
```yaml
---
title: "Custom Sensor Mount"
excerpt: "3D printed sensor mount for dVRK instruments"
collection: build
date: 2024-02-01
teaser: "build/sensor-mount-render.png"
---

## Overview

Description here...

## Build Process

![Assembly Animation](/images/build/assembly-process.gif)
![Final Result](/images/build/final-mount.jpg)
```

---

## Publications

**Folder:** `_publications/`

### Create New Publication

Create: `_publications/YYYY-short-name.md`

```yaml
---
title: "Full Paper Title"
collection: publications
category: conferences
permalink: /publication/YYYY-short-name
excerpt: "Brief description"
date: 2024-01-01
venue: "Conference Name"

paperurl: 'https://link.pdf'
arxiv_url: 'https://arxiv.org/abs/...'
code_url: 'https://github.com/...'
video_url: 'https://youtube.com/...'

citation: 'Zhou, H., Author2, (2024). "Title." Conference.'

under_review: true
award: "Best Paper"
---

Paper details here.
```

**Categories:** `conferences`, `manuscripts`, `books`

---

## Blog Posts

**Folder:** `_posts/`

### Create New Blog Post

Create: `_posts/YYYY-MM-DD-post-title.md`

```yaml
---
title: 'Post Title'
date: 2026-01-15
permalink: /posts/2026/01/post-title/
tags:
  - cooking
  - personal
---

Your content here.

## Image Gallery

<div class="image-gallery">
  <div class="gallery-item">
    <img src="/images/cooking/dish1.jpg" alt="Description">
    <div class="caption">Caption text</div>
  </div>
</div>
```

---

## CV Page

**File:** `_pages/cv.md`

The CV page contains:
- Download button (links to PDF in `/media/`)
- Education section
- Professional Experience section
- Technical Skills section
- Link to Publications page
- Training Certificates

### Update Resume PDF

1. Replace `/media/JackHaoyingZhou_Resume_2026.pdf`
2. Or update the link in `_pages/cv.md` and `_pages/about.md`

---

## Adding Images and Media

### Directory Structure

```
images/
├── cooking/       # Blog images
├── research/      # Research project images/GIFs
├── projects/      # Course project images/GIFs
├── build/         # Build project images/GIFs
└── profile.png    # Profile photo
```

### Quick Reference: Adding Images/GIFs to Projects

| Project Type | Image Folder | Teaser Example |
|-------------|--------------|----------------|
| Research | `/images/research/` | `teaser: "research/demo.gif"` |
| Projects | `/images/projects/` | `teaser: "projects/demo.gif"` |
| Build | `/images/build/` | `teaser: "build/demo.gif"` |
| Blog | `/images/cooking/` | N/A (use inline images) |

### Two Ways to Add Images

**1. Teaser Image (Project Card Thumbnail)**

Add in the YAML front matter to show on the listing page:
```yaml
---
title: "Project Title"
teaser: "research/my-project-demo.gif"  # Relative to /images/
---
```

**2. Content Images (Inside Project Page)**

Add in the markdown content below the front matter:
```markdown
## Demo

![Demo GIF](/images/research/my-project-demo.gif)

## Results

![Results](/images/research/my-project-results.png)
```

### Supported Formats

| Format | Best For |
|--------|----------|
| `.gif` | Animations, demos |
| `.png` | Diagrams, screenshots |
| `.jpg` | Photos |
| `.webp` | Optimized web images |
| `.mp4` | Videos (use HTML embed) |

### Embedding Videos

```html
<!-- YouTube -->
<iframe width="560" height="315"
  src="https://www.youtube.com/embed/VIDEO_ID"
  frameborder="0" allowfullscreen></iframe>

<!-- Local video -->
<video width="100%" controls>
  <source src="/images/research/demo.mp4" type="video/mp4">
</video>
```

### Image Gallery (for Blog Posts)

```html
<div class="image-gallery">
  <div class="gallery-item">
    <img src="/images/cooking/dish1.jpg" alt="Description">
    <div class="caption">Caption text</div>
  </div>
  <div class="gallery-item">
    <img src="/images/cooking/dish2.jpg" alt="Description">
    <div class="caption">Caption text</div>
  </div>
</div>
```

### Recommended Sizes

| Type | Recommended Size | Notes |
|------|-----------------|-------|
| Profile photo | 300x300 px | Square, PNG or JPG |
| Teaser thumbnail | 400x250 px | 16:10 aspect ratio |
| Content images | 800-1200 px width | Auto-scales |
| GIFs | Under 5MB | Compress if larger |

### Step-by-Step: Add Image to Research Project

1. **Create the image folder** (if not exists):
   ```bash
   mkdir -p images/research
   ```

2. **Copy your image/GIF**:
   ```bash
   cp ~/my-demo.gif images/research/project-name-demo.gif
   ```

3. **Edit your project file** (`_research/XX-project.md`):
   ```yaml
   ---
   title: "My Research Project"
   teaser: "research/project-name-demo.gif"
   ---

   ## Overview
   ...

   ## Demo
   ![Demo](/images/research/project-name-demo.gif)
   ```

4. **Test locally**:
   ```bash
   bundle exec jekyll serve -l -H localhost
   ```

---

## Styling and Colors

### Color Variables

Edit `_sass/theme/_default_light.scss`:

```scss
/* Sidebar */
--sidebar-bg-color         /* Background */
--sidebar-text-color       /* Text */
--sidebar-link-bg          /* Button background */
--sidebar-link-icon        /* Icon color */

/* Timeline */
--timeline-date-color      /* Date text */
--timeline-location-color  /* Location */

/* Badges */
--badge-highlight-bg
--badge-award-bg

/* Project cards */
--project-link-color
```

### Layout Adjustments

Edit `_sass/layout/_portfolio-custom.scss`:

**Sidebar width:**
```scss
.sidebar {
  flex: 0 0 280px;   /* Change 280px */
  max-width: 280px;
}
```

**Profile photo size:**
```scss
.author__avatar {
  width: 150px;
  height: 150px;
}
```

---

## Testing Locally

### Setup

```bash
# Install dependencies
bundle install

# Run server
bundle exec jekyll serve -l -H localhost

# View at http://localhost:4000
```

### Docker

```bash
docker compose up
# View at http://localhost:4000
```

**Note:** Restart server after editing `_config.yml`.

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| Build fails | Check YAML syntax (spaces, not tabs) |
| Images missing | Verify path starts with `/images/` |
| Page not found | Check `permalink` in front matter |
| Styles unchanged | Clear browser cache, restart Jekyll |
| Sidebar wrong | Check `_config.yml` author section |

### File Naming

| Type | Format |
|------|--------|
| Research/Projects/Build | `XX-name.md` |
| Publications | `YYYY-name.md` |
| Blog posts | `YYYY-MM-DD-title.md` |

### YAML Rules

- Use spaces, not tabs
- Quote strings with special characters
- Lists: `- item`
- Dates: `YYYY-MM-DD`

---

## Quick Reference

### Add Research Project
```bash
# Create file
touch _research/05-new-project.md
# Add front matter + content
# Add image to images/research/
```

### Add Publication
```bash
touch _publications/2026-paper-name.md
```

### Add Blog Post
```bash
touch _posts/2026-01-20-post-title.md
```

### Markdown

| Format | Syntax |
|--------|--------|
| **Bold** | `**text**` |
| *Italic* | `*text*` |
| Link | `[text](url)` |
| Image | `![alt](/path)` |
| Heading | `## Heading` |

### HTML Snippets

**Badge:**
```html
<span class="badge badge-award">Award Name</span>
```

**News item:**
```html
<li class="news-item">
  <span class="news-date">2026 Jan:</span>
  News text <a href="/link">link</a>
</li>
```

**Timeline item:**
```html
<div class="timeline-item">
  <div class="timeline-date">
    <span class="date">Date Range</span>
    <span class="location">Location</span>
  </div>
  <div class="timeline-content">
    <h3>Title</h3>
    <span class="organization">Organization</span>
  </div>
</div>
```

---

## Resources

- [Jekyll Docs](https://jekyllrb.com/docs/)
- [Markdown Guide](https://www.markdownguide.org/)
- [Font Awesome Icons](https://fontawesome.com/icons)
- [Academic Pages](https://academicpages.github.io/)
