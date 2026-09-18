# ECLASS+ — What's new since version 1.202609091613

*The version you started from was released 9 Sept 2026 (shown in the app as “Round 8: SF9/TGS
revert + modern .xlsx”). Everything below came after it. The app is still one single file — open
it in any browser, nothing to install, works with no internet.*

**Current file:** `ECLASS+ version 1.202609140000.html` · 1,387,491 bytes · md5 `39eb516b…`
(now shown as **Version 2.3.0 · Build 20260916**)
*(the file name stays the same while it is revised in place; the size + md5 tell the versions apart — see the update log below)*

**Last updated:** 16 Sept 2026 · Version 2.3.0 · Build 20260916 — every release, with its date, is listed under the update log below.

---

## Update log — every release and its date

*All dates and times are Philippines time (**Asia/Manila**). From 14 Sept 2026 onward the file name stays
`ECLASS+ version 1.202609140000.html` for every build — each release is revised in place, so the size +
md5 (or the build line under **Setup**) tell the copies apart.* <!--update-log-->

| Date (PH) | Build / version | What changed | Size | md5 (first 8) |
|---|---|---|---|---|
| **9 Sept 2026 · 16:13** | `1.202609091613` — **your starting point** | Round 8: SF9/TGS revert + the first modern `.xlsx` export/import | 1,107,580 B | `3f8b90f7` |
| **10 Sept 2026 · 12:34** | `1.202609101234` (Round 9) | Smaller footer + Setup footer controls · automatic file names · top-anchored, centred printing · header autofit · descriptor columns · legend counts | 1,127,807 B | `9dec9cc7` |
| **14 Sept 2026** | `1.202609140000` — first build of the living line | **Excel overhaul:** page-mirror workbook with the hidden `ECLASS+ Sync` sheet, real importer, final-grade override window, 0.25 in margins, slip / margin / signatory work | — | — |
| **14 Sept 2026** | same file name, revised in place | **“Can’t be opened in Excel” — root cause found and fixed** (the worksheet is written in the exact order Excel requires; checked against the ECMA-376 schemas) | 1,293,582 B | `a9bc5853` |
| **14–15 Sept 2026** | same file name | **“Columns not aligned / import changes nothing” fixed** — the legend edges no longer split the grid, and an edited workbook imports back into the right cells | 1,296,249 B | `9d8f3536` |
| **15 Sept 2026** | same file name (Round 13) | Grade-1 records show letters **A–E** (never 0) · **four grade slips per page** with equal margins · perfect Excel round trip · correct paper on every page | 1,301,152 B | `aa198cf3` |
| **15 Sept 2026** | **Version 2.2.0 · Build 20260915** (Round 14) | **EPP and TLE become composite subjects** — ICT + AFA in Term 1, ICT + FCS in Term 2, ICT + IA in Term 3; EPP for Grades 4–6, TLE for Grades 7–10 | 1,326,026 B | `161f85f4` |
| **15 Sept 2026** | **Version 2.2.0 · Build 20260915** (Round 15) | Grade-1 remarks in plain, varied words · **EPP/TLE component columns** on the Term and Final summaries (never on the SF9/TGS) · **“Override all subject areas”** (import a Term Summary workbook and every learning area’s class record follows) · refreshed demo data incl. Grade 4 · Grade-1 Term Summary trimmed to the table + signatories | 1,367,839 B | `6cb4ecff` |
| **16 Sept 2026** — today | **Version 2.3.0 · Build 20260916** (Round 16) | **Grade-1 descriptions are now editable:** click **What Your Child Can Do** or **What Your Child Is Learning To Improve** on the Term 1–3 Summary, the SF9 or the TGS and write your own words — the same text appears on all three, per learner and per term; marked light green like an overridden grade; **Restore automatic text** (in the editor) or **Clear edited descriptions (n)** (summary toolbar) puts the generated wording back; up to 2,000 characters; saved with the class and carried by the JSON backup, keyed by LRN so the words follow the child across the five Grade-1 area records | **1,387,491 B** | `39eb516b` |

**Which copy do I have?** Open the app → **Setup** → read the build line at the foot of the page (for
example `Version 2.3.0 · Build 20260916`). That is the quickest check. The file’s size + md5 above match
that same build.

---

## 1. Excel export & import — the biggest change

