# Companion repository for "Creating Intelligent Content with Lightweight DITA"

This repository contains code samples from the book ["Creating Intelligent Content with Lightweight DITA"](https://www.routledge.com/Creating-Intelligent-Content-with-Lightweight-DITA/Evia/p/book/9780815393825), by Carlos Evia.

## Contents

* [Code samples by chapter](#code-samples-by-chapter)
* [LwDITA updates](#lwdita-updates)
  - [Formatting of definition list in MDITA](#formatting-of-definition-list-in-mdita)
  - [Formatting of footnote in XDITA] (##formatting-of-footnote-in-xdita)
  - [Formatting of footnote in MDITA](#formatting-of-footnote-in-mdita)
  - [Formatting of note in MDITA](#formatting-of-note-in-mdita)
* [Errata](#errata)
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

### Formatting of footnote in XDITA

The content model for `<fn>` (footnote) presented in the book was breaking compatibility with DITA 1.3. In order to reestablish compatibility, `<fn>` in XDITA now requires a parent `<div>` (division, which is an existing element in DITA but new to XDITA). In XDITA, `<div>` will only be allowed as a container for `<fn>`. 

The following example shows an XDITA topic with a footnote inside a division:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE topic PUBLIC "-//OASIS//DTD LIGHTWEIGHT DITA Topic//EN" "lw-topic.dtd">
<topic id="program-bulbs-to-groups">
  <title>Programming Light Bulbs to a Lighting Group</title>
  <shortdesc>You can program one or more light bulbs to a lighting group to operate that group
    with your remote control.</shortdesc>
  <body>
    <section id="context">
      <p>Your <ph keyref="product-name"/> remote control can manage up to 250 network light bulbs on the same lighting
        network. When you add a light bulb to the network, you can program it to one or more
        lighting groups. You must assign a light bulb to at least one lighting group to
        operate that light bulb  A network light bulb that is not programmed to a
        lighting group will still operate when controlling all network light bulbs from
        the remote control. For non-residential installations, please consult the electrical standards from the Occupational Safety and Health Administration<xref href="#program-bulbs-to-groups/osha-electric"/>.</p>
    </section>
        <div>
      <fn id="osha-electric">
        <p>Available at <xref href="https://www.osha.gov/electrical" format="html" scope="external"/></p>
      </fn>
    </div>
    
  </body>
</topic>
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
class="note">`. That is no longer a recommended MDITA component.

## Errata

* **Page 14, paragraph 2:** "In their textbook DITA Best Practices, Bellamy et al. recommend using DITA maps to create an information set that specify which topics should be included in a user deliverable produced from the map." **Should be:** "In their textbook DITA Best Practices, Bellamy et al. recommend using DITA maps to create an information set that specifies which topics should be included in a user deliverable produced from the map."
* **Page 18, paragraph 1:** "The theoretical axis of the evolution of DITA analyzed in this book is based on the concept of computational thinking, which is defined by their main proponents as follows." **Should be:** "The theoretical axis of the evolution of DITA analyzed in this book is based on the concept of computational thinking, which is defined by its main proponents as follows."
* **Page 85, penultimate paragraph:** "Whereas XDITA and MDITA were designed to be functionally equivalent to each other..." **Should be:** "Whereas XDITA and HDITA were designed to be functionally equivalent to each other..."
* **Page 106, paragraph 2:** "In XDITA and MDITA, a topic requires an @id." **Should be:** "In XDITA and HDITA, a topic requires an @id." 

*(Thanks to Chris Despopoulos)*


## Relevant links

- [Lightweight DITA subcommittee at OASIS](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=dita-lightweight-dita)
- [List of LwDITA-aware tools](https://wiki.oasis-open.org/dita/LightweightDITASubcommittee/lwditatools)
