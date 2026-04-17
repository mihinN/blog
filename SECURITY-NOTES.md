# Fixes applied to Melk0reVSHere site

## Security

1. **Content Security Policy** added to every HTML file via `<meta http-equiv>`. Blocks inline scripts from unknown origins, restricts images/scripts/styles to same-origin, blocks the page from being framed (clickjacking defense via `frame-ancestors 'none'`), and blocks plugin content (`object-src 'none'`). `index.html` keeps `'unsafe-inline'` for scripts because the cat/CRT logic is inline — move that into a file and you can drop that allowance too.

2. **`rel="noopener noreferrer"`** added to every external link (github, linkedin, substack). Without this, a malicious landing page can use `window.opener` to redirect the tab you came from (tabnabbing). Also added `target="_blank"` for external links so they open in a new tab, which is the normal expectation.

3. **Referrer policy** set to `strict-origin-when-cross-origin` so you're not leaking full URLs to third parties.

4. **`X-Content-Type-Options: nosniff`** meta tag — prevents a browser from deciding a `.txt` (or anything else) is actually HTML/JS.

5. **XSS surface in chat bubbles closed.** The original code did `bubble.innerHTML = msg.text` with a static array — fine today, but the moment you wire it to URL params, localStorage, or an API, it becomes an XSS hole. Rewrote messages as structured segments (`{cls, text}` pairs) and render them via `createElement` + `textContent` with a whitelist of allowed classes. Same output, zero injection surface.

6. **Sprite filename sanitization** in `script.js`: `data-cat` attribute is now checked — only relative paths are accepted, not `http://…`, `javascript:`, or `data:` URLs. Small thing, but if someone ever loads your script on a page they control, they can't swap the sprite for an exfil URL.

## Bugs

7. **`prefers-reduced-motion` check was dead code.** `window.matchMedia(x) === true` is never true — `matchMedia` returns an object. The accessibility guard was half-broken. Fixed.

8. **`nekoEl.ariaHidden = true`** — wrong: the IDL reflects as a string, not a boolean. Changed to `setAttribute("aria-hidden", "true")`.

9. **Invalid HTML: stray `</div>`** after `</main>` in `index.html`, `the_9.html`, `rabbit_hole.html`. Removed.

10. **Invalid HTML: `<h3>` inside `<button>`** on `the_9.html` and `rabbit_hole.html`. Buttons can't contain headings semantically. Changed to plain button text.

11. **Invalid HTML: `<h3>` and `<br>` mixed inside `<p>`** on `index.html`. The `<p>` was auto-closing in weird places. Split into separate `<p>`/`<h3>` elements.

12. **`projects.html` global link override.** The rule `nav, a { color:#536EDF }` recolored *every* link on the page including footer/header links. Scoped to `.hero a` only.

13. **Missing `<br>`** between items 0x04 and 0x05 on `projects.html` — they ran into each other.

14. **`the_9.html` title said `RABBITHOLE 1.0v`** (copy-paste from the other project page). Fixed.

15. **Leftover AI prompt in `the_9.html`**: the sentence starting *"If you want it shorter, more technical, or more sales-focused…"* was visible on the public page. Removed.

16. **Typos**: "sniifing" → "sniffing", "Extesnion" → "Extension", "LINKDIN" → "LINKEDIN".

17. **Empty `<style>` blocks** in `whoami.html` — removed.

18. **Timeout leaks.** The chat sequence fired a chain of `setTimeout`s with no cancellation. If the user clicked the apologize button mid-sequence, timers kept firing and appending bubbles into a hidden element. All timers are now tracked and cleared on close.

19. **Static noise animation ran forever.** `stopStaticNoise()` was defined but not called when the overlay faded out during the shutdown sequence — only when the user pressed "apologize". Added a `stopStaticNoise()` call after the static fades so CPU drops to zero when invisible.

20. **`<button>` elements missing `type="button"`.** Inside a `<form>` they'd default to `type="submit"`. Not an issue today, but cheap insurance.

## Files that changed
- `index.html` — CSP, external-link hardening, XSS-safe chat renderer, timer cleanup, aria-hidden on overlay, button type, typos.
- `whoami.html` — CSP, cleanup.
- `projects.html` — CSP, scoped link color, added `<br>`, spelling.
- `projects/the_9/the_9.html` — CSP, fixed title, removed AI leftover, removed `h3`-in-button, fixed stray `</div>`, cleaned copy.
- `projects/rabbitHole/rabbit_hole.html` — CSP, same structural fixes as above.
- `js/script.js` — `prefers-reduced-motion` fix, `aria-hidden` fix, sprite-path sanitization, `'use strict'`.
- `css/style.css` — unchanged.
- `js/oneko.gif` — unchanged, moved into `js/` to match the script's expected path.

## Things I didn't touch (but you should know)
- Your site is entirely client-side static, so there's no server-side authz/input validation to worry about yet. If you add any backend (contact form, search, etc.), everything that comes from the URL/user/network needs to be treated as hostile — use `textContent`, not `innerHTML`, and validate types on the server too.
- The `#` placeholder links on `projects.html` (SOURCE, DOCUMENT entries 0x02/0x03) still go nowhere. Not a bug per se, but users will click them and bounce.
- Substack, GitHub, and LinkedIn links are fine and tested against normal phishing patterns — just make sure you never paste untrusted URLs there in the future without re-checking them.
