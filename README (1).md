# B2B Lead Generator & Qualifier – Phase 1

## What this is

This is the first phase of a B2B lead generation and qualification system built around rule-based, deterministic logic — no AI scoring, no black-box predictions, just clean and repeatable workflows.

The whole point is to give sales teams a reliable way to build verified, export-ready lead lists without having to clean up a mess of duplicates and bad emails afterward.


## What it actually does

- Lets you define an Ideal Customer Profile (ICP) that fits your target market
- Filters your company list down to only the ones that match
- Picks out the right decision-makers using job title mapping (no guesswork)
- Checks emails for syntax issues, bad domains, and disposable addresses
- Strips out duplicate contacts before anything gets exported
- Spits out a clean CSV that's ready to hand off to your sales team


## What's deliberately left out

This phase doesn't include:

- AI or ML-based lead scoring
- Intent signals or detection
- Outreach or sequencing tools
- Web scraping
- CRM automation

These are all on the roadmap for later phases — keeping Phase 1 focused made it easier to build, test, and trust.

## Project structure

b2b_lead_engine/
├── data/
│   ├── companies.csv
│   └── contacts.csv
├── app/
│   ├── icp.py
│   ├── company_filter.py
│   ├── role_normalizer.py
│   ├── verifier.py
│   ├── deduplicator.py
│   ├── exporter.py
│   └── main.py
├── requirements.txt
└── README.md


## How the pipeline runs

1. You define your ICP — industry, location, company size, and type.
2. The system filters your company list against those criteria.
3. Contacts tied to matching companies get pulled in.
4. Job titles get normalized into standard role buckets so you're not comparing apples to oranges.
5. Emails go through a verification pass — syntax, domain, and disposable address checks.
6. Duplicates are removed.
7. A final CSV gets generated, ready for sales use.


## Running it

Install dependencies:

```bash
pip install -r requirements.txt
```

Then kick off the pipeline:

```bash
cd app
python main.py

## Output

You'll get a file called `final_export.csv` — verified, deduplicated contacts with metadata included, ready to go.
