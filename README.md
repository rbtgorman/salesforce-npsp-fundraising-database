# Mock Salesforce NPSP Fundraising Database

Built a nonprofit fundraising database in Salesforce NPSP. Imported a bunch of data, broke a bunch of things, fixed them, and made some reports.

## What's In Here

- 224 contacts, 12 organizations
- $1.35M in donations (individual gifts, foundation grants, corporate partnerships)
- 14 recurring donors
- 7 reports + dashboard

## Things That Broke (and How I Fixed Them)

| Problem | Fix |
|---------|-----|
| Fields wouldn't auto-map | Use labels (`Account1 Name`) not API names (`npsp__Account1_Name__c`) |
| "Invalid Donation Donor" error | Add `Donation Donor` column = `Account1` for orgs, `Contact1` for people |
| Batch showed 0 records | Add `NPSP Data Import Batch` column with exact batch name |
| Recurring donations failed | Enable Enhanced Recurring Donations in NPSP Settings first |

## CSV Template That Works

```csv
Account1 Name,Donation Amount,Donation Date,Donation Stage,Donation Donor,NPSP Data Import Batch
Some Foundation,50000,2024-01-15,Closed Won,Account1,Your Batch Name Here
```

The key fields everyone forgets: `Donation Donor` and `NPSP Data Import Batch`. You're welcome.

## Reports

- Top Donors by Lifetime Giving
- Campaign Performance
- Monthly Donation Trends
- Recurring Donor Analysis

## Screenshots

*Coming soon*

---

Portfolio project for Salesforce admin skills. Steal the CSV templates if you need them.# salesforce-npsp-fundraising-database