| | |
|---|---|
| **Before** | The Excel file was a plain table of values. Column headings and values could drift one column apart in Terms 1–3, and Excel sometimes opened the file with a repair/“Removed Records” warning. Importing an edited file usually changed nothing. |
| **Now** | Export produces a workbook that **looks like the page you are looking at** — same fonts, colours, boxes, merged cells, the DepEd seal, school logo and learner photos, same column widths and row heights, same page set-up for printing. It carries a hidden `ECLASS+ Sync` sheet that remembers which cell belongs to which learner/activity, so the file can be edited in Excel and **imported back into the app**. |

Why you care:

* **Print straight from Excel** — the workbook carries the same geometry as the app's print preview.
* **Excel opens it cleanly** — no repair dialog, no “Removed Records: Cell information”. The file is
  written in the exact OOXML order Excel expects (checked against the official ECMA-376 schemas, and
  with LibreOffice, calamine and openpyxl).
* **Columns match their headings** — every Written / Performance / Examination score sits under its own
  activity column and in the right learner row, in Terms 1, 2 and 3 and in the summaries.
* **Edits really come back** — change a score in Excel, save, then press **Import Excel**: the new value
  appears in that same cell (totals, PS / WS, initial grade, term grade and descriptors recompute).
  Clearing a cell in Excel clears that score. Editing works after Excel (or LibreOffice) re-saves the file.
* **Safe import** — a workbook that belongs to another class/section will not overwrite the open class;
  the app says so instead of guessing.
* Every page family exports and re-imports: class records (Terms 1–3), term & final summaries, Final
  Grades, attendance, SF9, temporary grade slip, grade slip, individual reports, parent report log,
  PACE, dashboard and setup.

---

## 2. Grade slips (Grades 2–10) — made to cut perfectly into four

| | |
|---|---|
| **Before** | The four slips on a page came out sitting in a wide centred band, with big uneven white space around and between them. |
| **Now** | Exactly **four slips per page**, spread over the whole sheet: the **same ~6 mm (0.25 in) white band on the top, left, right and bottom, and the same ~6 mm gap between the slips** — so a printed page cuts into four identical slips. |

* Works on **A4, short bond (Letter) and folio / long bond**, portrait or landscape — and the printed
  sheet really is the paper you picked. (The old page-size hint was invalid CSS, so the browser quietly
  printed on the wrong paper — that was the real cause of the “very centred” look.)
* One sheet per four learners (24 learners → 6 sheets), no stray blank pages.

---

## 3. Grade 1 class records — the letters A–E now work

| | |
|---|---|
| **Before** | Type `A`, and the cell showed **0** — grade-1 records are graded with letters, but the app was reading them as numbers. |
| **Now** | Type **A, B, C, D, E** (or a, b, c…) and the cell keeps the letter, and the record stores the letter. It never turns into 0. |

* Works in **all five grade-1 subjects** (Reading & Literacy, Language, Mathematics, GMRC, Makabansa)
  and in **terms 1, 2 and 3**.
* A wrong key doesn't wipe the grade, blank clears it, and the letter survives clicking away, pressing
  Enter and pasting.
* The letters **export to Excel as letters and import back as letters**.
* Reading & Literacy and Language have **one page per term**; Mathematics, GMRC and Makabansa show a
  single **“Term 1–3”** page (one record for the whole year).
* **The remarks no longer sound like a robot.** The Grade-1 **Term 1–3 Summary** and the **SF9** used to
  open every learning area with the same “Kaya na ni *<name>*…” line. Now the learner's name appears once
  (in the first area) and the other areas use a different, equally natural opener — *Kaya na niyang…*,
  *Nagagawa na rin niyang…*, *Naisasagawa na niyang…* — chosen per learner, so a class of 30 does not read
  alike, and the same learner keeps the same wording every time you look again.
* **The Grade-1 Term 1–3 Summary is now just the table and the signatories.** The “Paano basahin”, code
  table and macro-skill blocks that used to sit under the table are gone, so the page prints shorter and
  the signatory lines follow the table immediately. <!--r16-g1-descriptions-->

### 3b. Write the Grade-1 descriptions yourself

| | |
|---|---|
| **Before** | “What Your Child Can Do” and “What Your Child Is Learning To Improve” were generated from the A–E letters and could not be changed — a teacher who wanted to say something more specific (or in her own voice) had no way to do it. |
| **Now** | **Click either description and write your own words.** |

