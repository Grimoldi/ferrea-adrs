# INF-03: Kubernetes external secrets

## Status

Accepted

## Context

With reference to [OPM-02 Bootstraping envinroment](https://github.com/Grimoldi/ferrea-adrs/blob/main/OPM-02-Bootstrap-environment.md), secrets need to be central managed, in order to have the less possible secrets to modify.

Also, since I want to upload anything to the git repo, secrets should not be in plain text.

## Decision

I'll use [External Secrets](https://external-secrets.io/latest/) in order to handle how secrets are created on the cluster.

I'll use [Doppler SecretOps Platform](https://www.doppler.com/) to host the secrets values. I chose Doppler over other provider since it has a nice free tier, the product seems stable and mature, and the integration seems effortless (on the contrary I tried also Bitwarden Secrets Manager, but it seems still under lot of growth and the integration was not so smooth, back in the days).

## Consequences

Apart from the connection to the vault secret, every secret will has to be uploaded to Doppler and later referred in the manifest.

The vault secret will be the only not uploaded, nor on the the vault nor on the git.
