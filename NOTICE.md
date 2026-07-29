# Third-party notices

`index.html` is self-contained: the 3D library and both typefaces are embedded
in the file itself so it runs with no network requests. Those components keep
their own licences, reproduced or referenced below.

*Not legal advice — I'm not a lawyer. This records what the upstream licences
ask for so you can check it yourself.*

---

## three.js (r169) and OrbitControls

Copyright 2010–2024 Three.js Authors
SPDX-License-Identifier: MIT
<https://github.com/mrdoob/three.js>

Embedded as `three.module.min.js` plus `examples/jsm/controls/OrbitControls.js`,
each wrapped in a function scope so they don't collide with the application's
own names. The upstream `@license` banner is preserved inline in `index.html`.

MIT requires the copyright notice and the permission notice below to travel
with any copy or substantial portion of the software:

```
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## IBM Plex Mono

Version 2.003, weights 400/500/600, latin subset, WOFF2, embedded as base64
data URIs. The copyright string carried inside those files reads:

> Copyright 2017 IBM Corp. All rights reserved.

The project licence states it as: Copyright © 2017 IBM Corp., with Reserved
Font Name "Plex". SIL Open Font License 1.1 — <https://scripts.sil.org/OFL>
<https://github.com/IBM/plex>

## Saira Condensed

Version 0.072, weights 500/600/700, latin subset, WOFF2, embedded as base64
data URIs. The copyright string carried inside those files reads:

> Copyright 2016 The Saira Project Authors (omnibus.type@gmail.com), with
> reserved font name "Saira".

SIL Open Font License 1.1 — <https://scripts.sil.org/OFL>
<https://github.com/Omnibus-Type/Saira>

Note the version skew: the upstream repository has moved on and its current
`OFL.txt` carries a 2020 notice. The 2016 line above is what is actually
inside the embedded binaries, which is the version being redistributed here.

### About the font files

Both are redistributed **byte-for-byte as served by Google Fonts**, not
re-subsetted or otherwise altered here. The notices above were read out of the
embedded binaries themselves, not copied from a font directory. That matters under the OFL: both
families carry a Reserved Font Name, and a *modified* version may not keep it.
Since these are unmodified copies of what the upstream distributor serves, the
names stand — but if you ever re-subset or convert them, rename the family.

The OFL asks that the copyright notice and the licence travel with the font
software. The notices are above and in the header of `index.html`; the full
licence texts ship alongside this file:

- `OFL-IBM-Plex.txt` — from <https://github.com/IBM/plex>
- `OFL-Saira.txt` — from <https://github.com/Omnibus-Type/Saira>

`OFL-Saira.txt` is the repository's current text and carries a 2020 notice,
while the embedded binary is v0.072 with the 2016 notice quoted above. The
licence body is identical either way; only the copyright line differs.

---

## The bridge model itself

The geometry, exporters and interface are original work. Pick whatever licence
you want for them and add it as `LICENSE`; it doesn't affect the components
above, which keep their own terms either way.
