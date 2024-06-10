## Project title

bookrtf-7.x

## Description

bookrtf-7.x is a Drupal 7 module that exports a Drupal book or book page to RTF format. The module was build to export books to something printable and readable as the printer friendly version isn't really reader firendly. bookrtf-7.x creates an A4 document of the book or book page that contains elements such as a front page, table of contents, page numbers, chapter references etc. The module integrates with anchor-7.x to make a page referenced index. The lay-out is customizable through CSS.

The module can be considered an alpha version, but is being used and works well. The coding was not brought to standards. Some website specific parts are hardcoded. The RTF document was tested in Microsoft Word en Libre Office writer. Options are available. A (useful) help page is not available, but some details are in help.md. Internationalisation and localisation is not available. The module is not in the Drupal module repository.

No further development is intended. The module has been ported to Drupal 9.x: [bookexportrtf-9.x](https://github.com/cterveen/bookexportrtf-9.x).

## Installation

Depends on the Drupal [Book](https://www.drupal.org/project/book) module which is part of Drupal Core

Download [Simple HTML DOM](https://simplehtmldom.sourceforge.io/) and copy it into libraries://simple_html_dom/

Download [Schepp's CSS Parser](https://github.com/Schepp/CSS-Parser) and copy it into libraries://schepp-css-parser/ 

Copy all the files into modules://bookrtf/

Enable the module

## Use

The download page can be accessed by book/rtf/1 (and possibly is only available if the book is node 1 and there are likely some other strange quirks).

Settings can be found in the admin area. Help can be found in help.md

## Credits

Written by Christiaan ter Veen <https://www.rork.nl/>

Depends on:

- Drupal <https://www.drupal.org/>
- Drupal book <https://www.drupal.org/project/book>
- Simple HTML DOM <https://simplehtmldom.sourceforge.io/>
- Schepp's CSS Parser <https://github.com/Schepp/CSS-Parser>

Technical details from:

- Microsoft RTF Specification
- RTF Pocket Guide by Sean M. Burke <https://www.oreilly.com/library/view/rtf-pocket-guide/9781449302047/>
- W3Schools CSS Reference <https://www.w3schools.com/cssref/index.php>

## License
To be decided, but consider it free to use, modify and distribute.
