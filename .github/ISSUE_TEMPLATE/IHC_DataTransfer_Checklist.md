---
name: IHC raw data transfer
about: Checklist for BI IHC projects
title: "[xxxx-xxxx] [y.yy] batch[n] IHC QC gate 1 (Raw Data Transfer) Checklist"
labels: ["BI Data Transfer"]
type: RAW DATA UPLOAD
assignees: []
projects: ["cbmed/12"]
---

If you have been assigned this task, please read:  
https://github.com/cbmed/IT_ops_documentation/wiki/Upload-to-AWS-S3-buckets


## 0. Meta data

- **BI project number:**  
  `xxxx-xxxx`

- **CBmed project number:**  
  `z.zz`

- **Sample-batch information:**  
  `samplebatch nr`

- **Basefolder on NAS3 (<basefolder>):**  
  `<NAS3>/<path-to-directory>`


---

## 1. **TQM Gate — STOP BEFORE UPLOAD**

**The operator must stop here and wait for approval from the TQM team.**  
Approval must be provided **as a comment to this issue**.

- [ ] 3.1 TQM approval received in comments  
      *(Operator checks this box only after approval comment is present.)*

:warning: **Do not proceed to upload before this approval is granted.**

## 2. Raw data transfer to BI

- [ ] **1.1** Approval for BI-S3 raw data upload granted by BI  
- [ ] **1.2** IHC data uploaded to BI S3 bucket  
      `/<path-to-directory>`
- [ ] **1.3** BI informed of completed upload  
      (including QC output in email)


---

## 3. Comments

```
Comments: 
```
