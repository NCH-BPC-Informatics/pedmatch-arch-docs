# Work Breakdown Structure (WBS)
#### NCH BPC Informatics work items
_Does not yet include:_
* _Additional STARS development for a "Test" to trigger Specimen Failure_
* _STARS Label Creator work_
* _Patient Shipping Manifest work_

#### Initial Design
* Finalize functional requirements (scenarios)
* Finalize non-functional requirements (logging, performance, firewall/security, exception handling, versioning)
* Finalize API design for scenarios
  * Specimen Received service (request skeleton, response skeleton, documentation)
  * Specimen Shipped service (request skeleton, response skeleton, documentation)
  * Specimen Failure service (request skeleton, response skeleton, documentation)
  * Advisements (awaiting additional specimen, etc.)
* Initial design - Message Tracking and Correlation schema
* Initial design - Message Tracking and Correlation services
* Initial schema - Ped-MATCH IQ schema
* Initial design - STARS Poller
* Initial design - Patient Shipping Manifest generation
* Initial design - Audits and alerts
* Initial design - Integration Messaging Facility/UI
* Deployment diagram (logical/physical architecture)
* Draft infrastructure requests (app servers, databases, security)
* Team design review

#### Development Iterations
* Establish development environment (IDE/tools, SCM repositories, databases, ESB server, unit test datasets, CI builds)
* Establish integration/QA platform (databases, ESB server)
* Iteration - TDD for STARS Poller skeleton, message generation, message tracking
* Iteration - TDD for Specimen Received polling and messaging
* Iteration - TDD for Specimen Shipped polling and messaging
* Iteration - TDD for Specimen Failure polling and messaging
* Iteration - Audits, alerts, message UI

#### Productionization
* Production infrastructure requests (app servers, databases, security)
* Deployments to production
* Security review of production platform
