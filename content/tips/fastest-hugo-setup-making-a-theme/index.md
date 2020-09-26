---
title: "Fastest Hugo Setup, Building a Theme"
date: 2020-09-25T20:06:44-05:00
tags: hugo, beginner, markdown, html
categories: tech
draft: true
---

## Orienting for Speed

Hugo is a way to write HTML and CSS using the Go programming language. It's nice to use a lot of HTML and CSS and a little Go. The fastest way to build a custom Hugo site is starting a custom theme.

## Command Line, Activate

Open your terminal, check your installation and version of Hugo, and we'll run three commands.

````
# if you already have a site, skip making a new site
hugo new site best-website-ever
# move into the project directory
cd best-website-ever
hugo new theme theme-time-now
````

This created a series of files you can examine with `ls themes/theme-time-now`. The file structure is similar to a `hugo new site` command. There is no `content`, and some default `layouts` have been created to start a custom Hugo website.

To make it appear in your browser, register your new theme by editing `config.toml`. Add this line: `theme = "theme-time-now"` and save. 

## Wiring Components Together

To hook your homepage to `_default` layouts, use this Go code.

````
{{- define "main" }}
{{- end }}
````

Add this code to a few files in `best-website-ever/themes/theme-time-now/layouts/`. To jump start your homepage, add it to `index.html`. Also add it to `_default/list.html` and `_default/single.html`, these are categories for Hugo content.

The `{{ define "main" }}{{ end }}` block allows these files to call `_default/baseof.html` as a template. Inside this file, you'll find an HTML skeleton, and calls to partials for `head`, `header`, and `footer`. Apply best practices to your website, and choose where to start. Use tools like Lighthouse and Wprig.org to increase the visibility and usability of your site. 

## Partials Every Website Needs
### Inside the [Head](https://www.w3schools.com/html/html_head.asp_) Tag

It's helpful to know every element a `<head>` tag [can contain](https://www.w3schools.com/html/html_head.asp). They're important for search engines. It's early in the `<html>` document, and search engines can load this without accidentally downloading every image on the world wide web.

-  ><head>
    1. A title tag, make a unique for every page 
    > <title>The Site Is Best When It's Done<title>
    1. Several `meta` tags with different `name` attributes.
    > <meta name="viewport" content="width=device-width, initial-scale=1.0">
    > <meta name="description" content="I want to be searched, engine.">
    > <meta name="keywords" content="My Interests, Growth, Happiness">
    1. Some [CSS style](https://www.w3schools.com/Css/css_intro.asp). We can use Hugo to process the file. This file also has a special home, in `best-website-ever/themes/theme-time-now/layouts/assets/css/main.css`. Create this file for CSS style!
    > {{ $style := resources.Get "css/main.css" }}
    > <link rel="stylesheet" href="{{ $style.RelPermalink }}>
    1. Some [HTML style]
- ></head>

### Taking on the Header

The header is visible to most visitors on most pages. This is a final moment to take a breath and carefully plan out your website. Decide what to share, what to highlight, how to invite feedback, and think carefully about personal information you're sharing.

A common choice is to build a [navigation system](https://www.w3schools.com/css/css_navbar.asp) to highlight the most important ideas of in website. 

### Footer

Put things y
ou want on every page, but don't need to be highlighted for users. This can be javascript that doesn't have to run right away, copyrights, or contact information. 


## Filling Out Main