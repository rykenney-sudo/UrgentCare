# Norwood Urgent Care — design system rollout

`site/` is the updated site. `uploads/norwood-urgent-care-site/` is untouched as the original.

## How it works
- **`site.css`** holds the whole shared layer, taken from `index.html`: tokens, type scale, buttons, header, footer, and shared components (service/testimonial/location/clinician cards, FAQ, comparison table, chips, bands, print rules).
- **Each page** links `site.css` first, then keeps only its own page-specific layout in its inline `<style>`. Every rule that duplicated the shared layer was removed, so a change to a button, nav item, or footer is now one edit in `site.css`.
- **`index.html` is unchanged** — it still carries its own inline copy of the same CSS. When you're ready, delete its shared block and link `site.css` too.

## What changed on the other 20 pages
- Fonts: Bricolage Grotesque / IBM Plex Sans → Oswald headings (`--head`) on Open Sans body (`--display`, `--body`).
- Serif accents: PT Serif → **Noto Serif** (`--serif`), per request.
- CTAs: navy `--cta` primary, outlined `--cta` ghost, uppercase labels with letter-spacing.
- Header and footer markup replaced with the index versions (same logo, nav, mobile panel, mobile action bar, 4-column footer).
- Link system: uppercase nav/utility/footer links with the red underline on hover.
- Layouts, content, and section order untouched.

## Tokens
Colors `--ink --ink-soft --ink-faint --brand --brand-deep --accent --brand-tint --cta --cta-deep --er --live --surface --surface-tint --border --border-soft`;
type `--head --display --body --serif`; `--shadow --shadow-hi --maxw --nav-h`.
