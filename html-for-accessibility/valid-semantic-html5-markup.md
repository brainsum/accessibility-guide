# ✅ Valid Semantic HTML5 Markup

Whenever you can use HTML5 semantic tags. Please avoid using too generic tags like `<div>` > `<div>` > `<div>` or all text as `<p>`. But be careful some content elements had got a new meaning than before in HTML4/XHTML!&#x20;

{% hint style="warning" %}
<mark style="color:orange;">HTML5 tags should be used for semantic meaning, not for representation/theming purposes!</mark>
{% endhint %}

## Semantic Structure elements

### `<header>`

Top group/container/wrapper of a page (document) or a page section.

If you can't use `<header>` element (e.g.: not an HTML5 document or can't access directly to the DOM), please add `role="banner"` ARIA role in that header area container `<div>`.

### `<footer>`

Bottom container/wrapper of a page (document) or a page section; mostly for metadata.

If you can't use `<footer>` element (e.g.: not an HTML5 document or can't access directly to the DOM), please add `role="contentinfo"` ARIA role in that footer area container `<div>`.

### `<section>`

Generic part of a page. `<header>` and `<footer>` are also a `<section>`, but for specific purposes.

{% hint style="warning" %}
<mark style="color:orange;">**Not confused with the**</mark><mark style="color:orange;">** **</mark><mark style="color:orange;">**`<div> element!`**</mark><mark style="color:orange;">`The <section> element`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">is for a different part of a page while</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`<div>`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">is for generic grouping anything.</mark>
{% endhint %}

If you can't use `<section>` element (e.g.: not an HTML5 document or can't access directly to the DOM), please add `role="region"` ARIA role to that section area container.

### `<main>`

It's telling screenreaders where the main content begins. There should be only one instance of the `<main>` element on a page! For not responsive websites, mobile devices can zoom on them.

If you can't use `<main>` element (e.g.: not an HTML5 document or can't access directly to the DOM), please add `role="main"` ARIA role in that main area container `<div>`.&#x20;

### `<aside>`

The container of related/secondary content (primary content is the `<article>` element).

**Within an `<article>` element:**\
it's related to this `<article>`, like a glossary.

**Outside of an `<article>` element:**\
it's related to the page, like a sidebar, or a list of related posts/articles.

{% hint style="warning" %}
<mark style="color:orange;">**Don't confuse it with the sidebar region.**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">The sidebar may contain one or more</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`<aside>`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">elements, but an</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`<aside>`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">element could be anywhere else too.</mark>
{% endhint %}

If you can't use `<aside>` element (e.g.: not an HTML5 document or can't access directly to the DOM), please add `role="complementary"` ARIA role to that aside area container.

### `<article>`

Independent (document, like an article, post, comment) part of a page. It could have own `<header>`, `<footer>.`

Multiple `<article>` could be on a page or section of a page.

### `<nav>`

Use for main navigations of the site (subpages, a site map), yes not only for primary navigation, but you can also use it in multiple places. Even more, you can use it for paginations, breadcrumbs, or table of contents too.

{% hint style="info" %}
Not confuse with `<menu>` tag, which is for a group of contextual commands, like Drupal's block contextual menus.
{% endhint %}

If you can't use `<nav>` element (e.g.: not an HTML5 document or can't access directly to the DOM), please add `role="navigation"` ARIA role to that nav area container.

### `<div>`

It's a very generic grouping element and doesn't have any semantic meaning. Use it for grouping, theming purposes, or when you can't find any more suitable semantic element, like `<article>`, `<section>`, `<header>`...

## Semantic Content elements

### `<h1>` - `<h6>`

Headings are very important for semantic, SEO, and accessibility reasons too. They provide the outline of the current page. Therefore you must always check the HTML5 document outline.

All pages should have at least a `<h1>` element.

{% hint style="warning" %}
<mark style="color:orange;">Don't forget that headings are for semantic and document structure not for text sizing purposes!</mark>
{% endhint %}

For sizing you can provide heading css classes, for example:

