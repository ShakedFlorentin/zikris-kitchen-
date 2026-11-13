# zikris-kitchen-

Website for **Zikry Kitchens · זיקרי מטבחים**, a family carpentry shop from Jerusalem that builds custom kitchens and interior woodwork.

**Live site:** https://shakedflorentin.github.io/zikris-kitchen-/ (deployed by GitHub Actions on every push to `main`)

## The idea

The page opens the way their work does.

- **Hero:** three cream cabinets with gold handles stand shut. The doors swing open in 3D, the light inside comes on, and each cabinet shows a kitchen. Moving the pointer lets you look around the open doors.
- **Materials strip:** materials from the real projects. It drifts slowly, speeds up with your scroll, and reverses when you scroll up.
- **Work:** on desktop the section pins and five kitchens pass by as you scroll, each panel turning like a door as it crosses the middle. On phones it is a swipe row with the same motion. Click a kitchen for a full-screen gallery.
- **Workshop:** a statement that lights up word by word, beside a photo that is uncovered as you scroll.
- **How it works:** four steps under a line that lights up like an under-cabinet LED strip.
- **Customer quote, contact, footer.**

## Contact form

There is no server. The form checks the name and phone number, then opens WhatsApp with a ready message to the business number. The visitor presses send. To change the number, search `index.html` for `972509358333`.

## Accessibility

Hebrew and RTL throughout. The accessibility menu has larger text, high contrast, a readable font, link highlighting and **stop animations**. Stop animations removes all GSAP and Lenis motion live, and `prefers-reduced-motion` gets the same treatment. Without JavaScript the content is all there, with the cabinet doors already open. The footer links to an accessibility statement. **The statement text should be reviewed by the business before launch**, in particular the compliance line and the contact details.

## Before moving to a custom domain

These hold the GitHub Pages address and need the new one:

- `index.html`: `og:url`, `og:image`, and the `url` and `image` fields in the JSON-LD block.
- `robots.txt` and `sitemap.xml`.
- `404.html`: the links start with `/zikris-kitchen-/`.

## Files

- `index.html`: the page, with inline CSS and JS.
- `404.html`, `robots.txt`, `sitemap.xml`, `.nojekyll`: GitHub Pages housekeeping.
- `assets/`: logo, project photos, favicon, touch icon and the share image (`og.jpg`).
- `assets/fonts/`: Frank Ruhl Libre and Assistant, self-hosted (SIL Open Font License).
- `assets/vendor/`: self-hosted libraries. The site makes no third-party requests.
  - GSAP 3.15.0 with ScrollTrigger and SplitText: free including plugins, under the [GSAP standard license](https://gsap.com/standard-license).
  - Lenis 1.3.27 (MIT).

There's no build step. `.github/workflows/deploy.yml` publishes the repository to GitHub Pages whenever `main` changes. To preview locally, serve the folder (for example `python3 -m http.server`).
