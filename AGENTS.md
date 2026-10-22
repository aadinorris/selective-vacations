# AGENTS.md — Selective Vacations

Single-file static site. `index.html` (~2600 lines) holds all CSS (`<style>`) and JS (one `<script>`); `assets/images/` holds 8 local JPGs. No bundler, tests, lint, CI, or README. Only external dep is Google Fonts CDN.

## Verify changes (no test runner exists)

```bash
python3 -c "
from html.parser import HTMLParser
src = open('index.html').read()
# fail on unclosed/mismatched tags; also check CSS '{' == '}' counts and </html> ending
"
grep -o -i -E "1F2A44|E8DCC8|C6A75E" index.html  # must be empty: old palette fully removed
```

Node is NOT installed — don't use it for JS checks. Balance-check JS braces/parens with python instead.

## Structure that breaks easily

- Hero slider JS queries exact hooks: `.hero-slide`, `.thumb-card`, `#hero-title-text`, `#hero-desc-text`, `#hero-eyebrow`, `#slide-num-current`. Renaming any of these breaks `switchSlide/prevSlide/nextSlide`.
- Inquiry form: `handleHeroSearchSubmit` + select IDs `hero-search-dest/season/party`. Modal: `openTripModal/closeTripModal` + `#trip-modal`. Drawer: `openItineraryDrawer/closeItineraryDrawer` + `#drawer-itinerary`.
- Anchor IDs used by nav: `#destinations #journeys #why-selective #contact` (footer carries `id="contact"`), `#styles #shailendra #hero`. Don't rename/remove without updating links.
- Hero is absolute-positioned zones (`.hero-left` at 7.5vw/37%, `.hero-thumbs-queue` at 78%/30%, `.hero-filter-bar-wrapper` at 5.5vw margins/5vh bottom) inside a `height:100vh` container — there is intentionally no content wrapper. Re-adding one breaks the composition.
- Design tokens live in `:root` (`--bg-*`, `--color-champagne/gold`, `--color-text-*`, `--border-glass*`). Approved palette: `#18263D #F1ECE2 #B89552 #A9A39A` (+ derived ivory card tints `#E7DECD/#F8F4EB`, WhatsApp greens, white neutrals). Never reintroduce gradients/glows/glassmorphism beyond what exists.

## Working conventions

- The owner scopes tasks tightly ("ONLY the hero", "palette only"). Respect the stated scope exactly; don't improve adjacent code.
- `index.html` usually has uncommitted changes (`git status`) — check the diff before editing so you don't clobber in-progress work.
- Prefer the `edit` tool with small unique `oldString` blocks over rewrites; the file is large and full rewrites risk damage.
