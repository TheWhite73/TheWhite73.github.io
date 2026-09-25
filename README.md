<h1 align="center">Daniel Amaya Zabala</h1>

<p align="center">
  <strong>Mathematician</strong> · Scientific machine learning<br>
  <sub>Inverse problems · Diffusion models · Measure theory · Interpretability</sub>
</p>

<p align="center">
  <a href="https://thewhite73.github.io"><img alt="Live site" src="https://img.shields.io/badge/live-thewhite73.github.io-ff9d3f?style=flat-square&logo=githubpages&logoColor=white"></a>
  <a href="https://www.linkedin.com/in/daz-math/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-daz--math-63b3d4?style=flat-square&logo=linkedin&logoColor=white"></a>
  <a href="mailto:amayazabaladaniel@gmail.com"><img alt="Email" src="https://img.shields.io/badge/email-contact-7b8ad4?style=flat-square&logo=gmail&logoColor=white"></a>
  <img alt="No dependencies" src="https://img.shields.io/badge/dependencies-none-5f7089?style=flat-square">
</p>

---

My academic homepage: research, publications, experience and CV. Plain HTML and CSS
in a single file, with no build step, framework or package manager. Clone it and
double-click `index.html` and it works exactly as it does live.

**→ [thewhite73.github.io](https://thewhite73.github.io)**

<br>

## 📐 What's on the page

Laid out like a typical researcher homepage: the things an advisor or recruiter looks
for come first.

| | Section | |
|:--:|---|---|
| 👤 | **Intro** | Photo, short bio, links (Email · CV · GitHub · LinkedIn) and a note that I am looking for MSc positions and research / ML roles |
| 📰 | **News** | Dated one-liners, newest first |
| 🧭 | **Research interests** | Inverse problems, diffusion models, approximation theory, probability and measure |
| 📄 | **Publications & writing** | Preprint in preparation, BSc thesis, UNAM notes, with `[pdf]` links |
| 🔬 | **Research experience** | SFU (Mitacs Globalink), BSc thesis, Saint Mary's, UNAM, and teaching at UdeA |
| 🧪 | **Projects** | GAN-balanced chest X-ray classifier, multi-currency expense tracker |
| 🎓 | **Education & awards** | Degrees, GPA, awards and skills |
| ⛰️ | **Outside research** | Hiking, languages, volunteering |

The earlier dark neon design, with its animations and compiled LaTeX, is kept at
[`retro.html`](https://thewhite73.github.io/retro.html) and linked from the footer.

<br>

## 🗂️ Repository

```
TheWhite73.github.io/
│
├── 📄 index.html                          the site: HTML and CSS
├── 🕹️ retro.html                          the previous retro/neon version
├── 📘 README.md                           this file
│
├── 🖼️ img/
│   ├── daniel.jpg                         portrait
│   ├── hike-panorama.jpg                  Panorama Ridge, Whistler
│   └── hike-garibaldi.jpg                 Garibaldi Lake
│
└── 📚 pdf/
    ├── Daniel_Amaya_CV.pdf                curriculum vitae
    └── TDA_Morse_Smale_Amaya_Segovia.pdf  directed reading, UNAM (Spanish)
```

<br>

## ⚙️ How it is built

- **One static file.** No JavaScript needed apart from one line that sets the footer
  year. Only the web fonts (Source Serif 4 and Inter) are fetched.
- **Light and dark.** Light by default and dark when the visitor's system asks for it,
  through `prefers-color-scheme`. All colours are custom properties in `:root`.
- **Findable.** Meta description, Open Graph tags for link previews, and schema.org
  `Person` data so search engines can connect the site to GitHub and LinkedIn.
- **Responsive and printable.** Works down to phone width with no horizontal scroll;
  the print stylesheet drops the navigation and photos.

<br>

## ✍️ Updating it

<details>
<summary><strong>Add a news item</strong></summary>

<br>

Add an `<li>` at the top of the list under `id="news"`:

```html
<li><time>Nov 2026</time><span>What happened, in one sentence.</span></li>
```
</details>

<details>
<summary><strong>Publish the thesis or a preprint</strong></summary>

<br>

Drop the PDF into `pdf/`, then in its entry under `id="publications"`, remove the
`in preparation` badge and add a links row:

```html
<div class="pub__links">
  <a href="pdf/thesis.pdf" target="_blank" rel="noopener">pdf</a>
  <a href="https://arxiv.org/abs/..." target="_blank" rel="noopener">arXiv</a>
  <a href="https://github.com/..." target="_blank" rel="noopener">code</a>
</div>
```

Wrap your own name in `<b>…</b>` in the author list so it stands out.
</details>

<details>
<summary><strong>Replace the CV or the photographs</strong></summary>

<br>

Same filename, same folder, nothing else to change. The portrait is shown at 4:5 and the
landscapes at 4:3, so images roughly in those proportions survive the crop best.
</details>

<details>
<summary><strong>Change the colours</strong></summary>

<br>

| Variable | Role |
|---|---|
| `--accent` | Links and the highlight bar |
| `--accent-soft` | Background of the "looking for" callout |
| `--text`, `--text-2`, `--text-3` | Three levels of text emphasis |
| `--bg`, `--surface`, `--rule` | Page, tags and hairlines |

Each is defined twice: once in `:root` for light mode and again inside the
`prefers-color-scheme: dark` block.
</details>

<br>

## 📫 Contact

**[amayazabaladaniel@gmail.com](mailto:amayazabaladaniel@gmail.com)** ·
[LinkedIn](https://www.linkedin.com/in/daz-math/) ·
[GitHub](https://github.com/TheWhite73)

<sub>Medellín, CO · Vancouver, CA</sub>
