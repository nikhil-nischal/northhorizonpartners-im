# North Horizon Partners

Marketing site for North Horizon Partners — *The Creator Access System*.

Static site (exported from Claude). Pages are plain HTML rendered client-side by `support.js`.

## Editing the booking link

The "Book a call" buttons across every page pull from one place — edit the single line in [`site-config.js`](site-config.js):

```js
window.SITE_CONFIG = {
  bookingUrl: "https://cal.com/nic.k/creator-strategy-call",
};
```

## Local preview

The pages must be served over HTTP (not opened as `file://`):

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

## Hosting

Deployed via GitHub Pages from the `main` branch. `.nojekyll` is present so all files serve as-is.
