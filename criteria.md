# Acceptance criteria — TakeMeter

These are my targets, not results. Model targets must hold on the held-out test set for each seed: 42, 7, and 2024.

## 1. Overall accuracy of at least 65%

The model should correctly label at least 65% of test posts.

**Why this target:** With three labels, random guessing would average about 33%. I want it to get roughly two out of three posts right, even when a cybersecurity question mixes worry with useful details.

## 2. F1 of at least 0.60 for every label

Each label must have an F1 score of at least 0.60 on the test set.

**Why this target:** I don't want a decent overall score to hide poor results for `underspecified_request` or either other label. The difference between evidence and context can be small, so 0.60 is a starting target I can defend with a planned dataset of 200 posts.

## 3. Each label makes up 20% to 60% of the dataset

In the final labelled dataset, no label should be below 20% or above 60%.

**Why this target:** At 200 posts, that gives each label at least 40 examples. I want enough examples of vague requests as well as detailed reports so the model cannot rely mostly on one label.

## 4. At least 80% agreement on 30 posts

Another person and I should independently assign the same label to at least 24 of 30 posts from my dataset, using my definitions before discussing disagreements.

**Why this target:** The rule about specific evidence should be clear enough for someone else to use. Six disagreements leave room for borderline posts like post 40, but more would make me question whether my definitions are clear.

## 5. Confident predictions are at least 10 percentage points more accurate

The most confident third of test predictions should have accuracy at least 10 percentage points higher than the least confident third, using the notebook's confidence report.

**Why this target:** I expect clear scan results or account changes to be easier than vague claims of being hacked. A 10-point gap would give me a reason to review uncertain predictions first.
