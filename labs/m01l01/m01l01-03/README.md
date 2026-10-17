# m01l01-03 · What that looks like on the page

**Lesson:** [What Is Infrastructure As Code?](https://learnsome.tech/learn/terraform-course/m01l01) (lesson 1.1, module 1: Core Concepts And Context) · Free  
**Check:** Read along

## Goal

You can explain what infrastructure as code is, say what a declarative tool does that a script does not, and name what Terraform is for and what it is not for.

## Files

- [`starter/network.tf`](starter/network.tf): the listing from the lesson
- [`check.json`](check.json): how `./check` runs and checks this lab

## Steps

1. Read `starter/network.tf` alongside the lesson.
2. Follow it the way the lesson builds it:
   - Lines 1–7: the first block
   - Lines 8–13: the second block
3. Notes from the lesson:
   - Line 1: resource, then the type, then a name you choose
   - Line 10: this reference is what creates the dependency between them

## How to check

**Read along.** Its Terraform configuration uses the `aws` provider, which needs a real cloud account. The lab sandbox has only the local, null and random providers.

There is nothing to check: `./check m01l01-03` says so and moves on.

---

[Open the lesson on LearnSome.tech](https://learnsome.tech/learn/terraform-course/m01l01) · [All labs of this lesson](../README.md) · [Course README](../../../README.md)
