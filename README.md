# Hexo Paper Theme

## Installation

`git clone https://github.com/Aspiring-Writer/hexo-paper-theme themes/paper`

## Usage

To use this theme, copy [the theme's config.yml](https://raw.githubusercontent.com/Aspiring-Writer/hexo-paper-theme/master/_config.yml) into your site folder. Then, change your theme to `theme: paper` in your site's `_config.yml`.

## Favicons

Generate your favicons using [a favicon generator](https://favicon.io) and add them to your `source/images/favicons` folder.

This theme has support for:

* apple-touch-icon.png
* favicon-32x32.png
* favicon-16x16.png
* favicon.png
* favicon.ico
* logo.svg

## Languages

* en
* es
* ja
* ko
* ru
* zh-cn
* zh-tw

If you have multiple languages, you can also change your site title to match whatever language the user has specified by adding `LANG_title` to your `config.paper.yml`. You can add a title for all of the supported languages if you'd like.

```yml
en_title: "Site"
es_title: "Sitio"
```

The same goes for location and bio. Make sure you don't remove `location: "Here"` and `bio: "Blah blah blah"`, those should be in your default language and they _must_ be present.

## Word Count

If you want include site and post word counts, install hexo-word-counter, `npm install hexo-word-counter`.

## toc

To add a Table of Contents to your post, add `toc: true` to the front-matter

## diff.blog

[diff.[blog](https://diff.blog/) is similar to Medium, but it's only for showing blog feeds, not hosting them. On their website, they advertise themselves as "a platform that helps you discover and follow amazing developer blogs. Whether your interests are in Python, Rust, AI, Distributed Systems or XYZ diff.blog has got amazing blogs for you to follow!"

You can check out more on their [about page](https://diff.blog/FAQ/).

You can use diff.blog with this theme by adding `diff_blog: CODE` to your theme config file. You can find your plugin code by going [here](https://dif.blog/plugin/) and copying the 50-character code.

```javascript
<script id="diffblog-plugin-script" async="false" src="https://diff.blog/static/js/diffblog_plugin_v1.js"></script> 
<script>
  document.getElementById("diffblog-plugin-script").addEventListener("load", function () {
    DiffBlog(
      "q7f864hffi8m218eaq6d623sezfgkz1vzfva4oxjeyxq9l2dwp" // Copy this
    );
  });
</script>
```

## Comments

At the current moment, this theme only supports [utterances](https://utteranc.es/) (mostly because I haven't used anything else). If you know the scripts for others, go ahead and open up a pull request for the [post layout](layout/_partial/comments.ejs)

```yml
utterances:
  repo: [ENTER REPO HERE] # Github repository owner and name
  # Available values: pathname | url | title | og:title
  issue_term: pathname
  # Available values: github-light | github-dark | preferred-color-scheme | github-dark-orange | icy-dark | dark-blue | photon-dark | boxy-light
  theme: preferred-color-scheme
```

## Prev/Next Posts

This is entirely optional but quite useful for those who write series. You could also use Hexo's post helper tags, but this method is designed to be easier for those on mobile devices (and just lazy, of course).

```yml
prev_post: post1
next_post: post2
```

This only works if the page(s) you're linking to is in the same path as the page you are on (e.g. /example/post1, /example/post2).
