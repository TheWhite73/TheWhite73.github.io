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

My personal site — research, writings, projects and CV, in a single self-contained
HTML file. No build step, no framework, no package manager. Clone it and double-click
`index.html` and it works exactly as it does live.

**→ [thewhite73.github.io](https://thewhite73.github.io)**

<br>

## 📐 What's on the page

| | Section | |
|:--:|---|---|
| 👤 | **About** | How I got from category theory to covering numbers, plus a *Now* panel with what I am reading and writing this month |
| 🧭 | **What I work on** | Probability and measure theory, inverse problems, diffusion models, interpretability — each with the equation it rests on |
| 🔬 | **Research** | Mitacs Globalink at Simon Fraser University, my BSc thesis, undergraduate research at Saint Mary's, and a directed reading with the UNAM |
| 📄 | **Mathematical writings** | Thesis, preprints and notes, with a PDF reader built into the page |
| 🧪 | **Projects** | A GAN-balanced chest X-ray classifier and a multi-currency expense tracker |
| 🎓 | **Teaching** | Linear algebra and analytic geometry at Universidad de Antioquia |
| ⛰️ | **Away from the board** | Hiking, languages, and volunteering |
| 📑 | **Curriculum vitae** | Embedded reader and a download |

<br>

## 🗂️ Repository

```
TheWhite73.github.io/
│
├── 📄 index.html                          the entire site — HTML, CSS, JS and equations
├── 📘 README.md                           this file
│
├── 🖼️ img/
│   ├── daniel.jpg                         portrait, About
│   ├── hike-panorama.jpg                  Panorama Ridge, Whistler
│   └── hike-garibaldi.jpg                 Garibaldi Lake
│
└── 📚 pdf/
    ├── Daniel_Amaya_CV.pdf                curriculum vitae
    └── TDA_Morse_Smale_Amaya_Segovia.pdf  directed reading, UNAM (Spanish)
```

<br>

## ⚙️ How it is built

**One file, zero dependencies.** Everything — layout, styles, behaviour — lives in
`index.html`. Nothing is fetched at runtime except the web fonts.

**🧮 Real LaTeX, no MathJax.** Every equation is compiled with `pdflatex`, converted to
SVG with `pdftocairo`, stripped to pure path data and inlined. They render identically
in every browser, appear instantly with no layout shift, and work offline. The trade-off
is that they are no longer editable as text.

**✨ Five animations, no libraries.** Plain `<canvas>` and SVG:

| | |
|---|---|
| **Hero** | A variance-preserving diffusion over a two-armed spiral — structure dissolves into Gaussian noise and reassembles. The clock and the equations below it stay in sync with the phase. |
| **Research · SFU** | A five-state Markov chain with a token hopping between states |
| **Research · thesis** | A feed-forward network with signals propagating through its layers |
| **Research · SMU** | A graph with node radius scaled by centrality |
| **Research · UNAM** | ε-balls growing over a point cloud — the filtration persistence reads |

**♿ Accessible and responsive.** Every animation honours `prefers-reduced-motion` by
freezing on a meaningful still frame. The layout works down to phone width with no
horizontal scroll.

**🎨 Deliberately single-theme.** Dark, with sodium amber against cold blue. All colours
are CSS custom properties in the `:root` block.

<br>

## ✍️ Updating it

Everything editable lives at the top of the `<script>` block at the end of `index.html`.

<details>
<summary><strong>Publish the thesis or a preprint</strong></summary>

<br>

Drop the PDF into `pdf/`, then point the entry at it in the `WRITINGS` list:

```js
file: null                  // before
file: "pdf/tesis.pdf"       // after
```

The card stops saying *In preparation* and grows three buttons: **Read here** (opens a
viewer inside the page), **New tab** and **Download**.

To add a new piece, copy a block into the list:

```js
{
  kind: "preprint",                     // "thesis" | "preprint" | "notes" | "talk"
  title: "Title of the piece",
  year: "2026",
  authors: "B. Adcock, D. Amaya, ...",  // optional — my name is highlighted automatically
  venue: "Where, with whom",
  blurb: "Two or three lines on what it is about.",
  lang: "Spanish",                      // optional, only if it is not in English
  file: "pdf/file.pdf"                  // or null if it does not exist yet
},
```
</details>

<details>
<summary><strong>Replace the CV or the photographs</strong></summary>

<br>

Same filename, same folder, nothing else to change. The embedded reader and the download
buttons already point there. The portrait is cropped to 4:5 and the landscapes to 4:3, so
images roughly in those proportions survive the crop best.
</details>

<details>
<summary><strong>Change the palette</strong></summary>

<br>

| Variable | Role |
|---|---|
| `--accent` | Sodium amber — the one warm light; buttons and primary links |
| `--cool` | Cold blue — equations, labels, detail |
| `--hot` | Signage red — used sparingly, on purpose |
| `--deep` | Indigo haze |
| `--ink`, `--ink-2`, `--ink-3` | The three background levels |

Changing one line in `:root` changes the whole page. The name in the hero cycles its glow
through blues and violets via `@keyframes led` — adjust the `12s` on the `h1` rule to
change the pace.
</details>

<details>
<summary><strong>Fonts</strong></summary>

<br>

From Google Fonts: **Michroma** for the wordmark, **Chakra Petch** for headings,
**IBM Plex Sans** for body text and **IBM Plex Mono** for labels and metadata. The mono
and sans pair deliberately with the Computer Modern of the compiled equations.
</details>

<br>

## 📫 Contact

**[amayazabaladaniel@gmail.com](mailto:amayazabaladaniel@gmail.com)** ·
[LinkedIn](https://www.linkedin.com/in/daz-math/) ·
[GitHub](https://github.com/TheWhite73)

<sub>Medellín, CO · Vancouver, CA</sub>2. En `index.html`, en la lista `WRITINGS`, cambia la línea del bloque de la tesis:

```js
file: null                  // antes
file: "pdf/tesis.pdf"       // después
```

Con eso la tarjeta deja de decir *In preparation* y aparecen tres botones:
**Read here** (lo abre en un visor dentro de la misma página),
**New tab** y **Download**.

**Para añadir un escrito nuevo**, copia un bloque entero y pégalo en la lista:

```js
{
  kind: "preprint",                     // "thesis" | "preprint" | "notes" | "talk"
  title: "Título del escrito",
  year: "2026",
  venue: "Dónde, con quién",
  blurb: "Dos o tres líneas de qué va.",
  file: "pdf/archivo.pdf"               // o null si todavía no lo tienes
},
```

**Las notas cortas** funcionan igual, en la lista `NOTES`:

```js
{ date: "2026", title: "Título de la nota", tag: "Functional analysis", file: "pdf/nota.pdf" },
```

---

## 3. Actualizar el CV

Reemplaza `pdf/Daniel_Amaya_CV.pdf` por la versión nueva, con el mismo nombre.
No hay que tocar nada más: el visor de la sección **Curriculum vitae** y los botones
de descarga ya apuntan ahí.

Si le cambias el nombre al archivo, hay que cambiarlo en tres sitios de `index.html`
(busca `Daniel_Amaya_CV.pdf`).

---

## 4. Las ecuaciones

No usan MathJax ni KaTeX ni ninguna librería externa: están compiladas con LaTeX real
y metidas en el HTML como SVG de trazos. Por eso se ven idénticas en cualquier
navegador, cargan al instante y funcionan sin internet.

El precio es que **no se editan como texto**. Si quieres cambiar una ecuación o añadir
otra, lo más simple es pedírmelo y te devuelvo el SVG listo para pegar.

Las que están ahora:

| Dónde | Qué |
|---|---|
| Hero | SDE de tiempo invertido (modelos de difusión) |
| Hero, panel | SDE hacia adelante |
| *Three objects* | Norma de operador entre espacios de Hilbert |
| *Three objects* | Teorema de Mercer |
| *Three objects* | Número de recubrimiento |
| *Research* | Problema inverso y posterior bayesiano |
| *Research*, figura | Cadena de Markov y distribución estacionaria |

---

## 5. Las animaciones

Cinco, todas en canvas o SVG puro, sin librerías:

- **Hero** — difusión variance-preserving sobre una espiral de dos brazos: la estructura
  se disuelve en ruido gaussiano y vuelve. El reloj `t` y las ecuaciones de abajo van
  sincronizados con la fase.
- **Research / SFU** — cadena de Markov de cinco estados con un token saltando.
- **Research / UNAM** — bolas de radio ε creciendo sobre una nube de puntos (la filtración).
- **Research / SMU** — grafo con los nodos escalados por centralidad.
- **Projects** — red neuronal feed-forward con señales propagándose.

Todas respetan `prefers-reduced-motion`: si el sistema del visitante pide menos
animación, se congelan en un fotograma fijo en vez de moverse.

---

## 6. Colores

Están todos como variables CSS al principio del archivo, en el bloque `:root`.
Cambiar `--cyan`, `--magenta` o `--amber` cambia la página entera.
