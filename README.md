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

## Email Setup (EmailJS)

To enable direct email sending:

1. Create a free account at https://emailjs.com
2. Add an Email Service (Gmail, Outlook, etc.)
3. Create an Email Template with these variables:
   - `{{to_email}}` — recipient
   - `{{customer_name}}`
   - `{{so_number}}`
   - `{{tech_name}}`
   - `{{inspection_date}}`
   - `{{condition_summary}}`
   - `{{findings_summary}}`
   - `{{generated_by}}`
4. Copy your Service ID, Template ID, and Public Key
5. Replace the placeholder values in `index.html`:
   - `EMAILJS_SERVICE_ID`
   - `EMAILJS_TEMPLATE_ID`
   - `EMAILJS_PUBLIC_KEY`

Free tier: 200 emails/month. Upgrade at emailjs.com for higher volume.
