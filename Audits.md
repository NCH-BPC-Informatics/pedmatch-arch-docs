This brainstorming/design document collects the various audits we may wish to run against the various systems and datasources that back the PedMATCH system at NCH.

## Audits
Audits are only sent if there is matching data. These should be viewed as warnings and could require additional investiagion.

* Specimens accessioned against PedMATCH protocol(s) but shipped elsewhere (past 30 days)
* Specimens accessioned against PedMATCH protocol(s) but with patient lacking PedMATCH protocol enrollment(s)
* MATCHBOX messages in "Queued" status for > X hours
* MATCHBOX messages in "Failed" status for > X hours
* Specimens received and QC in STARS with no corresponding MATCHBOX message to send
* Specimens shipped in STARS with no corresponding MATCHBOX message to send

## Reports
Reports are always sent, even if no data is present. These are primarily informative in nature and often will not require any additional action.

* Specimen Processing
  * Shows all samples that are not "complete"
  * Ordered by last action (e.g. QC, MATCHBOX message queued in stars poller, etc.)
  * Could help detect samples that are "behind schedule"
* Messages sent to MATCHBOX yesterday
   * Could be either at the message level or message tranmission level  
