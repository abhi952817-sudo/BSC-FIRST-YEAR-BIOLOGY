# Standard Syllabus Format — B.Sc. Biology

यह फाइल हर subject, year, semester और paper के syllabus को एक समान तरीके से व्यवस्थित करने का मानक तय करती है। मूल विश्वविद्यालय PDF के तथ्य/शब्द नहीं बदलने हैं; केवल headings, tables और क्रम साफ करना है।

## A. Subject file structure

हर विषय के लिए अलग फाइल रखें:
- `01-BIOCHEMISTRY/SYLLABUS.md`
- `02-BOTANY/SYLLABUS.md`
- `03-ZOOLOGY/SYLLABUS.md`

हर पेपर के लिए क्रम:
1. Subject, Year, Semester और Paper
2. Course Code और Course Title
3. Programme/Class और Core/Elective स्थिति
4. Credits, Marks और L-T-P / weekly hours
5. Course Outcomes
6. Unit-wise Detailed Syllabus
7. Practical / Lab syllabus (अलग paper हो तो अलग subsection)
8. Suggested Readings / References
9. Assessment / Evaluation
10. Prerequisites and Facilities
11. Source page(s), verification status और review date

## B. Paper template

```markdown
# [SUBJECT] — [YEAR] — Semester [N]

## Paper [N]: [Course Title]

| Field | Official source detail |
|---|---|
| Course Code | [as printed] |
| Programme/Class | [as printed] |
| Core / Elective | [as printed] |
| Credits | [as printed] |
| Maximum Marks | [as printed] |
| L-T-P / weekly hours | [as printed] |
| Source page(s) | [PDF page numbers] |
| Verification | OCR / Text extracted / Checked against original |

### 1. Course Outcomes
- [Outcome copied faithfully or carefully transcribed]

### 2. Detailed Syllabus

#### Unit I — [Unit title]
- Topic
- Subtopic

#### Unit II — [Unit title]
- Topic
- Subtopic

### 3. Practical / Laboratory Work
- Experiment / activity
- Required observation or record

### 4. Suggested Readings
1. [Reference exactly as sourced]

### 5. Assessment and Evaluation
| Component | Marks / method |
|---|---|

### 6. Prerequisites and Facilities
- Eligibility:
- Facilities / equipment:

### 7. Source and Review
- Source document:
- Source page(s):
- Status: Draft / OCR check needed / Verified
- Last reviewed:
```

## C. Chapter learning-material format (15-step system)

जब किसी syllabus unit को पढ़ाई के पूरे chapter में बदला जाए, तभी यह learning format लागू होगा:
1. Chapter Introduction and Learning Objectives
2. Complete Syllabus Mapping
3. Basic Concepts
4. Topic-wise Explanation (सरल हिंदी)
5. Scientific Terminology (English term + हिंदी अर्थ)
6. Important Definitions
7. Diagrams and Labelling
8. Examples and Applications
9. Comparison and Differences
10. Short and Long Questions
11. MCQ Practice with answers and explanations
12. Active Recall
13. Revision Summary and Test
14. Weak Topics Recovery
15. Final Chapter Examination

### Multi-format learning resources
हर chapter में जहाँ उपयोगी/उपलब्ध हों:
- रंगीन callout notes: Definition / Important / Example / Exam Tip
- labelled diagrams और उनके नीचे explanation
- mind map
- topic-matched YouTube lecture links (thumbnail + source + external fallback)
- print-friendly PDF
- short/long Q&A, MCQs, chapter test और revision sheet

## D. Quality rules

- मूल syllabus से बाहर कोई unit, paper, code, marks या credit अनुमान से न जोड़ें।
- OCR से पढ़े गए course codes, marks, Hindi text और tables को original PDF से verify करें।
- स्रोत में जानकारी न हो तो `Not stated in source` लिखें।
- हर paper के साथ source PDF page numbers दें।
- Unverified content को `Draft / Needs verification` रखें; `Approved` केवल review के बाद।
- Textbook का copyrighted chapter verbatim copy न करें; teaching notes अपने शब्दों में लिखें।
