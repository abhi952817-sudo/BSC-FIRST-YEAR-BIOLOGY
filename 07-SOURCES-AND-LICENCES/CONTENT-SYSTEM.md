# Dynamic content authoring guide

This PWA reads static JSON indexes and Markdown files from GitHub Pages. No backend is needed.

## Publish a chapter
1. Verify the title and topics against the official 2026–27 degree-awarding university syllabus.
2. Copy 00-DASHBOARD/CHAPTER-TEMPLATE.md into the correct subject's CHAPTERS folder.
3. Add a record to that subject's chapters.json, for example:

    {
      "id": "botany-ch-001",
      "title": "Verified chapter title",
      "file": "CHAPTERS/chapter-file.md",
      "unit": "Unit 1",
      "topics": ["Topic A", "Topic B"],
      "status": "approved"
    }

Use status "draft" until the syllabus mapping, facts, diagrams and sources have been reviewed. Only status "approved" is visible in the app. The file path is relative to the subject folder. IDs must be unique within a subject.

## Diagrams
Add records to 07-SOURCES-AND-LICENCES/diagrams.json under items. Fields: title, image, caption, subject, source and licence. Use a repository-relative image path or HTTPS URL. Check reuse rights and attribution.

## Video links
Add records to videos.json under items. Fields: title, topic, subject, teacher and url. Use valid public lecture URLs.

## MCQ practice tests
Add records to 04-QUESTION-BANK/tests.json under tests. Example:

    {
      "id": "botany-test-001",
      "title": "Reviewed practice test",
      "subject": "Botany",
      "minutes": 10,
      "questions": [
        {
          "question": "Question text",
          "options": ["A", "B", "C", "D"],
          "correctIndex": 0,
          "explanation": "Why option A is correct.",
          "source": "Reference and page/section"
        }
      ]
    }

Each question must have exactly four options and correctIndex from 0 to 3. The app supports countdown, question navigation, automatic timeout submission and answer review. Because this is a public static repository, answers in the JSON are visible to anyone; use this only for practice, never for secure examinations.

## Offline use
The service worker caches same-origin resources after successful network access. Open each chapter once while online to make a best-effort cache copy. Browser storage may be cleared, so this is not a guaranteed full-library download.


## Multi-format chapter reader

The chapter reader renders these linked resources for an approved chapter:
- Notes: Markdown headings, paragraphs, lists, emphasis, links, images and callout panels.
- Diagrams: entries in `diagrams.json` matched by `chapterId`, or by matching subject + chapter title.
- Mind maps: entries in `mindmaps.json` matched by `chapterId`, or by matching subject + chapter title.
- Videos: YouTube watch, youtu.be, embed and shorts URLs are embedded using the privacy-enhanced `youtube-nocookie.com` host where possible. The external video link remains available.
- Questions: chapter-linked tests are shown from `tests.json` when `chapterId` or subject + chapter title matches.
- PDF: use **Save / Print PDF** in the chapter reader and select **Save as PDF** in the browser print dialog. This prints the chapter's notes and supporting material; video players are omitted from print.

### Chapter callout syntax

Use a callout block with one of these classes:

```text
::: definition
**परिभाषा:** Verified definition.
:::

::: important
Exam-relevant point.
:::

::: example
A short worked example.
:::

::: term
Scientific term — सरल हिंदी अर्थ.
:::
```

Images may be included with standard Markdown image syntax: `![Alt text](relative-or-https-image-url)`. Ensure the URL is safe, the image is legible on mobile and its reuse licence is recorded.

### Mind map item example

```json
{
  "id": "botany-topic-map-001",
  "title": "Chapter concept map",
  "subject": "botany",
  "chapterId": "verified-chapter-id",
  "description": "A short overview of the chapter relationships.",
  "image": "01-BOTANY/DIAGRAMS/concept-map.png",
  "pdf": "01-BOTANY/DIAGRAMS/concept-map.pdf",
  "nodes": [
    { "label": "Main concept", "children": [{ "label": "Subtopic" }] }
  ],
  "source": "Author-created from verified references",
  "status": "draft"
}
```

### Chapter-linked videos and tests

For reliable chapter matching, include the exact chapter ID as `chapterId` in the video, diagram, mind map or test record. A fallback match uses subject + exact chapter title. Use subject IDs `botany`, `zoology`, `chemistry` consistently in catalogue data.

The public JSON test bank contains answer keys in browser-accessible files. These are practice questions only, not secure exam content.
