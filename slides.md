---
theme: none
colorSchema: light
layout: cover
title: 'Presentation Title'
info: |
  One or two sentences describing the talk.
# Shown on the cover and in every slide footer
footer: 'Your Name | Institute | Course / Event | Date'
# Logo files in public/ (not included, see README). Missing files are simply not shown.
logo: /logo.svg        # small mark, top right of content and section slides
logoLong: /logo-long.png  # long version, top right of the cover
drawings:
  persist: false
transition: slide-left
mdc: true
---

# Presentation Title

Subtitle goes here,<br/>can span two lines

---

# Plain Content Slide

<p class="takeaway">One-line takeaway: the single thing the audience should remember from this slide.</p>

- Bullets are 17px Arial in TU dark grey, headings in TU red.
- Everything below the title is centred between title and footer.
- Use `inline code`, **bold** and [links](https://sli.dev) as usual.
- Keep it to four or five bullets per slide.

---
layout: split
---

# Split Slide: Text Left, Visual Right

::left::

- `layout: split` gives you two columns.
- Put text in `::left::` and an image, table or diagram in `::right::`.
- Change the ratio with `cols: 3fr 2fr` in the frontmatter.

::right::

<img src="/placeholder.svg" />

---
layout: split
class: table-split
---

# Split Slide with a Table

::left::

- `class: table-split` makes the text column narrow so a wide table fits.
- Tables use `class="info-table"`.

::right::

<table class="info-table">
  <thead>
    <tr><th>Setting</th><th>Value</th><th>Notes</th></tr>
  </thead>
  <tbody>
    <tr><td>Runs</td><td>20</td><td>Per configuration</td></tr>
    <tr><td>Duration</td><td>60 s</td><td>Steady state</td></tr>
    <tr><td>Hardware</td><td>Example</td><td>Lab testbed</td></tr>
  </tbody>
</table>

---
layout: section
---

# Section Title

Short description of what this section covers

---

# Results at a Glance

<div class="stat-grid">
<div class="stat-card">
  <div class="number">42</div>
  <div class="label">Experiments</div>
</div>
<div class="stat-card">
  <div class="number">0</div>
  <div class="label">Failures</div>
</div>
<div class="stat-card">
  <div class="number">~4 s</div>
  <div class="label">Median Latency</div>
</div>
<div class="stat-card">
  <div class="number">3×</div>
  <div class="label">Speed-up</div>
</div>
</div>

- Stat cards work well for a summary slide before the details.

---

# Code

```python
def hello(name: str) -> str:
    return f"Hello, {name}!"
```

- Code blocks use Slidev's built-in Shiki highlighting.

---
layout: section
---

# Thank You

Questions?
