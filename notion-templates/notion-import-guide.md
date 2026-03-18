# Developer OS — Notion Import & Setup Guide

This guide walks you through importing each CSV file into Notion, configuring the views, and preparing the workspace for sharing on Gumroad.

---

## Before You Start

- All CSV files are UTF-8 encoded and ready to import.
- Each CSV becomes one Notion database.
- Plan 30–45 minutes for the full setup of all three templates.
- Use a dedicated Notion page as a parent container for each template group (e.g. "Tech Interview Tracker", "Side Project Dashboard", "Developer Learning Log").

---

## Step 1: Import a CSV into Notion

1. Open Notion and navigate to the page where you want to create the database.
2. Click the `+` button in the left sidebar (or type `/` in the page body).
3. Select **Import** from the menu.
4. Choose **CSV**.
5. Select the CSV file from your local machine.
6. Notion creates a new database with all columns auto-detected as Text properties.
7. Immediately after import, rename the page to match the database name below.

Repeat this step for every CSV file in the bundle.

---

## Step 2: Fix Property Types After Import

Notion imports all columns as plain text. Change them to the correct types.

To change a property type: click the column header > click the property type name > select the new type.

### Template 1: Tech Interview Tracker

**t1-leetcode-kanban** (rename to: LeetCode Kanban)
| Property | Change To |
|---|---|
| Difficulty | Select |
| Status | Select |
| Pattern | Select |
| Review Date | Date |

**t1-company-pipeline** (rename to: Company Pipeline)
| Property | Change To |
|---|---|
| Status | Select |
| Applied Date | Date |

**t1-problem-notes** (rename to: Problem Notes)
| Property | Change To |
|---|---|
| Difficulty | Select |
| Review Date | Date |

**t1-interview-checklist** (rename to: Interview Checklist)
| Property | Change To |
|---|---|
| Category | Select |
| Done | Checkbox — after changing type, manually tick rows where value was "Yes" |

### Template 2: Side Project Dashboard

**t2-sprint-kanban** (rename to: Sprint Board)
| Property | Change To |
|---|---|
| Status | Select |
| Priority | Select |

**t2-deploy-checklist** (rename to: Deploy Checklist)
| Property | Change To |
|---|---|
| Category | Select |
| Done | Checkbox — after changing type, manually tick rows where value was "Yes" |

**t2-feature-roadmap** (rename to: Feature Roadmap)
| Property | Change To |
|---|---|
| Status | Select |
| Impact | Select |
| Effort | Select |

**t2-bug-tracker** (rename to: Bug Tracker)
| Property | Change To |
|---|---|
| Severity | Select |
| Status | Select |
| Found Date | Date |

### Template 3: Developer Learning Log

**t3-book-notes** (rename to: Book Notes)
| Property | Change To |
|---|---|
| Status | Select |
| Date Read | Date |
| Rating | Number (set format to "Number") |

**t3-weekly-retro** (rename to: Weekly Retro)
| Property | Change To |
|---|---|
| Week Of | Date |
| Energy Level | Number |

**t3-til-log** (rename to: TIL Log)
| Property | Change To |
|---|---|
| Date | Date |
| Category | Select |

**t3-resource-library** (rename to: Resource Library)
| Property | Change To |
|---|---|
| Type | Select |
| Status | Select |
| Rating | Number |

---

## Step 3: Add Select Option Colors

After changing columns to Select type, add colors to make the views scannable.

Click any cell in a Select column > click the option name > pick a color.

Recommended color scheme:

**Status properties:**
- Todo / Unread / Idea → Gray
- In Progress / Reading / Planned → Blue
- Done / Completed / Shipped → Green
- Needs Review → Yellow
- Rejected / Dropped / Wontfix → Red
- Applied → Purple
- Phone Screen / Technical / Onsite / Offer → Orange

**Priority / Severity:**
- High / Critical → Red
- Medium / High → Orange
- Low → Gray

**Difficulty:**
- Easy → Green
- Medium → Orange
- Hard → Red

---

## Step 4: Add Views to Each Database

Switch from the default Table view by clicking **+ Add a view** at the top of each database.

### LeetCode Kanban
1. **Table view** (default) — rename to "All Problems"
2. **Board view** — rename to "Kanban", group by: **Status**
3. **Gallery view** — rename to "Review Queue", filter: Status = "Needs Review"
4. **Table view** — rename to "By Pattern", sort by: Pattern (A → Z)

### Company Pipeline
1. **Table view** (default) — rename to "All Companies"
2. **Board view** — rename to "Pipeline", group by: **Status**
3. **Timeline view** — rename to "Timeline", start date: Applied Date

### Problem Notes
1. **Table view** (default) — rename to "All Notes"
2. **Gallery view** — rename to "Review", filter: Review Date is within the next 7 days

### Interview Checklist
1. **Table view** (default) — rename to "All Items"
2. **Board view** — rename to "By Company", group by: **Company**
3. **Table view** — rename to "Pending", filter: Done is unchecked

### Sprint Board
1. **Table view** (default) — rename to "Backlog"
2. **Board view** — rename to "Sprint Board", group by: **Status**
3. **Board view** — rename to "By Priority", group by: **Priority**

### Deploy Checklist
1. **Table view** (default) — rename to "All Items"
2. **Board view** — rename to "By Category", group by: **Category**
3. **Table view** — rename to "Pending", filter: Done is unchecked

