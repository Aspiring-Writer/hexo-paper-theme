# Hexo Paper Theme

To use this theme, copy and fill out the following variables into `_config.paper.yml`. Then, change your theme in `_config.yml` to paper.

```yml
location: "Somewhere in the USA"
gravatar: "example@example.com"
bio: "A short bio"

menu:
  About Me: /about.html
  Github: https://github.com/Aspiring-Writer
```

## toc

To add a toc to your post, add `toc: true` to the front-matter

## diff.blog

[diff.blog](https://diff.blog/) is a similiar to Medium, but it's only for showing blog feeds, not hosting them. On their website, they advertise themselves as "a platform that helps you discover and follow amazing developer blogs. Whether your interests are in Python, Rust, AI, Distributed Systems or XYZ diff.blog has got amazing blogs for you to follow!"

You can check out more on their [about page](https://diff.blog/FAQ/).

You can use diff.blog with this theme by adding `diff_blog: CODE` to your theme config file. You can find your code by going [here](https://dif.blog/plugin/) and copying the 50-character code.

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

This is entirely optional, but quite useful for those who write series. You could also use Hexo's post helper tags, but this method is designed to be easier for those on mobile devices (and just lazy, of course).

```yml
prev_post: post1
next_post: post2
```

This only works if the page(s) you're linking to is in the same path as the page you are on (e.g. /example/post1, /example/post2).
