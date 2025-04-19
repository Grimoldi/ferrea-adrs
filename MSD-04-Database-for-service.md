# MSD-04: Database for service

## Status

Accepted

## Context

As much as I wanted to use the [Database-per-service pattern](https://microservices.io/patterns/data/database-per-service.html), using Neo4j as database, this would break any advantage gained from it, since it power comes from the ability to correlate different type of nodes.

Neo4j doesn't event uses schema, so I'm unable to separate also on a schema-per-service pattern.

## Decision

Instead of using different databases, I'll use just one instance.

The separation would be met with the following two methods (inspired by [this SO post](https://stackoverflow.com/questions/49606124/neo4j-in-microservices-architecture)):

- each microservices is responsible for the aggregation and not only for a node type. This should help also define the boundaries between microservices and which can create relationships between different nodes.
- I'll implement the [sub-graph ACL](https://neo4j.com/docs/operations-manual/current/tutorial/access-control/#auth-access-control-using-privileges), so that each microservices is unable to modify data in scope of another microservice.

## Consequences

The design takes more importance, since aggregation now has a critical role in the separation of duty between microservices.

Each microservice should have a specific user, with its ACL to implement.

However, since at the moment I'm running Aura free, there's only a single user.

As a POC/Hobby project with will be fine.
