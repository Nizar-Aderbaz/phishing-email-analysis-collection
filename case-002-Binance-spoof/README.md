# Overview

Case-002: Binance Spoof Phishing Email Analysis

This repository contains a hands-on analysis of a phishing email impersonating Binance, designed to mislead recipients into believing a withdrawal was processed. The analysis focuses on email headers, authentication checks, IP reputation, and phishing indicators.

## Project Details

Analyst: Nizar Aderbaz

Date of Analysis: 2025-06-19

Email Subject: "[Binance] Withdraw Successful – 2023-07-30 51:51:51(UTC)"

Sender (From): noreply-supportbinancewallet.irs@auswestbc.com.au (spoofed)

Recipient: phishing@pot

## Email Authentication

SPF: Pass (sender IP 69.169.224.12)

DKIM: Pass (signature verified for amazonses.com)

DMARC: None (no policy set for auswestbc.com.au)

## Received Path

Email sent via b224-12.smtp-out.eu-central-1.amazonses.com (69.169.224.12)

Received by MW2NAM12FT067.mail.protection.outlook.com with Microsoft SMTP Server

Message-ID: <01070189a93c67a5-2d72e19a-1525-41c6-92cb-347e9e7f27a5-000000@eu-central-1.amazonses.com>

## Tools & Resources

Thunderbird – email client inspection

MXToolbox Email Header Analyzer – automated header parsing

VirusTotal & AbuseIPDB – IP reputation checks

## Key Findings

Sender Spoofing: Email appears to be from Binance but uses a non-Binance domain (auswestbc.com.au).

Authentication: SPF and DKIM pass because the email is sent via Amazon SES, a legitimate email sending service, but the domain itself is not Binance.

Content Analysis: Urgent withdrawal notification designed to trick users into phishing schemes.

## Automation & Analysis

MXToolbox Email Header Analyzer was used to automatically parse headers, helping identify:

True originating IP and sending server (69.169.224.12)

SPF, DKIM, DMARC results

Relay servers

Automation reduces manual errors and speeds up phishing detection.
