# COVID Info Centre — Archived Landing Page

This is a single-file static site you can deploy **for free** on GitHub Pages and point your DreamHost-registered domain to it.

## Deploy on GitHub Pages
1. Create a new **public** GitHub repository (any name).
2. Upload `index.html` and the `CNAME` file from this folder.
3. Go to **Settings → Pages → Build and deployment → Source: Deploy from a branch**. Choose `main` and `/ (root)`.
4. After it publishes, GitHub Pages will serve your site from `https://<username>.github.io/<repo>/` or directly on your custom domain once DNS is set.

## Custom domain (covidinforcentre.com)
- Keep the `CNAME` file content as `covidinforcentre.com` to enable HTTPS on your apex domain.
- In DreamHost, set the domain to **DNS Only**, then add the following records:

Apex/root A records (add all four):
- 185.199.108.153
- 185.199.109.153
- 185.199.110.153
- 185.199.111.153

`www` CNAME:
- Host: `www`
- Points to: `<your-github-username>.github.io`

Propagation can take a while (commonly minutes, but up to 72 hours).

## Optional
- To show a contact button, edit `index.html` near the footer and uncomment the mailto link.
