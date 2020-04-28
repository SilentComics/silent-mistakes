---
layout: single
title: "Gumroad overlay post"
description: "How to post products with the Gumroad overlay"
permalink: /gumroad-overlay-post/
tags:
 - jekyll
 - tutorial
 - gumroad
date: "2019-10-13 23:19:16 +0200"
---

You'll find Gumroad integration snippets in `_includes`.
There are two ways to post a Gumroad product on your site: embed or overlay.
On this post we will look how to use the overlay method.

## Gumroad Overlay

This snippet: https://gum.co/strip

```liquid
{% raw %}{% include gumroad-overlay.html id="strip" %}{% endraw %}
```
will output this:

{% include gumroad-overlay.html id="strip" %}

If you click on this button, you'll get an overlay of the product page on your post page.

Now, this would be a lot nicer if we had an actual product image linking to Gumroad overlay, right?
Let's write this above our include liquid snippet:

```html
{% raw %}<a href="https://gum.co/strip" class=""><img class="" src="{{site.baseurl}}/images/customise-dashboard-strip-theme.jpg"></a>{% endraw %}
```

Note that you can add class to style your html and image according to your site styling and layout.
{: .notice}

It now looks much better:

<a href="https://gum.co/strip" class=""><img class="" src="{{site.baseurl}}/images/customise-dashboard-strip-theme.jpg"></a>

{% include gumroad-overlay.html id="strip" %}

Clicking on this image will prompt the Gumroad overlay on your page.

The overlay method is nice because it lets users buy securely from Gumroad without leaving your site.

## Related files:

- `gumroad-overlay.html` in `_includes`


You could tweak this to include the Gumroad ID in your post front-matter.
{: .notice}
