# Marketplace Review Intelligence

**Status:** 🚧 In progress

A system that reads customer reviews and automatically figures out what they're about, how the customer feels, and which ones need urgent attention — then checks, with real statistics, whether using an AI model to do this is actually better than a simple keyword approach.

## The problem

Companies get more customer reviews than any person can read. This project builds a tool that reads them for you: it pulls out the sentiment, the topic, and an "urgency" signal from each review, and flags the ones a team should look at first.

But it doesn't stop at "the AI does it." It asks a harder question: **is the AI approach actually worth it compared to a cheap, simple method?** So the project measures both, side by side, and proves the answer with numbers instead of assuming it.

## What it does

- **Reads a review** and extracts three things: sentiment (positive / negative), category (what it's about), and an urgency score.
- **Two ways to do it:** an AI language model, and a simple keyword-matching baseline — so we can compare them fairly.
- **Predicts which reviews need attention** using a small machine learning model, and explains *why* it flagged each one.
- **Runs a proper experiment** to check whether the AI approach beats the simple one — reporting not just accuracy, but also cost and speed.
- **Tests if it generalizes** by trying the same pipeline on a different kind of review data.
- **Ships as an app** you can actually use: paste in a review and see the results live.

## How it's built

- **Python** for the data and modeling work
- **SQLite** to store reviews and results
- An **open-source language model** (run locally for development) for the AI extraction
- **Streamlit** for the app you can click around in

## Datasets

- **Amazon product reviews** — the main dataset used to build and test everything
- **G2 / Capterra reviews** — a second, different dataset used to check whether the approach still works elsewhere

## Results

*Coming soon — this section will show the head-to-head comparison (AI vs. simple baseline), whether the difference is statistically real, and the cost/speed trade-off, once the build is done.*

## Roadmap

- [x] Project plan and design
- [ ] Load data and explore it
- [ ] Build the simple keyword baseline
- [ ] Hand-label a set of reviews to check accuracy against
- [ ] Add the AI extraction and compare it to the baseline
- [ ] Train the "needs attention" prediction model
- [ ] Run the formal experiment (AI vs. baseline)
- [ ] Test it on the second dataset
- [ ] Build and deploy the app

--