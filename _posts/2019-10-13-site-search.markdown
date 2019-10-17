---
layout: single
title: "site search"
description: ""
permalink: /site-search/
tags:
 - jekyll
 - tutorial
date: "2019-10-13 23:19:16 +0200"
---

If you have hundreds or even dozen of posts, a search box added to your Jekyll site can be useful.
You could add a search box, for instance with DuckDuckGo[^1]:

<iframe src="https://duckduckgo.com/search.html?width=196&site=https://silentcomics.github.io/silent-mistakes/&prefill=Search DuckDuckGo" style="overflow:hidden;margin:0;padding:0;width:254px;height:40px;" frameborder="0"></iframe>


With this theme you can simply add an include:

```liquid
{% raw %}{% include site-search.html %}{% endraw %}
```

Will output the following:

{% include site-search.html %}

[^1]: See [https://duckduckgo.com/search_box](https://duckduckgo.com/search_box)
