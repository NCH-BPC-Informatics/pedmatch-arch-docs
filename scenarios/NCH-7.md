# Scenario NCH-7
#### Variation - Blood arrives, Lengthy delay, No tumor available

1. Blood received
* Blood accessioned into STARS
* Blood sent to MGL (for DNA extraction, etc.) 
* Paperwork given to coordinator (next day)
* Paperwork QC'd against STARS accessioning info
* STARS poller sends specimen received message; See [NCH-7-IM-1](#nch-7-im-1)
* MGL extracts DNA from blood and records yield, QC, etc. in STARS
* Time passes
* Case shows up on "Cases with Incomplete Material Received (7-30 days)" and MGL attempts to arrange for receipt of matching tumor. _If successful, this is equivalent to [NCH-6](NCH-6.md)_
* MGL determines that no additional tumor is forthcoming and flags case failed due to insufficient materials
* STARS poller sends failure message; See [NCH-7-IM-2](#nch-7-im-2)

---

#### Sample Integration Messages (JSON format)
_FILL THESE IN_
