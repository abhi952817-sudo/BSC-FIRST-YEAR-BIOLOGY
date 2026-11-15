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
