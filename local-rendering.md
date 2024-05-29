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

## 3. Start the development server

Start the development server by running:

```bash
npm run dev
```

To view the final rendered page, open the link `http://localhost:3000/{baseURL}` in your browser, where `{baseURL}` is, by default, the name of your content folder repository. For example, if your content repo is named `research-software-support`, Nuxt will locally render the page at `http://localhost:3000/research-software-support`.

If you wish to use a different `baseURL` domain, you can set the `BASE_URL` environment variable right after setting `CONTENT_PATH` (as described [above](#set-the-path-of-your-content-folder)), using:
```bash
export BASE_URL="my-base-url"
```
