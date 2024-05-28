# Serving the site locally

## Setup `npm`

Assuming that you have already installed `npm` (the default Node Package Manager for the JavaScript runtime environment Node.js), run the following command inside the `NEBULA`'s root directory:

```bash
npm install
```

## Set content folder path

To be able to render your content folder with `NEBULA`, set the `CONTENT_PATH` environment variable to the path of your content repository, *i.e.*,

```bash
export CONTENT_PATH="path-to-your-content-repository"
```

## Development Server

Start the development server on `http://localhost:3000` by running:

```bash
npm run dev
```