# FUTURE_CS_02 – Phishing Email Detection & Awareness System

## Executive Summary

This report presents the analysis of five email samples to identify phishing attacks and improve user security awareness. Each email was examined based on sender authenticity, domain legitimacy, email content, embedded links, attachments, urgency, and social engineering techniques.

The emails were classified into three categories: Safe, Suspicious, and Phishing. The findings demonstrate common tactics used by attackers and provide practical recommendations to help users identify and avoid phishing attempts.

---

## Objective

The objective of this project is to analyze phishing email samples, identify common phishing indicators, classify emails based on their risk level (Safe, Suspicious, or Phishing), and improve user awareness of phishing attacks.

This assessment aims to help users recognize malicious emails by examining sender authenticity, email content, URLs, attachments, and social engineering techniques. The project also provides practical recommendations and security awareness guidelines to reduce the risk of phishing attacks in both personal and organizational environments.

### Project Objectives

- Analyze real-world phishing email samples.
- Identify phishing indicators and social engineering techniques.
- Classify emails as Safe, Suspicious, or Phishing.
- Explain phishing attacks in simple and non-technical language.
- Provide practical prevention and awareness recommendations.
- Improve user awareness of email-based cyber threats.

---

## Scope

This assessment focuses on identifying phishing indicators in publicly available educational email samples.

The scope includes:

- Sender verification
- Subject line analysis
- URL inspection
- Attachment analysis
- Social engineering techniques
- Email classification
- User awareness recommendations

The assessment does not involve interacting with malicious links, executing attachments, or exploiting systems.

---

## Tools Used

- Kali Linux
- Visual Studio Code
- Git & GitHub
- Public Phishing Email Samples
- Browser Developer Tools
- Google Message Header Analyzer (Reference)
- MXToolbox Email Header Analyzer (Reference)

---

## Methodology

Each email sample was analyzed using the following methodology:

1. Verify sender identity.
2. Inspect sender domain.
3. Analyze subject line.
4. Review links and attachments.
5. Identify phishing indicators.
6. Assess social engineering techniques.
7. Classify email risk.
8. Document findings and recommendations.

---

## Email Sample Analysis

### Email Sample 1

| Field | Observation |
|--------|-------------|
| Sender | notifications@github.com |
| Subject | New sign-in to your GitHub account |
| Sender Domain | github.com (Trusted) |
| Attachment | None |
| Links | Official GitHub Security Log |
| Grammar | Correct |
| Urgency | Low |
| Credentials Requested | No |
| Risk Level | Safe |
| Classification | Safe |

#### Findings

- The sender uses a trusted GitHub domain.
- The email does not request passwords or OTPs.
- The URL points to the official GitHub website.
- The message is informational.

#### Evidence

- Email File: `evidence/emails/email_01.txt`
- Screenshot: `evidence/screenshots/01_legitimate_email_sample.png`

#### Verdict

🟢 **Safe**

**Reason:**

The email originates from a trusted sender domain, contains only official links, does not request passwords, OTPs, or sensitive information, and follows a professional communication style. No phishing indicators were identified.

---

### Email Sample 2

| Field | Observation |
|--------|-------------|
| Sender | no-reply@amazon.in |
| Subject | Your Amazon Order Has Been Shipped |
| Sender Domain | amazon.in (Trusted) |
| Attachment | None |
| Links | Official Amazon Orders Page |
| Grammar | Correct |
| Urgency | None |
| Credentials Requested | No |
| Risk Level | Safe |
| Classification | Safe |

#### Findings

- The sender uses the official Amazon domain.
- The email contains no suspicious attachments.
- The link directs to the official Amazon website.
- No passwords, OTPs, or sensitive information are requested.
- The language is professional and informative.

#### Evidence

- Email File: `evidence/emails/email_02.txt`
- Screenshot: `evidence/screenshots/02_legitimate_email_sample.png`

#### Verdict

🟢 **Safe**

**Reason:**

