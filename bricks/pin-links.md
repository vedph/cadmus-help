---
layout: default
title: Pin Links
parent: Bricks
grand_parent: Reference
nav_order: 3
---

# Pin Links

Pin links, or more technically **asserted composite identifiers**, are identifiers which can be added to an object to link it to any internal or external resource while also specifying various metadata about the link itself.

For instance, a decorations part in a manuscript might link each element of its decorations to the respective author, stored elsewhere (e.g. in an external authority file, a LOD ontology, or a local taxonomy); but also to iconographic descriptors from a taxonomy, or to the IIIF URL of the image for that element; etc. All these are links, implemented inside that part editor with a links brick.

## Model Overview

The [model](https://github.com/vedph/cadmus-bricks/blob/master/docs/asserted-composite-id.md) of an asserted composite identifier is generic enough to be used for several types of links:

- **internal links**, pointing to other objects within the Cadmus database.
- **external links**, pointing to any external resource (e.g. an entry in an authority file, an entity in a LOD ontology, a web page URL, etc.).
- **taxonomy links**, pointing to an internal taxonomy separate from the Cadmus database and used as a writeable authority file acting as a middle layer between the Cadmus database and third-party external resources. For instance, in the a project iconographic descriptions are defined by a set of descriptors and subjects from two taxonomies. Each of these taxonomies often has corresponding or partially overlapping entries in third-party authority files, like Biblissima+ or Iconclass; while other entries are project-specific and thus are not found elsewhere. In this case, users want the best of both worlds: they still want to link their descriptions to standard authority files; but at the same time, they need to add their own. The taxonomy works like a middle layer between these two worlds, providing a writeable set of entities (either arranged in a flat set or in a hierarchy) which in turn can be linked to any number of external resources.

Additionally, each link can have **metadata** about itself and the relation it establishes between its source and its target, like:

- a generic **tag** to further classify or group links.
- a **scope** which defines the domain for the identifier used as the link target. For instance, if you link to a VIAF entry, you get a numeric ID. Typically you also want to specify that this number is a VIAF identifier, i.e. refers to the domain of identifiers curated by VIAF. The scope is an arbitrary string identifying that domain. When you pick an external ID (like VIAF) the scope is automatically set (but it is still possible to edit it if you want).
- a human-friendly **label** for the target. Here you can type what you want. In most cases a label is automatically set by lookup, but you are still free to edit it at will.
- a set of binary **features** from a thesaurus or from a taxonomy (this depends on your configuration): you can further add specific features to the link, useful when you need to specify the nature of the relationship defined by the link.
- a free text **note**.
- a structured **assertion** about the level of certainty of this link. For instance, if you are linking a decoration element with an artist, but you are not sure about the artist's identification, an assertion is used to assess the probability of that identification and provide further metadata (including a free text note and documental references about the identification hypothesis).

## Usage

Whatever the link type, you can always specify:

- an optional **tag** for the link.
- an optional **scope** for the link. This is recommended for external links.
- an optional set of **features** for the link. These are visible only if you have configured a source for them (a thesaurus or a taxonomy).
- an optional **assertion** for the link.

![UI](./img/asserted-composite-ids01.png)

To add a link, click the `+ID` button. You can edit links, reorder them or delete them with the buttons next to each link.

When you add or edit a link, the procedure for selecting its target is slightly different according to the link type.

### External Links

1. in `target`, pick the `external` source.
2. if you have configured a lookup service for that source (e.g. VIAF, Iconclass, Pleiades, etc.), you will find it in the `external lookup` panel. In this case, you will typically pick the target by just typing some of the letters of its name and selecting it from the list of results. Alternatively, just enter a human-friendly label and an ID for the target in `label` and `GID` (=global ID).
3. click the `target` button to save it.

### Internal Links

### Taxonomy Links
