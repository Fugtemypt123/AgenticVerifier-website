# VIGA: Vision-as-Inverse-Graphics as a VLM Coding Agent

Academic project website for VIGA.

## 🚀 Quick Start

Simply open `index.html` in a web browser to view the website locally.

For deployment, you can host the entire folder on any static hosting service (GitHub Pages, Netlify, Vercel, etc.).

## 📁 Project Structure

```
AgenticVerifier-website/
├── index.html              # Main website file
├── README.md               # This file
├── assets/                 # Image assets (create this folder)
│   ├── static/             # Static scene images
│   │   ├── scene1_input.jpg
│   │   ├── scene2_input.jpg
│   │   └── ...
│   └── dynamic/            # Dynamic scene images
│       ├── scene1_input.jpg
│       └── ...
└── video/                  # Video assets (create this folder)
    ├── pipeline.mp4        # Main pipeline video
    ├── static/             # Static scene output videos
    │   ├── scene1_output.mp4
    │   └── ...
    └── dynamic/            # Dynamic scene output videos
        ├── scene1_output.mp4
        └── ...
```

## 🎨 Customization Guide

### 1. Replace Placeholder Content

#### Hero Section
- Update the conference badge (e.g., "NeurIPS 2025")
- Modify the title and subtitle
- Update author names and affiliations
- Add links to paper, code, dataset, and video

#### Abstract
- Replace the placeholder abstract with your actual abstract

#### Pipeline Video
In the `#pipeline` section, uncomment the video element and update the path:
```html
<video controls poster="assets/pipeline_poster.jpg">
    <source src="video/pipeline.mp4" type="video/mp4">
</video>
```

#### Static Scenes
For each result card in the `#static` tab:
1. Update the scene title
2. Replace the image placeholder with actual image:
```html
<img src="assets/static/scene1_input.jpg" alt="Input">
```
3. Replace the video placeholder:
```html
<video controls muted loop>
    <source src="video/static/scene1_output.mp4" type="video/mp4">
</video>
```

#### Dynamic Scenes
For each result card in the `#dynamic` tab:
1. Update the scene title
2. Update the text description/prompt
3. Replace image and video placeholders (same as static scenes)

#### Quantitative Results
Update the tables with your actual experimental results:
- Modify method names
- Update metric values
- Add `.best-score` class to highlight best results

#### BibTeX
Update the citation with your actual paper information.

### 2. Adding More Results

To add more result cards, copy an existing card structure:

```html
<div class="result-card scroll-animate">
    <div class="result-header">
        <h4>Scene Title</h4>
        <p>"Optional description for dynamic scenes"</p>
    </div>
    <div class="result-media">
        <div class="media-item">
            <img src="assets/your_image.jpg" alt="Input">
            <span class="media-label">Input</span>
        </div>
        <div class="media-item">
            <video controls muted loop>
                <source src="video/your_video.mp4" type="video/mp4">
            </video>
            <span class="media-label">Output</span>
        </div>
    </div>
</div>
```

### 3. Styling Customization

The CSS uses CSS variables for easy theming. Modify these in `:root`:

```css
:root {
    --bg-primary: #0a0a0f;        /* Main background */
    --accent-primary: #f7b267;     /* Primary accent color */
    --accent-secondary: #e8985a;   /* Secondary accent color */
    /* ... more variables */
}
```

## 🌐 Deployment

### GitHub Pages
1. Push this folder to a GitHub repository
2. Go to Settings → Pages
3. Select the branch and folder containing `index.html`
4. Your site will be available at `https://username.github.io/repo-name/`

### Netlify / Vercel
1. Connect your repository
2. Set the publish directory to the folder containing `index.html`
3. Deploy

## 📝 Notes

- All fonts are loaded from Google Fonts
- Icons are from Font Awesome CDN
- No build process required - pure HTML/CSS/JS
- Responsive design works on mobile and desktop
- Scroll animations are enabled for visual polish

## 🎬 Video Recommendations

- **Pipeline video**: MP4 format, 1080p or 720p, H.264 codec
- **Result videos**: MP4 format, shorter clips (5-15 seconds), consider adding loop
- **Poster images**: Add `poster` attribute to video elements for thumbnails

## License

Feel free to use and modify this template for your academic projects.

