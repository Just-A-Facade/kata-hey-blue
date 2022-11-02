# 4. Store chat messages in DB until delivery

Date: 2022-11-02

## Status

Accepted

## Context

TBD

*The issue motivating this decision, and any context that influences or constrains the decision.*

## Considered options

* Store chat messages in DB until delivery
* Direct transmission with retry (exponential backoff)

## Decision outcome

We agreed to deliver chat messages via the server and store it in the DB until delivery.

## Consequences

Transmitting messages via the server is more robust regarding network or power outages, as in the worst case neither sender nor recipient of the message must be online at the same time. 

*What becomes easier or more difficult to do and any risks introduced by the change that will need to be mitigated.*
