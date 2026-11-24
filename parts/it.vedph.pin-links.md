---
layout: default
title: Pin Links
parent: Parts
grand_parent: Reference
nav_order: 3
---

# Pin Links Part

- 🔑 `it.vedph.pin-links`
- ⚙️ [model](https://github.com/vedph/cadmus-core/blob/master/docs/models/general/pin-links.md)
- 🎯 Links to internal, external or taxonomic resources.

The pin links part derives its "pin" prefix from its application to internal links, but it's a generic and flexible part to link an item (or part, when used in bricks) to any resource, using ["composite links"](https://vedph.github.io/cadmus-doc/linking/links.html).

The pin links part is just a wrapper around a [pin links brick](../bricks/pin-links.md); it is designed to link a whole item to any internal or external resource. Often, the same brick (either with a single link or with a list of them) is used inside specific parts with the same functionality. For instance, a decorations part in a manuscript might link each element of its decorations to the respective author, stored elsewhere (e.g. in an external authority file, a LOD ontology, or a local taxonomy); but also to iconographic descriptors from a taxonomy, or to the IIIF URL of the image for that element; etc. All these are links, implemented inside that part editor with a links brick.
