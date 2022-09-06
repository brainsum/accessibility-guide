# 📄 Creating accessible web content

## :warning:Prevent faulty HTML code

Avoid empty HTML tags, like:

* blank lines,
* blank tag pairs (these are mostly `div`s, `span`s)
* bad html tag pairs,
* ****:point\_up:**headings** (including SEO)
* :point\_up:**link elements**

Content embedded from other sources should be cleaned up (including inline colors, sizes specified in px, fonts) - Drupal and CKEditor are sure to add tools.

## ****:page\_facing\_up:**Well structured content**

Make sure that the title of the page / article describes its content. (even without opening / reading it is possible to deduce h about what the page is about)

If headings are used, they should follow in logical order.

Do not use only strong elements for interline highlighting, especially for longer parts.

`abbr` html tag for abbreviations and acronyms (there is a [Drupal CKEditor plugin](https://www.drupal.org/project/ckeditor\_abbreviation) for that).

default text with `lang` and optionally work with `dir` properties - which CKEditor does not yet know - until then you could write your own plugin.

## :link:Links

Do not link to consecutive items.

If you are not linking to an HTML page, the text of the link will include its type (e.g. PDF).

The text of the link always contains what we are linking to, not a URL or anything like that:&#x20;

* _more_,
* _read more_,
* _see more_,
* _click here_,
* _find more_,
* and so on...

## :frame\_photo:Media

Use images with appropriate contrast ratios.

Avoid images that contain content text. (if the same text is not present as text).

Avoid using flashing gifs.

Don’t mark anything by itself with just a color distinction (this also applies to text and images).

### Alternative text

Obligatory! (required; blank = no image)&#x20;

It contains what it means to a sighted person (not what is seen on it).&#x20;

Don't be too long (max about 100 characters)&#x20;

Choose your text carefully: do not have the same name as the file, do not have the same / similar as a text element next to it, contain only a blank space or any word that contains an image, picture, chart, photo, etc.- t means (this is predicted by screen readers).

### **Caption / title**

Not to be confused with `alt` text!&#x20;

Optional&#x20;

The text requirements are the same as for `alt` text.
