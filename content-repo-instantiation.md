# Creating a content repository

To create a platform with NEBULA the first thing that is needed is a content directory or repository that holds all the content. If you are starting a lesson from scratch, you can create your own content repository from the template repository using [NEBULA-content-template](https://github.com/esciencecenter-digital-skills/NEBULA-content-template). There, you can find more instructions on how to use the template, follow the steps in the [README](https://github.com/esciencecenter-digital-skills/NEBULA-content-template/blob/main/README.md).

You can also clone an already existing content repository, like for example the [Research Software Support](https://github.com/esciencecenter-digital-skills/research-software-support). 

If you only want to try NEBULA locally you can also create a new directory locally.

## Content directory structure
A content directory/repository has a few default files:

- README.md: The documentation of your platform
- LICENSE: The license under which the content is published, the content template default is [cc-BY](https://creativecommons.org/licenses/by/4.0/)
- CONTRIBUTING.md: Explanation on how others can contribute to the content
- config.json: The configuration file which defines its name/title, styling, organization and categories.

The `.github` directory holds the workflow files that are necessary to serve the platform on github pages, as well as additional tests and checks. All content lives in the `modules` directory.

Most modules are already set up: they contain the `index.md`, `info.md` and other content files, in addition to a `media/` directory. For further details, see [here](module-dir-structure.md).
If your module is not yet set up, please create both these inside the `modules` directory and follow [these instructions](module-dir-structure.md).
