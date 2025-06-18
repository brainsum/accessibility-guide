---
description: Accessible Rich Internet Applications Suite
---

# ♿ WAI-ARIA

## **What is WAI-ARIA?**

The W3C [Web Accessibility Initiative ](https://www.w3.org/WAI/)makes websites and web applications more accessible to people with disabilities.

Specifically, it tries to help you understand the clear relationships between dynamically changing elements and elements that are visible to the normal user:

* provide sections/areas of the page (like header, navigation, sidebar, footer, etc)
* gives names and assigns roles to each HTML element
* gives a title property to any HTML item that has no text content,
* tracks the current status of interactive items.

Latest release: [WAI-ARIA 1.2](https://www.w3.org/TR/wai-aria-1.2/), released in 2023.

## **WAI-ARIA tools**

1. Widget-type roles, e.g. `menu`, `menuitem`, `slider`, `progressbar`.
2. Roles according to web page structure (header, footer, sidebar), e.g. `banner`, `main`, `contentinfo`.
3. Identification of items, e.g. `aria-label`, `aria-labelledby`.
4. Indicate the relationship between several elements, e.g. `aria-describedby`, `aria-owns`, `aria-haspopup`.
5. Indication of current status, e.g. `aria-checked`, `aria-disabled`, `aria-extended`.

## **Using WAI-ARIA**

**HTML5 priority:** Use Semantic HTML5 elements instead of ARIA attributes wherever possible, as they have the appropriate ARIA role by default!

In HTML5, give `aria-role` to elements if it is different from the default, for example:

{% code overflow="wrap" lineNumbers="true" %}
```html
<div class="button" aria-role="button">
    Click here!
</div>
```
{% endcode %}

{% hint style="danger" %}
<mark style="color:red;">**Don't forget!**</mark> <mark style="color:red;"></mark><mark style="color:red;">No ARIA property is much better than a bad ARIA property!</mark>
{% endhint %}

### Be cautious with duplicates &#x20;

Since screen readers read the `role` of a given item (even if it was not provided manually),  `title` and `label` of that item should not be the same because it will be read twice. E.g. use `aria-labelledby` instead of `aria-label`:

{% code overflow="wrap" lineNumbers="true" %}
```html
<nav aria-labelledby="navTitle">
    <h4 id="navTitle">Navigation<h4>
</nav>
```
{% endcode %}

### Dynamic ARIA properties

Those attributes that indicate the state, if they can be changed (`aria-checked`, `aria-extended`) must be alternated with JS.

### Connect the logically related DOM elements

Associate elements in different locations in the DOM but associated with the corresponding ARIA properties, e.g. [example of tab navigation](https://developer.mozilla.org/en-US/docs/Web/Accessibility/An_overview_of_accessible_web_applications_and_widgets):&#x20;

{% code overflow="wrap" lineNumbers="true" %}
```html
<!-- Now *these* are Tabs! -->
<!-- We've added role attributes to describe the tab list and each tab. -->
<ol role="tablist">
  <li id="ch1Tab" role="tab">
    <a href="#ch1Panel">Chapter 1</a>
  </li>
  <li id="ch2Tab" role="tab">
    <a href="#ch2Panel">Chapter 2</a>
  </li>
  <li id="quizTab" role="tab">
    <a href="#quizPanel">Quiz</a>
  </li>
</ol>

<div>
  <!-- Notice the role and aria-labelledby attributes we've added to describe these panels. -->
  <div id="ch1Panel" role="tabpanel" aria-labelledby="ch1Tab">Chapter 1 content goes here</div>
  <div id="ch2Panel" role="tabpanel" aria-labelledby="ch2Tab">Chapter 2 content goes here</div>
  <div id="quizPanel" role="tabpanel" aria-labelledby="quizTab">Quiz content goes here</div>
</div>
```
{% endcode %}

### :tools:Developer tools

* Chrome Developer debug tool: [Accessibility Tree](https://developer.chrome.com/blog/new-in-devtools-90/?utm_source=devtools#accesibility-tree) (experimental)

### :blue\_book:Guides

{% embed url="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques" %}
WAI-ARIA on MDN
{% endembed %}

{% embed url="https://www.smashingmagazine.com/2025/06/what-i-wish-someone-told-me-aria/" %}
Smashing Magazin's ARIA article for beginners
{% endembed %}
