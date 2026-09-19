# Portafolio — Daniel Amaya Zabala

Página personal en un solo archivo. No necesita build, ni servidor, ni dependencias:
`index.html` se abre tal cual con doble clic y funciona igual en GitHub Pages.

```
Portfolio_daz/
├── index.html      ← toda la página (HTML + CSS + JS + ecuaciones)
├── README.md       ← esto
└── pdf/
    └── Daniel_Amaya_CV.pdf
```

---

## 1. Publicarla en GitHub Pages

Como tu usuario es **TheWhite73**, para que quede en `https://thewhite73.github.io`
el repositorio tiene que llamarse exactamente `TheWhite73.github.io`:

1. En GitHub → **New repository** → nombre `TheWhite73.github.io` → **Public** → Create.
2. Sube `index.html` y la carpeta `pdf/` a la raíz del repo (botón *Add file → Upload files*,
   o por terminal con los comandos de abajo).
3. **Settings → Pages →** Source: *Deploy from a branch*, Branch: `main` / `root` → Save.
4. En uno o dos minutos la página queda en `https://thewhite73.github.io`.

Por terminal, desde esta carpeta:

```bash
git init
git add index.html README.md pdf/
git commit -m "Portfolio"
git branch -M main
git remote add origin https://github.com/TheWhite73/TheWhite73.github.io.git
git push -u origin main
```

Si prefieres que viva dentro de un repo con otro nombre (por ejemplo `portfolio`),
la URL será `https://thewhite73.github.io/portfolio/` y todo funciona igual,
porque las rutas de los PDF son relativas.

---

## 2. Añadir tu tesis, un preprint o unas notas

Todo el contenido editable está **al inicio del `<script>`**, al final de `index.html`.
Busca el bloque que dice `CONTENIDO QUE VAS A ACTUALIZAR TÚ`.

**Para publicar tu tesis:**

1. Copia el PDF dentro de `pdf/`, por ejemplo `pdf/tesis.pdf`.
2. En `index.html`, en la lista `WRITINGS`, cambia la línea del bloque de la tesis:

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
