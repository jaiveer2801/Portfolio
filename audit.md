# Project Audit

An audit of the portfolio website's structure, accessibility, responsiveness, and content.

**How to read this document:**
- **Reviewed in code** means the item was checked by reading the HTML and CSS. It was not measured in a browser.
- **To verify** means you should confirm it yourself using the checklist at the end.

No automated tool (Lighthouse, WAVE, etc.) has been run on this site, so no scores are reported here. Run those tools after deploying and record your results in the table at the bottom.

## 1. Requirements Checklist

| Requirement | Status | Notes |
|---|---|---|
| Navigation with Home, About, Skills, Projects, Contact | Done | Links point to `#home`, `#about`, `#skills`, `#projects`, `#contact` |
| Hero with name, intro, and projects button | Done | Button links to `#projects` |
| About Me section | Done | Contains generic text that needs personalizing (see section 5) |
| Skills: Python, HTML, CSS, JavaScript, Prompt Engineering | Done | Five skill cards |
| Projects: Python, portfolio, college | Done | Three cards |
| Education with placeholders | Done | Not in the nav bar (see section 4) |
| Contact with placeholders | Done | Email, GitHub, LinkedIn |
| Footer with copyright | Done | Year is hardcoded as 2026 |
| Two files: `index.html` and `style.css` | Done | Linked with `<link rel="stylesheet" href="style.css">` |
| No external libraries | Done | No JavaScript, fonts, or CDNs |
| GitHub Pages compatible | Done | Static files with relative paths |

## 2. Accessibility

| Check | Status |
|---|---|
| Semantic landmarks: `header`, `nav`, `main`, `section`, `article`, `footer` | Reviewed in code |
| One `<h1>`, with headings in order (h1, h2, h3) | Reviewed in code |
| `lang="en"` set on `<html>` | Reviewed in code |
| Skip-to-content link | Reviewed in code |
| Visible keyboard focus (`:focus-visible`) | Reviewed in code |
| `aria-label` on the nav and project links | Reviewed in code |
| External links use `rel="noopener noreferrer"` | Reviewed in code |
| Reduced-motion media query | Reviewed in code |
| Color contrast (WCAG AA) | To verify. The text colors are light on a very dark background and are expected to pass, but check with a contrast tool, especially purple text on the card background |
| Screen reader behavior | To verify |

**Known accessibility issues:**
- Several links share generic text such as "View Project". Each has an `aria-label`, but update the labels when you add real project names.
- Contact links open in a new tab without warning the user. Consider adding "(opens in new tab)" to the label.

## 3. Responsiveness

| Check | Status |
|---|---|
| Viewport meta tag | Reviewed in code |
| Fluid grids (`auto-fit` / `minmax`) for skills and projects | Reviewed in code |
| Fluid hero heading with `clamp()` | Reviewed in code |
| Breakpoints at 768px and 480px | Reviewed in code |
| Actual rendering on phone, tablet, and desktop | To verify |

**Known limitation:** The nav bar has no hamburger menu. On narrow screens the links wrap onto multiple lines, which works but takes more vertical space.

## 4. Known Issues and Limitations

1. **Education is not in the navigation bar.** You specified five nav links, so it is reachable only by scrolling. Add `<li><a href="#education">Education</a></li>` if you want it in the nav.
2. **Placeholder links.** Project cards use `href="#"`, which scrolls to the top of the page when clicked. Replace them before publishing.
3. **Placeholder contact links.** The email, GitHub, and LinkedIn `href` values are examples and do not work until you edit them.
4. **No favicon.** Browsers will show a default icon.
5. **No social preview metadata.** There are no Open Graph tags, so shared links will not show a custom image or title.
6. **Gradient hero name.** The name uses `background-clip: text` with transparent text. This is supported in current major browsers, but a very old browser may show the name poorly.
7. **Hardcoded year** in the footer. Update it manually each year.

## 5. Content Review (important)

The following text was written as neutral filler and has not been verified by you. Edit anything that does not match your actual situation:

- **About Me:** the first two paragraphs are generic statements about your interests.
- **Hero text:** the line about "turning ideas into working software".
- **Skill descriptions:** one-line descriptions under each skill are generic and do not state a proficiency level.
- **Portfolio Website card:** it says the site is hosted on GitHub Pages. This is only true once you deploy it.

No achievements, grades, employers, certificates, or experience have been invented. All personal details are placeholders in `[square brackets]`.

## 6. Performance and Security

- **Performance:** only two small static files, no images, no scripts, and no external requests (reviewed in code). Add `loading="lazy"` and sized dimensions if you add images later.
- **Security:** no forms, no user input, and no third-party scripts. External links use `noopener noreferrer`.

## 7. Pre-Publish Checklist

- [ ] Replace every `[placeholder]` in `index.html`
- [ ] Update project card `href="#"` links
- [ ] Update email, GitHub, and LinkedIn links
- [ ] Review and personalize all text listed in section 5
- [ ] Test at mobile, tablet, and desktop widths (browser DevTools device mode)
- [ ] Tab through the whole page with the keyboard
- [ ] Click every nav link and confirm it reaches the right section
- [ ] Run Lighthouse (Chrome DevTools) and record the results below
- [ ] Check contrast with a tool such as the WebAIM Contrast Checker
- [ ] Validate HTML at https://validator.w3.org and CSS at https://jigsaw.w3.org/css-validator
- [ ] Confirm the live GitHub Pages URL works

## 8. Results Log

Fill this in after testing.

| Test | Date | Result |
|---|---|---|
| Lighthouse Performance | | |
| Lighthouse Accessibility | | |
| Lighthouse Best Practices | | |
| Lighthouse SEO | | |
| HTML validator | | |
| CSS validator | | |
| Manual keyboard test | | |
| Mobile device test | | |

## 9. Suggested Future Improvements

- Add a mobile hamburger menu (this needs a little JavaScript)
- Add a favicon and Open Graph tags
- Add screenshots to project cards
- Add a downloadable resume link
- Add an active-link highlight in the nav while scrolling
- Add a LICENSE file
