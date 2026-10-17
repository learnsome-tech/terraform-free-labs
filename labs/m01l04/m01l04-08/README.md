# m01l04-08 · Requiring a provider is not configuring one

**Lesson:** [Providers And The required_providers Block](https://learnsome.tech/learn/terraform-course/m01l04) (lesson 1.4, module 1: Core Concepts And Context) · Free  
**Check:** Read along

## Goal

You can declare the providers a configuration needs, explain the difference between requiring a provider and configuring one, read a version constraint, and say what the dependency lock file is for.

## Files

- [`starter/main.tf`](starter/main.tf)
- [`starter/requiring-a-provider-is-not-configuring-one.tf`](starter/requiring-a-provider-is-not-configuring-one.tf): the listing from the lesson
- [`check.json`](check.json): how `./check` runs and checks this lab

## Steps

1. Read `starter/requiring-a-provider-is-not-configuring-one.tf` alongside the lesson.

## How to check

**Read along.** Its Terraform configuration uses the `aws` provider, which needs a real cloud account. The lab sandbox has only the local, null and random providers.

There is nothing to check: `./check m01l04-08` says so and moves on.

---

[Open the lesson on LearnSome.tech](https://learnsome.tech/learn/terraform-course/m01l04) · [All labs of this lesson](../README.md) · [Course README](../../../README.md)
