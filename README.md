# +  bookrtf-7.x
A drupal 7 module to export books to RTF format

This module is in development and curruntly mainly written as a proof of
concept/demo for the book I'm working with. It's working, but assumes a
pretty standard document. It has been based on the HTML output of FCKEditor.

**Currently features**
- Basic HTML elements: p, h1, h2, h3, ul (li) ol (li), tbody (td, th), br, img
  - Images are scaled to A4 page width, png, possibly jpg/jpeg (not tested)
  - Tables are scaled to A4 page width, some adaptation in column width
  - Lists can be nested
  - Links are changed to footnotes.
- Basic HTML markup: b u i sup sub span
  - The span replacement [always] ends with a space
- CSS support for lay-out
  - Custom css files can be added to your theme directory
- Fancy lay-out
  - Chapters start on new pages
  - Custom front page (optional)
  - Flyleaf (optional)
  - Table of contents (optional)
  - Index (from the anchor module, optional)
  - Page headers and footers (facing pages; configurable: none, book title, chapter title, page number)

**Dependencies:**
- Drupal modules
  - book
  - libraries
- External libraries
  - Simple HTML DOM 
    - Available from https://simplehtmldom.sourceforge.io/
    - Files: simle_html_dom.php
    - Store in libraries://simple_html_dom/
  - CSS Parser: 
    - Available from https://github.com/Schepp/CSS-Parser 
    - Files: parser.php
    - Store in libraries://schepp-css-parser/

**CSS support:**

- A custom css file can be placed in theme://css/rtf.css
- The style is determined by:
  1. style attribute (can be turned off)
  2. id
  3. class
  4. element
  5. parents
- Supported elements: body, p, h1, h2, h3, li, td, th, span
  - The style of other elements will be used in the parental cascade
  - The span replacement always ends with a space!
- Classes used by bookrtf: .header-left .header-right .footer-left .footer-right
  - These define the lay-out of the headers and footers  
- Supported properties:
  - margin-top \[cm mm in px pt pc]
  - margin-right \[cm mm in px pt pc]
  - margin-bottom \[cm mm in px pt pc]
  - margin-left \[cm mm in px pt pc]
  - font-family \[first value only]
  - font-size \[cm mm in px pt pc]
  - font-weight \["bold", "normal"]
  - text-align \["left", "right", "center", "justify"]
  - color \[rgb(), #, color name]
- Note that values and colors should be in css format, this includes unit or
  type specification. All values will be converted to rtf appropriate values.
  Supported values are mentioned between square brackets behind the property.
