# MSD-02: Use Main and Dev branches

## Status

Accepted

## Context

I want to separate coding process from the release process for my microservices.

## Decision

Only for the repo about microservices:

- Use `main` branch for every process related to release.
- Use `dev` branch for every process related to the coding aspect.

Ideally this would separate the linting, testing, formatting on the `dev` branch, and the release, gitOps on the `main` branch.

Don't push directly in the `main` branch, but merge from `dev` to  `main`.

## Consequences

Since I already created a bunch of microservices repos without this pattern, I would have to create the new branch `dev`.

Every microservices repo would have to implement a policy that block pushes on the `main` branch.
