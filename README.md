# README

A collection of ADRs (architectural decision records) for the Ferrea project.

These decision record use [Michael Nygard's LADR format](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions).

## Operating model

* [OPM-01 Decision Tracking](./OPM-01-Decision-tracking.md)
* [OPM-02 Bootstraping envinroment](./OPM-02-Bootstrap-environment.md)

## Microservices Design

* [MSD-01 Use one repo per microservice](./MSD-01-Use-one-repo-per-microservice.md)
* [MSD-02 Use main and dev branches](./MSD-02-Use-only-one-branch-and-release-on-tags.md)
* [MSD-03 Use event storming instead of formal ddd](./MSD-03-Use-event-storming-instead-of-formal-ddd.md)
* [MSD-04 Database for service](./MSD-04-Database-for-service.md)
* [MSD-05 OpenApi spec to be manual](./MSD-05-OpenApi-spec-to-be-manual.md)

## Infrastructure

* [INF-01 Neo4j database](./INF-01-Neo4j-database.md)
* [INF-02 Kubernetes cluster](./INF-02-Kubernetes-cluster.md)
* [INF-03 Kubernetes external secrets](./INF-03-Kubernetes-external-secrets.md)
* [INF-04 API gateway and Service Mesh](./INF-04-API-gateway-and-service-mesh.md)

## Acknowledgments

These ADRs follow closely the one suggested in the [Microservices Up and Running (O'Reilly)](https://www.oreilly.com/library/view/microservices-up-and/9781492075448/) presented in the [public repo](https://github.com/implementing-microservices/ADRs).

Since this is a hobby project, I want to give a try to ADRs, and this is my shot.
