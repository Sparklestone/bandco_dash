# Brave & Co — The Next 90 Days

Static watch page. No build step, no dependencies.

    index.html                      the page
    explainer.mp4                   the film (11:17, 15 MB)
    poster.jpg                      video poster frame
    Brave-and-Co-Next-90-Days.pdf   the deck, linked from the page
    vercel.json                     caching + noindex headers

## Deploy

Import this repo at vercel.com/new. Framework preset **Other**.
Leave build command and output directory empty. Vercel serves the folder as-is.

Everything here must sit at the repo root. `index.html` uses relative paths,
so a subfolder means setting a matching Root Directory in project settings.

## Notes

- The page is set to `noindex, nofollow` in both the HTML and `vercel.json`,
  so it won't be indexed while it's a private link. Remove both if it goes public.
- The video is H.264 + AAC, faststart encoded, so playback begins before the
  whole file downloads.
- Chapter timestamps are the `CHAPTERS` array at the bottom of `index.html`.
  If the film is recut, those are the only numbers to change.
- This repo is currently public. The video and all deck copy are downloadable
  by anyone who finds it. Switching the repo to private does not affect Vercel.
