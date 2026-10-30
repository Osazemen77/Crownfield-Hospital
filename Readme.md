[README_First.md](https://github.com/user-attachments/files/34199952/README_First.md)
# CPU4103 – Blessing & Stelian Working Draft Package

**Important:** These are teaching-based *drafts*, not submission-ready proof of completed student work. Replace every bracketed placeholder, check the current official Moodle summative brief and use each student's authentic contributions and executed outputs.

## Files
- Blessing_CPU4103_Individual_Presentation_DRAFT.pptx — editable presentation with presenter notes.
- Stelian_CPU4103_Individual_Presentation_DRAFT.pptx — different individual emphasis; editable and with notes.
- Blessing_CPU4103_Individual_Report_DRAFT.docx — structured individual written report draft.
- Stelian_CPU4103_Individual_Report_DRAFT.docx — structured individual written report draft.
- SHARED_Book_Orders_Setup_Example.sql — runnable illustrative MySQL 8 database schema + 10 orders, 12 books, 10 publishers, 20 line items.
- Blessing_Individual_Queries_Example.sql — Blessing-specific SQL demonstration.
- Stelian_Individual_Queries_Example.sql — Stelian-specific SQL demonstration.
- OPTIONAL_Security_Learning_Notes.sql — optional privilege/hashing teaching snippets; uses no passwords.
- Submission_Checklist.md — what to replace and confirm.

## Basis and known assessment facts
- Module: CPU4103 / Introduction to Databases.
- Week 1 Session 1 teaching slides: group design/implementation, but individual report worth 50% and recorded presentation worth 50%.
- Week 4 Session 2 teaching slide: conceptual, logical, physical design, implementation, individual manipulation/validation, database protection/security.
- Week 3 Session 1 teaching slide excerpt: Part B implementation via MySQL with minimum 10 example records per main table.
- Workshop 2: Book Order example UNF→3NF, with Orders, Order Items, Book, Publisher.
- Formative 3: create tables with PK/FK and data types; INSERT, SELECT, WHERE and JOIN evidence; this is a *formative* requirement, not proof of exact summative requirements.
- University GitHub upload guide: upload SQL and include functioning repository link in report.
- A Week 5 Session 2 teaching slide lists a deadline of 6 July 2026; this is now in the past and MUST NOT be assumed to be a current submission deadline.

## How to use the SQL
1. Open local MySQL Workbench and connect to an available MySQL 8 instance.
2. Open the SHARED_...sql file; inspect first. It resets ONLY `cpu4103_book_orders_demo` and deletes demo tables under this schema; use only for this artificial example.
3. Run the full setup and count queries; confirm counts.
4. Open the corresponding individual query file. Run each separately and photograph genuine results.
5. Open each PPT and report; replace all screenshots, authorship claims, personal reflections and placeholder IDs with real evidence.
6. Upload SQL code to each permitted GitHub repo. Do not upload database credentials, private student data or any backup containing real PII.
7. Record each student presenting their own work and interpretation; verify Moodle's current required format, recording length, word count and deadline.

## Important schema choice
Order totals are calculated in `v_order_totals` instead of redundantly stored in `orders`. `unit_price` is kept on the order line to preserve the historical price even if `books.current_price` changes. Book authors are simplified to a single `author_name` field; an enhanced model can use Book_Author if needed.
