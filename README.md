# Personal Portfolio Website

A responsive personal portfolio for a college student learning programming, web development, and prompt engineering. It is built with plain HTML5 and CSS3, with no frameworks, no JavaScript, and no external dependencies.

**Live site:** `https://your-username.github.io/your-repo-name/` *(replace after deploying)*

## Features

- Sticky navigation bar with smooth-scrolling links
- Hero section with an intro and a call-to-action button
- About, Skills, Projects, Education, and Contact sections
- Dark theme with blue and purple accent colors
- Responsive layout for desktop, tablet, and mobile
- Semantic HTML, a skip-to-content link, and visible keyboard focus styles
- Respects the `prefers-reduced-motion` setting
- Hover effects built with CSS only

## Project Structure

```
.
├── index.html   # Page structure and content
├── style.css    # All styling and responsive rules
├── README.md    # Project documentation
└── AUDIT.md     # Quality, accessibility, and content audit
```

## Run Locally

1. Clone or download this repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```
2. Open `index.html` in any modern browser (double-click it).
3. Optional: in VS Code, install the **Live Server** extension, right-click `index.html`, and choose **Open with Live Server** for automatic reloads.

## Customize

Every item that needs your information is written in square brackets. Search `index.html` for `[` to find them all:

| Placeholder | Where |
|---|---|
| `[Your Name]` | Page title, nav, hero, footer |
| `[Your Degree]`, `[Your College Name]`, `[Graduation Year]` | Education section |
| `[Describe your ... project ...]` | Project cards |
| `[your.email@example.com]`, `[your-username]`, `[your-profile]` | Contact section (also update the matching `href` values) |

Also update the project card links (`href="#"`) to point to your real repositories or demos.

To change the colors, edit the variables at the top of `style.css`:

```css
:root {
  --bg: #0b1020;
  --accent: #38bdf8;
  --accent-2: #a78bfa;
}
```

## Deploy with GitHub Pages

1. Push `index.html` and `style.css` to the root of your repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose the `main` branch and the `/ (root)` folder, then click **Save**.
5. Your site will be live in a minute or two.

## Browser Support

Works in current versions of Chrome, Edge, Firefox, and Safari.

## License

This project is licensed under the [MIT License](LICENSE). *(Add a LICENSE file, or remove this section.)*
