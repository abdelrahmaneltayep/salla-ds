# Salla Design System — Component Kit

A self-contained reference kit for the **Salla merchant dashboard design system** — **38 components / 178 variants**. Each variant shows the live web component rendered from the Salla runtime plus its copy-pasteable markup.

## Contents

| Path | Description |
| --- | --- |
| [`index.html`](index.html) | The full interactive kit — nav, live previews, code toggles, RTL/LTR switch. Open in a browser (needs internet to hydrate). |
| [`assets/components/`](assets/components/) | Per-component snippet files, one `<slug>.html` per component, with each variant labelled. |

## Viewing the kit

The kit is a single static HTML file. Any of these work:

- Open `index.html` directly in a browser, **or**
- Serve it locally: `python3 -m http.server` then visit <http://localhost:8000/>, **or**
- Publish the repo with GitHub Pages / Cloudflare Pages and open the root URL.

> An internet connection is required at view time: the components hydrate from the live Salla runtime and CDN fonts. Nothing is bundled locally.

## Runtime sources

The components are Web Components (`<s-*>` custom elements). The kit loads the same runtime the Salla merchant dashboard Storybook uses:

| Source | URL |
| --- | --- |
| Component runtime (ESM) | `https://dashboard-ui-components.pages.dev/admin-ui.esm.js` |
| Component runtime (nomodule) | `https://dashboard-ui-components.pages.dev/admin-ui.js` |
| Component styles | `https://dashboard-ui-components.pages.dev/styles.css` |
| Fonts (PingARLT) | `https://cdn.salla.network/fonts/pingarlt.css` |
| Icons (Hugeicons) | `https://cdn.salla.network/fonts/hugeicons-font.min.css` |
| Icons (Salla icons) | `https://cdn.salla.network/fonts/sallaicons-light.min.css` |

Live component docs (Storybook): <https://dashboard-ui-components.pages.dev/?path=/docs/components-accordion--docs>

## Components

| Component | Tag | Variants | Snippets |
| --- | --- | --- | --- |
| Accordion | `<s-accordion>` | 5 | [`accordion.html`](assets/components/accordion.html) |
| AlertBox | `<s-alert-box>` | 5 | [`alertbox.html`](assets/components/alertbox.html) |
| Avatar | `<s-avatar>` | 5 | [`avatar.html`](assets/components/avatar.html) |
| Breadcrumbs | `<s-breadcrumbs>` | 5 | [`breadcrumbs.html`](assets/components/breadcrumbs.html) |
| Button | `<s-button>` | 8 | [`button.html`](assets/components/button.html) |
| ButtonsGroup | `<s-buttons-group>` | 5 | [`buttonsgroup.html`](assets/components/buttonsgroup.html) |
| Calendar | `<s-calendar>` | 5 | [`calendar.html`](assets/components/calendar.html) |
| Checkbox | `<s-checkbox>` | 5 | [`checkbox.html`](assets/components/checkbox.html) |
| ColorPicker | `<s-color-picker>` | 5 | [`colorpicker.html`](assets/components/colorpicker.html) |
| Dropdown | `<s-dropdown>` | 5 | [`dropdown.html`](assets/components/dropdown.html) |
| Editor | `<s-editor>` | 2 | [`editor.html`](assets/components/editor.html) |
| Header | `<s-button>` | 7 | [`header.html`](assets/components/header.html) |
| Icon | `<s-icon>` | 1 | [`icon.html`](assets/components/icon.html) |
| Input | `<s-input>` | 5 | [`input.html`](assets/components/input.html) |
| Item | `<s-list-item>` | 1 | [`item.html`](assets/components/item.html) |
| LingualField | `<s-lingual-field>` | 5 | [`lingualfield.html`](assets/components/lingualfield.html) |
| Loader | `<s-loader>` | 1 | [`loader.html`](assets/components/loader.html) |
| Maps | `<s-maps>` | 4 | [`maps.html`](assets/components/maps.html) |
| Modal | `<s-button>` | 1 | [`modal.html`](assets/components/modal.html) |
| OTP | `<s-otp>` | 5 | [`otp.html`](assets/components/otp.html) |
| Panel | `<s-panel>` | 5 | [`panel.html`](assets/components/panel.html) |
| Placeholder | `<s-placeholder>` | 3 | [`placeholder.html`](assets/components/placeholder.html) |
| Progress Bar | `<s-progress-bar>` | 5 | [`progress-bar.html`](assets/components/progress-bar.html) |
| Qty | `<s-qty>` | 5 | [`qty.html`](assets/components/qty.html) |
| Radio | `<s-radio>` | 5 | [`radio.html`](assets/components/radio.html) |
| Range Slider | `<s-range-slider>` | 5 | [`range-slider.html`](assets/components/range-slider.html) |
| Rate | `<s-rate>` | 5 | [`rate.html`](assets/components/rate.html) |
| Select | `<s-select>` | 5 | [`select.html`](assets/components/select.html) |
| Skeleton | `<s-skeleton>` | 5 | [`skeleton.html`](assets/components/skeleton.html) |
| Table | `<s-panel>` | 11 | [`table.html`](assets/components/table.html) |
| Tabs | `<s-tabs-group>` | 5 | [`tabs.html`](assets/components/tabs.html) |
| Tag | `<s-tag>` | 5 | [`tag.html`](assets/components/tag.html) |
| Tags Input | `<s-tags>` | 5 | [`tags-input.html`](assets/components/tags-input.html) |
| Telephone Input | `<s-tel-input>` | 4 | [`telephone-input.html`](assets/components/telephone-input.html) |
| Textarea | `<s-textarea>` | 5 | [`textarea.html`](assets/components/textarea.html) |
| Toggle | `<s-toggle>` | 5 | [`toggle.html`](assets/components/toggle.html) |
| Tooltip | `<s-tooltip>` | 5 | [`tooltip.html`](assets/components/tooltip.html) |
| Uploader | `<s-uploader>` | 5 | [`uploader.html`](assets/components/uploader.html) |

**Total: 38 components · 178 variants.**

## Usage

To use a component in your own page, load the runtime + styles in `<head>`:

```html
<link rel="stylesheet" href="https://dashboard-ui-components.pages.dev/styles.css">
<script type="module" src="https://dashboard-ui-components.pages.dev/admin-ui.esm.js"></script>
<script nomodule src="https://dashboard-ui-components.pages.dev/admin-ui.js"></script>
```

Then drop in any snippet from `assets/components/`, e.g.:

```html
<s-button theme="default" size="md">نص بديل</s-button>
```

The design system is RTL-first (Arabic). Set `dir="rtl"` on the document for Arabic layout; the kit's header has an **RTL ⇄ LTR** toggle to preview both.
