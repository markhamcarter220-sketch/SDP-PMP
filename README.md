# SDP-PMP

Loading Dock PM field inspection tool — a single-page HTML/CSS/JS app for capturing equipment (doors, levelers, truck restraints) preventive maintenance checklists and generating a printable PM report.

## Run locally

Just open `index.html` in a browser, or serve it statically:

```
npx serve .
```

## Deploy

This is a static site (no build step). Deploying with [Vercel](https://vercel.com):

```
npm i -g vercel
vercel
```

Or connect this repo in the Vercel dashboard — it will be auto-detected as a static project and serve `index.html` from the root.

## Email

Report sharing uses `mailto:` links — no third-party service or configuration required. From the report screen, "Open Mail App" opens the device's mail app with the report summary in the body (recipient left blank), or a specific address can be entered to pre-address the email.