{% code lineNumbers="true" %}
```html
<h2 class="h4">What a nice section title</h2>
```
{% endcode %}

### `<p>`

You should use it for **only** paragraphs or paragraphs like longer-length texts.

### `<span>`

The `<span>` is a very generic element, use it only when you don't find any more suitable/specific meaning tags.

{% hint style="info" %}
**Not for grouping purposes**, for grouping use the `<div>` element!

If you need to wrap content junk into an element and can't find it better, use the `<span>` tag.
{% endhint %}

### `<small>`

For small printed short-length text.

{% hint style="warning" %}
<mark style="color:orange;">Not for smaller font-sized text!</mark>
{% endhint %}

Use it for short length and less important texts, like a footnote, help text, an extension of another text, like:&#x20;

{% code lineNumbers="true" %}
```
<small>from </small><strong>$ 99.00</strong>
```
{% endcode %}

### `<strong>`

Use it for only very important text (like warnings, errors, sale price, etc.).

{% hint style="warning" %}
<mark style="color:orange;">Don't use it for bold styling!</mark>
{% endhint %}

{% hint style="warning" %}
<mark style="color:orange;">**Never use it for whole paragraphs, lines, or sentences!**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">Only for a bunch of important words.</mark>
{% endhint %}

### `<em>`

Use it only for text with emphasis. It doesn't have the importance the `<strong>` element has.

{% hint style="warning" %}
<mark style="color:orange;">Don't use it for italic styling!</mark>
{% endhint %}

{% hint style="warning" %}
<mark style="color:orange;">**Never use it for whole paragraphs, lines, or sentences!**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">Only for a bunch of words.</mark>
{% endhint %}

### `<b>`

Use for cases like keywords in a summary, product names in a review, or other spans of text whose typical presentation would be boldfaced (but not including any special importance, for that use `<strong>` element).

{% hint style="warning" %}
<mark style="color:orange;">If there is no semantic meaning, only want bold text.</mark>
{% endhint %}

{% hint style="success" %}
<mark style="color:green;">For theming purposes only set</mark> <mark style="color:green;"></mark><mark style="color:green;">`font-weight`</mark> <mark style="color:green;"></mark><mark style="color:green;">CSS property to</mark> <mark style="color:green;"></mark><mark style="color:green;">`bold:`</mark>

<mark style="color:green;">`<span class="bold">bold text, you see?</span>`</mark>
{% endhint %}

### `<i>`

For a text that is set off from the normal prose for readability reasons. This would be a range of text with different semantic meanings than the surrounding text.

{% hint style="success" %}
<mark style="color:green;">If there is no semantic meaning, only want italic style text, set</mark> <mark style="color:green;"></mark><mark style="color:green;">`font-style`</mark> <mark style="color:green;"></mark><mark style="color:green;">CSS property to</mark> <mark style="color:green;"></mark><mark style="color:green;">`italic:`</mark>

<mark style="color:green;">`<span class="italic">italic text, you see?</span>`</mark>
{% endhint %}

### `<u>`

It's a misunderstanding element, not underlining. Use it for the element including annotating spelling errors, applying a proper name mark to denote proper names in Chinese text and other forms of annotation.

{% hint style="success" %}
<mark style="color:green;">To underline text, you should instead apply a style that includes the CSS</mark> <mark style="color:green;"></mark><mark style="color:green;">`text-decoration`</mark> <mark style="color:green;"></mark><mark style="color:green;">property set to</mark> <mark style="color:green;"></mark><mark style="color:green;">`underline:`</mark>&#x20;

<mark style="color:green;">`<span class="underlined">underlined text, you see?</span>`</mark>
{% endhint %}

{% hint style="warning" %}
<mark style="color:orange;">Avoid using the</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`<u>`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">element with its default styling (of underlined text) in such a way as to be confused with a hyperlink, which is also underlined by default.</mark>
{% endhint %}

### `<hr>`

Use it for a thematic break for different paragraphs.

{% hint style="warning" %}
<mark style="color:orange;">Don't use the</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`<hr>`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">element to just display a horizontal line.</mark>
{% endhint %}

