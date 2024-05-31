# Serving the site locally

## 1. Set the path of your content folder

The first step to rendering your content folder with `NEBULA` is to set the `CONTENT_PATH` environment variable to the path of your content repository, *i.e.*,

```bash
export CONTENT_PATH="path-to-your-content-repository"
```

## 2. Setup `npm`

Now, assuming that you have `npm` installed (the default Node Package Manager for the JavaScript runtime environment Node.js), run the following command inside the `NEBULA`'s root directory:

```bash
npm install
```

Among other things, this command will install all the dependencies listed in the `package.json` file required for your `NEBULA` to run.

## 3. Start the development server

Start the development server by running:

```bash
npm run dev
```

To view the final rendered page, open the link `http://localhost:3000/{baseURL}` in your browser, where the `{baseURL}` variable is defined in the `config.json` file located in your content repository (see example [here](https://github.com/esciencecenter-digital-skills/NEBULA-content-template/blob/main/config.json))

> ``📝`` If you used the [NEBULA-content-template](https://github.com/esciencecenter-digital-skills/NEBULA-content-template) to generate your lesson content, `{baseURL}` will default to the name of your content folder repository.

If needed, `{baseURL}` can be overwritten upon building the page by using the environment variable `BASE_URL`. You can set `BASE_URL` right after setting `CONTENT_PATH` (as described [above](#set-the-path-of-your-content-folder)), using:
```bash
export BASE_URL="my-base-url"
```
