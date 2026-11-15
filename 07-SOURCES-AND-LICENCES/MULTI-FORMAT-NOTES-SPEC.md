# Multi-Format Chapter Notes Specification

This file defines the standard format for every approved B.Sc. First Year chapter.
Do not add invented syllabus units or unverified academic content. Confirm the degree-awarding university and official 2026–27 syllabus before publishing chapter records as approved.

## Required chapter package

Each chapter should have:

1. **Colourful notes** — clear headings, readable paragraphs, highlighted definitions, important facts, examples, scientific terms, tables and step-by-step explanations.
2. **Diagrams** — labelled images with captions, explanations, source and reuse licence.
3. **PDF** — print-friendly chapter notes containing the same reviewed notes and diagrams.
4. **Mind map** — a visual chapter overview, with a source/authoring record.
5. **Video lessons** — YouTube URLs, topic, teacher/channel and chapter mapping. Embed the video in the app when YouTube permits it; retain an external link as fallback.
6. **Questions** — short answers, long answers, MCQs with explanations and source/review notes.
7. **Revision** — summary, key terms, active-recall prompts and a chapter test.

## Content quality and publishing

- Keep notes in the subject's `CHAPTERS/` folder as Markdown.
- Keep diagrams in the subject's `DIAGRAMS/` folder.
- Keep video metadata in `07-SOURCES-AND-LICENCES/videos.json`.
- Keep diagram metadata in `07-SOURCES-AND-LICENCES/diagrams.json`.
- Keep mind-map metadata in `07-SOURCES-AND-LICENCES/mindmaps.json`.
- Keep practice tests in `04-QUESTION-BANK/tests.json`.
- Mark content `draft` until syllabus mapping, scientific accuracy, image rights and answer keys are checked. Only then set it to `approved`.
- Do not reproduce copyrighted textbook chapters or use unlicensed images.
- A YouTube embed can fail due to owner restrictions, network filtering or platform settings; always retain a normal YouTube link.

## Mind map catalogue schema

Each item may contain:
- `id`: stable unique identifier
- `title`: map title
- `subject`: Botany, Zoology or Chemistry
- `chapterId`: matching chapter ID
- `description`: short description
- `image`: repository-relative or HTTPS image URL
- `pdf`: optional PDF URL
- `source`: source/authoring attribution
- `status`: draft or approved

## Fifteen-day coverage planning

The 15-day timetable must be generated only after the official syllabus is mapped. Divide every paper into its actual units and topics, estimate topic workload, reserve daily time for recall and questions, and include a cumulative revision/mock-test day. Do not claim full coverage based only on chapter titles.
