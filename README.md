# Panel Bridge

A parametric generator for a 3D-printable military panel bridge — the Bailey
type, built the way the real thing is: two flat truss panels tied by a deck
whose tenons pass right through them.

Adjust the span, pick a Warren or Pratt web, and download a 3MF with every part
named, oriented and placed on the plate. **Nothing needs supports and nothing
is loose.**

Open `index.html` in a browser. That's the whole application — one file, no
build step, no server, no network requests once you have it.

---

## Using it

| Control | Range |
| --- | --- |
| Span | 120–200 mm |
| Truss | Warren or Pratt |
| Abutments | on / off |
| Approach ramps | on / off |
| Exploded view | shows how it assembles |

The schedule panel reports the live dimensions — panel pitch, diagonal angle,
member sections, assembled footprint and the print plate size — so you can see
whether it fits your printer before downloading anything.

**Download the 3MF** for nine named objects ready to slice. Individual STLs are
there too if you'd rather place parts yourself.

## Printing

PETG or PLA, 0.2 mm layers, 3 walls, 15% gyroid.

Every part is a flat plate printed on its face, so **no part has any
unsupported area at all** — measured layer by layer at a 45° threshold, the
whole plate comes back at 0.0 mm². Don't auto-orient and don't split to
objects: each part is several overlapping solids that the slicer unions at
slice time, and splitting them scatters the pieces.

Parts arrive Z-up and already on the plate.

## Assembly

1. Press each truss panel onto the deck's through-tenons — 0.08 mm, a firm push. The tenon ends show on the outside, which is correct.
2. Drop a staple into the notches at each end. Its legs run down outside the panels and stop them splaying.
3. Set each deck end over the two lugs on its ramp.
4. Lower the bridge onto the abutments; their keys rise into the end posts.

Everything drops into place and nothing slides. Dry-fit the whole thing before
you reach for glue — the panels are stiff in plane and floppy out of it until
the deck and staples are in, so assemble deck first and check it's square.

## Hosting

It's a single static file, so anything that serves static files will do.

- **GitHub Pages** — put `index.html` at the repo root, Settings → Pages, deploy from `main` / root. `.nojekyll` is included and matters: Jekyll parses `{{ }}` and `{% %}` in files it publishes, which inside minified JavaScript would be silent corruption.

This copy's canonical home is <https://panel-bridge.lccode.dev/> — set near
the top of `index.html` and in the `CNAME` file. If you fork and host it
elsewhere, change both (or remove them): a canonical pointing at a URL that
doesn't serve the page is worse than having none.

## What's inside

three.js and both typefaces are embedded in `index.html` so it runs offline.
They keep their own licences — see [NOTICE.md](NOTICE.md).

The full licence texts ship with the repo as `OFL-IBM-Plex.txt` and
`OFL-Saira.txt`, so the folder is complete however you pass it around.