* Click the cell on the **Term 1–3 Summary** (or on the **SF9** / **TGS**) — the box opens with the
  automatic wording already in it, so you can keep the parts you like and rewrite the rest.
* What you write is what **prints** — the Term Summary, the SF9 and the TGS all show the same text for
  that learner and that term. The three terms are separate, so Term 1 can say one thing and Term 3 another.
* The description belongs to the **learner** (matched by LRN), so it follows the child whichever Grade-1
  class record you are in — Reading & Literacy, Language, Mathematics, GMRC or Makabansa.
* Edited descriptions are marked **light green** exactly like an overridden grade, and the same
  **Hide / Show adjusted cells** button controls that colour.
* **Restore automatic text** (in the editor) or **Clear edited descriptions (n)** (in the Term Summary
  toolbar) puts the generated wording back — one learner at a time or for the whole term.
* Up to 2,000 characters per description; the editor shows the counter and refuses a text that is too long
  instead of cutting it off.
* The descriptions live in the app's saved data: they survive a reload, go into the **JSON backup** and
  come back on **Restore**. “Delete all data” removes them with the rest.
* Grades 2–10 are untouched — their summaries have no description columns.

---

## 4. EPP and TLE are now composite subjects (like MAPEH)

| | |
|---|---|
| **Before** | EPP/TLE was one plain subject. Schools that teach it the DepEd way — with two components per term — had nowhere to put them, and the SF9 could only carry one number. |
| **Now** | **Every term has two components, and their average IS the EPP/TLE grade:** |

| Term | Components | What appears |
|---|---|---|
| Term 1 | **ICT** + **AFA** (Agriculture and Fishery Arts) | one **EPP** or **TLE** grade = their average |
| Term 2 | **ICT** + **FCS** (Family and Consumer Science) | one **EPP** or **TLE** grade = their average |
| Term 3 | **ICT** + **IA** (Industrial Arts) | one **EPP** or **TLE** grade = their average |

* **EPP for Grades 4–6 · TLE for Grades 7–10.**
* Each component is a real class record with its own roster, Written Works / Performance Tasks /
  Examinations — so you encode a component exactly like any other subject.
* **Setup → Classes/Sections → “＋ Add EPP/TLE components”**: one click creates the four component
  subjects for that Grade + Section (EPP-ICT, EPP-AFA, EPP-FCS, EPP-IA — or TLE-…) and copies the
  class list into each of them. The class wizard's subject list offers them too.
* **Term 1–3 Summaries** show the parent column (**EPP** or **TLE**, bold, computed) followed by
  that term's two component columns (Term 1: ICT + AFA · Term 2: ICT + FCS · Term 3: ICT + IA).
* **Final Grade Summary** keeps a single EPP/TLE block (T1, T2, T3, Final) and prints the component
  pairs in the header (`T1 ICT+AFA`, `T2 ICT+FCS`, `T3 ICT+IA`).
