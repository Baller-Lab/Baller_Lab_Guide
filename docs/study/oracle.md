---
layout: default
title: Oracle
has_children: false
parent: Current Studies
has_toc: false
nav_order: 5
---

# Using Oracle
[Oracle](https://bbldm.pmacs.upenn.edu/bblmain/InitialDispatch) is the BBL-wide database that is used to keep track of all participants that choose to be a part of BBL studies. You will need to use Oracle to create a BBLID, which will become your participant’s identifier. You will also be able to see if your participant has participated in any other BBL studies, but the MS participants are typically new to the BBL and will have to have their information entered manually to create the ID. If there are ever any problems with Oracle, you can post in the Slack channel #oracle_isssues. 

## Making a BBLID in Oracle
Once you are onboarded, you should be able to log in to the [Oracle database](https://bbldm.pmacs.upenn.edu/bblmain/alarm/req_alarm.jsp). Navigate to the Main Menu and click on the `SUBJECT/FAMILY INFO`, and then `Search/Add New Proband`. Then, click `Enter New Proband`. Fill out the following information: Subject Status = Active, Firstname, Lastname, (check the box for no middle name), Date of Birth, Sex at Birth, Race, Ethnic, Source = Ext-Other, and write MS Patient in the Notes section. Once you are done adding this information, click `Enter`. Then, click `Add Contact/Family`, and hit `Yes` for “Do you need to add new contact for self/family”. Select “self_[FIRSTNAME]_[LASTNAME]”, and enter the Cphone and Email. Once you are done, click `Save`.

## Enroll Participant in MS/Depression Study
Now that you have a BBLID for your participant, you can enroll them in the MS Depression study. Navigate back to Home and click on `Study Enroll` in the left-hand toolbar. Enter the participant’s BBLID and click `get the subject`. Once their information populates, click `Do New Enroll`. Enter all required information. Select *853883_msdep_k23* for protocol, and *MS_group* for study group. Study_Status should be *not enrolled*. You can then hit `Save`. Your protocol participant should then appear as active in the protocol. After completing a study, return to this page and change the Study_Status to *completed*. 

## Logging Participant Contact in Oracle
You should also log how and when you contacted your participant in Oracle using the `Contact Entry` button in the left hand toolbar. Click `BBLID Search` to find your participant, and click `Contact Entry` to see a history of when and how the participant was contacted. Add new contact info at the bottom of the page if necessary. Click the envelope/phone icon on the far left to add a new contact entry for an existing mode of contact. Fill out necessary information to reflect the interaction you had with your participant. Make sure to also log contact and study information in the Saturn participant recruitment spreadsheet.

## Visit Info
During the visit, you will have to record the participants’ demographics. Starting at the Main Menu, navigate to `VISIT INFO` and then `Demos Store`. Enter the `BBLID`, click `Get the Subject`, and then click the red `Store` button. Select our protocol, and enter the following information:

- [ ]  Height(”)
- [ ]  Weight(lbs)
- [ ]  Measure_Way = Self-report
- [ ]  Gender_Identity
- [ ]  Sex Preference
- [ ]  Completed Education (in years)
- [ ]  Are you a student?
- [ ]  Are you currently employed?
- [ ]  What is your occupation/line of work?
    - [ ]  The question mark box will show the list of occupation categories. Choose the number that best corresponds with their job.
- [ ]  Name of Occupations
- [ ]  Marital Status
- [ ]  #Kids_Subject
- [ ]  Raised By
- [ ]  Ses_Income_Src*
- [ ]  Ses_Income_Household*
- [ ]  Living Arrangement
- [ ]  Ses_Property
- [ ]  Ses_Property_Value*
- [ ]  Ses_Residents
- [ ]  Ses_Bedrooms
- [ ]  Ses_Immigrant_Status
- [ ]  Ses_Citizenship
- [ ]  #Bio_Brothers
- [ ]  #Bio_Sisters
- [ ]  Birth_Order_Sub
- [ ]  #Half_Brother
- [ ]  #Half_Sister
- [ ]  Completed Education (in years)(Mother)
- [ ]  Mother Occupation
- [ ]  Name of Occupations
- [ ]  #Kids_Mother
- [ ]  Completed Education (in years)(Father)
- [ ]  Father Occupation
- [ ]  Name of Occupations
- [ ]  #Kids_Father
- [ ]  Were you ever adopted or in foster care?
- [ ]  Do you know bio parents?
- [ ]  Is English your primary/native language?
- [ ]  (Optional) Notes: If there is any additional information or something you need to clarify, you can write that here.
     
*For questions about education level, the question mark box will show the number of years and the corresponding degree.*

*For questions about occupation, the question mark box will show the job categories and their associated number. Choose the number that best corresponds with their job.*

*For the SES questions with a * use the ses PDF and share your screen when asking this question.*

## Medication
You will also have to enter the medications that the participant is on. Starting at the Main Menu, navigate to `MEDICATION`, the `Medicine Store`, enter `BBLID`, and then click `Get the Subject`. Choose `Do Medicine Entry`. Choose our `protocol`, your username for `CollectBy`, and then choose `Yes` for the questions “Are you taking any medicines regularly within the past 6 months, including aspirin and (females only) oral contraceptives?” and (if this shows up) “Do you have new medicines to enter for this collection?”. For each medication that they are on, enter the medicine name in *Medicine*, the total daily dosage in mgs in *Dosage(mg_day)*, *route*, when they started taking this medication in *Date/Med_Start*, and choose “yes” for *Is_Current*. Once you are done, click `Enter` to save. A few extra pieces of information:

- *Pharmclass* will generate automatically if you select one of the medicine options when typing it into the first column. It is okay if you cannot select a Medicine from the generated list, and it is okay if the Pharmclass is left blank.
- If the participant takes a certain medication more than once a day, enter the total daily dosage in *Dosage(mg_day)*, and then note the breakdown of usage in *Comments*.
- For *Route*, 1-PO is for pills and 2-DEC is for injections and infusions.
- We record supplements and vitamins.
