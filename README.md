# Project Architectural documentation NCH aspects of PED-MATCH

## Content
* [Presentations and Schematics](schematics)
* [Scenarios](scenarios/README.md)

## Project Contacts
- VIPER Contacts (digitial image review)
  - Dr. Stanley Hamilton and Dr. Savitri Krishnamurthy
  - Contact Leslie in production (keep Leslie as user)
  - Ryan Pepper (MDA) - RCPepper@mdanderson.org

## Tentative Milestone Dates
* BPC/MGL Internal Testing - March 20th
* Site visit by NCI – April 6th
* Fit for Purpose – May 22 - 26
* Study Activation / Go Live - June 15

## Testing Enviroments
- STARS UAT 1 - BPCI QA Testing  
- STARS UAT 2 - BPC/MGL Stars User Acceptance Testing  
- STARS UAT 3 - BPC/MGL Interal Integration Testing   
- STARS UAT 4 - External 4 way Integration Testing  
- StarsPedsmatchFit - Fit for Purpose External Integration Testing  

## Pediatric Match Fit for Purpose Testing Plan:

1)	COG will enroll three fake patient into their test system.  
2)	COG will provide Will Parsons with the three reg number to label specimens. 
3)	Will Parsons lab has pulled three tumor and three blood specimens for Fit for purpose testing  
  o	Blood and tumor will not be matched pairs  
  o	It is unclear if the blood will be frozen/fresh or processed ficolled/lysed  
  o	Tumor samples will be pediatric cancer samples  
4)	Parson’s lab will ship the tumor and blood specimens to the BP.  
  o	Specimens should be labeled with the registration number COG enrolled for testing.  
  o	Path reports will be included, but they may not be official.  They will likely be de identified and sections cut and copied onto a document sent to us.  
  o	Specimens should also come with a completed transmittal form and a site contact form.   
5)	BPC processing lab will receive the package.
6)	BPC will accession specimens into 'STARS_PedsMatch_Fit' test enviroment.  
  o	Standard QC process should occur. 
7)	BPC processing lab will send the blood specimens to MGL for extraction via a MGL request.
8)	BPC processing lab will send tumor blocks to CM to have slides cut via CM request.
9)	CM will cut 1 HE slide, 4 unstained charged slides, and 30 unstained uncharged slides. 
10)	CM will send HE slide and 4 charged slides back to the BPC processing lab.
11)	Shountea or designee will take HE to Dr. Conces with a paper review form.
12)	Dr. Conces will complete review and mark slide for macro dissection. 
13)	Shountea will enter the path review information into STARS.
14)	Shountea will create a macro dissection request in STARS for CM.  Stain slide will be dropped off to CM. 
15)	Shountea will QC specimens in STARS.  
  o	Received message will be sent to MATCHbox
16)	CM will macro dissect slide and create paraffin scrapings.
17)	Shountea will pick up scrapings from CM.  She will also inherit the path review to the correct specimens.
18)	Shountea will create a request for extraction and drop the scrapings off at MGL. 
19)	MGL will extract the paraffin scrapings.
20)	MGL will create QC nucleic acid specimens.
21)	MGL will create aliquots and add them to a STARS shipment.
22)	MGL will give information for the director to do a manual review.
23)	Director will sign off on shipment. 
24)	MGL will notify the BPC that specimens are ready to ship.
25)	BPC will contact MD Anderson and MOCHA to see if they are ready for the Fit for Purpose test specimens. 
26)	MGL will drop off nucleic acid specimens and send to MGL in STARS.
27)	BPC will prepare shipments.  
  o	Nucleic acid specimens need to go to MD Anderson and MOCHA.  Need to decide who gets 1 and who gets 2.  
  o	All slides for IHC will go to MD Anderson.
  o	Each case will need to have a shipping manifest, copy of path report, and site contact form (per package).
28)	BPC will ship specimens and send electronic copy of shipping manifest to the MD Anderson and MOCHA.  Specimens marked as shipped in STARS.
  o	Shipped message triggered to MATCHbox. 
