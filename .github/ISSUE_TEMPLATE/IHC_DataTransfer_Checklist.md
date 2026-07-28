---
name: IHC raw data transfer
about: Checklist for BI IHC projects
title: "[xxxx-xxxx] [y.yy/z.zz] batch[n] IHC QC gate 1 (Raw Data Transfer) Checklist"
labels: ["BI Data Transfer"]
type: RAW DATA UPLOAD
assignees: []
projects: ["cbmed/12"]
---

If you have been assigned this task, please read:  
https://github.com/cbmed/IT_ops_documentation/wiki/Upload-to-AWS-S3-buckets

## 0. Meta data:

- BI project number: `xxxx-xxxx`
- CBmed project numbers: 
    * `y.yy`
    * `z.zz`
- Panels:
    * `panel1`
    * `panel2`
- Sample-Batch information: `samplebatch nr`
- TSO500 type: `ctDNA/FFPE`
- Basefolder on NAS3 (<basefolder>):

 `<YYYYMMDD>_BI_<CBmedStudyNumber>_b<batchNumber>_r<runNumber>`

## 1. Raw data provision

- [ ] 1.1 Data provided & completeness confirmed by:

  * [ ] CBmed: `CBmed/IoP-employee`
 
  * [ ] IoP: `CBmed/IoP-employee`


- [ ] 1.2 Image data copied/writing to NAS3, location: 

    `NAS3/IHC/???/<basename>`
    
- [ ] 1.3 Image data checksum created on IoP server/NAS3 (ground truth)

    `NAS3/IHC/???/<basename>`

## 2. Quality Control & Metadata generation

- [ ] 2.1 Sample metadata generated
- [ ] 2.2 Stain metadata generated
- [ ] 2.3 Checked folder structure according to BI cloud transfer agreement 

---

## 3. **TQM Gate — STOP BEFORE UPLOAD**

**The operator must stop here and wait for approval from the TQM team.**  
Approval must be provided **as a comment to this issue**.

- [ ] 3.1 TQM approval received in comments  
      *(Operator checks this box only after approval comment is present.)*

:warning: **Do not proceed to upload before this approval is granted.**

---

## 4. Raw data transfer to BI

- [ ] 4.1 Approval for BI-S3 raw data upload granted by BI
- [ ] 4.2 Image data uploaded to BI S3 bucket: 

    `s3://bi-tmcp-cbsp-study-<study_id>/data/<assay_type>/`
    `s3://bi-tmcp-cbsp-study-<study_id>/data/<assay_type>/`

- [ ] 4.3 Checksums verified
- [ ] 4.4 BI informed of completed upload

    - Employee: `CBmed employee`
    - Date: `DD. MM. YYYY`

## 5. Comments

`comments, e.g. 0: Upload failed first time <reason>, specified handling for repeated measures: Copy mail`