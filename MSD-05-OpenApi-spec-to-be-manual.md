# MSD-05: OpenApi spec to be manual

## Status

Accepted

## Context

While some framework (like FastApi, that I will use) support the generation on the fly of the OpenApi spec, there's the problem they cannot be tested.

## Decision

Instead of letting the framework build the spec based on the code, I'll write the specs before.

This will produce several benefits:

- the specs could be shared prior to the service to be implemented
- more control on how it changes
- possibility for testing and validation of the schema, even automatically with [Spectral](https://docs.stoplight.io/docs/spectral)

The con is of course it has to be written, but I feel like doing so helps better understanding the expectation around a microservice.

## Consequences

For each microservice, there will be the OpenApi schema written.

This should go under the path `/docs/oas.yaml'

The exposing of the schema, however, must be prohibited.
