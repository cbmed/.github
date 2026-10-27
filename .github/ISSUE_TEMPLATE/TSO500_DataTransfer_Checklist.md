---
name: TSO500 raw data transfer 
about: This is the checklist to be followed for all BI TSO500 projects with data from Human Genetics
title: '[xxxx-xxxx] [y.yy] batch[n] TSO500 QC gate 1 (Raw Data Transfer) Checklist'
labels: BI Data Transfer
type: RAW DATA UPLOAD
assignees: 
projects: "cbmed/13"
---

If you have been assigned this task, please have a look at these wiki entires to help you complete it:
[WI_DU_TSO500: Raw Data QC and Transfer](https://labordatenbank.com/cbmed/documents/view/505)


## 0. Meta data:

- BI project number: `xxxx-xxxx`
- CBmed project number: `z.zz`
- Sample-Batch information: `samplebatch nr`
- Sequencing Run: `sequencingrun nr`
- TSO500 type: `ctDNA/FFPE`

## 1. Raw data transfer to CBmed

- [ ] 1.1 All runs finished sequencing & data transer to NAS3 complete:

    Date: `YYYY-MM-DD`
    Confirmed by: `HG/IoP-employee`

- [ ] 1.2 Flowcell writing to NAS3 finished, location: 

    `NAS3/Genomics/TSO500_[liquid/solid]/flowcells/<basename>`
- [ ] 1.3 Flowcell checksum created on NAS3 (ground truth)

    `NAS3/Genomics/TSO500_[liquid/solid]/flowcells/<basename>/<flowcell>.sha256`
- [ ] 1.4 DRAGEN output copy to NAS3 finished, location:

    `NAS3/Genomics/TSO500_[liquid/solid]/dragen/<basename>`
- [ ] 1.5 DRAGEN checksum at original source (HG-SSD) calculated
    
    `NAS3/Genomics/TSO500_[liquid/solid]/dragen/<basename>/<flowcell>.sha256`
- [ ] 1.6 DRAGEN checksum at NAS3 verified by: 
    
    `HG/IoP-employee or CBmed employee`


## 2. Quality Control

- [ ] 2.1 Checked folder structure according to BI cloud transfer agreement 
- [ ] 2.2 Run-QC & Bioinformatics-QC according to AP performed: 
    
     `NAS3/Genomics/TSO500_[liquid/solid]/dragen/<basename>/TSO500_QC_default_thresholds.<timestamp>.xlsx`
- [ ] 2.3 CBmed lab team informed of outcome
- [ ] 2.4 Internal QC investigation `completed/not necessary`
- [ ] 2.5 BI informed about QC outcome

---

## 3. **TQM Gate — STOP BEFORE UPLOAD**

**The operator must stop here and wait for approval from the TQM team.**  
Approval must be provided **as a comment to this issue**.

- [ ] 3.1 TQM approval received in comments  
      *(Operator checks this box only after approval comment is posted.)*

:warning: **Do not upload to BI before approval is given in writing.**

---

## 4. Raw data transfer to BI

- [ ] 4.1 Approval for BI-S3 raw data upload granted by BI
- [ ] 4.2 Flowcell data uploaded to BI S3 bucket: 

    `s3://bi-tmcp-cbsp-cbmed-validation-ctdna-liquid/data/cbmed_tso500_ctdna/`

- [ ] 4.3 DRAGEN uploaded to BI S3 bucket: 

    `s3://bi-tmcp-cbsp-cbmed-validation-ctdna-liquid/data/cbmed_tso500_ctdna/`

- [ ] 4.4 BI informed of completed upload

    - Employee: `CBmed employee`
    - Date: `DD. MM. YYYY`
    
---

## 5. Transfer Golden Helix results to BI

Transfer of Golden Helix data requested?

[ ] yes / [ ] no

If yes, please provide:

- [ ] 5.1 Golden-Helix data on NAS3, location: 

    `NAS3/Genomics/TSO500_[liquid/solid]/golden_helix/<basename>`

- [ ] 5.2 Golden-Helix uploaded to BI S3 bucket:

    `NAS3/Genomics/TSO500_[liquid/solid]/golden_helix/<basename>`

---

## 6. Comments

`comments, e.g. 0: measured together with other project on same flow cell; 2.1. Run-QC failed due to xyz`
