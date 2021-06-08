# Release Notes

## HIV metadata package 2.2.2 is out with some improvements

**The structure of the package has been revised**

Please see the [README](/README.md).

**Updates to the HIV program tracker**

- Mobile optimisation

The following Program rules have been updated for mobile optimisation

| PR name                                                                                                                                                          | PR UID      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------- |
| ART- Hide "Treatment substitution/switches" section                                                                                                              | C63lr9lInLz |
| ART- Populate "Current Regimen" field with new regimen from previous event                                                                                       | fBPt4Z3xDLW |
| GBV- Display message "Please, specify type of abuse" if Health facility-based human rights violation is selected                                                 | Xl4V65lK0VW |
| GBV- Hide "Additional follow up planned" field if Issue has not been resolved                                                                                    | NTPbek598sE |
| GBV- Hide "Completed PEP" field if PEP for HIV is not selected                                                                                                   | N9OZh5jJ3us |
| GBV- Hide "Failure...", "Forced...", "Sharing...", "Stigmatizing..." and "Withholding..." fields if Health facility-based human rights violation is not selected | yEaQUbytZxG |
| GBV- Hide "Investigation details and follow up" section if not Related to index testing                                                                          | M5OSK7IN0cc |
| GBV- Hide "PEP for HIV" and "Completed PEP" fields if Sexual Type of abuse is not selected                                                                       | fZLdWdhxbUN |
| HSP- Hide "Consent given" if no consent requested                                                                                                                | blveTdklwED |
| HSP- Hide "Hot spot profile" sections + warning if no consent given                                                                                              | qkBXgISSSWe |
| HST- Hide "Method" field and "All HIV testing" sections if no verbal consent                                                                                     | WdubOKZZVTU |
| HST- Hide "Supervised HIV self-testing" section                                                                                                                  | GHwwsn2nLK7 |
| HST- Hide "Unsupervised HIV self-testing" section                                                                                                                | aVUvk1S1o4J |
| HTS- Hide "Accepted Index Testing" field if not offered                                                                                                          | HBJGsfcvbUI |
| HTS- Hide coupon number if not referred from EPOA                                                                                                                | h4ZFjjQRdMl |
| HTS- Hide "RTRI result" field if Was a rapid test for HIV-1 recent infection (RTRI) given? != Yes                                                                | ZenQt5jpSQ0 |
| HTS- Show warning if "Accepted Index Testing" = yes                                                                                                              | YimYXOivrxC |
| PREP- Hide "All follow up" sections if not started PrEP                                                                                                          | PXht445LZVU |
| PREP- Hide "Date of initiation" and "PrEP number" fields if not Started PrEP                                                                                     | uBH5bi8quWu |
| PREP- Hide "Drug dispensing" section if previous status is "LTFU" or "Stopped" and ! "Started PrEP"                                                              | WCWQoxKNxnl |
| PREP- Hide "Result of screening" if no screened                                                                                                                  | MbCWn03vUqP |
| PREP- Hide "Started PrEP" if not Offered PrEP                                                                                                                    | xe5VJGqcVh0 |
| PREP- Warning for "Date of initiation" compulsory field                                                                                                          | jc7zyZg2V2D |
| PREP- Warning for "Offered PrEP" compulsory field                                                                                                                | ESlgWDIQkeg |
| PREP- Warning for "PrEP status" compulsory field                                                                                                                 | XG8SM0Ca8Ts |
| RSK- Hide field "Sex with no condom" if not taking PrEP                                                                                                          | xC9FpkEIBPw |
| RSK- Populate KP_PREV Known Positive                                                                                                                             | knGf9Oxq0nq |
| RSK- Show warning if client is experience violence                                                                                                               | D2sOkUwvGrS |
| STI- Hide "Syndromes/symptoms" and "Treatment" sections if not diagnosed with STI                                                                                | zWSETNcVQwy |
| STI- Warning for "Treated for STI" compulsory field                                                                                                              | nUZGskgQ0Ox |
| TB- Hide "Date treatment initiated" if not Initiated treatment                                                                                                   | Hm6rUNH13CU |
| VL- Display message if RTRI test performed in HTS PS                                                                                                             | YHraOz4xQth |

---

- New DE added to ART register PS to capture pregnancy status at ART initiation: _HIV-ART Was the client pregnant at initiation of ART?_ (oUjswBooeZV)
- Option sets

  - ARV Regimen option set updated to include “Other” option (VPcknLagtZD)
  - Prior ARV option set updated to include “PrEP” (Qy6L4GUiqKP)
  - Reason for switch option set added, and added to Reason for switch data element as described below (uSG9Kozg4qK)

