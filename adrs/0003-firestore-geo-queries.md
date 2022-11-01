# 3. PostgresDB without PostGIS

Date: 2022-10-30

## Status

Accepted

## Context
TBD

*The issue motivating this decision, and any context that influences or constrains the decision.* 

## Considered options

* Firestore Geo Queries
* Postgres with PostGIS
* ArcGIS
* QGIS

## Decision outcome

We decided that we will use [Firestore Geo Queries](https://firebase.google.com/docs/firestore/solutions/geoqueries) for querying near-by users. For the described use-case it shouldn't be necessary to add a full-fledged Geographical Information System (GIS). 

If more advanced GIS functionality is needed in the future, it shouldn't be difficult to add one of the alternatives at a later point in time.

## Consequences

TBD

*What becomes easier or more difficult to do and any risks introduced by the change that will need to be mitigated.*
