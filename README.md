# Cleveland Lead Abatement Pros - Bootstrap edition

Separate Bootstrap 5.3.8 rebuild of the Cleveland preview. This package does not replace the existing Astro site.

## Open it

Unzip the folder and open `index.html`. All 28 HTML pages, images, styles, Bootstrap CSS and Bootstrap JavaScript are included locally. Internal links use relative paths, so the site can be viewed from disk or served from any folder.

For a local server with Node.js 22 or newer:

    npm start

Then open http://localhost:8080.

## Change the phone

Edit only `phone` in `config/site.mjs`, then run:

    npm run build

No npm install is needed. The builder updates visible numbers, all call links and Organization schema across all 28 pages. The packaged number is (877) 378-5996. The site does not read Google Sheets.

## What is inside

- 27 site pages plus 404.html
- `config/site.mjs`: single phone configuration and canonical origin/base
- `source/pages.json`: complete copy and page templates
- `scripts/build.mjs`: dependency-free HTML builder
- `scripts/serve.mjs`: optional dependency-free local server
- `assets/css/site.css`: original design and call animations
- `assets/css/bootstrap-fidelity.css`: exact visual adjustments for Bootstrap
- `assets/vendor/bootstrap/`: local custom Bootstrap CSS, full bundle JS and MIT license
- `source/bootstrap.scss`: Bootstrap source component selection and exact breakpoints
- `assets/js/lead-form.js`: original lead form validation/confirmation logic
- `assets/img/`: all original images, logo and favicon

Pages are built as named .html files (services/lead-risk-assessment.html, not folder/index.html) so website importers keep each page's real name and slug. The root page stays index.html.

Hero backgrounds are emitted inline on the section element by scripts/build.mjs (literal gradient, image URL and fallback color, no CSS custom properties) so website importers keep the hero image and color at every viewport; assets/css/site.css keeps a literal fallback.

Bootstrap's responsive grid powers the hero and card grids. Bootstrap Collapse powers the mobile navigation and nested menus. Form controls, buttons and cards use Bootstrap components with the original design preserved. Bootstrap Reboot is omitted so it does not alter the approved typography. The precompiled custom CSS is included; to change its component selection, compile source/bootstrap.scss using Sass and Bootstrap 5.3.8.

The original form IDs and Airchatty tracking script are preserved. Submissions still require an internet connection and the existing external service; they were not submitted during verification. The emergency contact numbers in the copy are intentionally unchanged.

The pages retain noindex, follow and robots.txt blocks all crawling. Canonical/OG URLs remain the existing preview URL. Update origin/base and rebuild only if this separate version is later hosted elsewhere. No deployment, analytics setup, Search Console setup or production launch is included.
