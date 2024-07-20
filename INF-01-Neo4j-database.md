# INF-01: Neo4j database

## Status

Accepted

## Context

I like graph databases over relational databases.

I think that in the scope of the project (e.g. suggest reading for a user based on similar readings from other users) a graph db is way better than a SQL db.

## Decision

I'll use a Neo4j instance.

## Consequences

Since I don't want to spin up a Neo4j container on my cluster due to the facts that:

- it is supposed to run on minikube, k3d or similar (it's still a personal/hobby project)
- it will increase the latency in a container due another virtualization layer and any db requires high I/O

I'll go with [Neo4j Aura](https://neo4j.com/cloud/platform/aura-graph-database/), as it has a free tier that is suitable for this project and its fully hosted on Neo4j itself.

I'll have some network latency, but I'd rather prefer that on spinning up a container.

Another consequence of choosing Aura will be that if I don't use for a straight month it, it will be reclaimed; I need to forsee a suitable method to bootstrap the db any time, even from scratch.
