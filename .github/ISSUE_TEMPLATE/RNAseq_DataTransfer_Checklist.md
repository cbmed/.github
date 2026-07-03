---
name: RNAseq raw data transfer
about: This is the checklist to be followed for all BI RNAseq projects with data from Human Genetics
title: '[xxxx-xxxx] [y.yy] batch[n] RNASeq QC gate 1 (Raw Data Transfer) Checklist'
labels: BI Data Transfer
type: RAW DATA UPLOAD
assignees: 
projects: "cbmed/13"
---

If you have been assigned this task, please have a look at these wiki entires to help you complete it:
https://github.com/cbmed/IT_ops_documentation/wiki/Upload-to-AWS-S3-buckets

## 0. Meta data:

- BI project number: `xxxx-xxxx`
- CBmed project number: `z.zz`
- Sample-Batch information: `samplebatch nr`
- Sequencing Run: `sequencingrun nr`
- Basefolder on NAS3 (<basefolder>):

 `<YYYYMMDD>_BI_<CBmedStudyNumber>_b<batchNumber>_r<runNumber>`

## 1. Raw data transfer to CBmed

- [ ] 1.1 Sequencing finished at HG on YYYY-MM-DD, reported by:

    `HG-employee`
- [ ] 1.2 Flowcell writing to NAS3 finished, location: 

    `NAS3/Genomics/RNAseq_[liquid/solid]/flowcells/<basename>`
- [ ] 1.3 Flowcell checksum created on NAS3 (ground truth)

    `NAS3/Genomics/RNAseq_[liquid/solid]/flowcells/<basename>/<flowcell>.sha256`

## 2. Quality Checks of raw data

- [ ] 2.1 Checked folder structure according to BI cloud transfer agreement 
- [ ] 2.2 Created SampleSheet.csv and check with samshee2 was successful:
      `NAS3/Genomics/RNAseq_[liquid/solid]/flowcells/<basename>/SampleSheet.csv`
      
- [ ] 2.3 Run-QC according to AP performed: 
    
     `NAS3/Genomics/RNAseq_[liquid/solid]/flowcells/<basename>/SAV_RUN_QC_<flowcell>.xlsx`
- [ ] 2.4 CBmed lab team informed of outcome
      
## 3. **TQM Gate — STOP BEFORE UPLOAD**

**The operator must stop here and wait for approval from the TQM team.**  
Approval must be provided **as a comment to this issue**.

- [ ] 3.1 TQM approval received in comments  
      *(Operator checks this box only after approval comment is posted.)*

:warning: **Do not upload to BI before approval is given in writing.**

---

## 4. Raw data transfer to BI

- [ ] 4.1 Approval for BI-S3 raw data upload & subsequent analysis granted by BI
- [ ] 4.2 Flowcell data uploaded to BI S3 bucket: 

    `s3://bi-tmcp-cbsp-cbmed-validation-ctdna-liquid/data/cbmed_rnaseq_ctdna/`
- [ ] 4.3 BI informed of completed upload & checksum verification

## 5. Analysis on BI Seqera platform

- [ ] 5.1 All necessary pipelines run on BI Seqera platform (demultiplexing, RNA-seq, RNA fusions)
- [ ] 5.2 Results dowloaded to NAS3: 

    `NAS3/Genomics/RNAseq_[liquid/solid]/nf_core_rnaseq/<basename>/`
    `NAS3/Genomics/RNAseq_[liquid/solid]/nf_core_rnafusion/<basename>/`

## 6. Final Quality Checks
      
- [ ] 6.1 Run-QC according to AP performed: 
    
     `NAS3/Genomics/RNAseq_[liquid/solid]/nf_core_rnaseq/<basename>/RNAseq_QC_<timestamp>.xlsx`

- [ ] 6.2 Internal QC investigation `completed/not necessary`
- [ ] 6.3 BI informed about QC outcome

## 7. Comments

`comments, e.g. 0: measured together with other project on same flow cell; 2.1. Run-QC failed due to xyz`
