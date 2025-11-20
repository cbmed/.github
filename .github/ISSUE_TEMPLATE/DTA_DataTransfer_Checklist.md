---
name: BI EDT server upload checklist
about: This is the checklist to be followed for all BI EDT server uploads according to the according DTS
title: '[xxxx-xxxx] [y.yy] batch[n] QC gate (DTS Data Transfer) Checklist'
labels: BI Data Transfer
projects: "cbmed/13"
---

:yellow_dot: To be updated after internal discussion

## 0. Meta data:

- BI project number: `xxxx-xxxx`
- CBmed project number: `z.zz`
- Sample-Batch information: `samplebatch nr`
- Sequencing Run: `sequencingrun nr`

## 1. Quality Control

- 1.1 Should the Data Unit perform the Quality Control?
  - [ ] Yes
  - [ ] No
- [ ] 1.2 (if applicable) (Bioinformatics-)QC according to AP performed: 
    
     `<link/path to QC report>`

## 2. DTA Preparation

- [ ] 2.1 Scripts for Data transformation according to DTS finished
    - [ ] 2.1.1 Primary Script provided by:
       - Operator: `CBmed employee` (update wenn putting )
    - [ ] 2.1.2 Secondary Script provided by:
       - Operator: `CBmed employee` (update wenn putting )
    - [ ] 2.1.3 Both outputs were compared and are identical
    - [ ] 2.1.4 Post comparison checks/modification completed (No trailing new line etc.)

---

## 3. **TQM Gate — STOP BEFORE UPLOAD**

**The operator must stop here and wait for approval from the TQM team.**  
Approval must be provided **as a comment to this issue**.

- [ ] 3.1 TQM approval received in comments  
      *(Operator checks this box only after approval comment is present.)*

:warning: **Do not proceed to upload before this approval is granted.**

---

## 4. DTA Transfer
- [ ] 3.1 Upload to BI EDT Server completed and confirmed by BI:

    - Employee: `CBmed employee`
    - Date: `DD. MM. YYYY`
    - Filepath on Sharepoint: `<link/path to uploaded reults file(s)>`
    - Git-Commit: `__________________________________` 
    - Docker Image id: `__________________________________`

---

## 5. Comments

`comments, e.g. 0: Upload failed first time <reason>, specified handling for repeated measures: Copy mail`
