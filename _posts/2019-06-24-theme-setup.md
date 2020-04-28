{% include toc title="Table of content" icon="file-text" %}

General notes and suggestions for customizing *silent mistakes*.

## Basic Setup for a new Jekyll site

1. [Install Bundler](http://bundler.io) `gem install bundler` and then install [Jekyll](http://jekyllrb.com) and all dependencies `bundle install`.
2. Fork the [Silent Mistakes repo](http://github.com/SilentComics/silent-mistakes/fork).
3. Clone the repo you just forked and rename it.
4. Edit `_config.yml` to personalize your site.
5. Check out the sample posts in `_posts` to see examples for pulling in large feature images, assigning categories and tags, and other YAML data.
6. Read the documentation below for further customization pointers and documentation.

<div markdown="0"><a href="https://github.com/SilentComics/silent-mistakes/archive/master.zip" class="btn">Download the Theme</a></div>

**Pro-tip:** Delete the `gh-pages` branch after cloning and start fresh by branching off `master`.
{: .notice}

---

## Folder Structure

{% highlight text %}
silent-mistakes/
├── CNAME
├── Gemfile
├── Gemfile.lock
├── LICENSE.txt
├── README.md
├── SC_LOGO.svg
├── _config.yml
├── _data
│   ├── authors.yml
│   ├── comments
│   ├── navigation.yml
│   └── ui-text.yml
├── _drafts
│   └── theme-setup.md
├── _essays
│   └── essay-tips.md
├── _includes
│   ├── analytics-providers
│   │   ├── custom.html
│   │   ├── google-universal.html
│   │   └── google.html
│   ├── analytics.html
│   ├── archive-single.html
│   ├── author-profile.html
│   ├── base_path
│   ├── breadcrumbs.html
│   ├── browser-upgrade.html
│   ├── category-list.html
│   ├── comment-form.html
│   ├── comment.html
│   ├── comments-providers
│   │   ├── custom.html
│   │   ├── scripts.html
│   │   └── staticman.html
│   ├── comments.html
│   ├── feature_row
│   ├── figure
│   ├── footer
│   │   └── custom.html
│   ├── footer.html
│   ├── gallery
│   ├── group-by-array
│   ├── head
│   │   └── custom.html
│   ├── head.html
│   ├── masthead.html
│   ├── nav_list
│   ├── page__hero.html
│   ├── page__hero_video.html
│   ├── page__taxonomy.html
│   ├── paginator.html
│   ├── post_pagination.html
│   ├── read-time.html
│   ├── scripts.html
│   ├── sidebar.html
│   ├── signup-widget.html
│   ├── site-search.html
│   ├── social-share.html
│   ├── tag-list.html
│   ├── toc
│   └── video.html
├── _layouts
│   ├── archive-taxonomy.html
│   ├── archive.html
│   ├── compress.html
│   ├── default.html
│   ├── home.html
│   ├── single.html
│   └── splash.html
├── _pages
│   ├── 404.md
│   ├── Newsletter.md
│   ├── category-archive.html
│   ├── collection-archive.html
│   ├── essays-archive.html
│   ├── notes.html
│   ├── page-archive.html
│   ├── portfolio-archive.html
│   ├── sitemap.md
│   ├── tag-archive.html
│   └── year-archive.html
├── _plugins
│   └── svg_mime_type.rb
├── _portfolio
│   └── portfolio-sample.md
├── _posts
│   ├── 2019-06-24-theme-setup.md
│   ├── 2019-08-25-markdown-stylesheet.md
│   ├── 2019-09-26-sample-post.md
│   └── archive-layout-with-content.md
├── _sass
│   ├── _animations.scss
│   ├── _archive.scss
│   ├── _base.scss
│   ├── _buttons.scss
│   ├── _footer.scss
│   ├── _forms.scss
│   ├── _main.scss
│   ├── _masthead.scss
│   ├── _mixins.scss
│   ├── _navigation.scss
│   ├── _notices.scss
│   ├── _page.scss
│   ├── _print.scss
│   ├── _reset.scss
│   ├── _sidebar.scss
│   ├── _syntax.scss
│   ├── _tables.scss
│   ├── _utilities.scss
│   ├── _variables.scss
│   ├── comments.scss
│   └── vendor
│       ├── breakpoint
│       │   ├── _breakpoint.scss
│       │   ├── _context.scss
│       │   ├── _helpers.scss
│       │   ├── _legacy-settings.scss
│       │   ├── _no-query.scss
│       │   ├── _parsers.scss
│       │   ├── _respond-to.scss
│       │   ├── _settings.scss
│       │   └── parsers
│       │       ├── _double.scss
│       │       ├── _query.scss
│       │       ├── _resolution.scss
│       │       ├── _single.scss
│       │       ├── _triple.scss
│       │       ├── double
│       │       │   ├── _default-pair.scss
│       │       │   ├── _default.scss
│       │       │   └── _double-string.scss
│       │       ├── resolution
│       │       │   └── _resolution.scss
│       │       ├── single
│       │       │   └── _default.scss
│       │       └── triple
│       │           └── _default.scss
│       └── susy
│           ├── _su.scss
│           ├── _susy.scss
│           ├── _susyone.scss
│           └── susy
│               ├── _su.scss
│               ├── language
│               │   ├── _susy.scss
│               │   ├── _susyone.scss
│               │   ├── susy
│               │   │   ├── _background.scss
│               │   │   ├── _bleed.scss
│               │   │   ├── _box-sizing.scss
│               │   │   ├── _breakpoint-plugin.scss
│               │   │   ├── _container.scss
│               │   │   ├── _context.scss
│               │   │   ├── _gallery.scss
│               │   │   ├── _grids.scss
│               │   │   ├── _gutters.scss
│               │   │   ├── _isolate.scss
│               │   │   ├── _margins.scss
│               │   │   ├── _padding.scss
│               │   │   ├── _rows.scss
│               │   │   ├── _settings.scss
│               │   │   ├── _span.scss
│               │   │   └── _validation.scss
│               │   └── susyone
│               │       ├── _background.scss
│               │       ├── _functions.scss
│               │       ├── _grid.scss
│               │       ├── _isolation.scss
│               │       ├── _margin.scss
│               │       ├── _media.scss
│               │       ├── _padding.scss
│               │       └── _settings.scss
│               ├── output
│               │   ├── _float.scss
│               │   ├── _shared.scss
│               │   ├── _support.scss
│               │   ├── float
│               │   │   ├── _container.scss
│               │   │   ├── _end.scss
│               │   │   ├── _isolate.scss
│               │   │   └── _span.scss
│               │   ├── shared
│               │   │   ├── _background.scss
│               │   │   ├── _container.scss
│               │   │   ├── _direction.scss
│               │   │   ├── _inspect.scss
│               │   │   ├── _margins.scss
│               │   │   ├── _output.scss
│               │   │   └── _padding.scss
│               │   └── support
│               │       ├── _background.scss
│               │       ├── _box-sizing.scss
│               │       ├── _clearfix.scss
│               │       ├── _prefix.scss
│               │       ├── _rem.scss
│               │       └── _support.scss
│               └── su
│                   ├── _grid.scss
│                   ├── _settings.scss
│                   ├── _utilities.scss
│                   └── _validation.scss
{% endhighlight %}

---

## Customization

### _config.yml

Most of the variables found here are used in the .html files found in `_includes` if you need to add or remove anything. A good place to start would be to change the `title`, `description`, and `url` of your site. When working locally use `http://localhost:4000` or comment out `url` to avoid broken links prefixed with `{{ "{{ site.url " }}}}`[^1] in the various `_includes` and `_layouts`. Just remember to set `url` back to the live domain before deploying or pushing to GitHub Pages.

#### Owner/Author Information

Change your name, bio, and avatar photo (100x100 pixels or larger), Twitter url, email, etc. If you want to link to an external image on Gravatar or something similar you'll need to edit the path in `_author-profile.html` since it assumes it is located in `/images`.

#### Google Analytics and Webmaster Tools

If you want to waste time watching analytics, your Google Analytics ID goes here along with meta tags for [Google Webmaster Tools](http://support.google.com/webmasters/bin/answer.py?hl=en&answer=35179) and [Bing Webmaster Tools](https://ssl.bing.com/webmaster/configure/verify/ownershi) site verification.

#### Top Navigation Links

Edit page/post titles and URLs to include in the site's navigation. For external links add `external: true`.

{% highlight yaml %}
# sample top navigation links
links:
  - title: About Page
    url: /about/
  - title: Posts
    url: /posts/
  - title: Other Page
    url: /other-page/
  - title: External Page
    url: https://silentcomics.com
    external: true
{% endhighlight %}

### Adding Posts and Pages

There are two main content layouts: *post.html* (for posts) and *page.html* (for pages). Both have large **feature images** that span the full-width of the screen, and both are meant for long form articles and blog posts.

There are two rake tasks that can be used to create a new post or page with all YAML Front Matter. Using either `rake new_post` or `rake new_page` will prompt you for a title and tags to classify them. Example below:

{% highlight bash %}
rake new_post

Enter a title for your post: My Awesome Post
Enter category name to group your post in (leave blank for none): blog
Enter tags to classify your post (comma separated): web development, code
Creating new post: _posts/2014-02-10-my-awesome-post.md
{% endhighlight %}

There are a few configuration variables that can be changed in `Rakefile.rb`. By default posts and pages will be created in MarkDown using the `.md` extension.

#### Feature Images

A good rule of thumb is to keep feature images nice and wide so you don't push the body text too far down. An image cropped around around 1024 x 256 pixels will keep file size down with an acceptable resolution for most devices. If you want to serve these images responsively I'd suggest looking at the [Jekyll Picture Tag](https://github.com/scottjehl/picturefill) plugin[^2].

The two layouts make the assumption that the feature images live in the `images/` folder. To add a feature image to a post or page just include the filename in the front matter like so.

{% highlight yaml %}
image:
  feature: feature-image-filename.jpg
  thumb: thumbnail-image.jpg #keep it square 200x200 px is good
{% endhighlight %}

If you want to apply attribution to a feature image use the following YAML front matter on posts or pages. Image credits appear directly below the feature image with a link back to the original source.

{% highlight yaml %}
image:
  feature: feature-image-filename.jpg
  credit: Silent Comics #name of the person or site you want to credit
  creditlink: https://silentcomics.com #url to their site or licensing
{% endhighlight %}

#### Post Index Page

A [sample index page]({{ site.url }}/posts/) listing all posts grouped by the year they were published has been provided. The name can be customized to your liking by editing a few references. For example, to change **Posts** to **Writing** update the following:

* In `_config.yml` under `links:` rename the title and URL to the following:
{% highlight yaml %}
  links:
  - title: Writing
    url: /writing/
{% endhighlight %}
* Rename `posts.md` to `writing.md` and update the YAML front matter to match the title and URL set in `_config.yml`
* Update the **View all posts** link in `post.html` layout found in `_layouts` to match title and URL set previously.

#### Thumbnails for OG and Twitter Cards

Post and page thumbnails work the same way. These are used by [Open Graph](https://developers.facebook.com/docs/opengraph/) and [Twitter Cards](https://dev.twitter.com/docs/cards) meta tags found in *_head.html*. If you don't assign a thumbnail the default graphic *(default-thumb.png)* is used. I'd suggest changing this to something more meaningful --- your logo or avatar are good options.

#### Table of Contents

Any article or page that you want a *table of contents* to render insert the following HTML in your post before the actual content. [Kramdown will take care of the rest](http://kramdown.rubyforge.org/converter/html.html#toc) and convert all headlines into a contents list.

**PS:** The TOC is hidden on small devices because I haven't gotten around to optimizing it. For now it only appears on larger screens (tablet and desktop).
{: .notice}

{% highlight html %}
<section id="table-of-contents" class="toc">
  <header>
    <h3>Contents</h3>
  </header>
<div id="drawer" markdown="1">
*  Auto generated table of contents
{:toc}
</div>
</section><!-- /#table-of-contents -->
{% endhighlight %}

#### Videos

Video embeds are responsive and scale with the width of the main content block with the help of [FitVids](http://fitvidsjs.com/).

Not sure if this only effects Kramdown or if it's an issue with Markdown in general. But adding YouTube video embeds causes errors when building your Jekyll site. To fix add a space between the `<iframe>` tags and remove `allowfullscreen`. Example below:

{% highlight html %}
<iframe width="560" height="315" src="http://www.youtube.com/embed/PWf4WUoMXwg" frameborder="0"> </iframe>
{% endhighlight %}

---

## Theme Development

If you want to easily skin the themes' colors and fonts, take a look at `variables.scss` in `_sass` and make the necessary changes to the color and font variables. To make development easier I setup a Grunt build script to compile/minify the JS files into `main.js` and lint/concatenate/minify all scripts into `main.min.js`. [Install Node.js](http://nodejs.org/), then [install npm](http://gruntjs.com/getting-started), and then finally install the dependencies for the theme contained in `package.json`:

{% highlight bash %}
npm install
{% endhighlight %}


From the theme's root, use `grunt` to rebuild the CSS, concatenate JavaScript files, and optimize .jpg, .png, and .svg files in the `images/` folder. You can also use `grunt watch` in combination with `jekyll build --watch` to watch for updates to your LESS and JS files that Grunt will then automatically re-build as you write your code which will in turn auto-generate your Jekyll site when developing locally.

And if the command line isn't your thing (you're using Jekyll so it probably is), [CodeKit](http://incident57.com/codekit/) for Mac OS X and [Prepros](http://alphapixels.com/prepros/) for Windows are great alternatives.

---

## Questions?

Having a problem getting something to work? Please [file a GitHub Issue](https://github.com/silentcomics/silent-mistakes/issues/new).

---

## License

This theme is free and open source software, distributed under the [MIT License]({{ site.url }}/LICENSE). So feel free to use this Jekyll theme on your site without linking back or including a disclaimer.


[^1]: Used to generate absolute urls in `sitemap.xml`, `feed.xml`, and for canonical urls in `_head.html`. Don't include a trailing `/` in your base url ie: `https://silentcomics.com`. When developing locally remove or comment out this line so local .css, .js, and images are used.

[^2]: If you're using GitHub Pages to host your site be aware that plugins are disabled. So you'll need to build your site locally and then manually deploy if you want to use this sweet plugin.
