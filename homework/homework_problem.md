# Homework: Should You Always Take an RB Early?

**Data:** `homework/fantasy_adp_2015_2025.csv` in this repository. It has every QB, RB, WR and TE drafted within the first 200 picks of FantasyPros PPR drafts, 2015-2025.

Key columns:

| Column | Description |
|---|---|
| `season`, `player`, `position` | Season, player name and fantasy position |
| `adp` | Average draft position (overall pick) |
| `pos_adp_rank` | Rank among drafted players at the position (RB12 = 12) |
| `pos_finish_rank` | Season finish rank at the position |
| `por` | Points over replacement: season PPR points minus the points of the last starter at the position (RB30, WR30) |

## Question

Your friend says: **"Always take an RB in the first two rounds."**

Using RBs and WRs only, test this claim with two pieces of evidence:

1. **Accuracy:** for each season, compute the Spearman correlation between `pos_adp_rank` and `pos_finish_rank` for each position, then average across seasons.
2. **Value:** fit a LOESS curve of `por` on `adp` for each position (`frac=0.4`), plot both curves on one chart, and report each curve's expected POR at **pick 24** (the end of round 2).

In 3 to 4 sentences, explain whether the data support your league-mate's claim.


## What to Submit

Email Dr. Schuckers a link to a GitHub repository with a notebook that runs top to bottom, your chart, and your written answer in a markdown cell.
