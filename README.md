# Selim Medical Press website

A single-page static site for the Selim Medical Press catalog: books, MTTI courses, free companion tools, consulting, and a new-release email list.

Live address once published: https://abdu94-hash.github.io/selim-medical-press/

## Publish on GitHub Pages (about 5 minutes)

1. Sign in to GitHub as **abdu94-hash** and click **New repository**.
2. Name it `selim-medical-press`, set it to **Public**, and click **Create repository**.
3. Click **uploading an existing file**, then drag in everything from this folder, including `.nojekyll` and the `covers` folder. Click **Commit changes**.
4. Go to **Settings → Pages**. Under *Build and deployment*, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
5. Wait a minute or two and open https://abdu94-hash.github.io/selim-medical-press/

## Editing the content

Everything you'll change lives in one block near the bottom of `index.html`, under `SITE SETTINGS`:

- `BOOKS` — one entry per title. Set `status` to `"available"` or `"forthcoming"`. Put the book's own Amazon link in `amazon`; if it's empty the button says "Find on Amazon" and goes to your author page.
- `COURSES` — name, price, one-line description, course link.
- `TOOLS` — the free companion tools.
- `SETTINGS.mailerliteAction` — see below.

Edit the file directly on GitHub (open it, click the pencil icon, commit). The site updates within a minute or two.

## Connecting MailerLite

1. In MailerLite, go to **Forms → Embedded forms → Create**, add a *Name* field, and save.
2. Open the form's **HTML code** tab and find the `<form ... action="...">` URL. It looks like
   `https://assets.mailerlite.com/jsonp/1234567/forms/987654321/subscribe`
3. Paste it between the quotes of `mailerliteAction` in `index.html` and commit.

Until that's filled in, the signup form tells visitors the list opens soon.

## Using your own domain later

Buy the domain (e.g. selimmedicalpress.com), then in **Settings → Pages → Custom domain** enter it and follow GitHub's DNS instructions. Update the address in `robots.txt`, `sitemap.xml` and the `canonical` / `og:url` lines at the top of `index.html`.
