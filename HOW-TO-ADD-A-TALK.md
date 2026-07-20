# How to add a talk

Time estimate: **under 10 minutes.** You never touch layout code.

## 1. Create the file

From this repo's folder:

```
../.tools/hugo new content/en/talks/2026-11-14-lastname.md --kind talks
```

(Any editor works too — copy an existing talk file and rename it. The filename convention is `YYYY-MM-DD-speaker-lastname.md`.)

## 2. Fill in the fields

Open the new file and fill in the front matter:

```yaml
---
title: "Talk title here"          # LaTeX-ish unicode (H², λ) is fine in titles
date: 2026-11-14T12:00:00-05:00   # date + start time, with timezone
speaker: "First Last"
affiliation: "University"
talk_time: "12:00 pm Eastern"     # human-readable time shown on the page
math: true
---

The abstract goes below the front matter. Inline math like \(H^2\)
and display math between $$ … $$ both render automatically.
```

The talk sorts itself: future dates appear under **Upcoming**, past dates under **Archive**. Nothing else to edit.

## 3. After the talk

Add two lines to the same file and the page updates itself:

```yaml
youtube_id: "dQw4w9WgXcQ"     # the YouTube video id → embeds the recording
materials: "/slides/lastname.pdf"  # optional; put the PDF in static/slides/
```

## 4. Preview and publish

```
../.tools/hugo server --source .     # preview at localhost:1313
git add . && git commit -m "Add November talk" && git push   # live in ~1 minute
```
