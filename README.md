# +  bookrtf-7.x
A drupal 7 module to export books to RTF format

This module is in development and curruntly mainly written as a proof of
concept/demo for the book I'm working with. It's working, but assumes a
pretty standard document. It has been based on the HTML output of FCKEditor.

**Currently features**
- Basic HTML elements: p, h1, h2, h3, li, tbody, td, th, br, img
  - Images are scaled to A4 page width, png, possibly jpg/jpeg (not tested)
  - Tables are scaled to A4 page width, some adaptation in column width
  - Lists can be nested
  - Links are changed to footnotes.
- Basic HTML markup: b u i
- CSS support for lay-out
  - Custom css files can be added to your theme directory
- Fancy lay-out
  - Chapters start on new pages
  - Custom front page (optional)
  - Flyleaf (optional)
  - Table of contents (optional)
  - Index (from the anchor module, optional)
  - Page headers
  - Page number

**Dependencies:**
- Drupal modules
  - book
  - libraries
- External libraries
  - simple HTML DOM: https://simplehtmldom.sourceforge.io/
  - css parser: https://github.com/Schepp/CSS-Parser

**CSS support:**

Supported elements:
- body
- p
- h1
- h2
- h3
- li
- td 
- th
   
Supported classes: 
- .header-left
- .header-right
- .footer-left
- .footer-right
   
Supported properties \[values]:
- margin-top \[px]
- margin-right \[px]
- margin-bottom \[px]
- margin-left \[px]
- font-family \[first value only]
- font-size \[pt]
- font-weight \["bold"]
- text-align \["left", "right", "center", "justify"]
   
Note that values should be in css format including the unit. These will be
converted to rtf units and rounded to whole units. Supported values are
mentioned between square brackets behind the property. */
