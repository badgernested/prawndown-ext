# prawndown-ext

[![Gem Version](https://badge.fury.io/rb/prawndown-ext.svg)](https://badge.fury.io/rb/prawndown-ext)

An extension of [Prawndown](https://github.com/kaspermeyer/prawndown), used for Jekyll blogs (but can be used for other stuff too).

## Usage

When using prawn, you can call the ``markdown`` method in your calls to render markdown.

``content`` is the markdown content you want to render.
``options`` is a hash/dictionary of options that can modify how the text is rendered.

```
markdown (content, options: options)
```

## Supported Markdown

Supports the following effects:
* Header
* Links
* Bold, italic, strikethrough
* Images
* Quotes

Removes the following:
* ``<iframe>`` references such as YouTube videos

### Options

This is a list of possible options you can pass to prawndown-ext.

* ``"header1_size"`` - Header 1 font size (default 28)
* ``"header2_size"`` - Header 2 font size (default 24)
* ``"header3_size"`` - Header 3 font size (default 20)
* ``"header4_size"`` - Header 4 font size (default 18)
* ``"header5_size"`` - Header 5 font size (default 16)
* ``"header6_size"`` - Header 6 font size (default 14)
* ``"header[1-6]_font"`` - The quote font name as defined in ``Prawn::Document.font_families`` used for headers.
* ``"header[1-6]_margin"`` - The amount of margin on all sides the headers have (default 4)
* ``"header[1-6]_line_spacing"`` - The amount of space in between lines on header text.
* ``"quote_size"`` - Quoted text font size (default 14)
* ``"quote_font"`` - The quote font name as defined in ``Prawn::Document.font_families`` used for quotes.
* ``"quote_font_spacing"`` - Spacing between characters for quote font.
* ``"quote_margin""`` - The amount of margin on all sides the quotes have.
* ``"default_line_spacing"`` - The amount of space in between lines on regular text.
* ``"quote_line_spacing"`` - The amount of space in between lines on quote text.
* ``"no_image"`` - If true, no images will be rendered.
* ``"image_dir"`` - The base image directory to use for image references.

### Extra Commands

These commands allow for more customization.

* ``"<br><br>"`` - Creates a new page.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Other Stuff

Check out [PetitFelix](https://github.com/badgernested/petitfelix) which uses prawndown-ext for producing printable PDFs from markdown pages.