The email is sent from the official Amazon domain, provides order-related information only, contains a legitimate tracking link, and does not pressure the user to disclose confidential information.

---

### Email Sample 3

| Field | Observation |
|--------|-------------|
| Sender | support@micr0soft-security.com |
| Subject | Action Required: Verify Your Microsoft Account |
| Sender Domain | Look-alike domain (Not microsoft.com) |
| Attachment | None |
| Links | Non-official verification website |
| Grammar | Correct |
| Urgency | Medium |
| Credentials Requested | Verification Requested |
| Risk Level | Medium |
| Classification | Suspicious |

#### Findings

- The sender domain resembles Microsoft's official domain but is not genuine.
- The email creates urgency by mentioning account restrictions.
- The greeting is generic ("Dear Customer").
- Users should independently verify the sender before clicking any links.

#### Evidence

- Email File: `evidence/emails/email_03.txt`
- Screenshot: `evidence/screenshots/03_suspicious_email_sample.png`

#### Verdict

🟡 **Suspicious**

**Reason:**

The email contains multiple warning signs, including a look-alike sender domain, generic greeting, and urgency. Although it does not directly request credentials in the email body, users should avoid clicking the provided link and verify the request through Microsoft's official website.

---

### Email Sample 4

| Field | Observation |
|--------|-------------|
| Sender | security@icici-bank-support.com |
| Subject | Urgent: Your ICICI Bank Account Has Been Suspended |
| Sender Domain | Fake bank domain |
| Attachment | None |
| Links | Suspicious HTTP URL |
| Grammar | Mostly Correct |
| Urgency | High |
| Credentials Requested | Yes |
| Risk Level | High |
| Classification | Phishing |

#### Findings

- The sender domain does not match ICICI Bank's official domain.
- The email attempts to create panic using account suspension warnings.
- The verification link uses HTTP instead of HTTPS.
- The message attempts to trick users into revealing banking credentials.

#### Evidence

- Email File: `evidence/emails/email_04.txt`
- Screenshot: `evidence/screenshots/04_phishing_email_sample.png`

#### Verdict

🔴 Phishing

**Reason:**
The email impersonates a trusted financial institution, uses a fake sender domain, creates urgency, and attempts to redirect users to a fraudulent website to steal sensitive banking information.

---

### Email Sample 5

| Field | Observation |
|--------|-------------|
| Sender | billing@invoice-payment-services.com |
| Subject | Outstanding Invoice #45872 - Immediate Payment Required |
| Sender Domain | Unknown |
| Attachment | Invoice_45872.zip |
| Links | None |
| Grammar | Correct |
| Urgency | High |
| Credentials Requested | No |
| Risk Level | High |
| Classification | Phishing |

#### Findings

- The sender uses an unfamiliar domain.
- The email includes a ZIP attachment, which could contain malicious files.
- The message pressures the recipient with payment deadlines and penalties.
- The recipient is encouraged to open an unexpected attachment.

#### Evidence

- Email File: `evidence/emails/email_05.txt`
- Screenshot: `evidence/screenshots/05_phishing_email_sample.png`

#### Verdict

🔴 Phishing

**Reason:**
The email uses social engineering tactics, including urgency and financial pressure, to convince the recipient to open a suspicious ZIP attachment. Unexpected compressed attachments are a common method for distributing malware.

---

## Phishing Indicators Identified

| Indicator | Email 1 | Email 2 | Email 3 | Email 4 | Email 5 |
|-----------|:-------:|:-------:|:-------:|:-------:|:-------:|
| Trusted Sender Domain | ✅ | ✅ | ❌ | ❌ | ❌ |
| Generic Greeting | ❌ | ❌ | ✅ | ✅ | ✅ |
| Urgent / Fear-Based Language | ❌ | ❌ | ⚠️ | ✅ | ✅ |
| Suspicious URL | ❌ | ❌ | ✅ | ✅ | ❌ |
| Suspicious Attachment | ❌ | ❌ | ❌ | ❌ | ✅ |
| Requests Credentials | ❌ | ❌ | ⚠️ | ✅ | ❌ |
| Official HTTPS Website | ✅ | ✅ | ❌ | ❌ | N/A |

