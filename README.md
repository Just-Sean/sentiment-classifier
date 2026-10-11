# Sentiment Classifier
A binary (positive/negative) sentiment classifier for Amazon product reviews,
using the [Amazon Reviews 2023](https://amazon-reviews-2023.github.io/) dataset.

Final project for CS 345: Machine Learning Foundations and Practice,
Colorado State University, Fall 2026. Instructor: Prof. Sarath Sreedharan.

Tasks and open decisions are tracked on the [CS Sentiment Classifier project board](https://github.com/users/Just-Sean/projects/4).

## Decisions
- **Category:** `Health_and_Personal_Care` is the main focus. Other categories may be used later to test robustness.
- **Input:** the model uses review text only. Star ratings are never a model input.
- **Labels:** star ratings are used only to create the answer key (labels): 1–2★ → negative, 4–5★ → positive; 3★ reviews are dropped.

## Milestones
| Milestone | Due | Deliverable |
|---|---|---|
| Proposal | Nov 3, 2026 | 1–2 page PDF: methods, steps, timeline, team responsibilities |

## To-Do
- [ ] Enumerate tools, processes, and guidelines to use for each of the following 5 phases
  1. Massage Data (add labels, remove unnecessary data, etc.)
  2. Split data (train, validate, test, other data sets like 2018, etc.)
  3. Feature extraction (convert text to usable form)
  4. Training
  5. Testing/tuning
- [ ] Meet Sarath Tuesday 10/13 12:30pm mountain time.
- [ ] Decide: which models are in scope
- [ ] Decide: team responsibilities
- [ ] Decide: data sample size
- [ ] Decide: how to split train/validation/test
- [ ] Draft proposal
- [ ] Review proposal and submit PDF (due Nov 3)
