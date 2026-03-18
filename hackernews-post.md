# Developer OS — Hacker News "Show HN" Post

> HN 문화 특성상 과장이나 마케팅 언어는 즉시 다운보팅됩니다.
> 제목은 정직하고 구체적으로, 본문은 기술적 결정 근거와 실제 사용 경험 중심으로.
> 링크는 제목에 하나만. 본문에 반복하지 말 것.
> 런치 당일 오전 9-10시 (EST 기준) 제출 권장 — HN 트래픽 피크 시간대.

---

## TITLE

Show HN: Developer OS – Notion template bundle for tech interviews, side projects, and learning logs

---

## BODY

I built this for myself after spending too much time rebuilding the same Notion setups across three different job searches.

The bundle has three templates:

**Tech Interview Tracker** (free)
- LeetCode kanban organized by difficulty, with a "Needs Review" column for spaced repetition
- Company application pipeline with per-company interview prep checklists
- Problem notes DB with pattern tagging (two pointers, BFS, DP, etc.) so you can filter by pattern during late-stage prep

The pattern tagging was the thing I didn't expect to be useful — but being able to pull up every sliding window problem I'd ever solved, with my own notes, turned out to matter a lot.

**Side Project Dashboard** (paid bundle)
- Sprint kanban linked to a Sprint DB via relation — this is what makes it a real sprint system vs a to-do list with columns
- Pre-deploy checklist covering the things I consistently forget under launch pressure: error tracking, rate limiting on auth endpoints, og:image, analytics firing correctly
- Feature roadmap with impact and effort scoring to stop me from building clever things that don't matter

**Developer Learning Log** (paid bundle)
- Book notes DB with chapter-level breakdowns and action items
- TIL log (one entry per day, searchable by category)
- Weekly retrospective with four fixed prompts — kept minimal so I'd actually use it

The database structure for anyone who wants to see it before buying:

The interview tracker uses two main DBs (Problems and Companies) with the Problems DB having a "Pattern" multi-select that's been the most useful property I added.

The side project dashboard uses a Tasks DB related to a Sprint DB. The rollup on the Sprint DB (count of done tasks vs total) is what makes sprint progress visible without manual tracking.

The learning log uses a deliberately minimal TIL DB — I tried adding more properties and stopped using it, so I removed them.

Launch price is $39 for the full bundle (will go to $49 after two weeks). The interview tracker is free.

Happy to discuss the database structure or any design decisions.

---

## EXPECTED COMMENTS AND PREPARED RESPONSES

**"Why not just use a spreadsheet?"**
> You can. The value here is the relational DB structure — linking tasks to sprints, scheduling problem reviews, filtering by pattern. A spreadsheet can approximate it but the relations between databases are what make the sprint system work without manual tracking. If a spreadsheet works for you, use a spreadsheet.

**"Why Notion? It's slow and has no offline mode."**
> Fair criticism. The offline limitation is real. I use Notion because most developers I know already have it in their workflow, and duplicating a template is a lower barrier than migrating to a new tool. If you're already using Obsidian or Logseq, adapting the structure there is probably worth the effort.

**"Why charge for a template? This is just a few database views."**
> The structure took more iteration than it looks like — the first version of the side project dashboard had 11 databases before I got it down to 3. The $39 is for the setup time saved and the iteration cost. The interview tracker is free if you want to evaluate the approach first.

**"You could build this yourself in an afternoon."**
> Yes. I'm not arguing otherwise. The template is for people who'd rather spend that afternoon on something else.

**"What's your revenue after launch?"**
> I'll share an update in the comments after the first week if there's interest.

---

## POST-LAUNCH UPDATE TEMPLATE

> Use this as a follow-up comment 48-72 hours after the original post if it gets traction.

Update after 48 hours:

[X] downloads of the free interview tracker
[X] paid bundle sales
Most common feedback so far: [fill in]
Something I'm changing based on feedback: [fill in]

Thanks to everyone who tried it and left comments. The [specific thing] question from [username] made me rethink [specific design decision].
