# Roof Champ, Field Tools

Static site. No build step, no dependencies. Everything is plain HTML.

    index.html      launcher
    texts.html      the 21 text messages
    claim.html      the 50-card claim walkthrough
    manifest.webmanifest, icons, robots.txt, _headers

## Netlify (fastest, about a minute, no account needed to try it)

1. Go to https://app.netlify.com/drop
2. Drag this whole folder onto the page.
3. It gives you a URL immediately. Open it on your phone.
4. Share button -> Add to Home Screen. You get the icon.

To keep it: sign in and click "Claim site". Then Site settings -> Change site name
to something like roofchamp-tools, so the URL is memorable.

To lock it down: Site settings -> Access control -> Password protection.
That is a paid feature. Without it the URL is unlisted but not private.

## GitHub Pages

    git init
    git add .
    git commit -m "field tools"
    git branch -M main
    git remote add origin https://github.com/<you>/<repo>.git
    git push -u origin main

Then: repo Settings -> Pages -> Source: Deploy from a branch -> main -> / (root).
Live in a minute or two at https://<you>.github.io/<repo>/

Note: GitHub Pages on a free account requires a PUBLIC repo, which means the site is
readable by anyone who finds it. robots.txt and the noindex tags keep it out of search
results, but that is obscurity, not security. If that matters, use Netlify instead and
put a password on it.

## Updating it later

Replace the HTML file and re-drop the folder (Netlify) or commit and push (Pages).
Nothing else to do.
