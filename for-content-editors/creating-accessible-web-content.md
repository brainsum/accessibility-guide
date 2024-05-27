# 📄 Creating accessible web content

## :warning:Prevent faulty HTML code

Avoid empty HTML tags, like:

* blank lines,
* blank HTML tag pairs (these are mostly `div`s, `span`s)
* incorrect HTML tag pairs,
* :point\_up:**headings** (it's very important for SEO too)
* :point\_up:**link elements**

The content embedded from other sources should be cleaned up (including inline colors, sizes specified in px, and fonts) - Drupal and CKEditor can provide tools for this.

## :page\_facing\_up:**Well structured content**

Make sure that the title of the page/article describes its content. The visitor should figure out what the page/article is about without opening/reading it.

If headings are used, they should follow a logical order.

Don't use strong elements only for highlighting, especially true for longer texts.

Use the `abbr` HTML tag for abbreviations and acronyms. There is a [Drupal CKEditor plugin](https://www.drupal.org/project/ckeditor\_abbreviation) for that.

Use the `lang` and optionally the `dir` properties for paragraphs in a different language than the default of the current page. Currently, the CKEditor doesn't have a tool for this, but they are working on it! Until then we should write our own plugin.

## :link:Links

Elements that follow each other shouldn't link to the same target.

If you are not linking to an HTML page, the text of the link will include its type (e.g: [You can download my CV (in PDF).](https://app.gitbook.com/o/K4Ea26KknbCV5NcNGUaW/s/w15FEIBrSU7S7mHLcMoD/)).

The text of the link always contains what we are linking to, not a URL or anything like these:&#x20;

* _more_,
* _read more_,
* _see more_,
* _click here_,
* _find more_,
* and so on...

## :frame\_photo:Media

Use images with appropriate contrast ratios.

Avoid images that contain text content. (if the same text is not present as text).

Avoid using flashing gifs.

Don’t mark anything with color only (this applies to text and images too).

### Alternative text

{% hint style="danger" %}
<mark style="color:red;">**Obligatory!**</mark>

<mark style="color:red;">It's a required property of the</mark> <mark style="color:red;"></mark><mark style="color:red;">`<img>`</mark> <mark style="color:red;"></mark><mark style="color:red;">tag. Missing = the image does not exist!</mark>
{% endhint %}

It contains what it means to a visitor who can see it. (and not what we can see on it).&#x20;

Don't be too long. (max. \~100 characters)&#x20;

Choose your text carefully:

* don't use the filename as alt text,
* don't use the same/similar text as alt text as surrounding texts,
* alt text doesn't contain only a blank space,
* the following words are prohibited in the alt text (the screen readers know it's an image but don't know what about it):
  * image,
  * picture,
  * photo,
  * chart,
  * etc.

### **Caption / title**

Don't be confused with `alt` text! It's an optional complementary text. If you want to give a title for an image, use the `<figure>` and `<figcaption>` elements for this purpose.

{% hint style="danger" %}
<mark style="color:red;">Never use the</mark> <mark style="color:red;"></mark><mark style="color:red;">`title`</mark> <mark style="color:red;"></mark><mark style="color:red;">property on non-interactive elements, like</mark> <mark style="color:red;"></mark><mark style="color:red;">`<img>`</mark><mark style="color:red;">!</mark>
{% endhint %}

{% hint style="warning" %}
<mark style="color:orange;">The value of caption/title should be different than the value of alt property!</mark>
{% endhint %}

The text requirements are the same as for `alt` text.
