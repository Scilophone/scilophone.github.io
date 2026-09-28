# Scilophone website

The long-form companion to [@scilophone](https://www.instagram.com/scilophone/) on Instagram. Each Instagram post gives the key idea; each article here tells the full story, in English and Traditional Chinese.

Live site: **https://scilophone.github.io**

The site is built with [Jekyll](https://jekyllrb.com/), which GitHub Pages runs automatically. Nobody needs to build anything. Push Markdown files and the site updates within a minute or two.

---

## One-time setup

1. **Create the organization** (free). Signed in to your own GitHub account, open **+ → New organization → Free**, name it `scilophone`, then invite the rest of the team from **People → Invite member**. Everyone keeps their own login.
2. **Create the repository** inside the organization and name it exactly `scilophone.github.io`. Make it public.
3. **Push this folder** to the `main` branch.
4. In the repo, open **Settings → Pages**. Under *Build and deployment*, set **Source: Deploy from a branch**, **Branch: `main`**, folder **`/ (root)`**, then **Save**.
5. After the first build (see the **Actions** tab), the site is live at `https://scilophone.github.io`.

> If the organization name `scilophone` is taken and you pick another, say `scilophone-sci`, name the repo `scilophone-sci.github.io` and change `url` in `_config.yml` to `https://scilophone-sci.github.io`.

---

## Writing an article

Every article has an English file and a Chinese file that share a `ref`.

| Language | Folder | URL |
|---|---|---|
| English | `en/_posts/` | `/articles/<slug>/` |
| 繁體中文 | `zh/_posts/` | `/zh/articles/<slug>/` |

1. Copy `_templates/article.en.md` to `en/_posts/2026-10-05-my-topic.md`. The date comes first, then the slug.
2. Copy `_templates/article.zh.md` to `zh/_posts/2026-10-05-my-topic.md`. Use the **same slug**.
3. Put images in `assets/img/posts/my-topic/`.
4. Fill in the front matter (the block between the `---` lines) and write the article in Markdown.
5. Commit and push. The article appears on the home page for its language, newest first.

If an article only exists in one language for now, that's fine. The language switch then goes to the other language's home page.

### Front matter fields

| Field | Required | What it does |
|---|---|---|
| `title` | yes | Headline |
| `description` | yes | Subtitle, home page summary, search and social preview text |
| `ref` | yes | Shared ID that links the English and Chinese versions (use the slug) |
| `tags` | | Topics shown above the title, e.g. `[Physics, Atmosphere]` |
| `authors` | | e.g. `[Alex Chan, Sam Lee]` |
| `cover`, `cover_alt` | | Cover image and its description. Shown on the article and the home page card |
| `instagram` | | Link to the post the article expands. Shown in the "In brief" box |
| `key_points` | | 2–4 bullets summarising the post, shown at the top of the article |
| `math` | | `true` to render equations |
| `image` | | A `.jpg`/`.png` used as the preview when the link is shared on social media |

### Things you can use in the article body

- **Headings:** `## Section` and `### Subsection`
- **References:** `text.[^1]` in the body, then `[^1]: Author, "Title", *Journal* (year).` at the end. They're collected into a numbered "Notes & references" list automatically.
- **Figures:**
  ```liquid
  {% include figure.html src="/assets/img/posts/my-topic/chart.png" alt="What it shows" caption="Caption" credit="Source: …" %}
  ```
  Add `wide=true` to make a figure wider than the text.
- **Callout box:** a blockquote followed by `{: .callout}` on the next line.
- **Equations** (with `math: true`): inline `$$E = mc^2$$` inside a sentence, or on their own lines for a centred display equation.
- **Tables, lists, links, bold and italics:** standard Markdown.

### Before launch

`en/_posts/2026-09-28-why-is-the-sky-blue.md` and its Chinese twin are **sample articles** (`sample: true` shows a notice on the page). Delete them, along with `assets/img/posts/why-is-the-sky-blue/`, once your first real article is ready. Also rewrite `about.md` and `zh/about.md`, which contain placeholder copy.

---

## Changing the site

| To change | Edit |
|---|---|
| Home page headline, button labels, footer text (both languages) | `_data/i18n.yml` |
| Colours, fonts, spacing | `assets/css/main.css` (colour tokens are at the top) |
| Logo | `assets/logo/` (mark, wordmark, full logo) and `assets/favicon.svg` |
| Site title, description, URL | `_config.yml` |
| Page structure | `_layouts/` and `_includes/` |

## Previewing locally (optional)

You don't need this to publish. It's only useful for checking a draft before pushing.

GitHub Pages' Jekyll needs Ruby 3.x. The macOS system Ruby is too old, and Ruby 4 isn't supported yet.

```sh
brew install ruby@3.4
export PATH="/opt/homebrew/opt/ruby@3.4/bin:$PATH"
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve     # then open http://localhost:4000
```
# scilophone.github.io
