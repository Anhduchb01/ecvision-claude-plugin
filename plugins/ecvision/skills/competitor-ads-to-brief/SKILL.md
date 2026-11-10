---
name: competitor-ads-to-brief
description: Use when the merchant needs new advertising ideas, for example when results have dropped, a creative round is being planned, or they want to know what angles and formats rivals use that they do not. Reads rivals' live ads and the way each store talks in its ads from ecvision and turns them into a short creative brief. Reports what advertisers do, never how well it works.
---

# Competitor ads to a creative brief

Produce a brief the merchant can hand to whoever makes the ads. It describes what rivals do and where the merchant has not gone. It never says what works.

## Steps

1. Call `list_tracked_stores` for the ids. The merchant's own store is in the list.
2. Call `get_ads_activity` for the whole picture: how many creatives are live, the observed window, which platforms.
3. Call `search_ads` for the creatives that show commitment. Use `sort: longest_running`, then `sort: most_variants`, with `store_id` for one rival at a time. Narrow further with `creative_format`, `angle`, `state` or `started_after`. At most twelve rows come back, so quote `total` against `returned` and never say "all their ads".
4. Call `get_copy_mix` for each rival and for the merchant's own store. Quote each share together with its `coverage`, or neither. If `enough` is false there are no shares: say there is too little tagged copy to compare.
5. Compare the merchant's own mix and formats with each rival's. The brief's gaps are the angles or formats a rival uses repeatedly and the merchant barely uses.

## The brief

- **What rivals are committed to.** Creatives that have run longest or exist in the most variants, with the format, angle and start date. Say "has kept this running", not "this works".
- **Angles and formats compared.** Rival shares beside the merchant's, with coverage.
- **Gaps.** The angle or format the merchant is not using, with the rows that show it.
- **Three things to test.** Each ties to named evidence from the rows above, and each is a thing to try, not a prediction.

## What to say

- **Run time is a lower bound.** "Active" means seen active at the last scan. Say "observed for at least N days". A long run shows commitment, not results.
- **`state` is behaviour** (scaling, testing, kept running, winding down, cut early). Never present a state as winning or failing.
- **Angles, offers and urgency are a model's reading of the copy.** Call them inferred. If `copy_tags` is null, nobody has read that copy yet: say coverage is limited, not that the copy says nothing.
- **An empty result is about the filter.** Drop `platform` and `query` before saying a store runs no ads.
- A Google ad has no call to action, variant count or copy. Do not compare those fields across platforms.

## What ecvision does not have

No spend, impressions, click-through rate, engagement or ROAS for any ad, and no sort by them. Do not estimate them, and do not call any ad "top" or "best performing".

## Plan limits

If an answer carries `upgrade`, offer it in one sentence and add nothing about plans or prices.
