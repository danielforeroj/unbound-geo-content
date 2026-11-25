# Number check

The last step of every deliverable. It is how the skill refuses to invent a number.

## The rule

List every number in the deliverable and the report line it came from. A number with no line is deleted, and the sentence is rewritten so it works without it.

"Number" means any figure. Counts, percentages, ratings, review totals, dates, dollar amounts, times, "four things", "5 questions", "10 times". Ordinal labels used only as list markers (1, 2, 3) and slide numbers are not data, so they are not listed. A count the script says out loud ("four lines") is data, so it is listed.

## Before you start

Number the report lines as R1, R2, R3 as you read. If the user's report already has line numbers or row labels, use those. If it is a screenshot or a PDF, say "R1 is the first stat on page 1" and keep a consistent scheme. Never cite a line you did not read.

## The format

A markdown table, placed at the end of the deliverable.

| Number | Where it appears | Report line | Source text in report |
|---|---|---|---|

- **Number.** Exactly as written in the deliverable.
- **Where it appears.** Scene, slide or tweet number.
- **Report line.** The R# the fact came from.
- **Source text in report.** A short quote or paraphrase of what the report says, so a human can verify in 5 seconds.

Add a final status row or line. "All numbers traced. 0 deleted." or "2 deleted, see notes."

## Matching rules

- **Same unit.** If the report says "9 of 10", you cannot write "90 percent" without the report giving the percent. If the report gives only the count, write the count.
- **A percentage only next to its count.** "6 of 50 (12%)", never "12%" alone.
- **No arithmetic the report did not do,** unless it is plain and shown. If you add or subtract, mark the row "derived" and show the sum. Better to avoid derived numbers. Prefer the report's own figures.
- **Engine and date.** Every row in a caption table belongs to a report that states an engine and a date. If it does not, stop and ask.
- **Rounding.** Do not round. "2,194" stays "2,194".
- **Words count too.** "Nine of ten" is the same number as "9 of 10". List it once.

## What to do with a number that fails

1. Try to find it in the report under a different wording. Maybe it exists in a table you skimmed.
2. If it does not exist, delete the number.
3. Rewrite the sentence. "Most clinics skip this" becomes "Another clinic did this and was cited". A claim without a number is fine. A claim with a made up number is not.
4. Mention the deletion in one line under the table.

## Worked example

Report excerpt, from `examples/sample-report.md`.

- R1. Method. 5 questions, 10 runs each, fresh chats, 50 answers. ChatGPT, 2026-11-10.
- R3. Question 2, emergency dentist open Saturday. This clinic 0 of 10. Another clinic 9 of 10.
- R8. This clinic 312 reviews, 4.9 stars. Another clinic 2,194 reviews, 4.8 stars.
- R10. The other clinic's emergency page was cited in 7 of 10 answers to question 2.

Script line. "This clinic has a 4.9 star rating. ChatGPT named it in 0 of 10 answers for a Saturday emergency dentist. Why?"

| Number | Where it appears | Report line | Source text in report |
|---|---|---|---|
| 4.9 | Scene 1 | R8 | "312 reviews, 4.9 stars" |
| 0 of 10 | Scene 1 | R3 | "This clinic 0 of 10" |

A draft line that fails. "Most clinics lose about 40 percent of emergency calls." No line in the report, so it is deleted. The sentence becomes "Another clinic was named in 9 of 10." which passes with R3.

Status. All numbers traced. 1 deleted ("about 40 percent", no report line).

## Where the table goes

- Script. After the last scene.
- Carousel. After the closing slide.
- Caption and thread. After the last tweet, with a row for the caption lines and each tweet.

Each deliverable gets its own table. Do not combine them. The point is to check each piece on its own.

## Final scan

After building the table, scan the deliverable once more for any numeral or number word you did not list. Years in dates count. "Saturday" does not. "Four" does. Fix what you find.
