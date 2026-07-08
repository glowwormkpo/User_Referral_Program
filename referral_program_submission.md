# User Referral Program: Analysis and Recommendations

## Objective

Company XYZ launched a referral program on October 31, offering existing users $10 in credit when a referred user makes a purchase. The goal of this analysis is to assess whether the program appears effective, quantify the changes after launch, and recommend next steps for the Growth Product Manager.

The data covers purchase transactions from October 3, 2015 through November 27, 2015. This gives a balanced comparison window: 28 days before launch and 28 days after launch.

## Overall Impact

The referral program launch was followed by a meaningful increase in purchasing activity.

| Metric | Before Launch | After Launch | Change |
|---|---:|---:|---:|
| Transactions | 47,341 | 50,000 | +2,659 (+5.6%) |
| Unique purchasing users | 5,000 | 18,397 | +13,397 (+267.9%) |
| Revenue | $2,006,396 | $2,344,003 | +$337,607 (+16.8%) |
| Average order value | $42.38 | $46.88 | +$4.50 (+10.6%) |

The strongest signal is revenue growth. Revenue increased by 16.8%, which is higher than the transaction growth rate of 5.6%. This means the post-launch period did not just bring more purchases; it also brought higher-value purchases.

## Referral Contribution

After launch, referral-driven transactions represented a large share of activity.

| Metric | Post-Launch Value |
|---|---:|
| Referral transactions | 28,017 |
| Share of post-launch transactions from referrals | 56.0% |
| Referral revenue | $1,315,787 |
| Share of post-launch revenue from referrals | 56.1% |
| Users with at least one referral transaction | 12,715 |

Most new purchasing users in the post-launch period were associated with referral activity. Of the 13,809 users who purchased after launch but had not purchased before launch, 12,715 had at least one referral transaction. That means approximately 92.1% of new post-launch purchasers were connected to referrals.

This is a strong indication that the referral program was effective at bringing new purchasers onto the platform.

## Incremental Lift Estimate

Using the 28-day pre-launch period as a baseline, the post-launch period generated:

| Incremental Metric | Estimated Lift |
|---|---:|
| Additional transactions | +2,659 |
| Additional daily purchasing users, summed across days | +8,470 |
| Additional revenue | +$337,607 |

The revenue lift can be broken into two parts:

| Driver | Estimated Impact |
|---|---:|
| More transaction volume at pre-launch AOV | $112,693 |
| Higher post-launch AOV | $224,914 |
| Total revenue lift | $337,607 |

This suggests that the program may have improved both acquisition and purchasing quality.

## Incentive Economics

The program pays $10 in credit when a referred user makes a purchase. If the credit is paid once per unique referred purchasing user, estimated program cost is:

| Basis | Units | Estimated Cost |
|---|---:|---:|
| Unique referred purchasing users | 12,715 | $127,150 |

Compared with referral revenue of $1,315,787, the incentive cost is about 9.7% of referral revenue. Compared with estimated incremental revenue of $337,607, the incentive cost is about 37.7%.

This appears economically promising, assuming gross margins are healthy and referred users continue purchasing in future periods.

As a conservative upper bound, if the company paid $10 per referral transaction rather than per referred user, the cost would be $280,170. That would equal 83.0% of the estimated incremental revenue, making the program much less attractive. The exact payment rule should therefore be confirmed.

## Country-Level Insights

The referral program appears stronger in some countries than others.

| Country | Revenue Change | Transaction Change | Referral Revenue |
|---|---:|---:|---:|
| France | +$90,993 | +1,724 | $211,799 |
| United Kingdom | +$83,521 | +693 | $227,706 |
| Italy | +$71,172 | +1,318 | $159,439 |
| Mexico | +$57,617 | +1,051 | $109,023 |
| Spain | +$56,334 | +1,061 | $136,672 |
| United States | +$32,380 | -528 | $205,684 |
| Canada | +$11,536 | -480 | $122,343 |
| Switzerland | -$14,348 | -273 | $16,613 |
| Germany | -$51,598 | -1,907 | $126,508 |

France, the United Kingdom, Italy, Mexico, and Spain look like the strongest candidates for continued investment or expansion. Germany and Switzerland need further investigation because total revenue declined despite referral activity.

## Caveats

The biggest limitation is that the program was not launched as a controlled experiment. Because there is no control group, the before-and-after lift cannot be fully attributed to the referral program. Other factors, such as seasonality, marketing campaigns, product changes, promotions, or external market effects, could have contributed to the increase.

There is also a data interpretation issue: `is_referral` appears to be a transaction-level flag rather than a permanent user-level acquisition flag. Some users have both referral and non-referral transactions after launch. This means referral results should be interpreted as referral-associated transactions, not necessarily as a perfect count of referred users.

Finally, the dataset only includes purchases. It does not include invite sends, invite acceptances, signups without purchases, margins, credit redemptions, or long-term retention. Those metrics are needed to fully evaluate program profitability.

## Recommendations

The referral program appears successful and should continue, but the company should avoid scaling it aggressively until the impact is validated with a controlled test.

Recommended next steps:

1. Run an A/B test with a clear control group that does not receive referral incentives.
2. Confirm whether the $10 credit is paid once per referred user or once per transaction.
3. Track the full referral funnel: invite sent, invite accepted, signup, first purchase, repeat purchase, credit issued, and credit redeemed.
4. Measure margin-adjusted payback, not just revenue.
5. Analyze retention of referred users compared with non-referred users.
6. Expand referral promotion in France, the United Kingdom, Italy, Mexico, and Spain.
7. Investigate Germany and Switzerland before investing more in those markets.
8. Test incentive variants, such as giving both the referrer and referred user a reward, requiring a second purchase before issuing credit, or using tiered rewards for high-quality referrals.

## Conclusion

The referral program is associated with strong post-launch growth. Revenue increased by $337,607, average order value rose by 10.6%, and referral transactions accounted for more than half of post-launch revenue. The program looks promising, especially if the incentive is paid once per referred purchasing user.

However, because there was no A/B test, the company should treat this as encouraging evidence rather than definitive proof. The next step should be to continue the program while running a controlled experiment to measure true incremental impact and optimize the incentive structure.
