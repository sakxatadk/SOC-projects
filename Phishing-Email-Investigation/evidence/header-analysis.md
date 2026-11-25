Email Header Analysis

1. Sample Information

- Sample: Synthetic phishing email
- File: phishing-email.eml
- Investigation type: Email header analysis
- Purpose: Identify suspicious sender information and header inconsistencies.

2. Header Examination

| Header | Observed Value | Analysis |

| From | security@secure-bank.example | Claims to represent a bank |
| To | customer@example.com | Intended recipient |
| Reply-To | support@secure-bank-login.example | Different domain from From |
| Return-Path | Not available | Cannot identify envelope sender |
| Received | Not available | Delivery route cannot be established |
| Subject | Urgent: Your Account Will Be Suspended! | Uses urgency and fear |
| Message-ID | training-001@secure-bank.example | Matches From domain but does not authenticate sender |
| Date | Tue, 25 Nov 2026 | Weekday does not match calendar date |
| Authentication | Simulated SPF/DKIM/DMARC failures | Not independently verified |

3. Suspicious Indicators

1. Reply-To domain differs from From domain.
2. Subject uses urgent account suspension language.
3. The date contains a weekday mismatch.
4. The sample contains simulated authentication failures.
5. The message contains a suspicious account verification URL.

4. Missing Information

- Actual Return-Path header
- Actual Received headers
- Sending mail-server IP
- Verified authentication results

5. Preliminary Assessment

The sample contains multiple suspicious characteristics
consistent with a phishing attempt.

However, this is a synthetic training email. Its headers
were manually created and do not represent an actual
delivered email.

Further investigation is required to examine the URL,
authentication indicators and other evidence.

6. Conclusion

The email demonstrates several common phishing
characteristics, particularly sender/reply-address
inconsistency and urgency-based social engineering.

Verdict: Simulated phishing sample.
