# MSD-02: Use only one branch and release on tags

## Status

Accepted

## Context

I want to separate coding process from the release process for my microservices.

## Decision

Only for the repo about microservices:

- Use only the `main` branch.
- Use tags for marking a branch version ready to be deployed.
- Tags should follow [semver versioning](https://semver.org/#is-v123-a-semantic-version), so avoid the `v`, previously forseen.

Originally thought about `main` and `dev` branches, but as I am alone in the coding, this don't make much sense after all.

It's hard to have multiple feature branch at the same time, I think.

This means that a tag should just be enough, althoug this is not the best practice.

Linting and testing should be linked to commits, whereas building and pushing the image should be linked to tags push.

## Consequences

I should implement few workflows, both for linting/tests and for build/push.

However, since this should be almost the same, I can setup a "skeleton" repo to be cloned and to this just once.
