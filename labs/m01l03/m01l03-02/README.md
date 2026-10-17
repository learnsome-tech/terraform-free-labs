# m01l03-02 · Confirm it is installed and know what you have

**Lesson:** [Installing Terraform And Meeting The CLI](https://learnsome.tech/learn/terraform-course/m01l03) (lesson 1.3, module 1: Core Concepts And Context) · Free  
**Check:** Graded

## Goal

You can install Terraform, confirm the version you are running, and use the two commands that cost nothing and catch most mistakes: format and validate.

## Files

- [`starter/session.sh`](starter/session.sh): the listing from the lesson
- [`expected.txt`](expected.txt): the output the check compares with
- [`check.json`](check.json): how `./check` runs and checks this lab

## Steps

1. Go to the starter: `cd labs/m01l03/m01l03-02/starter`
2. Read `session.sh`.
3. The session types these commands, in order:

   ```sh
   terraform version
   ```
4. Run it: `bash session.sh`.
5. Check it from the repository root: `./check m01l03-02`.

## Expected output

```text
Terraform v1.16.4
on linux_amd64
```

## How to check

`./check m01l03-02` copies `starter/` into a scratch directory and runs `bash session.sh` there, the way the site's lab sandbox does: that directory is the working directory and `HOME`, `LANG=C.UTF-8`, `TZ=UTC`, a limit of 10 seconds and 256 KiB of output per stream.

It passes when the output matches `expected.txt` by the site's rules, within the limits. Standard output and standard error are compared after Terraform's machine-specific noise is set aside: provider download lines, advisory text, colour and blank lines are dropped, and resource ids, versions, durations, timestamps and working directories are masked. A pass here is a pass on the site.

---

[Open the lesson on LearnSome.tech](https://learnsome.tech/learn/terraform-course/m01l03) · [All labs of this lesson](../README.md) · [Course README](../../../README.md)
