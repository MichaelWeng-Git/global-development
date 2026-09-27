# Global Development

> A zoom-in field guide for my Humanity unit on global development: from the whole planet down to one room in one house, asking why some countries are rich and some are poor.

---

## What makes it different

It is **one continuous zoom, not a slideshow**. You start with Earth and click
an orange pin to fly into Asia, then the Philippines, Manila, Tondo, one house
and finally the room inside it. Each zoom starts from the pin you clicked, so
the path from the world down to one family is always visible.

Each stop pairs **quick facts and Gapminder data** (the 4 income levels, life
expectancy, fertility, child mortality, literacy, poverty trends) with a short
written reflection. The three lessons I took away, about hierarchy, the poverty
cycle, and luck plus choice, sit in the last three stops of the zoom.

## Features

| Feature | Description |
|---------|-------------|
| Earth | 8 billion people, Gapminder's 4 income levels, and the long-run drop in extreme poverty |
| Asia | 60% of all humans, and the continent with the biggest recent fall in poverty |
| Philippines | 117 million people on 7,641 islands, mostly Level 2, with about 10 million working abroad |
| Manila | All 4 income levels in one metro area, from BGC and Makati towers to Tondo |
| Tondo | About 630,000 people in 9 km², life on Levels 1 to 2. Lesson 01: hierarchy |
| A house | Two small rooms compared with Gapminder's Dollar Street photos. Lesson 02: the cycle |
| Inside | A mother teaching her child to read, and education as the climb between levels. Lesson 03: luck + choice |
| Pin navigation | Click the orange pin to zoom in toward that exact spot |
| Controls | Zoom in/out buttons, a clickable breadcrumb, a scale readout (1× up to 1,000,000×) and a progress bar |
| Keyboard | Arrow keys, Space, Enter, PageUp/PageDown and +/- move between levels |

## How it works

Seven levels, one illustration each. Only one level is shown at a time.

```
level 0   Earth         1×
level 1   Asia          10×
level 2   Philippines   100×
level 3   Manila        1,000×
level 4   Tondo         10,000×
level 5   A house       100,000×
level 6   Inside        1,000,000×
```

Clicking the pin zooms the current image in from the pin's position and swaps
in the next level. Pin positions are stored as percentages of each image and
recalculated for letterboxing, so they stay on the right spot at any window
size. Clicking the canvas on the last level goes back to Earth.

## Tech stack

- **Page:** a single HTML file with inline CSS and plain JavaScript, no framework and no build step
- **Fonts:** Fraunces and Inter from Google Fonts
- **Art:** one PNG illustration per level, plus small inline SVG vignettes
- **Data:** figures from Gapminder, written into the page by hand

## Local development

No build step. Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

`index.standalone.html` has every image inlined, so it opens on its own
anywhere, including offline.

## Project layout

```
index.html              the page (loads the PNGs next to it)
index.standalone.html   single-file version with all images inlined
earth.png               level 0
asia.png                level 1
philippines.png         level 2
manila.png              level 3
tondo.png               level 4
house.png               level 5
interior.png            level 6
```

## Credits

Data from [Gapminder](https://www.gapminder.org), including Dollar Street.
The reflection also draws on the film *Metro Manila* (2013) and a village
simulation we ran in class. By Michael Weng.
