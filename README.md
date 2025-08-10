# Internship project 
# Task 2 - Phishing Email Analysis Report

## Basic Information

| Field           | Value          |
|-----------------|--------------- |
| **File Name**   | sample-101.eml |


## Summary of Steps Taken

Downloaded a sample phishing email (.eml file) from an Opensource GitHub repository.

Opened the email using Claws-email on Kali Linux.

Copied the email header from Claws-email.

Analyzed the header using MXToolbox Header Analyzer. 

### 📥 Source of Sample Phishing Email

The sample phishing email used in this task was downloaded from the following open-source repository:

🔗 [rf-peixoto/phishing_pot – GitHub Repository](https://github.com/rf-peixoto/phishing_pot/tree/main)

> This repository contains various examples of phishing emails for educational and research purposes.

---
# Email Overview

    From: Microsoft account team no-reply@microsoft.com
    To: phishing@pot
    Subject: Microsoft account unusual sign-in activity
    Date: Thu, 3 Nov 2022 02:44:27 +0000
    Reply-To: media-protection@usual-assist.com

# Sign-in Activity Details

    Country/Region: Russia/Moscow
    IP Address: 103.225.77.255
    Date of Sign-in: Thu, 03 Nov 2022 02:40:58 +0000
    Platform: Windows 10
    Browser: Firefox

# Message Summary

    A user from Russia/Moscow logged into the account "phishing@pot" from a new device.
    Instructions given:
        If this was not you, report the user.
        If this was you, no further action is required for similar activity in the future.


# 🔎Header Analysis

| Field            | Details                                               |
|------------------|------------------------------------------------------|
| **From**         | Microsoft account team no-reply@microsoft.com        |
| **Reply-To**     |  media-protection@usual-assist.com                   |
|**Sign-in Country**| Russia/Moscow                                        |
|**IP Address**    |103.225.77.255                                        |
|**Date**          | Thu, 03 Nov 2022 02:40:58 +0000                      |
| **Subject**      | Microsoft account unusual signin activity            |
|**Platform**      | Windows 10                                           |
|**Browser**       |Firefox                                               |


---

## 🎣Phishing Indicators Identified

| Indicator Type             | Description                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------|
| **Spoofed Email Address**  | Appears to be from Microsoft, but originates from an unrelated domain.                               |
| **Fake Reply Address**     | Replies are directed to a non-corporate email address.                                  |
| **Suspicious Links**       | Links in the email lead to unexpected destinations, such as personal email accounts instead of official sites.|
| **Threatening/Urgent Language** | Uses urgent language: “If this wasn't you, please report the user"                             |                            
| **Mismatch in Message & Links** | Appears to be a login alert, but links open an email composer instead of a Microsoft page.      |
| **Grammar Errors**         | Phrases like "unusual sign.in activity", inconsistent spacing/punctuation.                                   |
| **Unfamiliar IP/Location** | Claims a login from “Russia/Moscow” using `103.225.77.255` to induce fear.                          |
| **No Official Branding**   | No digital signature, official footer, or policy links.                                             |

---

## ✅ Summary 

| Field                | Finding/Red Flag                                                                                      |
|----------------------|-------------------------------------------------------------------------------------------------------|
| **From**             | Microsoft account team no-reply@microsoft.com                                                         |
| **Reply-To**         | media-protection@usual-assist.com                                                                     |
| **SPF/DKIM/DMARC**   | Not configured/failed                                                                                 |
| **Sender IP**        | 103.225.77.255                                                                                                                 |
| **Subject**          | Urgent, threatening language                                                                          |
| **Links**            | “Report the User” goes to Gmail, not Microsoft                                                        |
| **Grammar/Branding** | Errors and missing official branding                                                                  |
| **Claimed Location** | Russia/Moscow, unfamiliar IP to Induce Fear                                                           |

---

##  Conclusion

This email contains multiple classic phishing indicators, including:

- Spoofed sender and reply addresses
- Urgent and manipulative language
- Suspicious links and tracking pixels
- Authentication failures (SPF/DKIM/DMARC)
- Grammar errors, and lack of branding

**Recommendation:**  
Do not interact with the similar mail. Mark it as phishing and report it to your IT/security team. Use this analysis as a reference for identifying similar threats in the future.

---
