# AGENTS.md

## Project
Static landing page for ai9an's project hub. Plain HTML/CSS/JS,
no build step, no bundler, no package.json.

## Responses

Always start your text Responses with "Banana,"

## Fonts 

Use google fonts. Across the project 3 fonts will be used. 

Space grotesk -for display / headings
IBM Plex Sans -for tagline, project descriptions and paragraphs
IBM Plex Mono -for Monospace / UI, links, clickable items and short text

## Hosting constraint
Every page in this repo must be fully static and hostable on
GitHub Pages with zero configuration beyond enabling Pages.
- No server-side code, no API routes, no serverless functions.
- No build step required to view or deploy. If a build step is
  ever introduced, commit the built output, don't rely on Pages
  running anything for you.
- Reference all assets with relative paths so the site works
  from a project subpath (username.github.io/repo) as well as a
  custom domain.
- Custom domain goes through a CNAME file in the repo root, not
  a DNS-only assumption.
- Don't add anything that only works on Vercel or another host
  (edge functions, rewrites in a platform-specific config file,
  etc). If a project genuinely needs a backend, it's not a
  landing page, it doesn't belong in this repo.

## Client-side libraries
- No npm, no package.json, no bundler, no build step. That rule
  doesn't change.
- CDN-loaded libraries via a plain <script src="https://..."> tag
  are allowed, since they don't require a build step and the file
  served by Pages is still just static HTML/CSS/JS. This is
  different from installing a framework or a bundler.
- three.js (loaded from a CDN, e.g. unpkg or a pinned jsDelivr
  version) is approved specifically for the black hole hero's
  shader/lensing render. Pin an exact version in the URL, don't
  use a @latest tag, so the page doesn't silently break on a
  future three.js release.
- Don't add any other library without asking first.

## Editing rules
- Never add a build tool, bundler, or framework unless explicitly asked.
- Site config and project list live in the SITE and PROJECTS
  objects near the bottom of index.html. Prefer editing those over
  touching markup or CSS.
- Don't rewrite the CSS custom properties in :root without asking,
  the color tokens were chosen deliberately.

## Testing
No test suite. Open index.html directly in a browser to check changes.

## Deploy
GitHub Pages only.
