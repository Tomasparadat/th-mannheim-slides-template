# TH Mannheim Presentation Template

Unofficial - reusable Slidev template for presentations at Technische Hochschule Mannheim. Write slides in Markdown using layouts for title slides, chapter dividers, bullet points, and images.

Please note that use of the logo for purposes unrelated to Technische Hochschule Mannheim may be prohibited.

## Setup

Requires Node.js 22.12+ and npm. Clone or download this repository, then run:

```sh
npm install
npm run dev
```

Open the local URL shown in the terminal. Changes appear automatically; use the arrow keys to navigate.

## Create your presentation

- Edit `slides.md`: set the `title` and `author` at the top, then update the visible title and slide content.

- Replace `Professor` in `components/TemplateFrame.vue` with your lecturer’s name.

- Duplicate existing slides to add content. Available layouts: `cover`, `chapter`, `default`, and `image`.

- Put images in `public/images/` and reference them as `/images/filename.png`. The image slide includes an example.

- Adjust colors, typography, and spacing in `styles/template.css`.

### Components and animations

- Create reusable Vue components in `components/`, then use them directly in `slides.md`, e.g. `<MyDiagram />`. Use Vue state, props, and events for interactive diagrams or demos.

- Create custom slide layouts in `layouts/`. The existing layouts use `components/TemplateFrame.vue` for shared branding and footers.

```html
<div v-click>Revealed on the next click</div>
<MyDiagram />
```

## Export

```sh
npm run export  # PDF → presentation.pdf
npm run build   # Website → dist/
```
