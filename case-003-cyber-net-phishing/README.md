🔹 Overview

Case-003: Cyber-Net Phishing Email Analysis

This repository contains a hands-on phishing email analysis conducted on a suspicious email claiming to be from “Philip Fredrick” (ghulammustafa@cyber.net.pk). The analysis focuses on identifying malicious indicators, verifying email authenticity, and assessing potential risks to users.

🔹 Project Details

Analyst: Nizar Aderbaz

Date: 2025-08-22

Email Subject: "86RE: Donation For You"

Sender: ghulammustafa@cyber.net.pk

Recipient: phishing@pot

🔹 Objectives

Analyze email headers for originating IPs and delivery paths.

Validate SPF, DKIM, and DMARC results.

Assess IP reputation using VirusTotal and AbuseIPDB.

Evaluate email content for phishing indicators.

Demonstrate automation in header analysis.

🔹 Tools & Resources

ThunderBird – email client inspection

MXToolbox Email Header Analyzer – automated header parsing

VirusTotal – IP reputation checks

AbuseIPDB – malicious IP reporting


🔹 Key Findings

Sender spoofing: From ghulammustafa@cyber.net.pk but replies redirected to philipffredrick3690@gmail.com

Authentication failures: SPF SoftFail, DKIM None, DMARC Fail

Malicious IPs:

147.78.103.9 → 191 reports on AbuseIPDB

159.27.24.86 → 29 reports on AbuseIPDB

Content quality: Poor grammar and social engineering attempts promising $10.5M

🔹 Automation & Analysis

MXToolbox Email Header Analyzer was used to automate parsing of email headers, quickly identifying:

SPF, DKIM, DMARC results

True originating IP

Relay servers
