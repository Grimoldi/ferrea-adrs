# INF-04: API Gateway and Service Mesh

## Status

Accepted

## Context

As I wanna stick with the Kubernetes cluster and I want to try to adhere the most to the industry standard, I need to implement a API Gateway (for north-south traffic) and a Service Mesh (for east-west traffic).

## Decision

I'll use [KrakenD](https://www.krakend.io/) as API Gateway.

I'll use [Linkerd](https://linkerd.io/) as Service Mesh.

The reason behind both choiches is that both products are graduated project from either the [CNCF (Cloud Native Computing Foundation)](https://www.cncf.io/) or the [Linux Foundation](https://www.linuxfoundation.org/), they aree or with a good free tier.

## Consequences
