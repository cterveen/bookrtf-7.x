# +  bookrtf
A drupal 7 module to export books to RTF format

This module is in developement and curruntly mainly written as a proof of concept/demo for the Book I'm working with. It's working, but particulary sensitive to the input. It has been based on the HTML output of FCKEditor and needs the right set op closing tags. If you use something else it might end up in a not so neat document with missing things.

Currently it supports:
- Page ends at chapter ends
- Lists (including nested lists)
- Images (A4 page width only, png, possibly jpg/jpeg (not tested))
- Tables (A4 page width only, columns all have the same width)
- Links (tekst is shown, link is added to a footnote if different from the text)
- Basic markup: bold, italic, underlined, paragraphs, h3, newlines
- Extended ASCII characters (except 0xab)
- HTML characters: &amp;nbsp; &amp;amp;
- Index (from the anchor module)
