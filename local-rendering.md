# Serving the site locally

## 1. Install `npm`
`npm` is the default Node Package Manager for the JavaScript runtime environment Node.js.
To see if you already have `Node.js` and `npm` installed, run the following:

```bash
node -v
npm -v
```

The above commands should output the installed versions, *e.g.*, `10.6.0` and `v20.9.0`. If not, check the [download instructions](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm).

## 2. Set the path of your content folder

The next step to rendering your content folder with `NEBULA` is to set the `CONTENT_PATH` environment variable to the path of your content repository (see the documentation on [setting up a content repository](content-repo-instantiation.md)), *i.e.*,

```bash
export CONTENT_PATH="path-to-your-content-repository"
```

## 3. Setup `npm`

Now, assuming that you have `npm` installed, run the following command inside the `NEBULA`'s root directory:

```bash
npm install
```

Among other things, this command will install all the dependencies listed in the `package.json` file required for your `NEBULA` to run.

## 4. Start the development server

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
