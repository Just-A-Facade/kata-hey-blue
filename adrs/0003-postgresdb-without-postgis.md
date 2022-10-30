# 3. PostgresDB without PostGIS

Date: 2022-10-30

## Status

Accepted

## Context
TBD

*The issue motivating this decision, and any context that influences or constrains the decision.* 

## Considered options

* Postgres
* Postgres with PostGIS
* ArcGIS
* QGIS

## Decision outcome

We decided that adding the PostGIS extension or a full-fletched Geographical Information System (GIS) like ArcGIS or QGIS is an overkill as only a very limited set of GIS functionality is needed.

According to [this article](https://blog.rebased.pl/2020/04/07/why-you-probably-dont-need-postgis) doing a simple near-by location query and visualizing points on a map can be done (at least once Postgres `earthdistance` module is enabled).

If more GIS functionality is needed in the future, it shouldn't be difficult to add one of the alternatives at a later point in time.

## Consequences

TBD

*What becomes easier or more difficult to do and any risks introduced by the change that will need to be mitigated.*
