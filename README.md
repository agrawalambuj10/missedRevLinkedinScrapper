# Missed Revenue Detector

We operate on a success-fee recruitment model, meaning revenue is generated only when a candidate successfully joins a client company.

In some cases:
- Companies do not inform us after a candidate joins.
- Candidates join the company months later through a delayed hiring process.

Both scenarios lead to missed revenue opportunities despite the sourcing and hiring effort already being done.

Manually tracking these cases across thousands of candidates and companies was not feasible, so this tool was built to automate the detection process.

---

## How It Works

1. Scrapes employee data from a company’s LinkedIn People page.
2. Compares the scraped employee list with candidates previously shared by us.
3. Flags potential matches for review.

---

## Workflow

### Step 1 — Employee Scraping
`linkedinScrapper`

- Uses Apify APIs to scrape employee data from LinkedIn company pages.
- Extracts employee names, profile information, and LinkedIn URLs.
- Stores/exports data to Airtable for matching.

### Step 2 — Match Detection
`matchCheck`

- Compares scraped employee records against internal candidate databases/shared candidate lists.
- Detects potential matches using `publicIdentifier` comparison logic.
- Flags identified matches for further verification.

---

## Tech Stack

- Python
- JavaScript
- Apify
- Airtable
- SQL
