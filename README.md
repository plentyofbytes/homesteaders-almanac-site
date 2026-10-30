# Homesteader's Almanac website

Three plain pages (home, contact and support, privacy) with no build step, no cookies, no analytics and no third-party requests. Hosted on GitHub Pages at homesteadersalmanac.com once it is made public.

This repo is **private** until the site is ready. GitHub Pages on a free plan only serves public repos. Keep it free of anything internal: it will be public the day it goes live, history included. The almanac itself (content, pipeline, apps) lives in a separate private repo and is never copied here wholesale.

## Preview

```
python -m http.server 8765
```

Then open http://localhost:8765.

## Files

| File | What it is |
| --- | --- |
| `index.html`, `contact.html`, `privacy.html`, `404.html` | The pages. Edit them directly; the header and footer are repeated in each. |
| `style.css` | Palette and type from the almanac's `docs/style-guide.md`; light and dark. |
| `fonts/` | IM Fell English and EB Garamond, subset to Latin, with their OFL licenses. Served from this site, not Google. |
| `img/` | Plant plates from the almanac (tomato, apple, sunflower, garlic). |
| `CNAME` | The custom domain, `homesteadersalmanac.com`. Change it if the domain changes. |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are. |

## Before it goes live

1. Buy the domain. Point it at GitHub Pages with DNS records (GitHub's "Configuring a custom domain" page lists the current A and CNAME values), and add Google's MX, SPF, DKIM and DMARC records for the mail.
2. Create the mailbox: `hello@homesteadersalmanac.com` appears on the contact and privacy pages. Until the address exists, mail sent to it bounces.
3. Privacy page: it is a draft written for the current plan. Add the LLC's legal name and re-check it against the shipped app and the App Store privacy answers (task P2-06 in the almanac repo).
4. Make the repo public, then Settings, Pages: deploy from the `main` branch, root folder, and tick "Enforce HTTPS".
5. Use `https://homesteadersalmanac.com/contact.html` as the App Store support URL and `https://homesteadersalmanac.com/privacy.html` as the privacy policy URL.
6. Replace the plates with App Store screenshots of the finished app if you want the home page to show the app itself.
