🔹 Overview

This repository contains a hands-on analysis of a phishing email impersonating Microsoft Account Team, designed to trick recipients with fake “unusual sign-in activity” alerts. The analysis focuses on email headers, authentication checks, IP reputation, and phishing indicators.

🔹 Project Details

Analyst: Nizar Aderbaz

Date of Analysis: 2025-06-04

Email Subject: "Microsoft account unusual signin activity"

Sender (From): no-reply@access-accsecurity.com (spoofed)

Recipient: phishing@pot

Reply-To: sotrecognizd@gmail.com

🔹 Email Authentication

SPF: None (sender IP 89.144.44.2)

DKIM: None (message not signed)

DMARC: Permerror (domain policy could not be validated)

🔹 Received Path

Sending IP: 89.144.44.2 (thcultarfdes.co.uk)

Message-ID: <032672b4-77ca-42f8-a036-9711e91bd1f3@DB8EUR06FT032.eop-eur06.prod.protection.outlook.com>

Return-Path: bounce@thcultarfdes.co.uk

🔹 Tools & Resources

Thunderbird – email client inspection

MXToolbox Email Header Analyzer – automated header parsing

VirusTotal & AbuseIPDB – IP reputation checks

🔹 Key Findings

Sender Spoofing: Email claims to be from Microsoft but originates from a non-Microsoft domain (access-accsecurity.com).

Authentication Failures: SPF and DKIM are missing; DMARC policy cannot be validated → high phishing risk.

Reply-To Mismatch: Any replies are redirected to attacker-controlled Gmail (sotrecognizd@gmail.com).

Content Analysis: Urgent “unusual sign-in” language designed to steal credentials.

🔹 Automation & Analysis

MXToolbox Email Header Analyzer was used to automatically parse headers, enabling:

Identification of SPF, DKIM, DMARC results

Discovery of originating IP and mail server path

Faster phishing detection and reduced manual errors
