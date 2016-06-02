# Scenario NCH-4
#### Variation - Tumor arrives, Lengthy delay, Blood arives

1. Tumor received
* Tumor accessioned into STARS
* Block sent to Core Morph (to cut slides)
* Tumor paperwork given to coordinator (next day)
* Tumor paperwork QC'd against STARS accessioning info
* STARS poller sends tumor specimen received message; See [NCH-4-IM-1](#nch-4-im-1)
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
* STARS poller sends specimen shipped messages; See [NCH-4-IM-2](#nch-4-im-2)
* Blood received
* Blood accessioned into STARS
* Blood sent to MGL (for DNA extraction, etc.) 
* Paperwork given to coordinator (next day)
* Paperwork QC'd against STARS accessioning info
* STARS poller sends specimen received message; See [NCH-4-IM-3](#nch-4-im-3)
* MGL extracts DNA from blood and records yield, QC, etc. in STARS
* MGL signing director reviews and approves QC documentation ("sign off")
* Shipment in STARS created to include: Aliquot of blood DNA
* STARS poller sends specimen shipped message; See [NCH-4-IM-4](#nch-4-im-4)

---

#### Sample Integration Messages (JSON format)
_FILL THESE IN_
