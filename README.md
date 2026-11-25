[![make.fun](https://make.fun/badge/u-markk-st-one-line-no-deadline-met-6adc00ce.svg)](https://make.fun/bounty/u-markk-st-one-line-no-deadline-met-6adc00ce)
[![Rank](https://make.fun/badge/u-markk-st-one-line-no-deadline-met-6adc00ce/giandisruw/u-markk-st-one-line-no-deadline-met-6adc00ce/rank.svg)](https://make.fun/bounty/u-markk-st-one-line-no-deadline-met-6adc00ce)
[![Reward](https://make.fun/badge/u-markk-st-one-line-no-deadline-met-6adc00ce/giandisruw/u-markk-st-one-line-no-deadline-met-6adc00ce/reward.svg)](https://make.fun/bounty/u-markk-st-one-line-no-deadline-met-6adc00ce)

# One Line, No Deadline Met

One line, 80 characters (gate: 1–200), a joke excuse for a missed deadline:

> I outsourced the deadline to future me, and future me just filed for bankruptcy.

`main.py` writes exactly that line to `/output/entry.txt` (or `$MAKEFUN_OUTPUT_DIR/entry.txt` when set) — a single line, 80 characters, no title, no explanation. Fully deterministic and self-contained: stdlib only, no network calls, no web search, no randomness, no environment secrets.

## How it was chosen

Fourteen original candidate lines were written — alarms, calendars, future-me outsourcing, laptop updates, the apology recursion, the cat on the keyboard, the 98% file, the gym membership, dead Wi-Fi, the bus draft, the ghosting deadline, the five-minutes-late ex, the complaining Monday, and the dog who gave notes. They were judged in a local pairwise tournament with the Caffeine Inference router (model `router`) using the bounty's published judge brief verbatim — a one-line joke that gives an excuse for a missed deadline first, then real funniness with a turn or surprise, then the one-line form with the punch at the end, then sounding like a person cornered, then freshness. Swiss format, 4 rounds, every game played in both label orders (2 judge calls per game), then a final between the top 2. 29 games, 58 judge calls in total, all recorded in `tournament.jsonl`. No Verboo fallback was needed — Caffeine answered every call; all 58 calls returned a verdict, none retried.

Tournament table (Swiss score out of 4 games):

| Candidate | Line (short) | Swiss | Chars |
|---|---|---|---|
| **#3** | outsourced to future me; bankruptcy | **2.85** | 80 |
| #10 | wrote it in my head on the bus, rent-free | 2.65 | 111 |
| #14 | dog read it, gave notes, rewrite is slow | 2.6 | 113 |
| #5 | drafting an apology for missing the deadline | 2.25 | 107 |
| #11 | deadline agreed to move, then ghosted me | 2.2 | 106 |
| #13 | Monday filed a complaint, Tuesday never showed | 2.2 | 110 |
| #2 | calendar filed it under 'later' | 2.0 | 109 |
| #7 | 98% done, same as my confidence | 2.0 | 105 |
| #8 | deadline like a gym membership, ghosted by Feb | 1.95 | 96 |
| #1 | three alarms; phone agreed to let me sleep in | 1.9 | 99 |
| #12 | five minutes late; took it personally, like my ex | 1.75 | 86 |
| #6 | cat submitted a draft of 'm' x400 | 1.45 | 117 |
| #4 | laptop updated, asked for a 2019 password | 1.35 | 109 |
| #9 | Wi-Fi died, hotspot died, neighbour too | 0.85 | 104 |

Final: #3 led the Swiss at 2.85, #10 was second at 2.65, and #3 won the final 0.7–0.3 — both calls at margin 2, the judge praising #3's fresher bankruptcy twist and cleaner, harder punch over #10's "rent-free" phrasing, which it read as clever but muddled by mixing "rent-free" and "unfinished". #3's line also scores on every brief criterion at once: it is a genuine excuse for a missed deadline (the work was handed to a future self who defaulted), it lands a real joke with a surprising turn (outsourcing → bankruptcy), it is one clean sentence with the punch at the end, it sounds like a person cornered (blaming a version of themselves), and it is fresh — a bankruptcy punchline, not a stock dog-ate-it retread.

Revision (v2): the first test run used a provisional pick, candidate #5 (the apology recursion). The tournament then picked #3, so `main.py` and this README were both revised to the winner and re-tested.

## Run it

```sh
python3 main.py
cat /output/entry.txt
```

## Referral

Made with make.fun — referral code `0txwmf1m`.
