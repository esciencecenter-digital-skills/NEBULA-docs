# Directory structure and content tags

To add a module, create a new folder inside the main `modules` directory
named after your new module, *e.g.*, my-new-module.

This new `modules/my-new-module/` directory has general structure:

```console
my-new-module
├── exercises.md
├── online_resources.md
├── index.md
├── info.md
├── media
│   ├── fig1.jpeg
│   └── fig2.png
└── slides.pmd
```

and should contain the following files:

- [index.md](#the-indexmd-file)
- [info.md](#the-infomd-file)
- [slides pmd file](#the-slides-pmd-file)
- [exercises and online resources files](#exercises-and-online-resources-files)
- [the `media` folder](#the-media-folder)

## The `index.md` file
This file is entirely defined by a YAML header.
An example `index.md` file is given below:

```yaml
---
id: 1
trl: medium
category: Development
title: Software Testing
abstract: Local testing of your software and using Continuous Integration and Continuous Deployment (CI/CD)
author: eScience Center
thumbnail: "thumbnail-testing.jpg"
visibility: visible
---
```
The only important fields at this point are `category`, `title`, `thumbnail`, and `visibility`.

The `category` field should be one of the categories defined in the `config.json` file which is located in the root directory. These are literally `sections` that group together modules within certain categories.

The `title` field should be the title of the module; it will be shown on the main overview page.

The `thumbnail` field should be the name of the thumbnail image, which should be placed in the `/modules/my-new-module/media` directory. This image shows up on the index page. You can add your own image to `/modules/my-new-module/media` and replace `thumbnail: "nlesc-dummy.png"` by `thumbnail: "my-module-thumbnail-image.png"`.

The `visibility` field should be `visible` if you want to make this specific module visible in the final lesson rendering.  

Finally, the `id`, `author`, `trl` (technical readiness level) and `abstract` properties are currently not used, but they are still here for legacy reasons.

## The `info.md` file

## The slides pmd file

## Exercises and online resources files

## The `media` folder

The `media` folder gathers any media used in your module, including presentation images, videos, and module's thumbnail image.

