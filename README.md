# Kayra Dillon Designs website

A one-page website built with plain HTML, CSS and JavaScript. There is no build step, so Vercel can host it as-is.

```
index.html          the whole page (styles and script included)
images/             illustrations, plans, favicon, link-preview image
```

## Before you launch

Her email, phone, and service area are already filled in. Two things are left. Open `index.html` in any text editor and search for `EDIT` to find them.

1. **Kayra's drawings**: `images/plan-backyard.svg` and `images/plan-waterwise.svg` are sample plans. Scan or photograph her real drawings, drop the files into `images/`, and change the two `src` and `data-full` paths in the "Design work" section to the new file names. JPG or PNG is fine.
2. **Link preview** (optional): once the site has a domain, change `og:image` near the top to the full address, for example `https://kayradillondesigns.com/images/og-image.jpg`.

To change contact details later, search `index.html` for the old value and replace every match. The email also appears as `CONTACT_EMAIL` in the script at the bottom, which is where form requests are sent.

## Consultation requests

The form works out of the box. When someone submits it, their email app opens with the request already written and addressed to Kayra.

To have requests land in her inbox directly (no email app needed), create a free form at formspree.io, copy the form URL it gives you, and paste it into `FORM_ENDPOINT` in the script at the bottom of `index.html`.

If she uses an online booking calendar (Calendly, Square, etc.), you can point the "Schedule a consultation" buttons straight at it: replace `href="#consult"` with the booking link.

## Deploy on Vercel

**Without the command line**

1. Create a new repository on GitHub and upload everything in this folder.
2. In Vercel, choose **Add New → Project**, import that repository, leave the framework preset as **Other**, and click **Deploy**.
3. Add a custom domain under **Project → Settings → Domains**.

After that, every change you push to GitHub goes live automatically.

**With the command line**

```
npm i -g vercel
cd kayra-dillon-designs
vercel          # first deploy creates the project and a preview link
vercel --prod   # publishes to the live address
```