* **Trusted, not typed:** the parent **EPP**/**TLE** column is *computed* — you encode the components and
  the app averages them for you.
* **SF9 and Temporary Grade Slip print only EPP or TLE** — one row, no component rows.
  **Music and Arts**, **PE and Health** and the **MAPEH** average are exactly as before.
* **Term 1–3 Summary:** the EPP/TLE column sits beside that term's two components (Term 1 ICT + AFA ·
  Term 2 ICT + FCS · Term 3 ICT + IA). **Final Grade Summary:** the EPP/TLE block (T1, T2, T3, Final)
  followed by a column per component — `T1 ICT · T1 AFA · T2 ICT · T2 FCS · T3 ICT · T3 IA` — so you can
  see every component behind the single EPP/TLE grade that goes to the SF9.
* Component columns appear for **Grades 4–10** only (Grades 1–3 have no EPP/TLE), and they never leak into
  the SF9 or the Temporary Grade Slip.
* Excel follows: the component columns and values export and re-import (a component grade typed on
  a summary page comes back to that same cell).

## 5. Final grades — a guarded editing window (“override”)

* You can adjust a final grade inside a **time-boxed window** (1, 5, 10, 30 or 60 minutes) that opens
  with a warning explaining what it will do.
* The app **back-solves the class-record scores** so the records stay consistent, and it **never pushes a
  cell above the Highest Possible Score**.
* Touched cells are marked **light green**; you can **Hide/Show** the marks and **Revert** any entry from
  the log panel.
* Changes apply **instantly** — every grade page updates without switching pages.

### 5b. “Override all subject areas” — the whole term in one import

| | |
|---|---|
| **Why** | A learner's grades often come from somewhere else — a paper record, a tracker, a spreadsheet. Re-typing them area by area, learner by learner, invites mistakes. |
| **How** | On **Term 1–3 Summary** or **Final Grade Summary**, press **“Override all subject areas…”**, choose a window (1–60 minutes), then use **Import Excel**. |

* Export the page first (**Export Excel**), edit the **grade columns** in real Excel (any learner, any
  learning area — Filipino, Math, MAPEH, EPP/TLE, the components…), then import it back inside the window.
* Every grade in the file is written into **that learning area's class record**, not just the summary
  cell: the app **back-solves the Written Works / Performance Tasks / Examinations** of that class record
  so the record, the Term Summary and the Final Grade Summary all agree again — and it **never pushes a
  score above its Highest Possible Score**.
* **MAPEH and EPP/TLE are handled as averages:** a value placed on MAPEH goes into both Music and Arts
  and PE and Health; a value placed on EPP/TLE (or on a component) lands on the component(s) of that term.
* Each adjusted class-record cell, summary cell and Final-Grade-Summary column turns **light green**, and
  the **Hide / Show adjusted cells** button controls that colour everywhere.
* The import ends with a **report**: what was applied, what was already the same, and what was skipped
  (e.g. no class record for that area in this section) — with **“Revert this import”** to undo the whole
  batch in one click.
* **Outside the window** the same workbook still restores data as a backup (scores, attendance), but the
  grade columns are ignored — the app tells you nothing was applied. Grades only move inside the window.
* The window is skipped for **Grade 1** (there the app uses A–E level remarks, not numeric grades).

---

## 6. Printing & paper (all pages)

* **Top-anchored and centred** — content starts at the top margin and is centred across the width (it used
  to float in the middle of the paper).
* **0.25 in (≈6 mm) margins** on all four sides for the Grade Slip and the Attendance Record.
* **Signatories**: 10 pt names / 8 pt positions on every page.
* **Automatic file names** for both Excel and Print / Save-as-PDF:
  `2026-09-15-07-22 7-Rizal Mathematics Grade Slip` (date-time, grade-section, subject, page).
* **Only the page you are on prints** — the print preview used to be able to print the whole app
  (dozens of pages).
* Grade-1 SF9 and temporary grade slip cards now fit the paper on **A4, short bond and folio** — no clipped
  lines (the short-bond overflow is gone).

---

## 7. Smaller improvements users notice

* **Smaller footer credit**, and a **Setup → Footer** card to show/hide it and write your own text.
* **Column labels fit**: `FIRST TERM`, `SECOND TERM`, `THIRD TERM`, `FINAL GRADES`, `ATTENDANCE RECORD`
  auto-shrink instead of being cut off.
* **Descriptor columns** added to the Term Summaries and the Final Grade Summary
  (Advancing / Benchmarking / Connecting / Developing / Emerging), computed from each learner's average.
* **Legends now count for you**: every grades legend shows **No. of Students** and **%** for that
  reporting context, and updates as you type.
* **Fresh demo data for Grades 4–10** (Setup → *Load demo*): each demo now carries the EPP/TLE component
  class records (ICT / AFA / FCS / IA) with ICT running through Terms 1–3, and the demo opens on the
  EPP/TLE class record so you can see the composite straight away. Term 1–3 records, Term Summaries,
  Final Grades and the Final Grade Summary all agree — try **Load demo → Grade 4** or **Grade 7**.
* **Runs fully offline** — no internet connection needed, and no background “ping” anywhere in the file.

---

## 8. Version trail (how to tell the builds apart)

*Same table as the update log at the top of this document — kept here so the versions are in one line when you print it.*

| Date (PH) | Build / version | What changed | Size | md5 (first 8) |
|---|---|---|---|---|
| **9 Sept 2026 · 16:13** | `1.202609091613` — **your starting point** | Round 8: SF9/TGS revert + the first modern `.xlsx` export/import | 1,107,580 B | `3f8b90f7` |
| **10 Sept 2026 · 12:34** | `1.202609101234` (Round 9) | Smaller footer + Setup footer controls · automatic file names · top-anchored, centred printing · header autofit · descriptor columns · legend counts | 1,127,807 B | `9dec9cc7` |
| **14 Sept 2026** | `1.202609140000` — first build of the living line | **Excel overhaul:** page-mirror workbook with the hidden `ECLASS+ Sync` sheet, real importer, final-grade override window, 0.25 in margins, slip / margin / signatory work | — | — |
| **14 Sept 2026** | same file name, revised in place | **“Can’t be opened in Excel” — root cause found and fixed** (the worksheet is written in the exact order Excel requires; checked against the ECMA-376 schemas) | 1,293,582 B | `a9bc5853` |
| **14–15 Sept 2026** | same file name | **“Columns not aligned / import changes nothing” fixed** — the legend edges no longer split the grid, and an edited workbook imports back into the right cells | 1,296,249 B | `9d8f3536` |
| **15 Sept 2026** | same file name (Round 13) | Grade-1 records show letters **A–E** (never 0) · **four grade slips per page** with equal margins · perfect Excel round trip · correct paper on every page | 1,301,152 B | `aa198cf3` |
| **15 Sept 2026** | **Version 2.2.0 · Build 20260915** (Round 14) | **EPP and TLE become composite subjects** — ICT + AFA in Term 1, ICT + FCS in Term 2, ICT + IA in Term 3; EPP for Grades 4–6, TLE for Grades 7–10 | 1,326,026 B | `161f85f4` |
| **15 Sept 2026** | **Version 2.2.0 · Build 20260915** (Round 15) | Grade-1 remarks in plain, varied words · **EPP/TLE component columns** on the Term and Final summaries (never on the SF9/TGS) · **“Override all subject areas”** (import a Term Summary workbook and every learning area’s class record follows) · refreshed demo data incl. Grade 4 · Grade-1 Term Summary trimmed to the table + signatories | 1,367,839 B | `6cb4ecff` |
| **16 Sept 2026** — today | **Version 2.3.0 · Build 20260916** (Round 16) | **Grade-1 descriptions are now editable:** click **What Your Child Can Do** or **What Your Child Is Learning To Improve** on the Term 1–3 Summary, the SF9 or the TGS and write your own words — the same text appears on all three, per learner and per term; marked light green like an overridden grade; **Restore automatic text** (in the editor) or **Clear edited descriptions (n)** (summary toolbar) puts the generated wording back; up to 2,000 characters; saved with the class and carried by the JSON backup, keyed by LRN so the words follow the child across the five Grade-1 area records | **1,387,491 B** | `39eb516b` |

All builds from the second line on use the same file name, `ECLASS+ version 1.202609140000.html`,
and are revised in place — so use the size/md5 (or the on-screen build line under **Setup**) to tell
them apart.

---

## 9. Quick self-check (5 minutes)

1. **Excel:** open a class record → **Export** → open the file in Excel. No repair warning; every score
   sits under its own activity. Change one score, save, then **Import Excel** in the app — the new value
   appears.
2. **Grade slip:** Grades 2–10 → **Grade Slip** → Print. Four slips per page with the same thin white band
   on every side and between them.
3. **Grade 1:** type `A B C D E` into a grade-1 record cell → the cell shows the letter (not 0), and the
   letters survive clicking away.
4. **EPP/TLE:** open a Grade 7 class → **Setup → ＋ Add EPP/TLE components** → encode TLE-ICT and
   TLE-AFA → the Term 1 Summary shows **TLE = their average**, and the SF9 shows one row named
   **TLE** (Music and Arts and PE and Health still listed).
5. **Override all subject areas:** Term 1 Summary → **Export Excel** → change two or three grades in
   the workbook → back in the app press **“Override all subject areas…”** → pick 5 minutes →
   **Import Excel** → every edited area's class record follows the file, the cells turn light green
   and the report lists what changed (**Revert this import** undoes it).
6. **Grade-1 descriptions:** open a Grade-1 class → **Term 1–3 Summary** → click a
   description cell → replace the wording → **Save changes**. It turns light green and the
   same words appear on the SF9 and the TGS of that term (**Restore automatic text** brings
   the generated wording back).
