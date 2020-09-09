---
title: "Getting Started With Hugo"
date: 2020-09-08T21:42:52-05:00
---

# Taking Inventory

Do you know how to use the terminal?  If you don't, [start here](https://www.learnenough.com/command-line-tutorial/basics).

The first step in the installation process is noting what software you have installed. We're running Linux (operating system Ubuntu 18.04) and have Hugo (0.74.3) installed. If you don't have Hugo, follow their [installation instructions](https://gohugo.io/getting-started/installing). With Hugo installed, run `hugo new site best-website` in the terminal.

{{< figure src="Lookup Operating System Version, Lookup Hugo Version, Create Hugo New Site.png" title="Lookup Operating System Version, Lookup Hugo Version, Create Hugo New Site" >}}

Know More!
This commands generates a folder structure, and two files. `config.toml` is an important file, it sets variables any page can access.

# Seeing HTML

The first command is running the server, this generates HTML for your web browser to read. Move into the correct directory with `cd best-website` and run `hugo server`.  This generates warnings in the terminal, and you should be able to open a web browser at http://localhost:1313/ 

{{< figure src="Change Directory into Hugo Project, Run Hugo Server, Examine Errors.png" title="Change Directory into Hugo Project, Run Hugo Server, Examine Errors" >}}

There is nothing there but an empty HTML page.

# Seeing Home

To make a home page interesting, you have to include your own layouts. The absolute easiest way to get started is creating your own theme.

Know More!
You could name this file many things. Anything in the [lookup order](https://gohugo.io/templates/lookup-order/#examples-layout-lookup-for-home-page) for a `home` page works.

# Seeing Content

If you stopped and restarted your server with `Ctrl-C`,`hugo server` you could see that we had removed one of the errors. Our home page has a template, and you can add almost everything you want here. Hugo has good suggestions about how to organize your information.

In your `layouts/home.html` you'll use Go code to read variables and content from other files. Replace "Best" with `{{ .Content }}`. The `{{}}` curly braces indicate Go code is happening, the `.` is all the information currently available, and the `Content` is a specific variable carrying data. If you look at localhost:1313, you'll see no content. To add content for the home page make the `content/_index.md` file and add some markdown, like `# *Best* Website Ever*` 

Know More!
Hugo encourages you to put the HTML the browser uses in `layouts` and populate it with content the user sees from `content`.

# Seeing Page

# Seeing Pages

