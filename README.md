# Siteleaf Pure Theme

A [Pure][Pure] theme for the [Siteleaf][Siteleaf] content management system.

## Status

WORK-IN-PROGRESS - I warned you ;)

So far there's only a `index` and a `default` template - leveraging the corresponding [Pure layouts](http://purecss.io/layouts/).

Next up: add a `blog` tpl (for *writing*)... and propably an image `gallery` tpl. as well.

## Credits

... where credit is due! 

The skeleton approach for the template (e.g. the use of [Guard][Guard], the integrated documentation of required meta fields, as well as the file and directory layout) was inspired by [Jonnie Hallman (@destroytoday)](https://github.com/destroytoday)'s [Skeleton theme for Siteleaf](https://github.com/destroytoday/siteleaf-skeleton).

## How to use this theme?

### Prerequisits

- [Ruby][Ruby] needs to be installed.
- [Livereload][Livereload] - OPTIONAL, e.g. make sure you have the [browser extension installed in your browser of choice](http://feedback.livereload.com/knowledgebase/articles/86242-how-do-i-install-and-use-the-browser-extensions).

### Setup

- Clone or fork this repo... and `cd` into the directory.
- If [Bundler][Bundler] isn't installed, run `gem install bundler`.
- Run `bundle install` to install the required Ruby gems.
- Run `bundle exec siteleaf config YOUR_DOMAIN` to configure your **existing** site to this directory or `bundle exec siteleaf new YOUR_DOMAIN` to create **a new** site on [siteleaf.com][Siteleaf].

### Instructions

- Run `bundle exec guard` to watch/ livereload changes.
- Run `bundle exec siteleaf server` in a new/ 2nd shell (or terminal tab) to preview your theme locally.
- Open [0.0.0.0:9292](http://0.0.0.0:9292/) in your browser of choice.

### Customization

There are the following templates available:

- `index` using Pure's [Landing Page (Marketing)](http://purecss.io/layouts/marketing/) layout
- `default` using Pure's [Side Menu](http://purecss.io/layouts/side-menu/) layout
- `blog` and `writing` using Pure's [Blog](http://purecss.io/layouts/blog/) layout
- `gallery` and `photos` using Pure's [Gallery](http://purecss.io/layouts/gallery/) layout

In order to use the *Side Menu* layout also for the `index` page one need to edit the templates `index.html` file, by simply replacing... 

    {% include 'layouts/index' %}
    
... with: 

    {% include 'layouts/default' %}

### Resources

- [Siteleaf Theme Documentation](http://www.siteleaf.com/help/themes/)
- [Liquid for Designers](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers)


[Siteleaf]: http://www.siteleaf.com/ "Siteleaf"
[Pure]: http://purecss.io/ "PURE"
[Ruby]: https://www.ruby-lang.org/ "Ruby"
[Bundler]: http://bundler.io/ "Bundler"
[Guard]: http://guardgem.org/ "Guard"
[Livereload]: http://livereload.com/ "Livereload"