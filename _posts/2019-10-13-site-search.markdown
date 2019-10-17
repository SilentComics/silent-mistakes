---
layout: single
title: "Site search"
description: ""
permalink: /site-search/
tags:
 - jekyll
 - tutorial
date: "2019-10-13 23:19:16 +0200"
---

If you have hundreds or even dozen of posts, a search box added to your Jekyll site can be useful.
With a few lines of code, you could add a search box, search engines provides snippets to do this easily.
Here is a search box for DuckDuckGo[^1]:

This snippet:

```html
{% raw %}<iframe src="https://duckduckgo.com/search.html?width=196&site=https://silentcomics.github.io/silent-mistakes/&prefill=Search DuckDuckGo" style="overflow:hidden;margin:0;padding:0;width:254px;height:40px;" frameborder="0"></iframe>{% endraw %}
```
will output this:

<iframe src="https://duckduckgo.com/search.html?width=196&site=https://silentcomics.github.io/silent-mistakes/&prefill=Search DuckDuckGo" style="overflow:hidden;margin:0;padding:0;width:254px;height:40px;" frameborder="0"></iframe>

Now, that search box will take users only to pages that are indexed by DuckDuckGo.

The theme has **search** backed in within the site, which will prompt pages relevant to a given inquiry. You can simply add an include:

```liquid
{% raw %}{% include site-search.html %}{% endraw %}
```

Will output the following:

{% include site-search.html %}

[^1]: See [https://duckduckgo.com/search_box](https://duckduckgo.com/search_box)

## Related files:

- `site-search.html` in `_includes`
- `search.json` in `assets`
- `fetch` in `assets/js`

The minified file with all JavaScript code is `assets/js/main.min.js` so you'll need to rebuild the site js with the `npm run uglify` command to reflect change to JavaScript functions.
{: .notice}
