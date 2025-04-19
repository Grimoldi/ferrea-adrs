# INF-05: Observability

## Status

Accepted

## Context

Observability relies on the `three pillars`:

- logging
- metrics
- trace

This LADR focus around how to implement them.

## Decision

I'll use Grafana (with Grafana Loki) to implement both logging and metrics.

No trace at the moment, as they could be resource eager and time consuming (for me), as I want to focus firstly on completing all the project and then I'd rather prefer focus on more interesting to me topics (such as Api Gateway and Service Mesh).

Few cornerstones:

- Logging will be implemented in json format.
- Accesslogs should come from the ingress controller and not from any Middleware or the application itself.
- Logging of the request on the web server should be disabled, but it's not a must.
- Metrics should at least be the time to fullfill a request. I should use some Middleware like [Starlette Prometheus](https://github.com/perdy/starlette-prometheus).
- Traces are forward to some time in the future...

## Consequences

For the logging I see no big issue, I already wrote a library to standardize the logging for all microservices.

For the metrics I have to see what could be used. The Middleware referred in the `Decision` paragraph is not updated from 24, unfortunately, so I have to choose if to use that, although being not up to date, or search for something else.
