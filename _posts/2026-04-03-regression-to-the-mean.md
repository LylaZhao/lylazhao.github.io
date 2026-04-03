---
title: "Regression to the Mean: Why Performance Doesn’t Last"
date: 2026-04-03
---

This is a reading note from *Thinking, Fast and Slow* by Daniel Kahneman (Chapter 17: Regression to the Mean).

---

## Summary

Not everything can be attributed to measurable factors. Often, it’s just luck.

Sometimes good, sometimes bad — randomness is always present in our outcomes. Even when we perform well, we don’t fully control the result.

This idea sounds simple, but we often forget it when we interpret performance.

---

## Why Praise Seems to Backfire

There’s a common belief in management:

- After you **praise** someone, their performance gets worse
- After you **criticize** someone, their performance improves

This pattern feels real. Many managers have observed it.

So it’s tempting to conclude:

- praise is ineffective
- punishment works better

But this is a mistake.

What we’re seeing is **correlation**, not causation.

## What’s Actually Happening

This is a classic example of **regression to the mean**.

When someone performs extremely well, it’s usually:

- their true ability
- plus some **positive randomness (luck)**

When someone performs poorly, it’s:

- their true ability
- plus **negative randomness**

Extreme outcomes are unstable.

So naturally:

- very strong performance tends to decline
- very weak performance tends to improve

Not because of praise or punishment —

but because **luck doesn’t persist**.

If we ignore randomness, we end up attributing the change to the wrong cause. And that leads to bad decisions.

## A Simple Forecasting Challenge

At the end of the chapter, Kahneman presents a practical problem:

> You are the sales forecaster for a department store chain. All stores are similar in size and merchandise selection, but their sales differ because of location, competition, and random factors.
> 
> 
> You are given the results for 2011 and asked to forecast sales for 2012. You are told that total sales will increase by 10%.
> 
> How would you complete the following table?
> 

| Store | 2011 Sales | 2012 Forecast |
| --- | --- | --- |
| 1 | $11,000,000 | ___ |
| 2 | $23,000,000 | ___ |
| 3 | $18,000,000 | ___ |
| 4 | $29,000,000 | ___ |
| **Total** | **$81,000,000** | **$89,100,000** |

---

## The Tempting (but Wrong) Answer

A natural approach is:

$yi=1.1xi$

Just increase every store by 10%.

This feels fair and straightforward.

But it assumes that last year’s performance is fully reliable and there is no randomness.

Which we already know is not true after reading about “Regression to the Mean”

## What a Better Forecast Should Do

A better forecast should recognize that part of last year’s performance was luck.

So:

- low-performing stores should increase **more than 10%**
- high-performing stores should increase **less than 10%** (or even decrease)

In other words, the forecast should be **regressive.** It should move values closer to the average.

## Solving the Problem

### Step 1: Find the average sales in 2011

$\bar{x} = 81 / 4 = 20.25$

### Step 2: Find the average sales in 2012

$\bar{y} = 89.1 / 4 = 22.275$

### Step 3: Apply a regressive forecast

$\hat{y}_i = 1.1(\bar{x} + r(x_i - \bar{x}))$

Substitute values:

$\hat{y}_i = 1.1(20.25 + r(x_i - 20.25))$

Equivalent form:

$\hat{y}_i = 22.275 + 1.1r(x_i - 20.25)$

## What This Formula Means

- $x_i$: store’s 2011 sales
- $r$: how reliable the past performance is
- $0 < r < 1$

This formula does two things at the same time:

1. It keeps the total growth at **10%**
2. It pulls each store **toward the average**

So:

- weaker stores get lifted
- stronger stores get pulled back

## Intuition

You can think of the process like this:

- Start from the **average store next year (22.275M)**
- Look at how each store performed relative to average
- **Shrink that difference using $r$** (because part of it is luck)
- Then apply growth

## Why This Matters

Most of the time, we assume performance is stable.

We treat extreme results as meaningful signals:

- “this store is excellent”
- “this campaign is bad”
- “this employee improved because of feedback”

But in reality, part of what we observe is just randomness.

If we don’t account for that, we:

- overreact to success
- overcorrect failure
- and misattribute causes
