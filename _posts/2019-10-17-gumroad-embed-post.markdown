---
layout: single
title: "Gumroad embed post"
description: "How to post products with the Gumroad embed code"
permalink: /gumroad-embed-post/
tags:
 - jekyll
 - tutorial
 - gumroad
date: "2019-10-13 23:19:16 +0200"
---

You'll find Gumroad integration snippets in `_includes`.
There are two ways to post a Gumroad product on your site: embed or overlay.
On this post we will look how to use the embed method.

## Gumroad embed

This snippet: https://gum.co/strip

```liquid
{% raw %}{% include gumroad-embed.html id="stript" %}{% endraw %}
```
will output this:

{% include gumroad-embed.html id="strip" %}

If you click on it, you'll get a link to the Gumroad product page.

Now, this would be a lot nicer if we had an actual product image linking to Gumroad overlay, right?
Let's write this above our include liquid snippet:

```html
{% raw %}<a href="https://gum.co/strip" class=""><img class="" src="{{site.baseurl}}/images/customise-dashboard-strip-theme.jpg"></a>{% endraw %}
```

```liquid
{% raw %}{% include gumroad-embed.html id="strip" %}{% endraw %}
```

Note that you can add class to style your html and image according to your site styling and layout.
{: .notice}

That will output the following:

<a href="https://gum.co/strip" class=""><img class="" src="{{site.baseurl}}/images/customise-dashboard-strip-theme.jpg"></a>
{% include gumroad-embed.html id="strip" %}

It now looks much better.

Clicking on the image or button will link to a new page: the embed code takes the visitor to the Gumroad product page.

## Related files:

- `gumroad-embed.html` in `_includes`

You could tweak this to include the Gumroad ID in your post front-matter.
{: .notice}
