## Elements of a module

A module can contain the following elements:

- [slides](#slides), to be used in a classroom setting.
- [text](#text), targeted at self study participants.
- [exercises](#exercises), both for self study and for classroom use.
- curated [online resources](#online-resources), both for self study and for classroom use.

Ideally, all modules contain all elements.

### Slices
Slides are essential when teaching a module in a classroom setting.
They do not need to be long, however; a few slides to provide context and motivation is sufficient.

It is important to include notes, however brief, on ever slide.
The notes are crucial for any instructor preparing to teach with the materials.
They are also relevant for self-study participants, who can use the slides with accompanying notes to get a quick introduction to the subject.

Slides are written in a markdown file, which should be placed in the `/modules/{modulename}` directory and rendered with Reveal.js. Technical information about the structure of these files [is here](#slides-with-revealjs).

### Text
As this material is partly targeted at self-study participants, we explicitly want to include text.

This type of section is meant to illustrate the concepts that are also covered in the presentations but for self study purpose. In the future we might replace many of these with recorded videos.

Texts are written in markdown, as chapters inside the `/modules/{modulename}` directory.

### Exercises
Any exercises are welcome, and there are no limits to the type of exercises that can be included.
However, be explicit about the type of exercise at the top of the page:

- Should it be done live or online?
- Is it done individually or in groups, and if in groups, how big should the groups be?
- What is the expected duration of the exercise?

Furthermore, provide information on preparation for the instructor:

- What materials, if any, are necessary?
- What preparation, if any, is necessary?

If there are online resources that are relevant for the exercise, provide direct links instead of descriptions.

Finally, provide information on the expected outcome of the exercise.

Exercises are written in markdown, as chapters inside the `/modules/{modulename}` directory.

### Online resources
The online resources are the meat of the modules.
They provide the most detailed information to relevant content, and their collection should be comprehensive.

An online resource should be linked, but in a specific way, and with clear context:

- Why is this resource relevant?
- What is the goal of reading the resource?
- What is the expected time investment?

In addition, be clear about the part of the resource that is important.
The links should go directly to the relevant part of the resource, and if that is not possible, clear pointers (e.g. the name of sub-headers) should be provided.
If the relevant part is over before the end of the linked page, explicitly add this information before the link.

And optionally, consider adding:

- Target audience or level of the resource (e.g. "technical resource, optional")
- Discussion points for the classroom

Online resources are written in markdown, as chapters inside the `/modules/{modulename}` directory.