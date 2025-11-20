---
name: TSO500 raw data transfer 
about: This is the checklist to be followed for all BI TSO500 projects with data from Human Genetics
title: '[xxxx-xxxx] [y.yy] batch[n] TSO500 QC gate (Raw Data Transfer) Checklist'
labels: BI Data Transfer
assignees: 
projects: "cbmed/13"
---

If you have been assigned this task, please have a look at these wiki entires to help you complete it:
[Upload-to-AWS-S3-buckets](https://github.com/cbmed/IT_ops_documentation/wiki/Upload-to-AWS-S3-buckets)


## 0. Meta data:

- BI project number: `xxxx-xxxx`
- CBmed project number: `z.zz`
- Sample-Batch information: `samplebatch nr`
- Sequencing Run: `sequencingrun nr`
- TSO500 type: `ctDNA/FFPE`
- Basefolder on NAS3 (<basefolder>):

 `<YYYYMMDD>_BI_<CBmedStudyNumber>_b<batchNumber>_r<runNumber>`

## 1. Raw data transfer to CBmed

- [ ] 1.1 Sequencing finished at HG on YYYY-MM-DD, reported by:

    `HG/IoP-employee`
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

- [ ] 2.1 Run-QC & Bioinformatics-QC according to AP performed: 
    
     `NAS3/Genomics/TSO500_[liquid/solid]/dragen/<basename>/TSO500_QC_default_thresholds.<timestamp>.xlsx`
- [ ] 2.2 CBmed lab team and HG informed of outcome
- [ ] 2.3 Internal QC investigation `completed/not necessary`
- [ ] 2.4 BI informed about QC outcome

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

## 5. Comments

`comments, e.g. 0: measured together with other project on same flow cell; 2.1. Run-QC failed due to xyz`