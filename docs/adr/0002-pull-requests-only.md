# 0002 - Nothing reaches main without a pull request

## Context

At first, changes to the count were committed straight to `main`, from more
than one laptop. A wrong number could land without anyone else seeing it, two
people could push at the same time and have to merge by hand, and the history
showed who changed a line but not who checked it, or why. The auditors need
every change to be checked before it becomes the count.

## Decision

Every change to `main` comes through a pull request on GitHub: a branch, a
commit, a pull request with What, Why and How I checked, and a review by
somebody else before it is merged. Nobody pushes to `main` directly.

## Consequences

- Every change has a second pair of eyes and a written reason, next to the
  diff, that the auditors can read later.
- Documents change in the same pull request as the thing they describe, so the
  README does not fall behind the count.
- A change takes longer: even a one-line fix waits for a review.
- Everybody needs a GitHub account and has to know the routine.
