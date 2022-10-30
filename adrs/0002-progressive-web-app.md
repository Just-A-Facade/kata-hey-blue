# 2. Progressive Web App (PWA)

Date: 2022-10-30

## Status

Accepted

## Context

TBD

*The issue motivating this decision, and any context that influences or constrains the decision.* 

## Considered options

* Progressive Web App (PWA)
* Apache Cordova
* Ionic
* Separate web and mobile applications

## Decision outcome

We chose to start the project with a PWA, as focusing on a single platform in the beginning should allow us to reach the Minimum Viable Product (MVP) faster (lower effort). Also, cross-platform frameworks like Apache Cordova and Ionic were considered, but as the required capabilities (location services, push notifications) should be supported by PWA as well, it is better to avoid accessing native APIs unless absolutely necessary to keep the web and mobile version as similar as possible. 

If native APIs not supported by PWA will be required in the future, it should still be simple to extend the web app with Apache Cordova at a later point in time.   

## Consequences

TBD

*What becomes easier or more difficult to do and any risks introduced by the change that will need to be mitigated.*
