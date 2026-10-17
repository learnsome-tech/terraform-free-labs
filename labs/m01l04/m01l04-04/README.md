# m01l04-04 · What the directory knows now

**Lesson:** [Providers And The required_providers Block](https://learnsome.tech/learn/terraform-course/m01l04) (lesson 1.4, module 1: Core Concepts And Context) · Free  
**Check:** Graded

## Goal

You can declare the providers a configuration needs, explain the difference between requiring a provider and configuring one, read a version constraint, and say what the dependency lock file is for.

## Files

- [`starter/main.tf`](starter/main.tf)
- [`starter/session.sh`](starter/session.sh): the listing from the lesson
- [`expected.txt`](expected.txt): the output the check compares with
- [`check.json`](check.json): how `./check` runs and checks this lab

## Steps

1. Go to the starter: `cd labs/m01l04/m01l04-04/starter`
2. Read `session.sh`.
3. The session types these commands, in order:

   ```sh
   terraform providers
   terraform version
   ```
4. Run it: `terraform init; sh session.sh`.
5. Check it from the repository root: `./check m01l04-04`.
6. The site offers these commands for this lab; the first is the default, and the only one graded. Run another with `./check m01l04-04 --command=<id>`:
   - `recorded` (Recorded session): `terraform init; sh session.sh`
   - `init` (Init): `terraform init`
   - `validate` (Validate): `terraform validate`
   - `plan` (Plan): `terraform plan`
   - `apply` (Apply): `terraform apply -auto-approve`
   - `fmt` (Format check): `terraform fmt -check -diff`
   - `output` (Output): `terraform apply -auto-approve && terraform output`

## Expected output

```text
Providers required by configuration:
.
├── provider[registry.terraform.io/hashicorp/local] ~> 2.5
└── provider[registry.terraform.io/hashicorp/random] ~> 3.6

Terraform v1.16.4
on linux_amd64
+ provider registry.terraform.io/hashicorp/local v2.9.1
+ provider registry.terraform.io/hashicorp/random v3.9.0
```

## How to check

`./check m01l04-04` copies `starter/` into a scratch directory and runs `terraform init; sh session.sh` there, the way the site's lab sandbox does: that directory is the working directory and `HOME`, `LANG=C.UTF-8`, `TZ=UTC`, a limit of 10 seconds and 256 KiB of output per stream.

It passes when the output matches `expected.txt` by the site's rules, within the limits. Standard output and standard error are compared after Terraform's machine-specific noise is set aside: provider download lines, advisory text, colour and blank lines are dropped, and resource ids, versions, durations, timestamps and working directories are masked. A pass here is a pass on the site.

---

[Open the lesson on LearnSome.tech](https://learnsome.tech/learn/terraform-course/m01l04) · [All labs of this lesson](../README.md) · [Course README](../../../README.md)
