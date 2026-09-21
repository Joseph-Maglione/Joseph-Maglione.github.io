# Joseph Maglione — app sites

GitHub Pages site for the apps. Two jobs, and nothing else belongs here.

## The root page is the site's own privacy policy

`index.html` at the root is the privacy policy **for this website**, not an
index of the apps. It says what the site itself does: static pages on GitHub
Pages, no cookies, no analytics, no scripts at all, no third-party embeds,
nothing collected — only the ordinary connection logging any host does.

**It names no app and links to no app folder.** Neither does `404.html`. That
is deliberate: one app's policy cannot be trimmed back to the root to discover
the others. GitHub Pages generates no directory listings, so adding a folder
exposes nothing on its own. The repository is public, so folder names are still
visible on github.com; only the site hides them.

## App privacy policies

One folder per app, serving `index.html` at `/<app>/`:

    https://joseph-maglione.github.io/<app>/

**Each app page is self-contained.** It carries no navigation, and it links
neither to the root nor to any other app page (a favicon `<link>` to the root
icon files is not navigation and is fine). A page covers exactly one app
and says so. Anything shared between them is copied, not linked.

Adding an app: create `/<app>/index.html` and use its address as the privacy
policy URL wherever it is asked for. Change nothing at the root.

Assets an app page needs (its icon, a background image) live inside that app's
own folder and are referenced relatively, so the folder stays portable.

## app-ads.txt

`app-ads.txt` must answer at the ROOT of whatever developer website an app's
store listing names, which is why it lives here rather than in a subfolder.
The line authorises AdMob publisher `pub-6313858681834032` to sell these
apps.

Set the developer website on every store listing to
`https://joseph-maglione.github.io` so the crawler finds it.

## Site plumbing

`robots.txt` at the root allows everything and points crawlers at
`sitemap.xml`. The sitemap lists the app pages only — the root and `404.html`
are noindex and deliberately stay out of it; the point above, that the root
names no app, still holds, because the sitemap is for search engines and App
Review reaching each policy directly, not for a person browsing the site, and
the folder names are public on github.com anyway.

`favicon.svg` and `favicon.ico` at the root are the site-wide fallback icon.
An app page that has its own icon (Water Play's, for instance) links it with
a relative `<link rel="icon">` instead of falling back to the root one.

Every app page also carries a `<link rel="canonical">` and a set of Open
Graph / Twitter tags (`og:type`, `og:site_name`, `og:title`, `og:description`,
`og:url`, `twitter:card`, plus `og:image` where a page has an icon to point
at). Keep new pages to that pattern.

## Why this is an organization

This account exists so the apps are not served from a personal custom domain.
A custom domain on a user site is inherited by every repository that account
owns, and every `github.io` link under it redirects to that domain. An
organization is a separate Pages namespace with no custom domain, so these
addresses stay on `github.io` permanently. Do not add a custom domain here
without deciding that is what you want.
