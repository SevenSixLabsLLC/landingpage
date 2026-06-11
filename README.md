# Seven Six Labs — Landing Page

Static landing site for sevensixlabs.com. Plain HTML/CSS, no build step.

## Local preview

Open `index.html` directly in a browser, or:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy (Cloudflare Pages)

1. Push this repo to GitHub.
2. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
3. Select the repo. Leave **build command** blank and **output directory** blank (or `/`).
4. Deploy. Then under **Custom domains**, add `sevensixlabs.com`.

Every `git push` to the production branch redeploys automatically.

## Contact form

The form posts to [Web3Forms](https://web3forms.com) (free, no backend).

1. Sign up at https://web3forms.com with the address you want submissions sent to
   (e.g. `hello@sevensixlabs.com`).
2. Copy your **Access Key**.
3. In `index.html`, replace `YOUR_WEB3FORMS_ACCESS_KEY` with the key.

Alternatives if you'd rather not use Web3Forms: Formspree, Getform, or a
Cloudflare Pages Function that emails via Resend / Postmark.

## Editing content

- App descriptions: search `id="apps"` in `index.html`.
- Consulting copy: search `id="consulting"`.
- Footer email / year: bottom of `index.html`.
- Colors / spacing: `styles.css` `:root` block.
