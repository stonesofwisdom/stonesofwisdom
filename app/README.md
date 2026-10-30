# Family Ledger

A shared family budget, in naira, for recording income and expenses month by month.

Live app: https://claude.ai/artifact/KELEGq5b7SUEzZHdqanxkW

`family-ledger.html` is the source of the page published at that link. The data
(entries, budgets, goals, categories) lives in the page's shared database on
claude.ai, not in this repository, so it is kept when the page is updated.

## What it does

- **This month**: money in, money out, budget left and amount kept, each compared with last month.
  A budget table per category shows spent, remaining and last month's figure.
- **Recurring items**: list fixed bills and salaries once; each month, one tap adds them.
- **Budget help**: copy last month's budget, or fill empty budgets from the last three months' average.
- **Next month at a glance**: likely spending and income, from recurring items plus recent averages.
- **Transactions**: every entry with filters, search, and who recorded it.
- **Trends**: 12-month income vs spending chart, six-month category history, year-on-year comparison.
- **Savings goals**: target, progress and the monthly amount needed to reach it on time.
- **Export**: download every entry and budget as a CSV file for Excel or a backup.

## Data layout

| Path | Contents |
| --- | --- |
| `settings/main` | categories, income sources, recurring items |
| `months/<YYYY-MM>` | budgets per category, expected income, notes |
| `months/<YYYY-MM>/tx/<id>` | one income or expense entry |
| `goals/<id>` | a savings goal |
