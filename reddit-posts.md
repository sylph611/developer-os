# Developer OS — Reddit Posts

각 서브레딧의 문화와 규칙에 맞게 맞춤 작성되었습니다.
- r/cscareerquestions: 커리어 실용 팁 중심, 자기 경험 공유 형식
- r/webdev: 제작 과정 + 기술적 결정 중심
- r/Notion: Notion 사용자 커뮤니티, 구체적 구조 설명 중심

---

## POST 1 — r/cscareerquestions

**Title:**
I tracked every LeetCode problem and job application in Notion for 4 months. Here's the system (free template inside)

---

**Body:**

Last year I went through a job search while working full time. The chaos was real — I had problems in a Google Sheet, applications in another spreadsheet, prep notes in a third doc, and I still showed up to one technical interview having forgotten to research the company's tech stack.

After bombing that one, I spent a weekend building a proper system in Notion. I just kept using and refining it for the next four months. Here's what actually helped:

**The LeetCode Kanban**

Instead of a flat list, I organized problems into four columns: Not Started / In Progress / Done / Needs Review. The "Needs Review" column was the key addition — it's where problems went after I solved them once but knew I'd forget the approach. Every Sunday I'd pull 3-4 cards from that column and re-solve them cold.

**The Company Pipeline**

Applied / Screening / Technical Interview / Onsite / Offer / Rejected. Each card had the job description snippet, key points about the company's stack, and a checklist of prep steps. Before every interview, I'd open that card and run through the checklist instead of trying to remember what I needed to prep.

**The Problem Notes DB**

For every medium and hard problem I solved, I wrote down: the approach in plain English, time complexity, space complexity, and a "next review date." Nothing fancy. But being able to search "sliding window" three months later and see all the problems I'd done with that pattern was actually useful during late-stage interviews.

---

I've cleaned this up and made it available as a free Notion template if anyone wants it. No email required, just duplicate it.

[Link to free template — Tech Interview Tracker]

The full bundle also includes a side project dashboard and a learning log, but the interview tracker is free by itself.

Good luck to everyone in the current market. It's rough out there, but a system helps.

---

**Suggested flair:** Advice

---

---

## POST 2 — r/webdev

**Title:**
I've rebuilt my side project setup in Notion five times. This is the version that finally stuck — here's what changed

---

**Body:**

Every time I started a new side project, I'd spend the first hour setting up a Kanban board and convincing myself this time I'd actually maintain it. I never did. By week three the Notion page was stale and I was back to winging it.

I've been a web developer for a few years and have shipped a handful of small things. The pattern that kept killing projects wasn't technical — it was organizational. I'd lose context between sessions. I'd fix interesting bugs instead of important ones. I'd keep adding features and never actually launch.

Here's what changed when I started treating my side project setup like a system I was responsible for maintaining:

**Sprint discipline over task lists**

I moved from a flat to-do list to weekly sprints with a hard backlog. Everything that isn't in this week's sprint goes in the backlog. This sounds obvious but it took me embarrassingly long to actually implement it. The constraint forces you to decide what matters before you start coding.

**A pre-deploy checklist**

I kept shipping things and forgetting basic stuff under pressure — no error tracking set up, missing meta tags, no rate limiting on API routes. So I made a checklist. Not a long one, but specific enough to catch the things I actually forget:

- Error monitoring set up (not just console.log)
- Environment variables confirmed in prod
- Basic rate limiting on auth endpoints
- og:image and meta description set
- Analytics firing correctly
- Lighthouse score above 85

**Feature tagging by impact vs effort**

Every feature idea goes into a DB with a rough impact score and effort score. It's not scientific. But it stops me from building clever things that don't matter.

---

I've packaged this up as a Notion template for other solo devs who keep fighting the same organizational battles. The side project dashboard is part of a larger Developer OS bundle — there's also an interview tracker and a learning log.

Bundle is $39 right now (launch pricing), and the interview tracker is free if you just want to see the structure before buying.

[Gumroad link]

Happy to talk through any of the organizational decisions if anyone's curious — some of it was intentional, some of it evolved from using it badly for a few months first.

---

**Suggested flair:** Showoff Saturday (if posted on a Saturday) or Tools

---

---

## POST 3 — r/Notion

**Title:**
Built a Developer OS template bundle after 6 months of iteration — sharing the database structure that actually worked

---

**Body:**

I've been building and refining a Notion setup for developers over the past several months. Wanted to share the structure here because this community has given me a lot of ideas over the years and I figure some of you might find it useful or have thoughts on what I got wrong.

The bundle has three templates. Here's the database structure behind each one and why I made specific choices:

---

**Template 1: Tech Interview Tracker**

Two main databases:

*Problems DB*
Properties: Name, Difficulty (select: Easy/Medium/Hard), Pattern (multi-select: Two Pointers, BFS, DP, etc.), Status (select: Not Started/In Progress/Done/Needs Review), Last Solved (date), Next Review (date), Notes (text), Link (URL)

The "Pattern" multi-select was the most useful addition. Filtering by pattern during active interview prep — seeing all your BFS problems in one place — was genuinely helpful.

*Companies DB*
Properties: Company (title), Role, Status (select: Applied/Screening/Technical/Onsite/Offer/Rejected), Applied Date, Last Contact Date, Job Description (text), Tech Stack (multi-select), Prep Checklist (checkbox sub-items via toggle)

I use a board view on Status for the pipeline visualization, and a table view for tracking follow-up dates.

---

**Template 2: Side Project Dashboard**

Three databases:

*Tasks DB* — linked to a Sprint DB via relation. Each task has: Name, Status, Sprint (relation), Type (select: Feature/Bug/Chore), Priority (select), Est. Hours (number), Actual Hours (number)

*Sprint DB* — Start Date, End Date, Goal (text), Status, linked Tasks (rollup: count of done vs total)

*Features DB* — separate from tasks. Idea-stage features with Impact (1-5), Effort (1-5), Status (select: Idea/Planned/In Progress/Shipped/Dropped)

The relation between Tasks and Sprints was the thing that made this actually work as a sprint system vs a glorified to-do list.

---

**Template 3: Developer Learning Log**

*Books DB*
Properties: Title, Author, Status (select: To Read/Reading/Done), Rating (select: 1-5), Started, Finished, Key Takeaways (text), Action Items (text), Chapter Notes (sub-pages via toggle or separate linked DB)

*TIL Log* — simple. Date, What I Learned (title), Category (select), Source (URL). Kept deliberately minimal so I'd actually use it.

*Weekly Retro* — template button that creates a new page each week. Structure: What went well / What didn't go well / What I'm focusing on next week / One thing I'm proud of. Four prompts. Nothing more.

---

This is available as a free template (interview tracker) and a paid bundle ($39 launch price for all three) on Gumroad if you want to duplicate it rather than rebuild from scratch.

But honestly, even if you build your own version, I hope the DB structure gives you something to start from. The structure took a lot more iteration than I expected.

Happy to answer questions about any of the design decisions.

[Gumroad link — free tier available]

---

**Note on self-promotion:** I've shared the full database structure above, not just a product link. If this crosses into promotional territory per subreddit rules, I'm happy to remove the link and just keep the structural breakdown.

---

**Suggested flair:** Template or Share
