# Threat Matrix — public showcase

This folder is the **public-facing shopfront** for the (private) `abuse-detection-platform`
repository. It's deliberately separate: the code stays private and by-request, while this page is
public and discoverable.

```
threat-matrix-showcase/
├── index.html        # the showcase landing page (GitHub Pages serves this)
├── FINDINGS.md       # the red-teaming write-up
├── README.md         # this file
└── images/
    ├── dashboard.png
    └── architecture.png
```

## Where to put it (GitHub Pages — ~5 minutes)

1. Create a **new public** repo, e.g. `threat-matrix-showcase`.
2. Push the contents of this folder to it:
   ```bash
   cd threat-matrix-showcase
   git init && git add . && git commit -m "Threat Matrix showcase"
   git branch -M main
   git remote add origin https://github.com/richiefrank-projects/threat-matrix-showcase.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Source: Deploy from a branch → `main` / root → Save.**
4. Your page goes live at `https://richiefrank-projects.github.io/threat-matrix-showcase/`
   within a minute or two. That's the single URL for a resume, a LinkedIn bio, or a cold email.

> Lower-effort alternative: skip Pages entirely and just make the repo public with `FINDINGS.md`
> as a second file — GitHub renders `index.html` as raw text in a repo, so for the no-Pages route,
> rename a copy of the page's content into the repo's `README.md` instead. Pages is worth the 5
> minutes; the page looks far more like a portfolio piece than a rendered README.

## Before you publish — three things to set

1. **The walkthrough video.** The page currently links the "Watch" button to the access section.
   To embed the real video, host it **unlisted on YouTube** (unsearchable, link-only) and replace
   the `<a class="frame" …>` block in `index.html` with an iframe:
   ```html
   <iframe class="frame" src="https://www.youtube.com/embed/VIDEO_ID"
     title="Threat Matrix walkthrough" frameborder="0" allowfullscreen
     style="border:1px solid var(--line);border-radius:10px"></iframe>
   ```
   (Unlisted keeps it off your channel while still letting a visitor watch in one click instead of
   emailing first.)
2. **Contact details.** The page shows `richiepfrank@gmail.com`, your LinkedIn, and your GitHub org.
   Confirm you want that email public, or swap in a contact address you'd rather use. Update the
   LinkedIn/GitHub URLs if the handles differ.
3. **The repo link.** The access section points at `github.com/richiefrank-projects`. If you'd
   rather link the specific (private) repo so people can request access via GitHub, point it there.

## Keeping the code private is fine

Nothing here exposes the source. The page uses only two screenshots and published metrics. The
`abuse-detection-platform` repo stays exactly as private as it is now; this showcase is what makes
it *discoverable* without opening it.
