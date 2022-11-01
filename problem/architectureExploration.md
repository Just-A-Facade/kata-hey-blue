# Architecture Exploration

## Architecture characteristics

performance    responsiveness    availability    fault-tolerance    testability    extensibility    agility    reliability    security    recoverability    interoperability    concurrency    adaptability    scalability    modularity    data integrity    deployability    workflow    abstraction    cost    simplicity    elasticity    configurability    integration

1. Identify no more than 7 driving characteristics.
2. Pick the top 3 in any order.
3. Identify implicit characteristics.
4. State other characteristics considered.
 
### Driving Architecture Characteristics

| Top 3 | Characteristic               | Considerations                                                                   |
| ----- | ---------------------------- | -------------------------------------------------------------------------------- |
|       | performance                  | A high number of cuncurrent interactions shall be expected                       |
| X     | responsiveness               | The platform shall be responsive in notifying the opportunity of an interaction  |
| X     | availability                 | The platform shall guarantee no downtime in order to maximize the chances of an interaction |
|       | fault-tolerance              | The platform consists of many different aspects (interactions, points management, purchases, analytics) and so it must be prevented that error propagations take the whole system down. |  
|       | scalability                  | Some domains such as analytics, notification, interactions likely to require more resources at different times |
| X     | data integrity               | The platform shall guarantee the correctness of data (points, users, goods) |  
|       | data consistency             | A transactional behaviour shall be guaranteed when transfering and reedeming points |

### Implicit Architecture Characteristics

    Feasibility - cost
    Security - authentication and authorisation
    Ease to Use - simplicity
    Mantainability and Quality - deployability and testability

### Others Considered

    Domain-partitioning
    Configurability
    Interoperability

## Architecture Quanta

| Domains            | Sub-domains                      | Applicable Architectural Characteristics                                               | Strategic Domain |
| ------------------ | ---------------------------------| -------------------------------------------------------------------------------------- | ---------------- |
| User               | Profile, Catalog                 | Authorisation, Configurability, Data Integrity, Fault Tolerance                        | Supportive       | 
| Security           | Authentication, Authorisation    | Authorisation, Data Integrity, Data Consistency                                        | Generic          |
| DataStore          | Database, User Interface         | Authorisation, Data Integrity, Data Consistency                                        | Generic          |
| Notification       | Live Tracking, Matchmaker        | Authorisation, Performance, Responsiveness, Scalability, Availability, Fault Tolerance | Core             |
| Interaction        | Handshake, Social Media          | Authorisation, Performance, Responsiveness, Scalability, Availability, Fault Tolerance | Core             |
| Point              | Redemption, Transfer, Conversion | Authorisation, Data Integrity, Data Consistency, Fault Tolerance                       | Core             |
| Analytics          | Engagement                       | Authorisation, Fault Tolerance, Performance, Scalability, Data Integrity               | Core             |
| User Interface     | Mobile app, Web app              | Authorisation, Interoperability, Simplicity, Data Integrity                            | Supportive       |