# Portfolio Website — Project Overview

Hugo-based static site hosted on Netlify at `aartodding.nl`. Content is written in Markdown, Hugo builds it to static HTML/CSS, and Netlify deploys it (likely on push to master, but verify in the Netlify dashboard).

## Adding a New Project

1. Create `content/projects/my-project.md` with frontmatter:
   ```toml
   ---
   title: "My Project"
   image: "/img/my-project/thumbnail.jpg"
   rank: 110
   ---
   ```
2. Add images/videos to `static/img/my-project/`
3. Write content body using shortcodes

The `rank` field controls display order — higher rank appears first in the grid. Same applies to `content/about/` pages.

## Shortcodes Reference

```
{{< gallery >}}
  {{< gallery_img src="/img/project/image.jpg" >}}
{{< /gallery >}}

{{< mp4_gif "/img/project/video.mp4" >}}

{{< paragraph >}}Text here.{{< /paragraph >}}

{{< break >}}
```

## Design System

- **Background:** `#1D1F20` (near-black)
- **Text:** `rgb(230, 230, 230)` (light gray)
- **Links/accent:** `rgb(53, 168, 225)` (blue)
- **Headings:** `rgb(198, 100, 100)` (rose/mauve)
- **Font:** Libre Baskerville (Google Fonts, serif)
- **Grid:** Bootstrap 4.3.1

## Dependency Versions

| Dependency | Version | Notes |
|---|---|---|
| Hugo | 0.82.0 | Pinned in netlify.toml. ~4 years behind current. |
| Bootstrap | 4.3.1 | Loaded from CDN in head.html / footer.html |
| jQuery | 3.3.1 | Bootstrap 4 dependency, loaded in footer.html |
| Popper.js | 1.14.7 | Bootstrap 4 dependency, loaded in footer.html |

Do not upgrade Hugo without testing locally first — newer versions have breaking template changes.
