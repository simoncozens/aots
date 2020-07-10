# CommonType

The **CommonType** project is work-in-progress. Its immediate aim is to provide [publicly accessible documentation](http://commontype.org/) of the common font format that is based on the “SFNT container” developed by Apple in the TrueType® format, and later refined in the OpenType® format and the ISO Open Font Format (OFF) standard.

## Current situation

Currently, SFNT-based fonts are specified in several places:

1. **The OpenType® format**. OpenType® is a [registered trademark](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/en-us.aspx) of [Microsoft®](https://www.microsoft.com/). The **[OpenType® specification](https://docs.microsoft.com/en-us/typography/opentype/spec/)** is available at no charge on the Microsoft website. The text for the format specification is © Microsoft.
2. **The TrueType® format**. TrueType® is a [registered trademark](https://www.apple.com/legal/intellectual-property/trademark/appletmlist.html) of [Apple® Inc.](https://www.apple.com/) The **[TrueType® Reference Manual](https://developer.apple.com/fonts/TrueType-Reference-Manual/)** is available at no charge on the Apple website. The text of the reference manual is © Apple Inc.
3. **The Open Font Format standard**. The Open Font Format standard is an international standard published as ISO/IEC 14496-22:2019 “Information technology — Coding of audio-visual objects — Part 22: Open Font Format” by [ISO®](https://www.iso.org/) (International Organization for Standardization) and [IEC](https://www.iec.ch/) (International Electrotechnical Commission). The **[Open Font Format standard](https://standards.iso.org/ittf/PubliclyAvailableStandards/c074461_ISO_IEC_14496-22_2019.zip)** is available at no charge on the ISO website. The text of the standard is © ISO.

However, over the last two decades, many people in the font technology world expressed concerns about the quality of the specifications. The SFNT-housed fonts “work”, but the way they work in various environments is often the result of developers reading the specs and then relying on a lot of fragmented knowledge that is not easily accessible. In June 2020, @simoncozens forked AOTS and @twardoch [tweeted](https://twitter.com/adamtwar/status/1274803202450436096): 

> While I’ve enjoyed being part of a few ad-hoc groups over the past few years, at the same time it has worried me that they’ve increasingly been “ad-hoc”. When working with font makers & font tool makers, I know that a lot of energy goes into working around problems introed by OS makers and end-user app makers, and I know these problems are often because there is no real font format spec.

To which @davelab replied:

> We will make one

So, here we go!

## Brief history: AOTS

In 2002, [Eric Muller](https://github.com/eric-muller) at Adobe created the **[Annotated OpenType specification](https://github.com/adobe-type-tools/aots)** (AOTS). It included the text of the OpenType specification, “(approximately) that of the 1.4 specification, but some parts [were] absent” (current version of the OpenType spec is 1.8.3). AOTS also included annotations witten by Eric, as well as Java tools for manipulating OpenType font files. In 2016, Adobe published [AOTS](https://github.com/adobe-type-tools/aots) on Github under the [Apache 2 license](https://github.com/adobe-type-tools/aots/blob/master/LICENSE.md).

The Java code in the AOTS project is of limited use today (2020). Instead: 

- The [fontTools](https://github.com/fonttools/fonttools/) Python toolkit provides much more up-to-date code to create and manipulate SFNT-housed (OpenType, TrueType, OFF) fonts. Many tools and apps have been created with it.
- The [HarfBuzz](https://github.com/harfbuzz/harfbuzz) text shaping engine and the [FreeType](https://www.freetype.org/) renderer are freely available, opensource libraries for typesetting with and rendering of SNFT-housed fonts.
- Software programs (operating systems, desktop and mobile apps, and web browsers) use these libraries, or proprietary libraries developed by the vendors of those programs, to deal with SFNT-housed fonts.

However, we have recognized that the AOTS project includes a liberally licensed version of the text of the OpenType® font format specification, though not the up-to-date version.

## CommonType goals

The **CommonType** project provides a [publicly accessible rendition](http://commontype.org/) of the AOTS text, and aims to improve and extend it. We are using the term “CommonType” as a working name, as we do not guarantee that the content of the project will fully match OpenType, TrueType or OFF.

We want CommonType to be **open**: liberally licensed, open source and based on open and transparent procedures. We want to:

- review the documentation (spec), identify weaknesses, for example ambiguous terminology
- bring the documentation on-par with OpenType, TrueType and/or OFF
- revise the documentation: formalize the language, improve writing clarity, remove inaccurate legacy language outdated by later revisions
- possibly reorganize the documentation, provide a clear specification of the format, and separately, provide recommendations for font developers and for implementers of software that uses fonts
- develop the documentation further
- create transparent procedures for working on the documentation
- use CommonType as a platform for discussion about future font formats, and for drafting proposals that extend the SFNT-housed font formats

These goals may change.

## Current structure

- The [commontype.org](http://commontype.org/) website contains the specification text in readable form, and lets you comment on the text right in the browser using [hypothes.is](http://hypothes.is/)
- The [`master`](https://github.com/commontype-standard/commontype-standard.github.io/tree/master) branch contains a Markdown representation of the text.
- The [`source`](https://github.com/commontype-standard/commontype-standard.github.io/tree/source) branch contains the AOTS sources

## Discussion

- Use the _hypothes.is annotations_ on the right side [commontype.org](http://commontype.org/) website for brief comments
- Use the [issues](https://github.com/commontype-standard/commontype-standard.github.io/issues) to discuss
- Use the [wiki](https://github.com/commontype-standard/commontype-standard.github.io/wiki) for drafting texts, but keep in mind that the wiki content may be removed or changed without notice (we want to keep the wiki a “sketchboard”)

## Team

CommonType is currently a personal project of select individuals who have an interest in font technology:

- [Simon Cozens](https://github.com/simoncozens)
- [Adam Twardoch](https://github.com/twardoch)
- [Dave Crossland](https://github.com/davelab6)

CommonType is not currently backed or endorsed by any organization or company. We are looking forward to your comments and discussion.