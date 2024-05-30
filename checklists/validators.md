# 🤖 Validators

## The official recommended validators by W3C

### W3C Markup Validator

could check: valid HTML5 code, regular use, no open tags

versions: web (there are some third-party browser extensions)

{% embed url="https://validator.w3.org" %}

### W3C CSS Validator

&#x20;could check: correct or at least usable in any browser you want to support

versions: web

{% embed url="https://jigsaw.w3.org/css-validator/" %}

### List of other recommended validators

{% embed url="https://www.w3.org/WAI/WCAG21/Techniques/general/G134.html" %}

## Third-party recommended, battle-tested validators

### Google Lighthouse

versions: web, browser extension

{% embed url="https://pagespeed.web.dev" %}

### HTML\_CodeSniffer

versions: web (source code paste), bookmarklet, Drupal module (see [Editoria11y Accessibility Checker](validators.md#page-subtitle))

supported standards:

* WCAG 2.1 A
* WCAG 2.1 AA
* WCAG 2.1 AAA
* Section 508

{% embed url="http://squizlabs.github.io/HTML_CodeSniffer/" %}

### ARC Toolkit

versions: browser extension

supported standards:

* WCAG 2.0 AA (links to the official doc)
* WCAG 2.1 AA (links to the official doc)

<figure><img src="../.gitbook/assets/Screenshot 2022-09-06 at 17.26.24.png" alt=""><figcaption><p>For localhost audit you must enable URL access for it!</p></figcaption></figure>

{% embed url="https://chrome.google.com/webstore/detail/arc-toolkit/chdkkkccnlfncngelccgbgfmjebmkmce" %}

### Accessibility Insights

versions: browser extension

{% embed url="https://accessibilityinsights.io" %}

### WebAIM WAVE

The most popular accessibility audit tool

versions: web, browser extension

supported standards:

* WCAG 2.0 (links to its simplified own docs)

{% embed url="https://wave.webaim.org" %}

### A11ygator

versions: web, Chrome extension

supported standards:&#x20;

* WCAG 2.0 A-AAA
* Section 508

{% hint style="info" %}
In the web version, we can choose between standards.
{% endhint %}

{% embed url="https://a11ygator.chialab.io" %}

### ANDI by the [US government](https://github.com/SSAgov)

versions: browser bookmarklet

supported standards:

* Section 508

{% hint style="warning" %}
<mark style="color:orange;">If we need to comply with</mark> [<mark style="color:orange;">**Section 508**</mark>](../standards/section-508.md)<mark style="color:orange;">, don't miss it.</mark>
{% endhint %}

{% embed url="https://www.ssa.gov/accessibility/andi/help/install.html" %}

### Deque Axe

versions: browser extension

It's used by [Google Lighthouse](validators.md#google-lighthouse) too under the hood.

supported standards:

* WCAG 2.0 (links to its simplified own docs)

{% embed url="https://www.deque.com/axe/" %}

### Mozilla Firefiox Accessibility Tools

* Tab order inspector
* Checking issues for:
  * Koyboard navigvation
  * Text labels
  * Color contrast
* Color-blind modes

<figure><img src="../.gitbook/assets/Screenshot 2024-05-30 at 07.09.14.png" alt=""><figcaption><p>Firefox Accessibility Tools tab with activated Tab order</p></figcaption></figure>

### Editoria11y Accessibility Checker <a href="#page-subtitle" id="page-subtitle"></a>

Primary for content editors.

versions: Drupal module (9.x, 10.x, 11.x)

{% embed url="https://www.drupal.org/project/editoria11y" %}

### Devel Accessibility

For testing these Drupal features easier:

* `Drupal.announce` announcements
* `Drupal.TabbingManager` tabbing constraints

{% embed url="https://www.drupal.org/project/devel_a11y" %}

### Pa11y

CLI tool for quick checkout, monitoring multiple sites via dashboard and CI.

{% embed url="https://pa11y.org/" %}
