# Nexar.io website

A small static website for GitHub Pages. No package installation, build step, JavaScript, database, or server is needed. Uses the real Nexar.io app icon and public support email.

## Publish

1. Create a GitHub repository, such as `nexar-support`. Use a **public repository** for GitHub Pages on the Free plan. This package contains only website files; the app source can stay private.
2. Unzip this package. Put the **contents of `nexar-website`** at your repository root, so `index.html` is directly at the root. Include the hidden `.nojekyll` file if your upload method allows it.
3. Commit and push the files to `main` (or upload them using GitHub’s Add file → Upload files).
4. Open the repository’s **Settings → Pages**. Under Build and deployment choose **Deploy from a branch**, select **main** and **/(root)**, then Save.
5. Wait for GitHub’s Pages deployment to finish. Use the published URL shown in Settings → Pages and open all three pages to confirm they load.

[GitHub’s official publishing instructions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

All internal links and assets use relative paths, so the same files work at a project address (`https://OWNER.github.io/REPOSITORY/`), an organization homepage, or a custom domain.

## Links for App Store Connect

Use the actual published base address shown by GitHub, keeping its repository path if present:

| Apple field | Page |
| --- | --- |
| Marketing URL (optional) | `index.html` or the site’s base URL |
| Support URL | `support.html` |
| Privacy Policy URL | `privacy.html` |

For example, if your published site is `https://OWNER.github.io/nexar-support/`, the Support URL is `https://OWNER.github.io/nexar-support/support.html` and the Privacy Policy URL is `https://OWNER.github.io/nexar-support/privacy.html`. Replace OWNER with the actual account or organization; these example URLs are not live.

## Optional custom domain

In Settings → Pages → Custom domain, enter your chosen domain/subdomain and configure DNS using [GitHub’s custom-domain instructions](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site). Enable **Enforce HTTPS** when available. GitHub adds a CNAME file for branch-based publishing; pull that commit before your next push. No domain has been preconfigured in this package.

If the domain already handles business email, preserve the existing mail-related DNS records. A dedicated support subdomain can leave the current main website in place.

## Files

- `index.html` — small app homepage; no nonworking App Store download button before launch.
- `support.html` — contact details, purchase restoration, progress, and troubleshooting.
- `privacy.html` — app privacy policy, support correspondence, and GitHub Pages hosting disclosure.
- `assets/style.css` — responsive styling with keyboard focus indicators.
- `assets/icon.png` — existing Nexar.io icon.
- `.nojekyll` — serve the static files without Jekyll processing.

The support address is **preston@radonresearchkorp.com**. Keep the privacy policy and course information current when app behavior changes. This package has not created a GitHub repository or published the website.

To preview before pushing, open `index.html` in a browser. Navigation also works directly from local files.
