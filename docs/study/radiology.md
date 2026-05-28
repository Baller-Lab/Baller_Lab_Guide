---
layout: default
title: Radiology
has_children: false
parent: Current Studies
has_toc: false
nav_order: 14
---
# Navigating Scans from Radiology and RADAR
This study uses clinical scans that need to be acquired from RADAR or another radiology group. Please follow these steps to understand how to:
1) Find scan accession numbers and where to record them
2) Request scans from RADAR
3) Sort through the scans
4) Process the scans

# Finding Accession Numbers
Accession numbers are the unique identifer that is used for each unique scan or group of scans. To run the analysis pipelines, each participant needs to have a (preferably sagittal) FLAIR and T1 scan. Use the following steps to find and record accession numbers, that will later be used to request the scans be delivered from RADAR.

1) Open PennChart/Epic and search for the patient in `Chart Review` using their MRN.
2) Navigate to the `Imaging` tab and click on the **MR HEAD MS [W AND WO IV Contrast, Post Processing, etc.]** scan that is closest to when their visit was.
3) First, record the accession number associated with this scan in the Call Log, in the `MR MS HEAD Accession Number` column.
4) Then, click the hyperink `Show images for [scan name]`, which will open Sectra UniView.
5) Look for the following scans: **"SAG T1 MPRAGE BRAIN"** and **"SAG T2 FLAIR BRAIN"** (or something very similar). They should have 160 or 176 slices.
6) If you find either or both of those scans within the first folder of scans, record the accession numbers in their respective columns in the Call Log: `FLAIR Acc Num` and `T1 Acc Num`.
7) If you didn't find either or both of the scans, find the **MR SOURCE IMAGES** folder from the same date, and look for the missing scans there.
8) Record all accession numbers in the Call Log, and if you cannot find one or both scans, record that in the Call Log (but this should be screened before scheduling a participant).

# Requesting Scans from RADAR
To receive the desired scans, you will have to submit a request through [RADAR](https://www.med.upenn.edu/radar/how-to-request-data). 

1. Submit the request through this [application form](https://redcap.med.upenn.edu/surveys/?s=7WDNCDR8EW8H9D4F).
2. Fill out all the required information. Indicate that you would like the images transferred to on-premise storage. 
3. You must attach an excel sheet with a single column of accession numbers. These will come from the Call Log from the previous section.
4. Dr. Baller will follow up with an email of the exact location in PMACS that the scans will be delivered to.

# Sorting Through Scans
RADAR will deliver all scans associated with each accession number, which will include more scans than you need. These steps will guide you through the process.

## Dcm2bids
All scans will be delivered in dicom format, but we want them as niftis in [BIDS format](https://bids.neuroimaging.io/index.html).

1. On PMACS, navigate to `/project/msdepression/data/20251014_radar_transfer_k23/bids_orig/code/convert_dicom_to_bids.sh`.
   i.  Change `root` to the new directory of scans. 
2. Once this is done, you will run CuBIDS.

## CuBIDS
To organize the scans, use [CuBIDS](https://cubids.readthedocs.io/en/latest/).

1. on PMACS, navigate to `/project/msdepression/elena_mimosa_project/scripts/cubids`.
  i. Refer to the README_cubids document for information on how to prepare your terminal and steps to take before running the code.
2. Run the appropriate script.

## Analyzing the CuBIDS Output
To make sure that all scans were received and filtered appropriately through dcm2bids and CuBIDS, you should use the following steps:

1. Run cubids on bids output (after dcm2bids) and move output to local directory.
2. Run `~/Library/CloudStorage/Box-Box/BBL/msdepression/scripts/checking_radar_pull_completeness/20260513_checking_radar_completeness_late_2025_pulls.Rmd`
3. Open spreadsheet to identify where there are full sets and gaps `~/Library/CloudStorage/Box-Box/BBL/msdepression/CuBIDS_outputs/RADAR_pulls/late_2025_early_2026/eb_summary_radiology_pulls_mapped_to_good_data_20260515`
4. Next, you should start looking at why there are gaps. Here are some common trends and how to look them up:
   1. **Scan has the wrong dimensions.**
      1. This suggests that the scan was reconstructed somehow.
      2. First, go into the sourcedata_niftis directory, navigate to the NEW accession number, do ls `*MPRAGE*` or `*FLAIR*` to see if you can find the scans.
      3. If you find the scans, run a 3dinfo <name of scan> to see if you can find a scan with the right dimensions (1x1x1)
         1. If yes:
            1. more `/project/msdepression/data/20251014_radar_transfer_k23/bids_orig/code/dcm2bids_config.json`
            2. Look for SeriesDescription options, copy into your terminal and do an ls *copied material*. You are trying to identify whether the scan that is good would be caught by the current cubids search.
            3. If yes:
               1. more <name of file.json> | grep "ImageType"
               2. If ImageType in your json does not match any of the dcm2bids_config.json, you need to add a new group that searches for the string that will capture your file and contains the imageType that you have.
            4. If no:
               1. Develop a wildcard search that would capture your scan.
               2. more <name of file.json> | grep "ImageType"
               3. Add a new group that searches for the string that will capture your file and contains the imageType that you have.
               4. If no, it might be in the MR Source folder:
                  1. First, check second new accession to see if it exists in the appropriate pull. If not,
                  2. Check for good files in the 20251126_radar_transfer_source_images_k2. Check both new accession numbers.
                  3. If not available, go to Epic, and search patient by EMPI/UID.
                  4. Navigate to Images, and search for the scans that happened on the Scan.Date.
                  5. Look for MR Source Images, record the accession number and verify that it is different than the MS post process or MS BRAIN accession.
                  6. Open the scan, click "show images" and look for a SAG T1 with 176 slices, or a SAG T2 FLAIR with 160 slices.
                  7. If you find these, record which folder you found it in, and what the accession is for the missing scan.
    2. **Scan cannot be found.**
       1. It may be in the MR Source folder. First, check second new accession to see if it exists in the 20251014 pull. If not,
       2. Check for good files in the 20251126_radar_transfer_source_images_k2. Check both new accession numbers.
       3. If not available, go to Epic, and search patient by EMPI/UID.
       4. Navigate to Images, record the accession number and verify that it is different than the MS post process or MS BRAIN accession.
       5. Open the scan, click "show images", and look for a SAG T1 with 176 slices, or a SAG T2 FLAIR with 160 slices.
       6. If you find these, record which folder you found it in, and what the accession is for the missing scan.

    After following these steps and retrieving all the scans, you can run any of the pipelines in PMACS.








