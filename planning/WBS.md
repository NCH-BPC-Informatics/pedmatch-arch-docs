# Work Breakdown Structure (WBS)
#### NCH BPC Informatics work items
_Does not yet include:_
* _Additional STARS development for a "Test" to trigger Specimen Failure_
* _STARS Label Creator work_
* _Patient Shipping Manifest work_

#### Initial Design
* Finalize functional requirements (scenarios)
  * NCH-1 - Reference Baseline
  * NCH-2 - ...
  * NCH-3 - ...
  * ...
* Finalize non-functional requirements (logging, performance, firewall/security, exception handling, versioning)
* Finalize API design
  * Specimen Received service (request skeleton, response skeleton, documentation)
  * Specimen Shipped service (request skeleton, response skeleton, documentation)
  * Specimen Failure service (request skeleton, response skeleton, documentation)
* Deployment diagram
* Draft infrastructure requests (app servers, databases, security)
* Team design review

#### Development Iterations
* Establish development environment (IDE/tools, SCM repositories, databases, ESB server, unit test datasets)
* Iteration 1 - TDD for Specimen Received polling and messaging
* Iteration 2 - TDD for Specimen Shipped polling and messaging
* Iteration 3 - TDD for Specimen Failure polling and messaging

#### Productionization
* Establish integration/QA platform (databases, ESB server)
* Production infrastructure requests (app servers, databases, security)
* Security review of production platform
