# Scenario NCH-5
#### Variation - Tumor arrives, Lengthy delay, No blood available

1. Tumor received
* Tumor accessioned into STARS
* Block sent to Core Morph (to cut slides)
* Tumor paperwork given to coordinator (next day)
* Tumor paperwork QC'd against STARS accessioning info
* STARS poller sends tumor specimen received message; See [NCH-5-IM-1](#nch-5-im-1)
* Stained slide sent to BPC
* Stained slide sent to path reviewer
* Block sent to Core Morph when path review complete
* Scrolls cut; Unstained slides cut sent to BPC
* Slides held by BPC (for later shipment to MDA)
* Scrolls sent to MGL for extraction
* Block remaining, if any, banked at BPC
* MGL extracts DNA, RNA from tumor and records yield, QC, etc. in STARS
* MGL creates cDNA from extracted tumor RNA and records yield, QC, etc. in STARS
* MGL signing director reviews and approves QC documentation ("sign off")
* Shipment in STARS created to include: Aliquot of tumor DNA, Aliquot of tumor cDNA, Tumor slide(s)
* STARS poller sends specimen shipped messages; See [NCH-5-IM-2](#nch-5-im-2)
* Time passes
* Case shows up on "Cases with Incomplete Material Received (7-30 days)" and is handled manually

---

#### Sample Integration Messages (JSON format)
_FILL THESE IN_
