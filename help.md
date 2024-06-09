# +  bookrtf-7.x
A drupal 7 module to export books to RTF format

This module is in development and curruntly mainly written as a proof of
concept/demo for the book I'm working with. It's working, but assumes a
pretty standard document. It has been based on the HTML output of FCKEditor.

**Currently features**
- Basic HTML elements: p, h1, h2, h3, li (ol, ul), tbody (td, th), br, img
  - Images are scaled to A4 page width, png, possibly jpg/jpeg (not tested)
  - Tables are scaled to A4 page width, column width can be set in CSS
  - Lists can be nested
  - Links are changed to footnotes
- Basic HTML markup: b strong u i sup sub span ins del s strike
- CSS support for lay-out
  - A custom css file can be added to your theme directory
- Fancy lay-out
  - Chapters start on new pages
  - Custom front page (optional)
  - Flyleaf (optional)
  - Table of contents (optional)
  - Index (from the anchor module, optional)
  - Page headers and footers (facing pages; configurable: none, book title,
    chapter title, page number)

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
- Supported elements: body, p, h1, h2, h3, h4, h5, h6, li, td, th, span, ins, del, s
  - The style of other elements (e.g. div) will be used in the parental cascade
- Classes used by bookrtf: .header-left .header-right .footer-left .footer-right
  - These define the lay-out of the headers and footers
- Supported properties:
  - margin-* \[cm mm in px pt pc]
  - font-family \[first value only]
  - font-size \[cm mm in px pt pc]
  - font-weight \[bold normal]
  - text-align \[left right center justify]
  - color \[rgb(), #, color name]
  - text-decoration \[line-through underline none]
    - RTF does not support overstrike.
  - text-decoration-color \[rgb() # color name]
    - RTF only supports color definition for underline.
    - Libre Office does not implement underline color from RTF.
  - text-decoration-style \[solid double dashed dotted wavy]
    - RTF only supports style for underline
- Properties only applied in table cells \(td, th):
  - border-\*-width \[cm mm in px pt pc]
  - border-\*-style \[solid dotted dashed double none hidden]
  - valign \[top middle bottom]
  - width \[cm mm in px pt pc]
    - Note that the default page width (ex. margins) is about 554 pixels
- Note that values and colors should be in css format, this includes unit or
  type specification. All values will be converted to rtf appropriate values.
  Supported values are mentioned between square brackets behind the property.
