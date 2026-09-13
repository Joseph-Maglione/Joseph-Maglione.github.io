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
neither to the root nor to any other app page. A page covers exactly one app
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

## Why this is an organization

This account exists so the apps are not served from a personal custom domain.
A custom domain on a user site is inherited by every repository that account
owns, and every `github.io` link under it redirects to that domain. An
organization is a separate Pages namespace with no custom domain, so these
addresses stay on `github.io` permanently. Do not add a custom domain here
without deciding that is what you want.