- New DEs added to ART register PS to capture additional information as requested by FHI 360 treatment team
  - HIV-ART Baseline CD4 added to initiation section (jPfI4GNXACX)
  - HIV-ART How many days of ART do you still have at home? Added to collect number of days of medication still at home during each visit. (I13RFEoZYjz)
  - HIV-ART Is client pregnant? Added for each visit if sex at birth= Female, to enable tracking of who is eligible for PMTCT. (QHhp1ewPO5i)
  - HIV-ART Notes about adherence added to Adherence section to allow recording of any notes. (PXyhzfBg2kG)
  - HIV-ART Other Reason for switch. Text field added after Reason for switch and displayed if Reason for switch=Other. (opKtYwYbqzu)
  - HIV-ART Other Regimen. Text field added after “Current regimen” and displayed if Current Regimen= Other. (TTbCuKjaAOl)
  - HIV-ART Other Regimen switch.Text field added after “New regimen” and displayed if New Regimen= Other. (a6jTONE9LXE)
  - HIV-ART Referred for: CD4. Referral field to allow documentation of CD4 referrals (aEWXJKtRk2F)
  - HIV-ART Referred for: PMTCT. Referral field to allow documentation of PMTCT referrals (w43Qhy11sai)
  - HIV-ART Referred for: Cervical cancer screening Referral field to allow documentation of Cervical cancer screening referrals (Yjsyom6DAVN)

* DEs in ART Register PS updated as described below:
  - HIV-ART Adherence counselling provided- Form name changed to “Adherence counselling provided” instead of “Discussed U=U” (kPGusGaXkds)
  - HIV-ART Reason for switch - Value type changed to Positive integer and option set added. (jf3UTHm5a8W)
  - HIV-ART Referred for: Tuberculosis- Form name changed from “Tuberculosis” to “TB diagnosis/treatment” (H4G6G1aB343)

Program rules updated/added

- **Updated**

  - fsKiuqxCfCW - ART- Hide "Current regimen", "Days of ART", "WHO clinical stage", "How many pills..." "Dispensing location", "Last date ART", "Next FU", Adherence questions, and "Treatment switches" fields if "Treatment status" is not Ongoing
    - Updated to hide new fields in ART Visit section.
  - S7olCzwAdBW ART- Populate "Last date with ART" - 2
    - Updated to match the design of the PrEP section, with two program rules used to calculate last date with ART. Last date with ART - 1 is added to account for new field How many days of ART do you still have at home?
  - yHeF4XOWsWt - ART- Show message on "Follow up date"
    - Updated to account for “How many days of ART do you still have at home?” when calculating the follow up date.

- **New**
  - Rr8qNO8dCKk - ART- Hide "How many pills do you still have at home" sections if Treatment status from previous event !=Ongoing
  - rkubKSxJKIs -ART- Hide "Is client pregnant" and "referred for PMTCT" and "referred for Cervical cancer" if sex at birth !=Female
  - hVFVcN63WUS - ART- Hide "New Regimen Other" field if New regimen !=Other
  - n5Zir9HxhBc - ART- Hide "Other reason for switch" field if Reason for switch!=Other
  - nw9DKMHbjY0 - ART- Hide "Other" field if Current Regimen !=Other
  - R9F2bYgfjkf -ART- Populate "Last date with ART" - 1
  - WMgw8EUQjy3 - ART- Populate "Other Regimen" field with new regimen from previous event
  - wGNkJ20FYa5 - ART- Populate "Other Regimen" field with other regimen from previous event
  - PWlM9SmWQOL - ART- Show warning for "How many pills at home" if value is > number of pills client had from last visit

## Program indicators

PIs corresponding to the MER indicators and required disgaggreations.  
Base PI are located in the MER Base PIs group (gFzL14jexLO)

## Indicators

Indicators corresponding to the MER indicators and required disgaggreations and match with the MER DE.  
Indicators are located in group prefixed by MER

## Data Set

Create two quarterly MER DS

- MER R: Community Based (zL8TlPVzEBZ)
- MER R: Facility Based (TBcmmtoaCBC)

Create a financial Year MER DS

- MER Target Setting: PSNU (Facility and Community Combined) (TARGETS) (YfZot37BbTm)

## Analytics

A new part has been added that contains the following element

- PI group that contains PIs used in the dashboards

PIs for case management reports (TqB4Yoo3HbJ)

- Dashboards
  - Achievement this Fiscal Year
  - ART Case Management
  - ART Dispensing
  - Custom reports
  - HIV Testing Appointments
  - PrEP Case Management
  - Referrals
