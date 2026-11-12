# zikris-kitchen-

Landing page prototype for **Zikry Kitchens · זיקרי מטבחים**, a family carpentry shop making boutique, custom kitchens and interior woodwork.

## Concept: a slow ballet

The site presents luxury, boutique kitchens with controlled, theatrical movement:

- **Curtain intro** (first visit in a session): the logo appears, then the curtain parts.
- **Hero, the stage:** the serif headline rises letter by letter. Three kitchens in stage arches sway out of step. A brass ribbon draws itself between them, and the stage lights swing slowly. Photos and a spotlight follow the pointer. On scroll, the dancers drift away at different depths.
- **Details strip:** materials from the real projects (gold handles, oak, smoked glass…). It drifts slowly, speeds up with your scroll, and reverses when you scroll up.
- **The collection:** on desktop the section pins and the five kitchens pass by as you scroll, dancing on an arc as they cross the centre, with a counter and progress line. On phones it's a native swipe row with the same arc motion. Click a kitchen for a full-screen gallery.
- **Studio:** a statement that lights up word by word, beside a photo revealed like a rising curtain.
- **Process:** four counts on a wave that draws itself as you scroll.
- **Testimonial, contact, footer:** lines rise out of a mask. Includes a phone link, WhatsApp, and a lead form (preview only).
- **Details:** a custom cursor reads "לצפייה" over kitchens, buttons are magnetic, and Lenis gives smooth, weighted scrolling.

## Accessibility

Hebrew and RTL throughout. The accessibility menu has larger text, high contrast, a readable font, link highlighting and **stop animations**. Stop animations tears down all GSAP and Lenis motion live, and the page is complete without it. `prefers-reduced-motion` gets the same treatment. Without JavaScript, everything is visible and static.

## Files

- `index.html`: the page, with inline CSS and JS.
- `assets/`: logo and project photos.
- `assets/vendor/`: self-hosted libraries, so there's no CDN dependency.
  - GSAP 3.15.0 with ScrollTrigger, SplitText and DrawSVG: free including plugins, under the [GSAP standard license](https://gsap.com/standard-license).
  - Lenis 1.3.27 (MIT).

There's no build step. Drag the folder onto Netlify, or serve it locally (for example `python3 -m http.server`).
