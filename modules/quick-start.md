<!--
name: quick-start
version : "0.1"
title : "Path Building Quick Start"
description: "Help authors get up and running with a path in 10 min."
license : "CC Attribution-ShareAlike 4.0"
-->

<!-- @section -->

## Fork the repository

We know you are busy and would rather focus on writing awesome content than setting up directory structures. Never worry, you'll be all set with our path template Github repository. Your first step is to fork this repo. The easiest way to organize content is to keep all your Outlearn content in one repository. The name of the repo does not matter, it could be for example "yourname-outlearn."  If you need a refresher on forking, check out Github's guide on [Forking Projects](https://guides.github.com/activities/forking/). You can also check out other [Github guides](https://guides.github.com) if you want to brush up on other Github skills.

<!-- @asset, "contentType" : "outlearn/prototype-feature", "text" : "{ \"task\": \"Fork the path-template repository. \"}"-->

Once you have forked the repository, open up `outlearn.json` found at the root of the repo. Update the following path metadata fields in the file:


| Field | Description |
| ----- | ----------- |
| name | used for the database, must be unique for your user account or organization |
| title | shown at the top of path cards |
| description | shown on the path card as additional information |

Your relevant part of your file should look like this:

    "paths" : [
      {
      "name" : "path-template",
      "title" : "Path Template",
      "description" : "Template for getting started quickly in path building",
      "privacy" : "public",
      "pages" : [
          {"title" : "Welcome", "content" : "./context-pages/welcome.md"},
          {"module" : "template-module"},
          {"module" : "outlearn://user/module"},
          {"module" : "outlearn://user/module"},
          {"title" : "See you later!", "content" : "./context-pages/goodbye.md"}
          ]
        }
    ],

<!-- @asset, "contentType" : "outlearn/prototype-feature", "text" : "{ \"task\": \"Update path metadata\"}"-->

<!-- @section -->

## Add your content

### Pages and Modules

Now that you've laid out what your path is all about, it's time to get some content in it. Paths are made up of two basic components: pages and modules. The modules are the building blocks of a path. You might write them all yourself or you can include modules written by others. Each module should be self-contained so that it can be easily reused and reordered for other paths. To balance out the independence of the modules, you can put in pages that are the glue that holds the blocks together. They let you add in more of your own personality. Pages are specific to a path so you can talk about why you chose the modules you did, how they fit together, what parts are super important, etc.

The pages are written in markdown and you just provide the location of the markdown file in the outlearn.json manifest.

### Outlearn Uses Markdown

We wanted to have an authoring experience that integrates seamlessly with Github and is easy as well as expressive. That's why we chose Markdown as the format for Outlearn. You can read the [official Markdown Syntax](http://daringfireball.net/projects/markdown/syntax) for more details. Outlearn also supports all the extensions of [Github Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/). If you already have your content in Markdown, importing it to Outlearn is a breeze.

The easiest way to create a module is to use a single markdown file. In that case you need some metadata at the top of the markdown file. The simplest possible example is:

TODO: Add new syntax

### Organize Your Path

Once you have your Markdown ready for a module, this is how you make it part of your path:

* Open the `template-module.md` file in the `modules` directory
* Update the metadata at the beginning of the file, including a new name for the module, e.g. `my-module-name`.
* Add your markdown content to the file
* Save your file with a new name, we recommend using `my-module-name.md`
* Edit `outlearn.json` and replace `{"module" : "template-module"}` with `{"module" : "my-module-name"}`. This tells the path where the module belongs.  
* Declare the module in the `modules` section in `outlearn.json` by replacing `"olm" : "./modules/template-module.md"` with `"olm" : "./modules/my-module-name.md"`. This tells Outlearn where the source file for the module is.

Your `outlearn.json` will now contain the lines:

    "paths" : [
      {
      "name" : "path-template",
      "title" : "Path Template",
      "description" : "Template for getting started quickly in path building",
      "privacy" : "public",
      "pages" : [
          {"title" : "Welcome", "content" : "./context-pages/welcome.md"},
          {"module" : "my-module-name"},
          {"module" : "outlearn://user/module"},
          {"module" : "outlearn://user/module"},
          {"title" : "See you later!", "content" : "./context-pages/goodbye.md"}
          ]
        }
    ],

    "modules" : [
        {
          "olm" : "./modules/my-module-name.md"
        }
    ],

<!-- @asset, "contentType" : "outlearn/prototype-feature", "text" : "{ \"task\": \"Add your first module into the path.\"}"-->

### Including images and videos

Outlearn supports the regular markdown syntax for including images. However, you will get nicer rendering and better progress tracking using our own annotation. The Outlearn image annotation looks like this:

```markdown

<!-- @section, type: 'image/jpeg', title: 'Architecture Diagram', location: 'http://ad009cdnb.archdaily.net/wp-content/uploads/2011/05/1304980266-ad30-circulation-diagram.jpg' -->

```

Besides `jpeg`, you can also use `png` images. You can add videos with the following annotations:

```markdown

<!-- @asset, type: 'video/vimeo', title: 'Watch the Video', location: 'https://vimeo.com/61887298' -->

<!-- @asset, type: 'video/youtube', title: 'Watch the Video', location: 'https://www.youtube.com/watch?v=CmjeCchGRQo' -->

<!-- @asset, type: 'video/mp4', title: 'Watch the Video', location: 'http://www.example.com/training/video1.mp4' -->

```

<!-- @section -->

## Enhance your content

### Adding sections

The simplest way to enhance your content is to divide it into sections. Each module can have one or more sections that also show up on the side of the content and serve as a handy table of contents. They can also be checked off as completed and help learners and path creators see what progress has taken place.

You create a section by adding the following annotation:

```markdown
<!-- @section, "title": "Getting started" -->
```

Alternatively, you can leave out the "title" attribute and the platform will take the first heading after the section tag and make it the title. It does not matter if the heading is h1, h2, etc. So you could replace the above code with:

```markdown
<!-- @section -->

## Getting started
```

This can be especially helpful when you just quickly want to add sections to an existing markdown file and also makes the file render more nicely on Github.


### Add tasks, links

Nothing kills learner motivation like hours of videos or reading without a way to try it out yourself. The easiest way to create meaningful interactions with the learners is to add tasks, some of which may contain deliverables. A task can be as simple as "Run make in your project directory" or more involved such as "Download this library and compile it in your system." With deliverables, you get even more flexibility. For example, you can ask learners to "Fork the project repo on Github, add in your function and send a pull request to the original repo. Paste the url to the pull request below." Path authors and organization admins can see which tasks have been done and what learners have submitted. They can then organize further activities such as code reviews.

TODO: ADD IN SYNTAX

### Add cover images

Your path and each module in the path can have a cover image that's a visual representation of the path or module.
