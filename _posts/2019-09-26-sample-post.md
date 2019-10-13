---
layout: single
title: "Sample Post"
description: ""
permalink: /sample-post/
excerpt: "Just about everything you'll need to style in the theme: headings, paragraphs, block quotes, tables, code blocks, and more."
author: false
tags:
 - jekyll
 - tutorial
comments: true
header:
    image: /images/sky.jpg # Set a background image.
    caption: "Test image" # Create captions with support for markdown urls.
---

{% include toc title="Table of content" icon="file-text" %}

## HTML Elements

Below is just about everything you'll need to style in the theme. Check the source code to see the many embedded elements within paragraphs.

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

### Body text

Lorem ipsum dolor sit amet, test link adipiscing elit. **This is strong**. Nullam dignissim convallis est. Quisque aliquam.

*This is emphasized*. Donec faucibus. Nunc iaculis suscipit dui. 53 = 125. Water is H2O. Nam sit amet sem. Aliquam libero nisi, imperdiet at, tincidunt nec, gravida vehicula, nisl. The New York Times (That’s a citation). Underline.Maecenas ornare tortor. Donec sed tellus eget sapien fringilla nonummy. Mauris a ante. Suspendisse quam sem, consequat at, commodo vitae, feugiat in, nunc. Morbi imperdiet augue quis tellus.

HTML and CSS are our tools. Mauris a ante. Suspendisse quam sem, consequat at, commodo vitae, feugiat in, nunc. Morbi imperdiet augue quis tellus. Praesent mattis, massa quis luctus fermentum, turpis mi volutpat justo, eu volutpat enim diam eget metus.

## Blockquotes

Single line blockquote:

> Stay hungry. Stay foolish.

Multi line blockquote with a cite reference:

> People think focus means saying yes to the thing you've got to focus on. But that's not what it means at all. It means saying no to the hundred other good ideas that there are. You have to pick carefully. I'm actually as proud of the things we haven't done as the things I have done. Innovation is saying no to 1,000 things.

<cite>Steve Jobs</cite> --- Apple Worldwide Developers' Conference, 1997
{: .small}

## List Types

### Definition Lists

Definition List Title
:   Definition list division.

Startup
:   A startup company or startup is a company or temporary organization designed to search for a repeatable and scalable business model.

#dowork
:   Coined by Rob Dyrdek and his personal body guard Christopher "Big Black" Boykins, "Do Work" works as a self motivator, to motivating your friends.

Do It Live
:   I'll let Bill O'Reilly [explain](https://www.youtube.com/watch?v=O_HyZ5aW76c "We'll Do It Live") this one.


### Ordered Lists

1. Item one
   1. sub item one
   2. sub item two
   3. sub item three
2. Item two

### Unordered Lists

* Item one
* Item two
* Item three

## Unordered Lists (Nested)

  * List item one
      * List item one
          * List item one
          * List item two
          * List item three
          * List item four
      * List item two
      * List item three
      * List item four
  * List item two
  * List item three
  * List item four

## Tables

| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|----
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=====
| Foot1   | Foot2   | Foot3
{: rules="groups"}

## Code Snippets

{% highlight css %}
#container {
  float: left;
  margin: 0 -240px 0 0;
  width: 100%;
}
{% endhighlight %}

## Buttons

Make any link standout more when applying the `.btn` class.

{% highlight html %}
<a href="#" class="btn btn-success">Success Button</a>
{% endhighlight %}

<div markdown="0"><a href="#" class="btn">Primary Button</a></div>
<div markdown="0"><a href="#" class="btn btn--inverse">Inverse Button</a></div>
<div markdown="0"><a href="#" class="btn btn--success">Success Button</a></div>
<div markdown="0"><a href="#" class="btn btn--warning">Orange Button</a></div>
<div markdown="0"><a href="#" class="btn btn--danger">Red Button (Danger)</a></div>
<div markdown="0"><a href="#" class="btn btn--info">Info Button</a></div>
<div markdown="0"><a href="#" class="btn btn--blue">Blue Button</a></div>
<div markdown="0"><a href="#" class="btn btn--yellow">Yellow Button</a></div>
<div markdown="0"><a href="#" class="btn btn--pink">Pink Button</a></div>
<div markdown="0"><a href="#" class="btn btn--purple">Purple Button</a></div>
<div markdown="0"><a href="#" class="btn btn--black">Black Button</a></div>


The `.btn` class code:

{% highlight html %}
<div markdown="0">
<a href="{{ site.url}}/notes"
class="btn btn--yellow align-right"
>View all notes</a>
</div>
{% endhighlight %}

<div markdown="0"><a href="{{ site.url}}/notes" class="btn btn--yellow align-right">View all notes</a></div>

moves the button to the right like this:

## Notices

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice}

## images
![Test Image]({{ site.url }}/images/sky.jpg)
{: .align-right}

...
(to be continued)
