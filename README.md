# User Referral Program

> Data Engineer Academy module project: evaluating a user referral program.

This folder contains the cleaned deliverables for the User Referral Program analysis.

## Files

- `clean_user_referral_program_solution.pdf`  
  Final polished report with charts, tables, limitations, incentive economics, and recommendations.

- `user_referral_program_analysis_notebook.ipynb`  
  Reproducible notebook version of the analysis workflow. It loads the referral CSV, cleans the referral flag, calculates the metrics, and includes a cell to regenerate the PDF report.

- `referral_program_analysis.md`  
  Earlier detailed markdown analysis with before/after metrics and recommendations.

- `referral_program_submission.md`  
  Written challenge-style response summarizing the findings.

## Data

The analysis uses:

`/Users/jerrywyatt/Downloads/referral.csv`

The dataset contains transaction-level purchase data with:

- `user_id`
- `date`
- `country`
- `money_spent`
- `is_referral`
- `device_id`

The referral program launched on `2015-10-31`.

## Main Findings

- Revenue increased from `$2,006,396` before launch to `$2,344,003` after launch.
- Average daily revenue increased by `16.8%`.
- Average daily purchasing users increased by `21.8%`.
- The raw data contains `5,857` users who appear as both referred and non-referred.
- After cleaning referral status at the user level, referred users generated `$1,321,404` in post-launch revenue.
- Estimated referral credit cost is `$103,910`, assuming `$10` per cleaned referred user.
- Device behavior suggests possible referral abuse or self-referral activity.

## Recommendation

The referral program appears promising, but the company should not treat the before/after lift as causal proof. The best next step is to continue the program with stronger fraud controls while running a controlled test with a holdout group.

Recommended actions:

- Continue the program with guardrails.
- Add anti-fraud checks for repeated devices and self-referrals.
- Track the full referral funnel.
- Measure retention, LTV, and margin-adjusted payback.
- Run a controlled market-level or user-level experiment before scaling incentives.

## Reproducing the Report

Open and run:

`user_referral_program_analysis_notebook.ipynb`

The final cell calls the report builder and regenerates:

`clean_user_referral_program_solution.pdf`

