# Scenario NCH-1b
*Reference Baseline - Slides and blood received in same shipment; no tumor blockl; processed as expected; shipped as expected*

---
#### Workflow
1. Pediatric match email group receives enrollment notification.
1. BPC receives blood and tumor slides.
1. BPC accessions specimens in STARS.
1. BPC sends blood to MGL for DNA extraction.
1. BPC takes stained slides to Pathologist for review and slide annotation.
1. BPC takes H&E annotated slides and unstained slides to CM for macro dissection.
1. BPC enters path review forms into STARS.
1. BPC coordinator receives paperwork from the previous day and QC specimens in STARS.
   1. Surgical event ID assigned to tumor specimen.
   1. STARS poller sends specimen received messages; See [NCH-01b-IM-1](#nch-01b-im-1)
1. Core Morph scrapes the tumor section of the slides into a vial.
1. BPC picks up stained slides and vial of scrapings.
1. BPC sends vial of scrapings to MGL.
1. BPC sends annotated stained slides to VM.
1. VM scans stained slides.
1. BPC sends slides for IHC to MD Anderson.
   1. A shipped message triggered to Match Box.
1. VM makes stained H&E images available to MD Anderson (VIPER or file transfer).
1. MGL extracts DNA and RNA from paraffin scrapings.
1. MGL creates cDNA and run QC on all nucleic acid specimens.
1. MGL director performs review of nucleic acid specimens.
1. Create shipment in STARS > assign specimens.
   1. Molecular ID is assigned.
1. Relabel specimen vials with sequencing center requirements.
   1. Molecular ID in 2D barcode
1. MGL physically ships and marks shipment in STARS as shipped.
   1. STARS poller sends specimen shipped messages; See [NCH-01b-IM-2](#nch-01b-im-2)
1. MGL runs identity panel on tumor and blood specimens.
1. BPC banks stained slides.

---
#### Specimen Labels - Sequencing

###### Specimen #1 (DNA from Blood)

||||
|----------------|-----------------|----------------|
| **Registration #** | 894561          | _(Patient ID)_ |
| **NCH Barcode**    | 0BJ64A          |                |
| **Molecular ID**   | 00013D          |                |
| **2D Barcode**     | 00013D          | _(Molecular ID)_          |
| **Specimen Type**  | Blood Fresh DNA |                |
| **Concentration**  | 25 ng/ul        |                |
| **Volume**        | 10 ul           |                |

###### Specimen #2 (DNA extracted from Tumor)

||||
|----------------|-----------------|----------------|
| **Registration #** | 894561          | _(Patient ID)_ |
| **Surgical Event ID** | 125             |                |
| **NCH Barcode**    | 0BJ64B          |                |
| **Molecular ID**   | 00012D          |                |
| **2D Barcode**     | 00012D          | _(Molecular ID)_  |
| **Specimen Type**  | Paraffin Scroll Primary DNA |    |
| **Concentration**  | 25 ng/ul        |                |
| **Volume**          | 10 ul           |                |

###### Specimen #3 (cDNA generated from Tumor)

||||
|----------------|-----------------|----------------|
| **Registration #** | 894561          | _(Patient ID)_ |
| **Surgical Event ID** | 125          |                |
| **NCH Barcode**    | 0BJ64F          |                |
| **Molecular ID**   | 00012C          |                |
| **2D Barcode**     | 00012C          | _(Molecular ID)_   |
| **Specimen Type**  | Paraffin Scroll Primary cDNA |   |
| **Concentration**  |                 |                |
| **Volume**          | 10 ul           |                |

#### Specimen Labels - Slides

###### Slide Specimen #1

||||
|----------------|-----------------|----------------|
| **Registration #** | 894561          | _(Patient ID)_ |
| **Surgical Event ID** | 125          |                |
| **NCH Barcode**    | 0BJ6A5          |                |
| **2D Barcode**     | 125          | _(Surgical Event ID)_     |
| **Specimen Type**            | Paraffin Unstained Primary          |                |
| **Block #**     | B          |           |

###### Slide Specimen #2

||||
|----------------|-----------------|----------------|
| **Registration #** | 894561          | _(Patient ID)_ |
| **Surgical Event ID** | 125          |                |
| **NCH Barcode**    | 0BJ6A6          |                |
| **2D Barcode**     | 125          | _(Surgical Event ID)_          |
| **Specimen Type**            | Paraffin Unstained Primary          |                |
| **Block #**     | B          |           |

###### Slide Specimen #3

||||
|----------------|-----------------|----------------|
| **Registration #** | 894561          | _(Patient ID)_ |
| **Surgical Event ID** | 125          |                |
| **NCH Barcode**    | 0BJ6A7          |                |
| **2D Barcode**     | 125          | _(Surgical Event ID)_          |
| **Specimen Type**            | Paraffin Unstained Primary          |                |
| **Block #**     | B          |           |

---
#### Shipping Manifests

---
###### Sequencing Specimens
![Image](../documents/Nucleic Acid Pedatric match shipping manfiest 5.xls.png)

---
###### Slide Specimens
![Image](../documents/Slides Pedatric match shipping manfiest 5.xls.png)

---
##### Integration Messages

###### NCH-01b-IM-1
_(2 specimen received messages)_
```json
{
  "header": {
    "msg_guid": "5c64192f-8a25-4874-9db6-fd55c398822d",
    "msg_dttm": "2016-04-25T18:42:13Z"
  },
  "specimen_received": {
    "study_id": "APEC1621",
    "patient_id": "894561",
    "type": "BLOOD",
    "collection_dt": "2016-04-25",
    "received_dttm": "2016-04-25T12:34:56Z"
  },
  "internal_use_only": {
    "stars_patient_id": "ABCXYZ",
    "stars_specimen_id": "ABCXYZ-0AK64L",
    "stars_specimen_type": "Blood Fresh",
    "received_dttm": "2016-04-25T12:34:56Z",
    "qc_dttm": "2016-04-25T13:45:56Z"
  }
}
```

```json
{
  "header": {
    "msg_guid": "ab6d8d37-caf2-4dbb-a360-0032c7a7a76c",
    "msg_dttm": "2016-04-25T18:42:13Z"
  },
  "specimen_received": {
    "study_id": "APEC1621",
    "patient_id": "894561",
    "type": "SLIDE",
    "surgical_event_id": "125",
    "collection_dt": "2016-04-25",
    "received_dttm": "2016-04-25T15:17:11Z"
  },
  "internal_use_only": {
    "stars_patient_id": "ABCXYZ",
    "stars_specimen_id": "ABCXYZ-0AB11A",
    "stars_specimen_type": "Slides",
    "received_dttm": "2016-04-25T15:17:11Z",
    "qc_dttm": "2016-04-25T16:21:34Z"
  }
}
```

```json
{
  "header": {
    "msg_guid": "c003d68f-c369-4d7e-ad65-a1e55d86f058",
    "msg_dttm": "2016-04-25T18:42:13Z"
  },
  "specimen_received": {
    "study_id": "APEC1621",
    "patient_id": "894561",
    "type": "SLIDE",
    "surgical_event_id": "125",
    "collection_dt": "2016-04-25",
    "received_dttm": "2016-04-25T15:17:11Z"
  },
  "internal_use_only": {
    "stars_patient_id": "ABCXYZ",
    "stars_specimen_id": "ABCXYZ-0AB11B",
    "stars_specimen_type": "Slides",
    "received_dttm": "2016-04-25T15:17:11Z",
    "qc_dttm": "2016-04-25T16:21:34Z"
  }
}
```

(More slides omitted for brevity...)

```json
{
  "header": {
    "msg_guid": "c938d0a4-4db9-4b6c-b9cb-7ffce9715a0f",
    "msg_dttm": "2016-04-25T18:42:13Z"
  },
  "specimen_received": {
    "study_id": "APEC1621",
    "patient_id": "894561",
    "type": "SLIDE",
    "surgical_event_id": "125",
    "collection_dt": "2016-04-25",
    "received_dttm": "2016-04-25T15:17:11Z"
  },
  "internal_use_only": {
    "stars_patient_id": "ABCXYZ",
    "stars_specimen_id": "ABCXYZ-0AB11Q",
    "stars_specimen_type": "Slides",
    "received_dttm": "2016-04-25T15:17:11Z",
    "qc_dttm": "2016-04-25T16:21:34Z"
  }
}
```

##### NCH-1-IM-2
_(5 specimen shipped messages)_

```json
{
  "header": {
    "msg_guid": "7912901b-7285-40cc-9269-1cae961a0ea7",
    "msg_dttm": "2016-05-01T19:42:13Z"
  },
  "specimen_shipped": {
    "study_id": "APEC1621",
    "patient_id": "894561",
    "type": "BLOOD_DNA",
    "molecular_id": "00013",
    "destination": "MDA",
    "carrier": "Federal Express",
    "tracking_id": "7956 4568 1235",
    "shipped_dttm": "2016-05-01T19:42:13Z",
    "dna_volume_ul": 10,
    "dna_concentration_ng_per_ul": 25
  },
  "internal_use_only": {
    "stars_patient_id": "ABCXYZ",
    "stars_specimen_id": "ABCXYZ-0BJ64A"
  }
}
```

```json
{
  "header": {
    "msg_guid": "3037ddec-0081-4e22-8448-721ab4ad76b4",
    "msg_dttm": "2016-05-01T19:42:13Z"
  },
  "specimen_shipped": {
    "study_id": "APEC1621",
    "patient_id": "894561",
    "surgical_event_id": "125",
    "molecular_id": "00012",
    "type": "TISSUE_DNA_AND_CDNA",
    "destination": "MDA",
    "carrier": "Federal Express",
    "tracking_id": "7956 4568 1235",
    "shipped_dttm": "2016-05-01T19:42:13Z",
    "dna_volume_ul": 10,
    "dna_concentration_ng_per_ul": 25,
    "cdna_volume_ul": 10
  },
  "internal_use_only": {
    "stars_patient_id": "ABCXYZ",
    "stars_specimen_id_dna": "ABCXYZ-0BJ64B",
    "stars_specimen_id_cdna": "ABCXYZ-0BJ64F"
  }
}
```

```json
{
  "header": {
    "msg_guid": "37c491ec-d91a-4e95-a0cf-291dadf60b2f",
    "msg_dttm": "2016-05-02T18:30:17Z"
  },
  "specimen_shipped": {
    "study_id": "APEC1621",
    "patient_id": "894561",
    "surgical_event_id": "125",
    "slide_barcode": "0BJ6A5",
    "type": "SLIDE",
    "destination": "MDA",
    "carrier": "Federal Express",
    "tracking_id": "1234 1234 1234",
    "shipped_dttm": "2016-05-02T18:30:17Z"
  },
  "internal_use_only": {
    "stars_patient_id": "ABCXYZ",
    "stars_specimen_id": "ABCXYZ-0BJ6A5"
  }
}
```

```json
{
  "header": {
    "msg_guid": "0cbfe261-293b-4ef2-ade6-eec2e342bb57",
    "msg_dttm": "2016-05-02T18:30:17Z"
  },
  "specimen_shipped": {
    "study_id": "APEC1621",
    "patient_id": "894561",
    "surgical_event_id": "125",
    "slide_barcode": "0BJ6A6",
    "type": "SLIDE",
    "destination": "MDA",
    "carrier": "Federal Express",
    "tracking_id": "1234 1234 1234",
    "shipped_dttm": "2016-05-02T18:30:17Z"
  },
  "internal_use_only": {
    "stars_patient_id": "ABCXYZ",
    "stars_specimen_id": "ABCXYZ-0BJ6A6"
  }
}
```

```json
{
  "header": {
    "msg_guid": "5c5f38ea-c2b4-4519-b252-82d8b8043975",
    "msg_dttm": "2016-05-02T18:30:17Z"
  },
  "specimen_shipped": {
    "study_id": "APEC1621",
    "patient_id": "894561",
    "surgical_event_id": "125",
    "slide_barcode": "0BJ6A7",
    "type": "SLIDE",
    "destination": "MDA",
    "carrier": "Federal Express",
    "tracking_id": "1234 1234 1234",
    "shipped_dttm": "2016-05-02T18:30:17Z",
  },
  "internal_use_only": {
    "stars_patient_id": "ABCXYZ",
    "stars_specimen_id": "ABCXYZ-0BJ6A7"
  }
}
```
