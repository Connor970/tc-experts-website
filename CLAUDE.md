# TC Experts website

Static site for TC Experts LLC (tc-experts.com), a transaction coordination company for real estate wholesalers and investors. Hosted on Netlify, which publishes the `site/` folder whenever `main` changes. No build step.

## Layout
- `site/index.html` — landing page (lead form uses Netlify Forms: `name="contact"`, keep `data-netlify="true"` and the hidden `form-name` input).
- `site/thanks.html` — form success page.
- `site/blog/index.html` — blog listing. New posts go between `<!-- POSTS:START (newest first) -->` and `<!-- POSTS:END -->`, newest at the top, as a `.card` block like the existing one.
- `site/blog/<slug>.html` — one file per post. Copy the structure of an existing post exactly (head meta, canonical, Open Graph, BlogPosting + FAQPage JSON-LD, header nav, `.hero`, `.article`, `.cta`, footer). Styles live in `site/assets/blog.css`; do not add inline style blocks.
- `site/sitemap.xml` — add a `<url>` per post before `<!-- URLS:END -->`, with `<lastmod>`.
- `BLOG_LOG.md` — running list of published posts and target keywords. Read it before choosing a topic so posts never repeat a topic or primary keyword.

## Blog writing rules
- Audience: real estate wholesalers, fix-and-flip investors, creative-finance investors (subject-to, seller finance, wraps).
- Goal: rank in Google for transaction-coordination searches and convert readers into leads via the "Get started" CTA (`/#start`).
- 1,200–1,800 words, plain helpful language, short paragraphs, H2/H3 structure, one primary keyword in the title, H1, first paragraph, meta description, slug and at least one H2.
- Include an FAQ section (3 questions) mirrored in FAQPage JSON-LD.
- Where relevant, mention that on wholesale deals the TC fee is typically paid by the end buyer at closing, so TC is usually free to the wholesaler.
- Never invent statistics, studies, quotes, testimonials, prices or legal rules. No "studies show." State-specific legal claims only if general and well established; otherwise suggest consulting a title company or attorney.
- Link internally to at least one earlier post when it fits, and to `/#start`.
- Brand voice: confident, practical, investor-friendly. No emoji.
