# OPM-01: Decision Tracking

## Status

Debating

## Context

Following [INF-01 Neo4j database](https://github.com/Grimoldi/ferrea-adrs/blob/main/INF-01-Neo4j-database.md), I need to make myself sure I can spin up the environment even if the database is empty.

## Decision

I will implement a microservice for bootstraping (calling the other microservices under the hood with random data).

The credentials for the connection have to be centralized so I need to change only one data to switch from an old-non-existing-instance to the new empty-instance

## Consequences

I'll have to implement a new microservice.

For the credentials centralization this doesn't seems to be a problem, due to the choice of using Kubernetes and External Secrets.
