---
title: "Hugo Fastest Custom Start, Making A Theme"
date: 2020-09-12T10:26:18-05:00
---

## Getting Set Up

You've installed Hugo, run `hugo new site best-website` and want to make a new custom website from scratch. It's a great learning experience to step through each file type you can make, but if you already understand page leafs and bundles, and are familiar with the lookup order, getting started fast also becomes essential.

## Starting a Theme in Hugo

The fastest way to scaffold out a new Hugo site is to start your site in a theme. The `hugo new theme best-theme` is a gem in the Hugo code base. This command creates many of the files you need to see a complete site.

There is some overlap with the `hugo new site` command, this also creates an `best-website/theme/best-theme/archetypes/default.md` file and a .toml file for storing configurations, with a new themed named: `theme.toml`.

## Theme Created Layouts
This command also creates 8 essential files that appear in almost every well organized Hugo Theme.

* 404.html
* _default/baseof.html
* _default/list.html
* _default/single.html
* index.html
* partials/footer.html
* partials/head.html
* partials/header.html

## Where To Put Content

Content normally doens't make much sense in a theme file. A theme is great for holding reuasable components that create visual effects, or set the flow of different pages. It doesn't make sense to put much content in reusable place, because the content Keep content files in your project directory.
