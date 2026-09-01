# Decision Memo: _short title here_

> Copy to `delivery-leadership-package/decision-memo.md`. Target length: ~250 words. Write for a non-technical reader. Name the options you **rejected**, not just the one you picked.

**Date:** 9/1/2026
**Author:** Kristen Marturano, Delivery Lead
**Decision area:** Defer the ZIP-code field to next round; do NOT add it this week.

## Context

Marketing has asked us to add a ZIP-code field to the quote form by Thursday to support a regional-pricing A/B test. Our committed goal this week is a working, typed, data-loading Evergreen Quote app merged to main with a green build. The question is whether the ZIP field fits inside this week without putting that goal at risk.

## Options considered

1. **Option A: Add the ZIP field this week** Meets Marketing's Thursday date, but the field is not a cosmetic "box". To do it properly, ZIP has to travel through every layer of the app: the data definition that describes a quote, the form the customer fills in, the pricing calculation, and the saved-quote records. Our tooling deliberately blocks the build until every one of those layers agrees, which is a safety feature, but it means this is a multi-part change, not a one-line add. Doing it under time pressure risk the green build we owe by Thursday.
2. **Option B: Deliver the committed app this week; schedule ZIP for the next round** We ship the assembled, typed, data-loading app on time with a green build, and take the ZIP field as the first item of the next round, done properly end-to-end with the regional-pricing table Marketing says is ready.

## Recommendation

**Option B:** Deliver what we committed this week; schedule the ZIP field for the next round. 

## Why

The value we promised this week is a trustworthy, working quote experience merged cleanly. The ZIP field is a real, worthwhile feature, but because it touches every layer of the app, adding it in the last two days would put the green build at risk for a change that isn't finished being designed on the pricing side. Deferring it one round lets us do it correctly and verifiably, rather than rushing a customer-facing pricing change. The cost of the ZIP field is *knowable* precisely because our tooling forces every layer to be updated, so we can plan it, not gamble on it.

## What would change my mind

If Marketing's A/B test has a hard external deadline this week that can't move, or if the ZIP field can be scoped as display-only (collected but not yet affecting price), I'd revisit, a display-only field is a far smaller change than one wired into pricing.
