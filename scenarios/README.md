## Key Workflow Scenarios:
* [NCH-1](NCH-1.md) - Reference Baseline
* NCH-2 - Variation: Tumor arrives, Short delay, Blood arives (i.e., different shipments)
* NCH-3 - Variation: Blood arrives, Short delay, Tumor arives (i.e., different shipments)
* [NCH-4](NCH-4.md) - Variation: Tumor arrives, Lengthy delay, Blood arives
* [NCH-5](NCH-5.md) - Variation: Tumor arrives, Lengthy delay, No blood available
* NCH-6 - Variation: Blood arrives, Lengthy delay, Tumor arives
* [NCH-7](NCH-7.md) - Variation: Blood arrives, Lengthy delay, No tumor available
* NCH-8 - Variation: Nothing arrives; _expect COG to send withdrawal/failure_
* NCH-9 - Variation: QC paperwork failure (Blood)
* NCH-10 - Variation: QC paperwork failure (Tumor)
* NCH-11 - Variation: Failure during extraction, Cut more from existing block (maybe same block, maybe diff but from same surgery)
* NCH-12 - Variation: Failure during extraction, Request more from site, Lengthy delay
* NCH-13 - Variation: Failure during extraction, Request more from site, Told no more available
* NCH-14 - Variation: Failure during extraction, Request more from site, Received more
* NCH-15 - Variation: Failure during extraction, Request more from site, Received more, Failure during extraction
* NCH-16 - Variation: Tumor fails QC, Request more, Receive more
* NCH-17 - Variation: Tumor fails QC, Request more, Told no more available
* NCH-18 - Variation: Tumor fails QC, Request more, Lengthy delay, Receive more
* NCH-19 - Variation: Tumor fails QC, Request more, Lengthy delay, Told no more available
* NCH-20 - Variation: Additional (unrequested/unnecesary) blood arives
* NCH-21 - Variation: Additional (unrequested/unnecesary) tumor arives
* NCH-22 - Variation: COG registration data indiates no enrollment in relevant protocol(s); _expect COG to send withdrawal/failure_
* NCH-23 - Variation: Sequencing center requests additional DNA/cDNA; were able to use existing specimen
* NCH-24 - Variation: Sequencing center requests additional DNA/cDNA; requested more; received more specimen
* NCH-25 - Variation: Sequencing center requests additional DNA/cDNA; were able to use existing specimen
* NCH-26 - Variation: Sequencing center requests additional DNA/cDNA; requested more; received more specimen
* NCH-27 - Variation: Genetic identity mismatch determined to be upstream from NCH
* NCH-28 - Variation: Genetic identity mismatch determined to be upstream from Sequencing center
* Variation: ...other failure scenarios (e.g., case level)...?
* Variation: ...other failure scenarios (e.g., specimen level)...?

## Cross-cutting Aspects
* Surgical event ID represents a specific surgery for a specific patient at a specific timepoint
* "Rebiopsy" situations do not alter the scenarios since they represent a new surgical event and thus have a new surgical event ID

## Audits:
_Put these elsewhere..._
* Cases with Incomplete Material Received (7-30 days)
* Specimens lacking "Specimen Received" messaging (2-30 days)

## Outstanding Questions
* If we receive additional specimens can we send receive messsages? (could be more of the same or new stuff)
* How to mark/trigger failures so that messages are sent
* Is it helpful to send "intermediate" failures as we await more material after failing on existing material?
