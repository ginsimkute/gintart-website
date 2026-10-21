# Gint Art website

A free, single-page, bilingual (German / English) static website for GitHub Pages.

## Publish

1. Upload `index.html`, `style.css`, `script.js`, and the `images` folder to the root of your public GitHub repository.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Choose branch **main**, folder **/(root)**, and click **Save**.
5. Wait a few minutes and open the URL GitHub shows under Pages.

## Replace photos

The large placeholders use CSS. To replace them, edit `style.css` and add an image background to `.photo-hero`, `.photo-nature`, or `.photo-vitrine` (and hide `.photo-label` in those blocks). Example:

```css
.photo-hero { background: url('images/portrait.jpg') center / cover no-repeat; }
.photo-hero .photo-label { display: none; }
```

To add gallery photos, upload them to `images/`, then edit the `products` array at the top of `script.js`:

```js
const products = [
  { id: '001', image: 'images/item-001.jpg' },
  { id: '002', image: 'images/item-002.jpg' }
];
```

Remove entries for pieces no longer available, and add new entries with unique numbers. Keep numbers stable so customers can refer to them.

## Edit contact information

The email and phone number in `index.html` are provisional: **verify them before publishing**. Update both the visible text and the `mailto:` / `tel:` links if necessary. Also check all website wording before publishing.

## Domain

Do not change your domain's DNS until the temporary GitHub Pages URL works. Then use **Settings → Pages → Custom domain** and follow GitHub's official DNS instructions for your registrar. HTTPS can be enabled once DNS is configured.

## Notes

The website uses Google Fonts, so fonts are loaded from Google's servers. The default language is German, with a persistent DE / EN switch in the header.
