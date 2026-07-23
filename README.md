# Al's PDF Splitter

A tiny, single-file web app that splits a PDF into one file per page and downloads them all as a ZIP.

**No install, no server, no upload.** Everything — reading the PDF, splitting the pages, and zipping the output — happens locally in your browser. The file never leaves your device, and the app works fully offline once the page has loaded.

## Try it

Once hosted (see below), just open the URL, drop in a PDF, and click **Split & download ZIP**.

## How it works

- The entire app — HTML, CSS, and JavaScript — lives in a single file: [`index.html`](./index.html).
- PDF parsing/splitting is done with a bundled copy of [pdf-lib](https://pdf-lib.js.org/), and the per-page files are packaged with a bundled copy of [JSZip](https://stuk.github.io/jszip/). Both libraries are embedded directly in the file, so there are no external network requests or CDN dependencies at runtime.
- Drop a PDF (or click to browse), then click **Split & download ZIP** — you'll get a ZIP containing one PDF per page, named after the original file.

## Hosting it yourself with GitHub Pages

This repo is already set up to be hosted with [GitHub Pages](https://pages.github.com/), which serves static files straight from the repo for free.

1. In this repo on GitHub, go to **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Under **Branch**, select `main` and folder `/ (root)`, then click **Save**.
4. Wait a minute or two for the first deployment to finish (check the **Actions** tab for progress).
5. Your app will be live at:

   ```
   https://<your-github-username>.github.io/als-pdf-splitter/
   ```

Because the page is a single static `index.html` file with everything bundled in, there's nothing else to configure — no build step, no dependencies to install.

## Privacy

Nothing is uploaded anywhere. All processing happens client-side in your browser using JavaScript.