## Risk Matrix

| Risk Level | Description | Action Required |
|------------|-------------|----------------|
| 🟢 Safe | Legitimate email | No action required |
| 🟡 Suspicious | Requires manual verification | Verify the sender before interacting with the email. |
| 🔴 Phishing | Malicious email | Report the email immediately and delete it without interacting. |


## Risk Assessment

| Classification | Number of Emails |
|----------------|-----------------:|
| 🟢 Safe | 2 |
| 🟡 Suspicious | 1 |
| 🔴 Phishing | 2 |

### Common Social Engineering Techniques Observed

The following social engineering techniques were identified during the analysis:

- Urgency and fear-based language
- Fake sender domains
- Generic greetings
- Credential harvesting attempts
- Malicious attachments
- Look-alike domains (Typosquatting)


### Overall Assessment

Out of five analyzed email samples:

- **2** were identified as legitimate and safe.
- **1** contained suspicious characteristics that required verification before taking action.
- **2** were classified as phishing due to clear social engineering techniques, suspicious sender domains, and attempts to manipulate the recipient.

The analysis highlights the importance of verifying sender identity, checking links carefully, and avoiding unexpected attachments before interacting with email content.

## Prevention Guidelines

Users should follow these best practices to reduce the risk of phishing attacks:

- Verify the sender's email address before responding.
- Hover over links to inspect the destination URL before clicking.
- Never share passwords, OTPs, or sensitive information through email.
- Avoid opening unexpected attachments, especially ZIP or executable files.
- Access websites by typing the official URL manually instead of clicking email links.
- Enable Multi-Factor Authentication (MFA) on important accounts.
- Keep operating systems, browsers, and antivirus software updated.
- Report suspicious emails to the organization's IT or Security team.

## Do's and Don'ts

### ✅ Do's

- Verify the sender's domain.
- Inspect URLs before clicking.
- Report suspicious emails immediately.
- Enable Multi-Factor Authentication (MFA).
- Confirm unexpected requests through official communication channels.

### ❌ Don'ts

- Do not share passwords or OTPs via email.
- Do not click suspicious links.
- Do not download attachments from unknown senders.
- Do not trust urgent messages without verification.
- Do not ignore unusual account activity notifications.

## Recommendations

To reduce phishing risks, organizations and individuals should:

- Conduct regular phishing awareness training.
- Implement Multi-Factor Authentication (MFA).
- Enable email filtering and spam protection.
- Verify sender domains before responding.
- Block suspicious attachments.
- Encourage users to report suspicious emails immediately.
- Regularly update endpoint security software.

## Key Learnings

- Learned how to differentiate between Safe, Suspicious, and Phishing emails.
- Improved understanding of phishing indicators and social engineering techniques.
- Gained practical experience in analyzing email content, links, and attachments.
- Developed professional documentation skills by preparing a structured phishing awareness report.
- Understood the importance of user awareness in preventing phishing attacks.

## Business Impact

Effective phishing awareness reduces the likelihood of credential theft, financial fraud, malware infections, and unauthorized access to organizational systems. Regular user awareness training, combined with strong security practices, helps organizations strengthen their cybersecurity posture and reduce human-related security risks.


## Conclusion

This project demonstrated the practical process of identifying and classifying phishing emails based on sender authenticity, email content, URLs, attachments, and social engineering techniques.

The analysis showed that phishing attacks commonly rely on urgency, impersonation, fake domains, and malicious links or attachments to deceive users.

By following proper verification procedures and security awareness practices, individuals and organizations can significantly reduce the risk of successful phishing attacks.

This assessment also reinforces the importance of user awareness as one of the strongest defenses against modern cyber threats.