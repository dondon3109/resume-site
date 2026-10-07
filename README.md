# Resume site

One static page (`index.html`, no build step) for https://dondon3109.online.

## Preview locally

```bash
python3 -m http.server 8080
```

Open http://localhost:8080.

## Deploy to Cloudflare Pages

1. Push this folder to a GitHub repository.
2. In the Cloudflare dashboard go to **Workers & Pages → Create → Pages → Connect to Git** and pick the repository.
3. Build settings: framework preset **None**, build command empty, build output directory `/`.
4. Click **Save and Deploy**. The site goes live at `<project>.pages.dev`.
5. Open the project's **Custom domains → Set up a custom domain**, enter `dondon3109.online`, and follow the prompts.
   - If the domain's DNS is on Cloudflare, the record is added for you.
   - Otherwise, add the CNAME record Cloudflare shows at your registrar, or move the domain's nameservers to Cloudflare.
6. Optional: also add `www.dondon3109.online` and redirect it to the apex domain.

Without Git: **Create → Pages → Upload assets**, then drag in this folder.

## Editing

All content and styles live in `index.html`. Colors are CSS variables in `:root`, with dark values under `prefers-color-scheme: dark`. To remove the phone number, delete the Phone `<li>` in the header.
