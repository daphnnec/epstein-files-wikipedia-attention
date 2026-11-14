# Data

The clean/ folder holds the full cleaned data, which is small. The raw email archive and raw API responses are not committed; see the main README for why.

## people.csv

One row per person.

| Field | Meaning |
|---|---|
| person | The person's name |
| wiki_title | Current title of their English Wikipedia article |
| email_mentions | Emails in the archive (excluding the two hacked sets and promotional mail) whose subject, participants, or body match the person's search pattern |
| epstein_mentions_before | Times "Epstein" appears in the article on November 11, 2025, the day before the first release |
| epstein_mentions_mar2026 | Times "Epstein" appears in the article on March 1, 2026 |
| epstein_mentions_now | Times "Epstein" appears in the article on the collection date |
| epstein_heading_now | True if the current article has a section heading containing "Epstein" |
| article_bytes_now | Size of the current article's text in bytes |

## pageviews_daily.csv

One row per person per day, from August 1, 2025 to two days before collection.

| Field | Meaning |
|---|---|
| person | The person's name |
| date | Calendar date (UTC) |
| views | Views by human readers that day across desktop and mobile, summing old and new titles for renamed articles. Days the API did not report are filled with 0 |
