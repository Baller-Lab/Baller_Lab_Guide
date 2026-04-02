---
layout: default
title: Computerized Neurocognitive Battery (CNB)
has_children: false
parent: Current Studies
has_toc: false
nav_order: 7
---

# Penn Computerized Neurocognitive Battery (CNB)

[The Penn Computerized Neurocognitive Battery (CNB)](https://webcnp.med.upenn.edu) is a web application tool to assess cognitive function. The battery measures performance accuracy and speed on specific neurobehavioral domains using tests that were previously validated with functional neuroimaging. The Baller Lab uses an MS specific version of the CNB to collect cognitive data during participant visits. This battery takes approximately 1-2 hours depending on the participant, and includes 18 tasks with three built in breaks. 

## Accessing and Administering the CNB

You will need to complete a CNB training before you are able to access the administration site. This is currently organized by Tarlan Daryoush, and involves some readings, videos, and submitting a recording of you administering a CNB to a friend or colleague. Once you have login access, the test can be administered [here](https://webcnp.med.upenn.edu/). Make sure that you are provided with access to the battery msdep_k23_v3and the sites PRACTICE (for practicing) and  MSDEP (for administering the test to participants). Implement ProctTract as you go through the CNB to log data quality and make any notes about deviations or technical difficulties throughout the battery administration. Technical difficulties encountered during administration can be reported in the slack channel ‘cnb_issues_reports’ to get real-time troubleshooting help. Anything not resolved should be logged in notes.

## Steps to Start an Assessment

1. Click `Start Testing` to begin.
2. Under Battery, select `msdep_k23_v3`.
3. Under Site, if you are administering an actual assessment to a participant, select `MSDEP`. If you are doing a practice test, choose `PRACTICE`.
4. Enter the participants BBLID in `Subject ID`.
5. Select Browser in `Test platform`
6. Then, `Register Session`.
7. Click `Start`, and a new tab will appear. 
    1. Additionally, click the hyperlink `Track`. Read below for steps on using ProctTract. 
8. Enter the following information in the new page: Age, Year of birth, Sex, Handedness, Where are you taking the test?, and Do you speak English as a primary language?
    1. For education levels, you only need to enter EITHER the number of years completed or the highest level (text). You do not need to fill out both for all three people. 
9. Then, click `Register Session`. 
10. IF your participant is in-person, click `START`. IF your participant is on Zoom, copy the link in the middle of the page, and paste it into the Zoom chat, and ask your participant to open the link and share their screen. 
11. Then, administer the CNB based on the training you will have received.

## MS/Depression CNB Tasks

1. Motor Praxis Task
2. Psychomotor Vigilance Test
3. Digit Symbol Substitution Test
4. Penn Face Memory Test
5. Penn Word Memory Test

Break

6. Penn Continuous Performance Task
7. Penn Computerized Finger-Tapping Task
8. Penn Face Memory Test--Delayed Version
9. Penn Word Memory Test--Delayed Version

Break

10. Penn Conditional Exclusion Task
11. Letter N-Back Test
12. Measured Emotion Differentiation Test
13. Penn Matrix Analysis Test

Break

14. Visual Object Learning Test
15. Penn Logical Reasoning Test
16. Penn Emotion Recognition Test
17. Variable Short Line Orientation Test
18. Visual Object Learning Test

## Downloading CNB Data

You will have to download CNB data for analyses. On the [home page](https://webcnp.med.upenn.edu), select `VIEW DATA`, and then `REPORTS & NORM DATA`. Under `Raw data`, select `MSDEP` as the site, and then click Generate data report. Then, click `Export data`, and you will get the CSV including all CNB data. 

## Creating Feedback Reports

Some participants may ask for feedback on their CNB performance. Feedback can be obtained by making a request on behalf of the participant through [WebCNP](https://webcnp.med.upenn.edu/results.pl). 
1. Click `NEW REQUEST` and enter the participants' datasetID. You can find the participants' dataset ID using [this](https://webcnp.med.upenn.edu/results.pl) website, entering the BBLID into `SubID` in the basic search.
3. Keep Ruben Gur as the publisher and then hit `Continue`, and finish the request
4. Then, navigate to the website where you will [create the feedback report](https://webcnp.med.upenn.edu/feedback.pl)
5. Find the datasetID, and click `Create` and then `Generate Report`
6. The next page shows Participant Information, Battery Information and the Normative set Information (who your participant will be compared to) and Session Information. Please ensure all of this is correct before proceeding to the `Continue` to the next page.
7. Click `Edit` at the bottom of the page
8. Add your descriptive report in the comment box. Refer to the PennCNB_Clinical_Feedback_Report_SOP_v2.docx on the cnb_clinical_feedback channel on how to write the report.
9. Click `Save` after the report is completed
10. Post the url of the edited report on slack channel cnb_clinical_feedback and tag @Ruben Gur that report is ready for him to review/publish
11. Once the feedback report has been published by Ruben Gur, you can return to [this](https://webcnp.med.upenn.edu/request_feedback.pl) website, search for the report, and click `Download`
12. Save this report in Saturn, in the participants' feedback_materials folder

## Schedudling a Feedback Session

Dr. Baller will have to meet with the participant to review the feedback. Dr. Baller typically has three feedback slots available per week on Tuesday, from 9:00am-9:20am, 9:20am-9:40am, and 9:40am-10:00am. You will use the script below to offer feedback times to the participant. Once the participant has chosen a slot, you will email them a confirmation (with Dr. Baller cc'ed, script also below), and the Zoom link. Make sure that you have added Dr. Baller as a co-host in Zoom, and that you have added her as a required person on the outlook calendar invite. Furthermore, replace the slot in the Google Cal with the appointment, titled "BBLID Feedback Session", and add the Zoom link in the description. Once the session has been completed, Dr. Baller will let you know if they would like a copy of their report, if they are interested in being re-contacted for future studies, and if they want their report shared with their neurologist. If they want their report, use the Post Feedback Session Script, and include a copy of their report. If they want their neurologist to have access as well, bcc the neurologist on that same email. If they are interested in being re-contacted, add a 1 to the "Interested in Long. CNB Study?" column in the MS_Dep_Call_Log. If they aren't interested, add a 0. 

### Scheduling Script

Hi [Participant Name],

I hope this email finds you well! It was a pleasure getting to work with you this [week, month, etc.]. I wanted to follow up on the conversation we had regarding setting up a feedback session with Dr. Baller to discuss the results of your cognitive testing. Dr. Baller has the following appointments available over the next few weeks:

[insert multiple available appointments]

As a reminder, this would be an approximately 15–20 minute virtual appointment. Do any of these appointment times work for you? If not, please let me know and I can see what additional times may work.

Thanks again for participating in our research and I look forward to hearing from you soon!

Best,
[Coordinator Name]

### Confirming a Feedback Session Script

Hi [Participant Name],

You are scheduled for a feedback session with Dr. Baller (cc’d) on [date: day of the week, month, day, time]. Dr. Baller will meet you at the following link at that time: [insert link]. In the meantime, feel free to reach out to me if you have any questions or if any conflicts come up. 

Thank you again for participating in our research!

Best,
[Coordinator Name]

### Post Feedback Session Script

Hi [PT NAME],
 
Thank you again for participating in our study. Please find the results of your Computerized Neurocognitive Assessment. With your permission, we have sent your results to your MS Provider, [MS PROVIDER]. If you have any further questions or concerns, please feel free to contact me. 
 
Have a great rest of your day!
 
Best,
[COORDINATOR NAME]

