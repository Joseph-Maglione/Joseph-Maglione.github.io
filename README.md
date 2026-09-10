# Joseph Maglione — app sites

GitHub Pages site for the apps. Two jobs, and nothing else belongs here.

## Privacy policies

One folder per app, serving `index.html` at `/<app>/`:

    https://joseph-maglione.github.io/<app>/

**There is deliberately no index of the apps.** The root page and `404.html`
name no app and link to no folder, so one app's policy cannot be trimmed to
discover the others. GitHub Pages generates no directory listings, so adding a
folder exposes nothing on its own. The repository is public, so folder names
are still visible on github.com; only the site hides them.

Adding an app: create `/<app>/index.html` and use its address as the privacy
policy URL wherever it is asked for. Change nothing at the root.

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
