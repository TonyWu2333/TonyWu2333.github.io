# Tony Wu

Personal website of Tony Wu (Wu Tianzhuo): Product Manager and Full-Stack AI Engineer, based in Singapore.

Live at [me.tonywu.top](https://me.tonywu.top) (Vercel), also served at [tonywu2333.github.io](https://tonywu2333.github.io).

A single static `index.html` with no build step. Open it in a browser to preview.

The site is bilingual: English is the default, and a `中文 / EN` button in the navigation switches the whole page to Simplified Chinese (choice is remembered and default-served as English).

## Keep the two copies in sync

This site lives in two repositories:

- [TonyWu2333/portfolio](https://github.com/TonyWu2333/portfolio) → Vercel, [me.tonywu.top](https://me.tonywu.top)
- [TonyWu2333/TonyWu2333.github.io](https://github.com/TonyWu2333/TonyWu2333.github.io) → GitHub Pages, [tonywu2333.github.io](https://tonywu2333.github.io)

The two `index.html` files share the same content but are styled differently on purpose: me.tonywu.top keeps the original editorial design, and this repo uses a comic-book design. The `<head>`, the visible text, the `data-i18n` keys and the Chinese translation table match in both, so a content change is made in both `index.html` files by hand. Never copy one `index.html` over the other.

Every other file stays identical. Pull both first, edit one, copy the changed files to the other, and commit and push both.

`vercel.json` (security headers, the `/index.html` redirect) only takes effect on Vercel. GitHub Pages ignores it, but it stays in both repos so the shared files remain identical. Both copies point their canonical at me.tonywu.top.

## SEO files

- The `<head>` of `index.html` holds the canonical, Open Graph tags and Person JSON-LD. When a role, employer or profile changes, update the JSON-LD, `llms.txt` and the visible text together.
- `og-image.png` is the 1200×630 link-preview card.
- `robots.txt`, `sitemap.xml` and `llms.txt` describe the site to crawlers. Bump `<lastmod>` in `sitemap.xml` after a content change.
