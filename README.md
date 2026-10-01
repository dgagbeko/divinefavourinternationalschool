# Divine Favour International School website

Static website for Divine Favour International School, a private early childhood school in Jasikan, Oti Region, Ghana. Plain HTML, CSS and a little JavaScript: no build step, works on GitHub Pages or any web host.

## Folder structure

```
index.html           Home
about.html           Story, mission, vision, founders
programmes.html      Creche, Nursery, Kindergarten, school hours
admissions.html      How to apply, documents, fees
contact.html         Phone, WhatsApp, email, location
404.html             Page-not-found page
css/
  fonts.css          @font-face rules for the self-hosted fonts
  styles.css         All site styles (colours and sizes are at the top in :root)
js/
  main.js            Mobile menu and footer year
assets/
  fonts/             Bricolage Grotesque (headings), Atkinson Hyperlegible (body) + licences
  images/
    logo.svg           Full logo with name (use on documents and letterheads)
    logo.png           Same, as a transparent PNG
    logo-mark.svg      Symbol only (arch, sun and open book); also the favicon
    logo-mark-512.png  Symbol only, large PNG for social media profiles
    favicon-32.png     Browser tab icon
    apple-touch-icon.png  Phone home-screen icon
    hero-sunrise.svg   Home page illustration (sunrise over the hills)
    social-card.png    Preview image when the site is shared on WhatsApp/Facebook
```

## Brand colours

| Name        | Hex       | Use                                         |
|-------------|-----------|---------------------------------------------|
| Blue-black  | `#14213D` | Text, footer, outlines                      |
| School blue | `#1F4FA3` | Links, bands, logo arch                     |
| Orange      | `#F28C1B` | Buttons, sun, highlights (not for small text on white) |
| Pale blue   | `#EAF1FB` | Section backgrounds                         |
| Pale orange | `#FFF4E5` | Section backgrounds                         |

## Fill in before going live

Search the HTML files for `[` to find every placeholder:

- **Phone number, WhatsApp number, email address**: contact.html, admissions.html. Also update the `tel:`, `wa.me/` and `mailto:` links (WhatsApp number in international format without `+`, e.g. `233XXXXXXXXX`).
- **Street or landmark**: footer of every page and contact.html.
- **Age range** for each class: index.html and programmes.html.
- **School hours and office hours**: programmes.html and contact.html.
- **Number of passport photos**: admissions.html.
- **Local language** taught in Nursery: programmes.html.
- **Story, mission, vision and founder bios**: about.html (draft wording is in brackets; replace or keep).
- **Fee payment options** (optional): admissions.html.

The header and footer are repeated in each page, so a change there needs to be made in every `.html` file.

## Adding photos

Put photos in `assets/images/` (resize to about 1600px wide and compress first so pages load fast on mobile data), then add them with:

```html
<img src="assets/images/classroom.jpg" alt="Kindergarten pupils reading together" width="1600" height="1067" loading="lazy">
```

Get parents' permission before publishing photos of children.

## Publishing with GitHub Pages

1. In this repository on GitHub, go to **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
3. The site appears at `https://dgagbeko.github.io/divinefavourinternationalschool/` within a few minutes.
4. To use your own domain, add it under **Custom domain** on the same page.

Once the final web address is known, change the `og:image` line in each page to the full address (e.g. `https://yourdomain/assets/images/social-card.png`) so link previews show the image.
