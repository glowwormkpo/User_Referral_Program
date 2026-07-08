# User Referral Program Analysis

## Executive Summary

Company XYZ launched the referral program on 2015-10-31. The dataset contains 97,341 purchase transactions from 2015-10-03 through 2015-11-27, giving a balanced 28-day pre-period and 28-day post-period.

The post-launch period shows a clear increase in purchasing activity:

| Metric | Pre Launch | Post Launch | Change |
|---|---:|---:|---:|
| Transactions | 47,341 | 50,000 | +2,659 (+5.6%) |
| Unique purchasing users | 5,000 | 18,397 | +13,397 (+267.9%) |
| Revenue | $2,006,396 | $2,344,003 | +$337,607 (+16.8%) |
| Average order value | $42.38 | $46.88 | +$4.50 (+10.6%) |

Using a simple same-weekday paired baseline, post-launch daily revenue increased by $12,057 per day on average, with all 28 post-launch days exceeding the comparable pre-launch day. This is directionally strong, but it should not be treated as causal proof because there was no control group.

## Referral Contribution

Post-launch referral transactions were substantial:

| Metric | Post-Launch Referral Value |
|---|---:|
| Referral transactions | 28,017 |
| Referral transaction share | 56.0% |
| Referral revenue | $1,315,787 |
| Referral revenue share | 56.1% |
| Users with at least one referral transaction | 12,715 |

Among post-launch users, 13,809 had not purchased in the pre-period. Of those new post-launch users, 12,715 had at least one referral transaction, meaning 92.1% of new post-period purchasers are associated with referral activity.

## Baseline Lift Estimate

The post period produced $337,607 more revenue than the pre period. This lift decomposes into:

| Driver | Estimated Revenue Impact |
|---|---:|
| More transaction volume at old AOV | $112,693 |
| Higher AOV on post-launch transactions | $224,914 |
| Total revenue lift | $337,607 |

This suggests the program was not only associated with more transactions; post-launch orders were also higher value.

## Incentive Cost View

If the $10 credit is paid once per unique referred purchasing user, estimated cost is:

| Cost Basis | Units | Cost | Cost / Referral Revenue | Cost / Incremental Revenue |
|---|---:|---:|---:|---:|
| Unique referred users | 12,715 | $127,150 | 9.7% | 37.7% |
| Referral transactions, conservative upper bound | 28,017 | $280,170 | 21.3% | 83.0% |

The unique-user interpretation is the more likely program mechanic. Under that view, the program appears economically promising before gross margin and retention effects. Under the per-transaction interpretation, the economics are much tighter.

## Country Patterns

Revenue lift was uneven by country:

| Country | Revenue Change | Transaction Change | Referral Revenue |
|---|---:|---:|---:|
| FR | +$90,993 | +1,724 | $211,799 |
| UK | +$83,521 | +693 | $227,706 |
| IT | +$71,172 | +1,318 | $159,439 |
| MX | +$57,617 | +1,051 | $109,023 |
| ES | +$56,334 | +1,061 | $136,672 |
| US | +$32,380 | -528 | $205,684 |
| CA | +$11,536 | -480 | $122,343 |
| CH | -$14,348 | -273 | $16,613 |
| DE | -$51,598 | -1,907 | $126,508 |

France, the UK, Italy, Mexico, and Spain are the strongest expansion candidates. Germany and Switzerland need diagnosis before additional spend because overall revenue fell despite referral activity.

## Important Caveats

- The launch was not run as an A/B test, so observed lift cannot be attributed solely to referrals.
- The `is_referral` field behaves like a transaction-level flag, not a perfectly stable user-level acquisition flag. Some post-period users have both referral and non-referral transactions.
- The analysis uses purchases only. It cannot measure impressions, invites sent, invite conversion rate, unpaid signups, margin, retention, or cannibalization.
- Weekend volume is much higher than weekday volume, so comparisons should preserve day-of-week alignment. The pre/post windows are fortunately exactly 28 days each.

## Recommendations

1. Keep the referral program running, but do not scale incentives globally until a controlled test confirms incremental impact.
2. Launch an A/B test at the user or geography level with holdout users who cannot receive or send referral incentives.
3. Track the full referral funnel: invite sent, invite accepted, signup, first purchase, repeat purchase, referrer credit issued, and credit redemption.
4. Analyze referred-user retention and margin-adjusted payback. The current top-line revenue lift is encouraging, but profitability depends on gross margin and repeat purchases.
5. Expand or promote more heavily in FR, UK, IT, MX, and ES, where revenue lift and referral contribution look strongest.
6. Investigate DE and CH before scaling. Referral transactions exist there, but total revenue and transaction volume declined post-launch.
7. Consider testing incentive variants such as referrer-only $10, referred-user discount, tiered rewards, or delayed rewards based on second purchase to improve quality and reduce gaming risk.