### Feature Roadmap
1. **Table view** (default) — rename to "All Features"
2. **Board view** — rename to "Roadmap", group by: **Status**
3. **Table view** — rename to "High Impact", filter: Impact = "High", sort by: Effort (A → Z)

### Bug Tracker
1. **Table view** (default) — rename to "All Bugs"
2. **Board view** — rename to "By Status", group by: **Status**
3. **Table view** — rename to "Open", filter: Status = "Open" or "In Progress", sort by: Severity

### Book Notes
1. **Table view** (default) — rename to "All Notes"
2. **Gallery view** — rename to "By Book", group by: **Book Title**
3. **Table view** — rename to "Action Items", filter: Action Item is not empty

### Weekly Retro
1. **Table view** (default) — rename to "All Retros"
2. Sort by Week Of (newest first) by default.

### TIL Log
1. **Table view** (default) — rename to "All TILs"
2. **Board view** — rename to "By Category", group by: **Category**
3. **Gallery view** — rename to "Recent", sort by: Date (newest first)

### Resource Library
1. **Table view** (default) — rename to "All Resources"
2. **Board view** — rename to "By Status", group by: **Status**
3. **Table view** — rename to "Unread", filter: Status = "Unread"
4. **Gallery view** — rename to "Top Picks", filter: Rating = 5

---

## Step 5: Create the Parent Template Pages

For each template, create a parent Notion page that contains all related databases. This is the page you will share with customers.

### Recommended page structure:

```
Developer OS (root page)
├── Tech Interview Tracker
│   ├── [description callout block]
│   ├── LeetCode Kanban
│   ├── Company Pipeline
│   ├── Problem Notes
│   └── Interview Checklist
├── Side Project Dashboard
│   ├── [description callout block]
│   ├── Sprint Board
│   ├── Deploy Checklist
│   ├── Feature Roadmap
│   └── Bug Tracker
└── Developer Learning Log
    ├── [description callout block]
    ├── Book Notes
    ├── Weekly Retro
    ├── TIL Log
    └── Resource Library
```

### Description callout blocks (copy-paste into each template page):

**Tech Interview Tracker:**
> Track every problem, every company, and every interview step in one place. Use the LeetCode Kanban to manage your practice queue, the Company Pipeline to track applications, and the Interview Checklist to make sure you're fully prepared before every round.

**Side Project Dashboard:**
> Ship your side project faster with a clear sprint board, a production-ready deploy checklist, a feature roadmap to keep scope in check, and a bug tracker so nothing falls through the cracks.

**Developer Learning Log:**
> Build a compounding knowledge base. Log what you learn every day, capture key insights from books chapter by chapter, run weekly retrospectives to improve your process, and save the best resources for easy retrieval later.

---

## Step 6: Set Up Template Buttons (Optional but Recommended)

For databases like Interview Checklist, you can create a template button so users can generate a fresh checklist for each new company.

1. Open the database in full-page view.
2. Click the blue **New** button dropdown arrow.
3. Click **+ New template**.
4. Fill in the default properties (e.g. set Done to unchecked, set all Category values).
5. Name the template "New Company Checklist".
6. Users can now click the dropdown and pick this template each time they start a new application.

Repeat for Sprint Board (template: "New Sprint Task") and Weekly Retro (template: "New Week").

---

## Step 7: Publish to Web and Get the Share Link

This is required before you can sell the template on Gumroad.

1. Open the **root parent page** ("Developer OS" or each individual template page).
2. Click **Share** in the top-right corner.
3. Toggle **Share to web** to ON.
4. Make sure **Allow duplicate as template** is toggled ON. This is the key setting — it adds a "Duplicate" button to the top of your shared page so buyers can copy the entire template to their own workspace.
5. (Optional) Set **Search engine indexing** to OFF to keep the page from showing up in Google before launch.
6. Copy the share link.

The link looks like:
`https://www.notion.so/Your-Template-Name-abc123def456...`

---

## Step 8: List on Gumroad

1. Go to [gumroad.com](https://gumroad.com) and create a new product.
2. Set the product type to **Digital product**.
3. In the product description, paste your sales copy and screenshots of the template views.
4. In the **Content** section, add a text block with your Notion share link (the one from Step 7). This is what the buyer receives after purchase.
5. Optionally attach the CSV files as a download as well, in case buyers want to set up manually.
6. Set your price and publish.

**Tip:** Gumroad lets you set a "pay what you want" minimum. Starting at $0 with a suggested price of $9–$19 drives more initial volume and social proof.

---

## Troubleshooting

**CSV imported but columns are in wrong order.**
Notion respects the column order in the CSV. The Name column must be first — Notion uses it as the page title. All CSVs in this bundle are already formatted correctly.

**Select options are imported as plain text and I can't pick colors.**
This is expected. After import, click the property header, change the type to "Select", and Notion will convert all existing text values into select options automatically. Then add colors.

**Date columns show as text after import.**
Change the property type to Date. Notion will parse YYYY-MM-DD format automatically.

**The "Allow duplicate as template" toggle is not visible.**
This option only appears after you toggle "Share to web" on first. Make sure the page is published before looking for this setting.

**I want to link databases across templates (e.g. link a LeetCode problem to a company).**
Use a **Relation** property. Add a new property to one database, set the type to Relation, and select the other database. This is an advanced step not required for the initial setup but useful for power users.