{% hint style="success" %}
<mark style="color:green;">If no thematic breaking meaning draw it by CSS.</mark>
{% endhint %}

### `<ol>`, `<ul>`

Use them for all listed elements, but watch out: do not use `<div>` or other HTML elements between `<ul>`/`<ol>` and `<li>` elements. When we use a slider script, it's very typical it will wrap the `<li>` elements into one or more `<div>`s.

{% hint style="warning" %}
<mark style="color:orange;">However, we can override the bullets via CSS, do it only for theming purposes, and</mark> <mark style="color:orange;"></mark><mark style="color:orange;">**don't use CSS for content printing!**</mark>
{% endhint %}

### `<dl>`

You can use the definition list for many-to-many relationships. It's not a typical list: when you have more label/content like data. ex.:

{% code lineNumbers="true" %}
```html
<h3>Addresses</h3>

<dl>
    <dt>Office</dt>
    <dt>Customer Service</dt>
    <dd>Carl street 20, Bay Area, Los Angeles</dd>
    
    <dt>Storage Department</dt>
    <dd>Old King Street 236, Industry Area, San Francisco</dd>
</dl>
```
{% endcode %}

### \<table>

Use the `<table>` element only for table data.

{% hint style="warning" %}
<mark style="color:orange;">Never use it for layout or styling!</mark>
{% endhint %}

### `<address>`

It's a section of the page as well. It's grouping all contact info about the page/article/website's author.

{% hint style="warning" %}
<mark style="color:orange;">**The**</mark><mark style="color:orange;">** **</mark><mark style="color:orange;">**`<address>`**</mark><mark style="color:orange;">** **</mark><mark style="color:orange;">**element isn't for any postal address**</mark><mark style="color:orange;">, but you can use it for contact names, phones, email addresses, and postal addresses if it belongs to the current article/page/site's author.</mark>
{% endhint %}

{% hint style="success" %}
<mark style="color:green;">For normal addresses use</mark> <mark style="color:green;"></mark><mark style="color:green;">`<p>`</mark> <mark style="color:green;"></mark><mark style="color:green;">tag combinate with</mark> <mark style="color:green;"></mark><mark style="color:green;">`<br>`</mark><mark style="color:green;">-s (and optionally microformats).</mark>
{% endhint %}

{% embed url="https://schema.org/address" %}

### `<figure>`, `<figcaption>`

The `<figure>` element represents self-contained content, potentially with an optional caption, like images, quotes, or code blocks.

Use it when an image, group of images, a quote, or a code sample is closely related to the document flow.

It could contain one or more `<img>` elements. Optional, but it could contain a `<figcaption>` as a label that could be on top or bottom of a `<figure>` element.

You can use the `<figure>` element with the `<figcaption>` element for important images with hidden descriptive text, like a logo:

{% code lineNumbers="true" %}
```html
<figure>
    <img src="" alt="">
    <figcaption class="invisible"></figcaption>
</figure>
```
{% endcode %}

{% hint style="danger" %}
<mark style="color:red;">If you need to add a caption or title for an image, use the</mark> <mark style="color:red;"></mark><mark style="color:red;">`<figcaption>`</mark> <mark style="color:red;"></mark><mark style="color:red;">element for that, instead of the title property for an</mark> <mark style="color:red;"></mark><mark style="color:red;">`<img>`</mark> <mark style="color:red;"></mark><mark style="color:red;">element!</mark>
{% endhint %}

### `<blockquote>`, `<cite>`

For block-level quotes use the `<blockquote>` with `<figure>`, `<figcaption>`, and if possible with `<cite>` element, like in the MDN's example:

{% code lineNumbers="true" %}
```html
<figure>
    <blockquote cite="https://www.huxley.net/bnw/four.html">
        <p>Words can be like X-rays, if you use them properly—they’ll go through anything. You read and you’re pierced.</p>
    </blockquote>
    <figcaption>—Aldous Huxley, <cite>Brave New World</cite></figcaption>
</figure>
```
{% endcode %}

