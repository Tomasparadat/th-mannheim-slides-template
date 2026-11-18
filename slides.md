---
theme: none
title: Präsentationstitel
author: Student
info: |
  Slidev implementation of Disclaimer-und-Layoutvorgabe.pptx.
  German placeholders and reusable slide layouts.
lang: de
aspectRatio: 24382413/13684250
canvasWidth: 1280
colorSchema: light
fonts:
  sans: Plus Jakarta Sans
  local: Plus Jakarta Sans
drawings:
  enabled: false
transition: none
layout: cover
---

# Präsentationstitel

---
layout: chapter
---

# Neues Thema

---
layout: default
---

# Überschrift

- Punkte
- Punkte
- Punkte

---
layout: image
---

# Überschrift

<div class="image-area">
  Bild
</div>

<!-- Replace the image-area div with an image, for example:
<div class="image-area"><img src="/images/your-image.png" alt="Beschreibung" /></div>
-->

---
layout: default
---

# Komponenten und Animationen

<v-clicks>

- Inhalte mit jedem Klick einblenden
- Vue-Komponenten direkt in Markdown verwenden
- Den Zähler unten mit den Buttons ausprobieren

</v-clicks>

<!-- Defined in components/CounterDemo.vue; the label is a Vue prop.
     Vue state updates the counter; <Transition> animates each change. -->
<div style="position: absolute; left: 8.586%; top: 43%; width: 60%;">
  <CounterDemo label="Interaktives Beispiel" />
</div>
