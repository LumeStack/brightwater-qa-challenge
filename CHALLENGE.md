**From:** Alex Morgan, Engineering Manager, Brightwater Compliance Cloud
**To:** Bruna Ferreira
**Subject:** Brightwater Compliance Cloud | QA Automation Engineer | Stage 2: Technical Challenge

> Fictional company and exercise created for interview practice. Any resemblance to a real company is a coincidence.

---

Hi Bruna,

Thank you for your time in the first conversation. The team liked your background, so I would like to move you to the technical stage.

This stage is a small, realistic challenge. It is not a trick test. It mirrors what you would do in your first weeks in our squad: receive a ticket, work out what it means, decide what to automate, and tell us what you find.

**Time box:** about 4 to 5 hours of work, delivered within **72 hours** after you receive the application link.
**Language:** everything in English (code, commit messages, written answers).

## The ticket

You have been assigned this ticket, exactly as written:

> **BW-1427** | Story | Priority: High
> **Title:** Add discount code field to invoice payment
> **Description:** Customers should be able to enter a discount code when paying an invoice.

The feature is already deployed to our staging environment. The application is in this repository: https://github.com/LumeStack/brightwater-qa-challenge (see its README to run it).

## What we ask you to do

### Part 0: Questions first (before you write any test)
Within 24 hours of receiving this email, reply with the questions you need answered about BW-1427. Our product owner will answer them. The answers are the only source of truth for the business rules, so ask what you need. Please send your questions in one message, grouped by topic.

### Part A: Test plan (max 1 page)
Based on the answers, write a short, risk-based test plan:
- What you would test, and at which level (unit, API, UI, manual exploratory).
- What you would automate first and why.
- What you would deliberately leave manual or not test.

### Part B: Automation (Playwright with TypeScript)
Create a test project in your own GitHub repository:
- UI tests for the main payment flow with a discount code (happy path and at least two negative paths).
- API tests for the discount rules. Cover the combinations that matter, not just one example.
- A clear project structure (we expect Page Objects and fixtures) and typed code.
- Explicit assertions, no fixed waits, no hardcoded credentials or URLs, and tests that do not depend on each other. The environment has a reset endpoint described in the README.
- Tests must run with a single command and a short README explaining how.

### Part C: Bug reports
Report every defect you find, in a format a developer can act on (title, steps to reproduce, expected result, actual result, severity, evidence). Quality matters more than quantity. Mark which bugs you found through the UI and which through the API, and which you could prove with an automated test.

### Part D: Three short written answers (max 150 words each)
1. The UI of this application has no stable CSS classes. Explain why selectors based on CSS classes or XPath are fragile, what you used instead, and what you would ask the development team to change.
2. The release is tomorrow and you have 4 hours left for this feature. What exactly do you do, in order?
3. Which AI tools did you use, for what, and how did you verify their output?

## About AI tools
You may use AI assistants. We care about your judgement more than about typing speed. Tell us what you used, and be ready to explain every line you submit.

## Next step
If we move forward, we will schedule a 30-minute call where you walk us through your repository, your bug reports and your decisions. You will be asked "why" a lot, so choose what you submit carefully.

## How to submit
Reply to this email with:
1. The link to your repository (public, or private with access granted to `brightwater-reviewer`).
2. Your test plan and bug reports (inside the repository in a `docs/` folder is fine).
3. Your written answers (Part D) in the same folder or in the email body.

You do not need to fix or change the application. Please do not look for or rely on its source code. Treat it as a black box, like a staging environment you do not own.

Good luck, and please reply if anything is unclear about the logistics. Questions about the **feature** go in Part 0.

Best regards,
Alex Morgan
Engineering Manager | Brightwater Compliance Cloud
