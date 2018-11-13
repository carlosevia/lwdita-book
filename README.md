# Companion repository for "Creating Intelligent Content with Lightweight DITA"

This repository contains code samples from the book ["Creating Intelligent Content with Lightweight DITA"](https://www.routledge.com/Creating-Intelligent-Content-with-Lightweight-DITA/Evia/p/book/9780815393825), by Carlos Evia.

## Contents

* [Code samples by chapter](#code-samples-by-chapter)
* [LwDITA updates](#lwdita-updates)
* [Formatting of definition list in MDITA](#formatting-of-definition-list-in-mdita)
* [Formatting of footnote in MDITA](#formatting-of-footnote-in-mdita)
* [Formatting of note in MDITA](#formatting-of-note-in-mdita)
* [Relevant links](#relevant-links)

## Code samples by chapter

This repository includes folders for each chapter of the book. Each folder contains all the code samples with the same labels that they have in the book.

You can click on the `Clone or download` green button in this repository and download a zip file with all the code samples organized by chapter.

## LwDITA updates

Since the publication of "Creating Intelligent Content with Lightweight DITA," the Lightweight DITA subcommittee at OASIS has implemented the following changes, which supersede the content included in the book:

### Formatting of definition list in MDITA

In MDITA extended profile, a definition list is represented by a "single-line term followed by a colon and the definition for that term," following the [PHP Markdown Extra syntax for definition list](https://michelf.ca/projects/php-markdown/extra/#def-list)

The following example shows an MDITA topic with a definition list:

```
---
id: install-and-setup
author: Kevin Lewis
---
# Installing and Setting up Remote Lighting
Installation of your Lighting Kit includes installing the light bulbs into light
fixtures, preparing the remote control, and programming lighting groups.

Before you attempt to install your Lighting Kit, please turn off the power in your
electrical circuit panel.

## Important Terms
Circuit panel
:   Also known as the breaker panel, it represents the main point of distribution
circuits in a building.

Lighting Kit
:   The commercial product covered by this information materials.
```

### Formatting of footnote in MDITA

In MDITA extended profile, a footnote is represented by a component "made of two things: a marker in the text that will become a superscript number; a footnote definition that will be placed in a list of footnotes at the end of the document," following the [PHP Markdown Extra syntax for footnote](https://michelf.ca/projects/php-markdown/extra/#footnotes)

The following example shows an MDITA topic with a footnote:

```
---
id: install-and-setup
author: Kevin Lewis
---
# Installing and Setting up Remote Lighting
Installation of your Lighting Kit[^1] includes installing the light bulbs into light
fixtures, preparing the remote control, and programming lighting groups.

[^1]: This document occasionally uses the term "lighting kit" (all lowercase letters)
for generic statements that do not apply exclusively to your product.

```

### Formatting of note in MDITA

There is no specific markup for expressing a note in MDITA. A previous recommendation suggested using an HDITA snippet of `<div data-
class="note">`. That is no longer an MDITA component.

## Relevant links

- [Lightweight DITA subcommittee at OASIS](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=dita-lightweight-dita)
- [List of LwDITA-aware tools](https://wiki.oasis-open.org/dita/LightweightDITASubcommittee/lwditatools)
