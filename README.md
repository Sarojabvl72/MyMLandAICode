# MyMLandAICode
Repository a part of UCB ML and AI certification program.
Interesting to re-code in a new language, in a new era.

## Title: Coupon Acceptance Rate Analysis

## Summary
Overall coupon acceptance rate was **56.84%** (n = 12,684). Acceptance varies substantially by coupon type: **Carry out & Take away** and **Restaurant (<$20)** show the highest acceptance (73.55% and 70.92% respectively), while **Bar** and **Restaurant ($20–$50)** show the lowest acceptance (41.00% and 44.10% respectively). The association between **coupon type** and **time of day** is highly significant (p ≈ 1.50×10⁻²²⁴).

---

## Key numbers

| Coupon type | Acceptance | n | 95% Wilson CI |
|---|---|---|---|
| Carry out & Take away | 73.55% | 2,393 | 71.74% – 75.28% |
| Restaurant (<$20) | 70.92% | 2,786 | 68.94% – 72.72% |
| Coffee House | 49.92% | 3,996 | 48.38% – 51.47% |
| Restaurant ($20–$50) | 44.10% | 1,492 | 41.61% – 46.63% |
| Bar | 41.00% | 2,017 | 38.87% – 43.16% |
| Overall | 56.84% | 12,684 | — |

**Top performing coupon:** Carry out & Take away (73.55%, n=2,393).

**Lowest performing coupon:** Bar (41.00%, n=2,017).

---

## Interpretation and Statistical Takeaways

**Clear ranking by type.** Carry out and inexpensive restaurant coupons are far more likely to be accepted than coffee, mid-range restaurants, or bar coupons. The top two categories exceed 70% acceptance, well above the overall mean.

**Precision and sample size.** All five categories have substantial sample sizes (≥1,492), so the estimated rates are reasonably precise; Wilson confidence intervals are relatively narrow and do not overlap completely between the highest and lowest groups, indicating meaningful differences in acceptance.

**Context matters.** The extremely small p-value for coupon vs time (≈1.50×10⁻²²⁴) indicates time of day strongly modifies acceptance. This suggests temporal targeting (morning vs evening) will materially change conversion.

**Business impact framing.** Per 1,000 offers:

- Carry out & Take away → ~736 acceptances.
- Restaurant (<$20) → ~709 acceptances.
- Coffee House → ~499 acceptances.
- Restaurant ($20–$50) → ~441 acceptances.
- Bar → ~410 acceptances.

Translating acceptance into expected redemptions and revenue will depend on redemption rates and average order value per coupon type.

---

## Practical Recommendations

**Prioritize distribution by coupon type and time.**

Push carry-out and less-expensive restaurant coupons broadly, especially during high-convenience windows (lunch, early evening).

Schedule coffee house coupons for morning commute windows where they are likely to perform better.

Reserve bar and more expensive restaurant coupons for evening/leisure segments and test targeted messaging.

**Segment offers by context.**

Use time of day, destination, and passenger presence to personalize offers. The strong coupon×time association implies large gains from simple temporal segmentation.

**A/B test messaging and urgency for lower-performing categories.**

For bar and $20–$50 restaurant coupons, test limited-time language, bundled incentives, or location-based nudges to raise acceptance.

**Translate acceptance into revenue scenarios.**

Model expected redemptions and revenue per 1,000 offers for each coupon type using historical redemption rates and average order values to prioritize marketing spend.

---

## Limitations and Next Analyses

**Intent vs behavior.** These are self-reported intentions (would drive right away / later). Actual redemption rates may be lower; validate with observed redemption data if available.

**Unobserved confounding.** Other scenario features (e.g., distance, traffic, coupon value, user demographics) may influence acceptance; include them in multivariable models.

**Recommended follow-ups:**

- Run a multivariable logistic regression to estimate adjusted effects of coupon type, time, destination, passenger, and weather.
- Test interactions (e.g., coupon type × time, coupon type × passenger) to identify the highest-value microsegments.
- Estimate lift and ROI by combining acceptance → redemption conversion and average order value.