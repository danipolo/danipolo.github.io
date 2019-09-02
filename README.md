# xscrü 

Technical SEO Magazine.

## Features

* Live Search
* Image lightbox
* Contact form (FormSpree)
* Image lightbox and slider
* Disqus comments for posts (lazy loading on scroll down)
* Configurable home page
* Optimised for [GitHub](https://pages.github.com/) pages
* RSS feed
* SEO tags
* Google Tag Manager

## TODO
* Fix code for loading Disqus comments (it triggers 100 times)
* Add "Load more" to cagegories and disable pagination


## Installation

Install the dependencies with [Bundler](http://bundler.io/):

```bash
bundle install
```

Run the following to generate your site:
```bash
bundle exec jekyll serve
```

You can find more on [Deployment Methods](https://jekyllrb.com/docs/deployment-methods/) page on Jekyll website.

## Setup

### Site and author details
Add your site and author details in `_config.yml`:


### Navigation Bar
Set in the main navigation links in `_data/navbar_primary.yml`:
```yaml
- title: About
  url: /about/
```

### Widgets
Set in the page sidebar and footer sidebar widgets in `_data/sidebars.yml`. Chose from the following widgets: `categories`, `recent`, `authors`, `about`, links. Edit copyright notice in about widget in `_config.yml`:
```yaml
footer:
    copyright:
```

## Posts

To create a new post, you can create a new markdown file inside the `_posts` directory by following the recommended file naming format:
```
YEAR-MONTH-DAY-title.MARKUP
```
Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. For example, the following are examples of valid post filenames:

```
2011-12-31-new-years-eve-is-awesome.md
2012-09-12-how-to-write-a-blog.md
```

Post requires front matter, everything in between the first and second --- are part of the YAML Front Matter, and everything after the second --- will be rendered with Markdown and show up as “Content”.
The following is a post file with different configurations you can add as example:

```yaml
---
title: Best tech companies to work for in 2019
image: post-image.jpg       # Upload the image to uploads directory
categories: [business]      # Same as category post tag
tag: [spotlight, featured]  # Optional: spotlight tag adds post to spotlight section, featured tag add post to featured section
hidden: true                # Optional: exlude the post from blog page posts
author: sarah               # Reference author username
---
```

You can rebuild the site in many different ways, but the most common way is to run `bundle exec jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To keep things more organized you can organize post images in subdirectiories e.g. `/uploads/2019/01/`.

### Adding images
To add an image to a post or page use the following codes:
Local image from `/uploads/` directory:
```yaml
{% include image.html img="girl.jpg" alt="Alt for image" caption="Girl on a rock" %}
```
External wide image with lightbox:
```yaml
{% include image.html img="https://source.unsplash.com/TT-ROxWj9nA.jpg" lightbox="true" alt="Alt for image" caption="Image in lightbox" %}
```

### Responsive Videos
Embed local videos:
```html
<video controls playsinline uk-video="automute: true">
    <source src="http://www.quirksmode.org/html5/videos/big_buck_bunny.mp4" type="video/mp4">
    <source src="http://www.quirksmode.org/html5/videos/big_buck_bunny.ogv" type="video/ogg">
</video>
```
Embed YouTube videos:
```html
<iframe src="http://www.youtube.com/embed/YE7VzlLtp-4?autoplay=0&amp;showinfo=0&amp;rel=0&amp;modestbranding=1&amp;playsinline=1" width="600" height="340" frameborder="0" allowfullscreen uk-responsive uk-video="automute: true"></iframe>
```

To create a draft post, create the post file under the `_drafts` directory, and you can find more information in [Working with Drafts](https://jekyllrb.com/docs/drafts/).


## Authors

To create an author, create a new post inside the `_authors` directory and add the following YAML Front Matter:
```
---
title:          John Dow
username:       john
image:          avatar_john.jpg
bio:            Super SEO guy.
email:          me@mysite.com
website:        https://mysite.com
facebook:       https://www.facebook.com/
flickr:         https://www.flickr.com/
dribbble:       https://dribbble.com/
github:         https://github.com/
reddit:         https://www.reddit.com/
instagram:      https://www.instagram.com/
linkedin:       https://www.linkedin.com/
pinterest:      https://www.pinterest.com
twitter:        https://twitter.com/
vimeo:          https://vimeo.com/
youtube:        https://www.youtube.com/
---
```

Add post content and upload author `avatar_john.jpg` avatar to `uploads` folder.

## Categories

To create a category, create a new post inside the `_category` directory and add the following YAML Front Matter:
```
---
tag: business
permalink: "/category/business/"
---
```

## Development

Install [UIkit](https://getuikit.com/) font end framework dependency via Npm:
```bash
npm install
```
Enable live browser reload with the following:
```bash
bundle exec jekyll s --livereload
```
