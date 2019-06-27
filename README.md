<p align="center">

    <h2 align="center"> <a href="https://mxnkpl.com/blog/"> Max's blog</a><br> </h2>
</p>

<p align="center">A "quick-launch" blog powered by the <a href="https://github.com/sergiokopplin/indigo/">Indigo</a>
theme on
<a href="https://jekyllrb.com"> Jekyll</a>
</p>

<p align="center">
    <b><a href="README.md#blog">About Blog</a></b>
    |
    <b><a href="README.md#setup">Setup</a></b>
</p>

<p align="center">
    <img src="assets/images/screenshot.png"/>
</p>

## Blog

<a href="https://mxnkpl.com/blog/"> About Blog:</a>
Max's Blog! Extrapolating thinker.
Working on ways to fix things, fuse together or dismantle when necessary.

<br>

Intersectional Exploration Advocate.
<br>

Blue Skies Dreamer.  |  _*Goin There, With Care*_


## Max's Full Website

Check <a href="https://mxnkpl.com"> MXNKPL.COM </a> for more projects and information.

![MX seafoam logo](https://i.ibb.co/cDdKmJ0/mx-seafoam.png)

***


## About Indigo Theme on Jekyll

-[Indigo Theme](https://github.com/sergiokopplin/indigo/) : [Live-demo](http://sergiokopplin.github.io/indigo/)
- Google Speed: [98/100](https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Fsergiokopplin.github.io%2Findigo%2F);

## Setup
To use Indigo Theme locally on your machine, do the following steps:

1. Install [Jekyll](https://jekyllrb.com/docs/), [NodeJS](https://nodejs.org/) and [Bundler](http://bundler.io/).
1a. Fork the project [Indigo](https://github.com/sergiokopplin/indigo/fork)
2. Clone the forked repo on your machine
3. Enter the cloned folder via terminal and run `bundle install`
4. Then run `bundle exec jekyll serve --config _config.yml,_config-dev.yml`
5. Open it in your browser: `http://localhost:4000`
6. Test your app with `bundle exec htmlproofer ./_site`
7. Do you want to use the [jekyll-admin](https://jekyll.github.io/jekyll-admin/) plugin to edit your posts? Go to the admin panel: `http://localhost:4000/admin`. The admin panel will not work on GitHub Pages, [only locally](https://github.com/jekyll/jekyll-admin/issues/341#issuecomment-292739469).

You must fill some informations on `_config.yml` to customize your site.

```
name: Maxi Moe
bio: 'Tough Cookie.'
picture: 'assets/images/profile.jpg'
...

and lot of other options, like width, projects, pages, read-time, tags, related posts, animations, multiple-authors, etc.
```

---
Indigo Theme © :
[MIT](http://kopplin.mit-license.org/) License © Sérgio Kopplin
