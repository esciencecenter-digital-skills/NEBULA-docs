# Directory structure and content tags

To add a module, create a new folder inside the main `modules` directory
named after your new module, *e.g.*, `my-new-module`.

This new `modules/my-new-module/` folder should be organized according to the following general structure:

```console
my-new-module
├── index.md
├── info.md
├── media
└── some-other-content.md
```

The important files in this folder include:

- [index.md](#the-indexmd-file)\*
- [info.md](#the-infomd-file)\*
- [the `media` folder](#the-media-folder)\*
- [slides file](#the-slides-file)
- [additional files: text, exercises and online resources](#text-exercises-and-online-resources)

\* = required files.

## The `index.md` file
This file represents the core of your module and is entirely defined by a YAML header.
An example `index.md` file is given below:

```yaml
---
id: 0
category: Development
title: Software Testing
abstract: Local testing of your software and using Continuous Integration and Continuous Deployment (CI/CD)
author: eScience Center
thumbnail: "thumbnail-testing.jpg"
visibility: visible
---
```
- The `category` field should match one of the categories defined in the `config.json` file (`"categoryOrder"` field), which is located in the content's repo root directory; see, *e.g.*, [here](https://github.com/esciencecenter-digital-skills/NEBULA-content-template/blob/main/config.json). These categories are essentially sections that group together modules within specific thematic areas.

- The `id` field is used to determine the position of the current module within the specified `category`.

- The `title` field should be the title of the module; it will be shown on the main overview page.

- The `thumbnail` field should be the name of the thumbnail image, which should be placed in the `/modules/my-new-module/media` directory. This image shows up on the index page. You can add your own image to `/modules/my-new-module/media` and replace `thumbnail: "nlesc-dummy.png"` by `thumbnail: "my-module-thumbnail-image.png"`.

- The `visibility` field should be set to `visible` if you want to make this specific module visible in the final lesson rendering. Otherwise, set it to, *e.g.*, `not visible`.

- The `author` and `abstract` fields do not influence the final module rendering, but they can be useful for internal control and for developers.

## The `info.md` file
This file defines the learning objectives of your module and is generally the first chapter to appear on the main module's overview page. An example `info.md` file is shown below:
```markdown
---
title: Learning objectives
type: info
order: 0
---

- Appreciate the importance of testing software
- Understand the various benefits of testing
- Understand the types of tests and what info they convey
- Get familiar with the idea of continuous integration and its importance
```

Here, the `title` corresponds to the title of your chapter as shown in the module's overview page.

Within a module, the `type` field defines the chapter type and assumes the following options:
- `info`: for chapters containing general information material.
- `slides`: for chapters defining presentations; see example [here](#the-slides-file).
- `reading`: for chapters containing focused reading material and on-line resources; see example [here](#exercises-and-online-resources-files).
- `exercise`: for exercises; see example [here](#exercises-and-online-resources-files)

Finally, the `order` field determines the sequence in which chapters appear on the module's overview page. Since the learning objectives are expected to come first, `order` should be set to `0` in the `info.md` file.

## The `media` folder

The `media` folder gathers any media used in your module, including presentation images, videos, and module's thumbnail image. The thumbnail image is mandatory, as it is required by the `thumbnail` field in `index.md`.

To include any media in your `md` files, use, for example, `media/my-image.png` as shown below using markdown syntax:
```markdown
![Some text](media/my-image.png)
```
For further information, see [below](#slide-content).

## The slides file

Similar to `info.md`, the slides file is also embedded as a chapter on the module's main page, using the `slides` chapter type, as described [above](#the-infomd-file).

Like `info.md`, they also require an initial YAML heading, *e.g.*,
```markdown
---
title: Software Testing
type: slides
order: 1
---

<!-- .slide: data-state="title" -->

## Software Testing

---
...
```

> 📌 **Is your first slide not rendering correctly?** Make sure that your YAML heading is included and formatted according to the example above. Pay special attention to the proper placement of the `---` separator.

Although the slides are written in Markdown, they are rendered using [Reveal.js](https://revealjs.com/), and for this reason, they follow a special format. This is discussed below.

### Slide types

There are four different slide types:

- Title slide, `data-state="title"`
- Default slide, `data-state="standard"`
- "About us", `data-state="about"`
- "Let's stay in touch", `data-state="keepintouch"`

A slide is fenced by three dashes, and (optionally) an HTML comment that indicates the slide type:

```markdown

---

<!-- .slide: data-state="standard" -->

```

Always keep an empty line before and after the slide fence.

The dashes indicate the slide borders; the are therefore only necessary between the slides, and not at the beginning or end of a presentation.

### Slide content

Slide content can be written in Markdown.

To keep slides clean, use single images per slide.
Styling in Reveal is not trivial, and it is best to keep it simple.

Images can be embedded using either markdown syntax:

```markdown
![Mapping the Via Appia](media/viaappia.png)
```

Or, for more customisation, using HTML:

```html
<center>
<img src="media/researchcycle.png" width="60%">
</center>
```

### Slide notes

Notes should be added at the bottom of the slide, as follows:

```markdown

Note:
Here is the text of a note.

---
```

where the `---` indicates the fence to the following slide.

### Final slide

The final slide should provide the contact information for the eScience Center.
This is not hardcoded into the slides, so it should be provided explicitly.

The code for the final slide is as follows:

```markdown

---

<!-- .slide: data-state="keepintouch" -->


www.esciencecenter.nl

info@esciencecenter.nl

020 - 460 47 70

```

## Text, exercises and online resources
These chapters are defined by simply Markdown `*.md` files with an initial YAML heading.

As discussed [before](module-elements.md), a text chapter is intended to cover the same content as in the slides but in a descriptive and readable way, potentially with a time indication. An example is shown below:

```markdown
---
title: Software Testing
type: reading
order: 2
---

## Software Testing (5 minutes)

Software testing is the process of evaluating and verifying that software meet specified requirements...
```
It uses the `reading` chapter type as described [above](#the-infomd-file) and is the defined as the third chapter of the module (`order: 2`).

In turn, an exercise can be defined as follows:

```markdown
---
title: Exercise 1
type: exercise
order: 3
---

## Scenario

You are part of a research team working on....

---

## Question

Which of the following best describes...
```
where the chapter type `exercise` is now explicitly used.

Finally, a chapter with online resources, providing in-depth material about the chapter's content, is also of the `reading` type. An example file would be:

```markdown
---
title: Further reading
type: reading
order: 4
---

# Further reading

## Testing

Follow the links below to read more about software testing.
....
```

