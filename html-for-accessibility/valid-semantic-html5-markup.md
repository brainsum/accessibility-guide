# ✅ Valid Semantic HTML5 Markup

Whenever you can use HTML5 semantic tags. Please avoid using too generic tags like `<div>` > `<div>` > `<div>` or all text as `<p>`. But be careful some content element had got a new meaning than before in HTML4/XHTML!&#x20;

{% hint style="warning" %}
<mark style="color:orange;">HTML5 tags should be used for semantic meaning, not for representation/theming purposes!</mark>
{% endhint %}

## Semantic Structure elements

### `<header>`

Top group/container/wrapper of a page (document) or a page section.

If you can't use `<header>` element (e.g.: not a HTML5 document or can't access directly to the DOM), please add `role="banner"` ARIA role to that header area container `<div>`.

### `<footer>`

Bottom container/wrapper of a page (document) or a page section; mostly for metadata.

If you can't use `<footer>` element (e.g.: not a HTML5 document or can't access directly to the DOM), please add `role="contentinfo"` ARIA role to that footer area container `<div>`.

### `<section>`

Generic part of a page. `<header>` and `<footer>` are also a `<section>`, but for specific purposes.

{% hint style="warning" %}
<mark style="color:orange;">**Not confuse with the**</mark><mark style="color:orange;">** **</mark><mark style="color:orange;">**`<div> element!`**</mark><mark style="color:orange;">`The <section> element`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">is for a different part of a page while</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`<div>`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">is for generic grouping anything.</mark>
{% endhint %}

If you can't use `<section>` element (e.g.: not a HTML5 document or can't access directly to the DOM), please add `role="region"` ARIA role to that section area container.

### `<main>`

It's telling for screenreaders where the main content begins. There should be only one instance of the `<main>` element in a page! For not responsive websites, mobile devices can zoom on it.

If you can't use `<main>` element (e.g.: not a HTML5 document or can't access directly to the DOM), please add `role="main"` ARIA role to that main area container `<div>`.&#x20;

### `<aside>`

The container of related/secondary content (primary content is the `<article>` element).

**Within an `<article>` element:**\
****it's related to this `<article>`, like a glossary.

**Outside of an `<article>` element:**\
****it's related to the page, like sidebar, list of related posts/articles.

{% hint style="warning" %}
<mark style="color:orange;">**Don't fonfuse with sidebar region.**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">The sidebar may contain one or more</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`<aside>`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">elements, but an</mark> <mark style="color:orange;"></mark><mark style="color:orange;">`<aside>`</mark> <mark style="color:orange;"></mark><mark style="color:orange;">element could be anywhere else too.</mark>
{% endhint %}

If you can't use `<aside>` element (e.g.: not a HTML5 document or can't access directly to the DOM), please add `role="complementary"` ARIA role to that aside area container.

### `<article>`

Independent (document, like an article, post, comment) part of a page. It could have own `<header>`, `<footer>.`

Multiple `<article>` could be in a page or section of a page.

### `<nav>`

Use for major navigations of the site (subpages, a site map), yes not only for main navigation, but you can also use it multiple places. Even more you can use it for paginations, breadcrumbs, or table of contents too.

{% hint style="info" %}
Not confuse with `<menu>` tag, which is for a group of contextual commands, like Drupal's block contextual menus.
{% endhint %}

If you can't use `<nav>` element (e.g.: not a HTML5 document or can't access directly to the DOM), please add `role="navigation"` ARIA role to that nav area container.

### `<div>`

It's very generic grouping element, doesn't have any semantic meaning. Use it for grouping, theming purposes or when you can't find any more suitable more semantic element, like `<article>`, `<section>`, `<header>`...

## Semantic Content elements

* `<ul>`, `<ol>`, `<dl>`
* `<figure>`, `<figcaption>`
* `<blockquote>`, `<q>`, `<cite>`
* `<address>`
* `<small>`
* `<h1>` ... `<h6>`
* `<em>`
* `<strong>`
* \[...]
