# AtlasBot

AtlasBot is a small web crawler that reads the **public home page** of a company's website so that a search tool can check whether the company matches what a user is looking for (for example, "independent pharmacies in Texas").

## What it does

- Requests a company's home page, and at most one other public page on the same site (such as an "About" page).
- Reads the text to judge fit, then keeps only a short excerpt and the page URL. It does not store or republish full pages.
- Identifies itself with the User-Agent `AtlasBot/0.1 (+https://github.com/a-khandel/atlasbot)`.

## How it behaves

- Respects `robots.txt`.
- Makes at most one request at a time per site, and keeps the overall request rate low.
- Fetches HTML only, with a size cap. It does not log in, submit forms, or visit login-protected pages.
- Never fetches LinkedIn or other social media pages.
- Does not collect personal data about individuals.

## Opt out or ask a question

Email **khandelwal.aryan2416@gmail.com** with your domain and we will stop crawling it and add it to a block list. You can also block AtlasBot yourself in `robots.txt`:

```
User-agent: AtlasBot
Disallow: /
```
