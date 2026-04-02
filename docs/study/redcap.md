---
layout: default
title: REDCap
has_children: false
parent: Current Studies
has_toc: false
nav_order: 6
---

# REDCap Axis vs PMACS
We use two different versions of REDCap: [REDCap Axis](https://axis.med.upenn.edu/index.php?action=myprojects) and [REDCap PMACS](https://redcap.med.upenn.edu). Axis is used for the consent forms and self-report questionnaires, while PMACS is used for C2 forms. 

## REDCap Axis
You will have two projects: “MS Depression [853883] Consent #consents” and “MS Depression Collection Scales #collection”.

### Consents
At the beginning of each visit, you will have to read the consent form to the participant, and they will have to sign it prior to participating in the study. To create a new consent form:

1. Click `Add / Edit Records`
2. Click `+ Add new record`
3. Click the bubble on the Admin row in the `Status` column
4. Enter the required information
    1. Ensure that the Consent Approval Date is the most recent date
5. Then, click `Save & Go To Next Form`
6. Ensure that all the rows are set to “Yes”
7. Set the form to be “Complete” in the `Complete?` row
8. To open it up for a participant, click `Survey options`, and then `Open Survey`
9. If virtual, send this newly opened link to your participant. If in-person, this will be done on the assessment room desktop computer. 

You will read each page to the participant, allowing them to ask questions after each page, and at the end of the consent form. You will also offer the the option to download the signed consent form at the end. After the consent form has been signed, you will save it:

1. By Actions:, click `This data entry form with saved data (via browser’s Save as PDF)`
2. Save PDF, naming it [BBLID]_MSDepression853883Consent_MM_DD_YY
3. Put the saved PDF into Saturn in the Virtual_Consents folder

### Self-Report Questionnaires
You will also be collecting self-report scales from each participant. To create a new scale form:

1. Click `Add / Edit Records`
2. Click `+ Add new record`
3. Click the bubble on the Admin row in the `Status` column
4. Enter the required information
    1. If the participant is in-person, select *In-person proctored* in `Assessment Method`
    2. If the participant is virtual, select *Self-administered but monitored* in `Assessment Method`
5. `Time point` will always be 1
6. Set the form to “Complete”
7. Then, click `Save & Go To Next Form`
8. Set the form to be “Complete” in the `Complete?` row, and then click `Save & Go To Next Form`
9. To open it up for a participant, click `Survey options`, and then `Open Survey`
10. If virtual, send this newly opened link to your participant. If in-person, this will be done on the assessment room desktop computer. 

*Once the scales are completed, navigate to the `Scales Validation` page, and set it to `Valid` (assuming the scales are valid). Then set it to `Complete`, and `Save and & Exit Form`.* 

You will download them as a PDF and save in Saturn:

1. Navigate to the `Scales Admin` page
2. By Actions:, click `All forms/surveys with saved data (compact)`
3. Save PDF, naming it [BBLID]_MSDepressionCollectionScalesCo_[YYYY]-[MM]-[DD]_[####].pdf
4. Put the saved PDF into Saturn in the `Participants` folder, within the folder of their BBLID
    1. Path: Participants/[BBLID]/feedback_materials/ADD SCALES HERE
  
### Downloading All REDCap Axis Data
You will occasionally have to download all REDCap collection scales for analysis. You can do so by:
1. Click `Data Exports, Reports, and Stats` under the `Applications` list on the left hand side.
2. In the `All Data` row, choose `Export Data`
3. Export format will be CSV / Microsoft Excel (raw data)
4. Click `Export Data`

****

## REDCap PMACS

REDCap PMACS can be accessed [here](https://redcap.med.upenn.edu). The project is named “Neuropsych Subject Payment Signature #clinical”. 

**To create a new C2 form:**

1. `Add / Edit Records`
2. `+ Add new record`
3. Select the bubble next to `Payment Admin`
4. Enter all required information
    1. *Fund number*: 587537
    2. *CREF Number*: 5273
    3. *Description of Visit*: Visit 1 of 1, CNB+GOA, MM/DD/YYYY
    4. *Payment method*: Greenphire ClinCard
    5. *Remuneration/5316 Human Subject Payments (dollars)*: 80.00 (assuming they completed BOTH the CNB and GOA)
    6. *5206 (Non-Employee Travel) Expenses (dollars)*: 0.00
    7. *Other (5241 Patient Care Supplies) Expenses (dollars)*: 0.00
    8. *Grand Total Payment Amount (dollars)*: 80.00
5. Set form to `Complete`, then hit `Save & Go To Next Record`
6. Click the following boxes:
    1. This study does not have an IRB waiver of HIPAA
    2. No W-9 required - petty cash payment is less than $2,000. 
    3. (If applicable): Subject is an employee of UPHS, CPUP, or UPenn
7. `Save & Exit Form`

**To get their signature:**

1. Open the `Subject Signature Collection` page
2. In Survey options, choose `Open Survey`
3. Send the link to the participant
4. Ask them to type their signature, sign their signature, and enter today’s date (can press the Today button to generate)
5. Once they click to the second page, ask them to verify that all the information looks correct by clicking on the white box within the yellow box at the bottom.
6. Once that has been clicked, they can submit

**Saving a C2 form:**

1. Download as a PDF
2. Navigate to Saturn, using the *Virtual_C2 folder*
3. Each month and year should have its own folder
4. Choose the appropriate one, and then create a new folder within, named the BBLID
5. Within that folder, put the saved C2 form in
    1. The path should look like: Virtual_C2/[Month]_[YYYY]/[BBLID]/PUT C2 FORM HERE
