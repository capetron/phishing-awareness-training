# Phishing Awareness Training

A comprehensive phishing awareness training resource with safe, redacted phishing email examples, identification techniques, reporting procedures, quiz questions for security awareness programs, and a presentation slides outline. Designed for organizations building or improving their security awareness training program.

## Table of Contents

- [Why Phishing Training Matters](#why-phishing-training-matters)
- [Types of Phishing Attacks](#types-of-phishing-attacks)
- [Phishing Email Examples (Safe/Redacted)](#phishing-email-examples-saferedacted)
- [How to Identify Phishing Emails](#how-to-identify-phishing-emails)
- [Reporting Procedures](#reporting-procedures)
- [Social Engineering Beyond Email](#social-engineering-beyond-email)
- [Building a Security Awareness Program](#building-a-security-awareness-program)
- [Quiz Questions](#quiz-questions)
- [Presentation Slides Outline](#presentation-slides-outline)
- [Phishing Simulation Best Practices](#phishing-simulation-best-practices)
- [Metrics and Measurement](#metrics-and-measurement)
- [About Petronella Technology Group](#about-petronella-technology-group)

## Why Phishing Training Matters

Phishing remains the number one initial access vector for cyberattacks. According to industry reports, over 90% of successful cyberattacks begin with a phishing email. The median time for a user to click a phishing link is under 60 seconds after opening the email.

Technical controls (email filtering, safe links, sandboxing) catch most phishing attempts but cannot stop all of them. The human layer is both the most vulnerable and the most adaptable defense. A well-trained workforce reduces phishing click rates from an industry average of 30% to under 5%.

**Business impact of phishing:**
- Average cost of a successful phishing attack: $4.76 million (per IBM Cost of a Data Breach Report)
- Business email compromise (BEC) losses: $2.7 billion annually (FBI IC3)
- Average downtime from ransomware delivered via phishing: 20+ days

## Types of Phishing Attacks

| Type | Description | Target | Example |
|------|-------------|--------|---------|
| **Email phishing** | Mass phishing sent to many recipients | Anyone | Fake invoice, package delivery |
| **Spear phishing** | Targeted at specific individuals | Specific employee | Personalized message referencing real projects |
| **Whaling** | Targeted at executives | C-suite | Fake legal notice, board meeting |
| **BEC** | Impersonates executive or vendor | Finance team | "Wire $50K to new vendor account" |
| **Smishing** | SMS-based phishing | Mobile users | Fake bank alert, package tracking |
| **Vishing** | Voice/phone phishing | Anyone | Fake IT support, IRS scam |
| **QR phishing (Quishing)** | Malicious QR codes | In-person/email | Fake parking meter, Wi-Fi login |
| **Clone phishing** | Resends legitimate email with malicious link | Previous recipients | "Updated attachment" from known sender |
| **Callback phishing** | Email asks you to call a number | Anyone | Fake subscription renewal |

## Phishing Email Examples (Safe/Redacted)

The following examples are redacted recreations of real phishing emails. All URLs, email addresses, and identifying information have been replaced with safe placeholders.

### Example 1: Fake Microsoft 365 Password Expiry

```
From: security@micros0ft-support[.]com      <-- Misspelled domain
To: employee@example.com
Subject: [Action Required] Your password expires in 24 hours

Your Microsoft 365 password will expire on April 8, 2026.

Click here to update your password now:
https://login.micros0ft-support[.]com/update  <-- Fake URL

If you do not update within 24 hours, your account will be locked.

Microsoft 365 Security Team
```

**Red flags:**
- Misspelled sender domain (`micros0ft` with a zero instead of 'o')
- Urgency and threat ("locked in 24 hours")
- Link URL does not go to microsoft.com
- Microsoft never sends password expiry emails with direct links

### Example 2: Fake Invoice / Payment Request

```
From: accounting@trusted-vendor[.]net       <-- Lookalike domain
To: accounts-payable@example.com
Subject: Invoice #INV-2026-4419 - Payment Overdue

Please find attached the overdue invoice for services rendered.

Payment of $12,450.00 is due immediately. Wire transfer details
have been updated -- please use the new bank account below:

   Bank: First National Bank
   Routing: 021XXXXXX
   Account: 98XXXXXXXX

Please confirm payment within 24 hours to avoid late fees.

[ATTACHMENT: Invoice-INV-2026-4419.pdf.exe]   <-- Double extension
```

**Red flags:**
- Changed bank account details (common BEC tactic)
- Urgency ("due immediately," "within 24 hours")
- Attachment has double extension (.pdf.exe)
- Sender domain is similar but not the actual vendor's domain

### Example 3: Fake HR / Shared Document

```
From: hr-department@example-corp[.]com
To: all-staff@example.com
Subject: Updated Employee Handbook - Please Review and Sign

Hi Team,

The updated 2026 Employee Handbook is now available. All employees
must review and acknowledge by end of business Friday.

Review Document: https://docs-google[.]com/shared/handbook
                  <-- Fake Google Docs lookalike domain

Please log in with your company credentials to access the document.

Human Resources
```

**Red flags:**
- Sender domain is not the actual company domain
- Link goes to `docs-google[.]com` instead of `docs.google.com`
- Asks for credentials on an external page
- Generic greeting ("Hi Team")
- Deadline pressure

### Example 4: Fake IT Support / MFA Request

```
From: helpdesk@example.com (SPOOFED)
To: employee@example.com
Subject: MFA Verification Required - Unusual Sign-In Detected

We detected an unusual sign-in attempt on your account from:
   Location: Moscow, Russia
   Device: Unknown Linux Desktop

If this was not you, verify your identity now:
https://example-verify[.]com/mfa-check

If you do not verify within 1 hour, your account will be suspended.

IT Security Team
```

**Red flags:**
- Spoofed internal sender address (check email headers)
- Fear-based urgency (unusual sign-in, suspension threat)
- External link for an internal process
- Legitimate MFA alerts do not ask you to click links

### Example 5: QR Code Phishing

```
From: parking@example.com (SPOOFED)
Subject: Updated Parking System - Scan to Register

We have upgraded our parking management system. All employees
must register their vehicles by scanning the QR code below.

[QR CODE IMAGE - Would link to: https://evil-site[.]com/parking]

Scan with your phone camera to complete registration.
You will need to enter your employee ID and network password.

Facilities Management
```

**Red flags:**
- QR codes hide the destination URL
- Asks for network password for a parking system
- Unexpected change notification with no prior communication
- Cannot hover over a QR code to preview the URL like you can with a link

## How to Identify Phishing Emails

### The SLAM Method

| Letter | Check | What to Look For |
|--------|-------|------------------|
| **S** | Sender | Is the email address legitimate? Check the full address, not just the display name |
| **L** | Links | Hover over links before clicking. Does the URL match the expected destination? |
| **A** | Attachments | Were you expecting this attachment? Is the file type suspicious? |
| **M** | Message | Does the content use urgency, threats, or too-good-to-be-true offers? |

### Detailed Identification Checklist

- [ ] **Check the sender's full email address** -- Not just the display name. `CEO Name <ceo@evil-domain.com>` is not your CEO
- [ ] **Hover over all links** -- The displayed text and actual URL may be different
- [ ] **Look for urgency and threats** -- "Act now," "Account suspended," "Legal action"
- [ ] **Check for generic greetings** -- "Dear Customer" instead of your actual name
- [ ] **Look for spelling and grammar errors** -- Though AI-generated phishing is increasingly polished
- [ ] **Verify unexpected requests** -- Call the sender using a known phone number (not one in the email)
- [ ] **Check attachment file types** -- Be wary of .exe, .scr, .zip, .js, .vbs, and double extensions
- [ ] **Look for mismatched branding** -- Slightly wrong logos, colors, or formatting
- [ ] **Verify the "Reply-To" address** -- It may differ from the "From" address
- [ ] **Be suspicious of requests for credentials** -- Legitimate services rarely ask for passwords via email

## Reporting Procedures

### When You Receive a Suspicious Email

1. **Do not click any links or open attachments**
2. **Do not reply to the email**
3. **Do not forward the email** (except to IT/Security)
4. **Report using the phishing report button** in your email client (if available)
5. **Forward as an attachment** to your security team (e.g., security@yourcompany.com)
6. **Delete the email** after reporting

### If You Clicked a Phishing Link

1. **Disconnect from the network** immediately (unplug Ethernet or disable Wi-Fi)
2. **Do not enter any credentials** if you landed on a login page
3. **Contact IT/Security immediately** -- Call, do not email
4. **Change your password** from a known-safe device if you entered credentials
5. **Enable or verify MFA** on all accounts
6. **Document what happened** -- What did you click? What did you enter? When?

### If You Entered Credentials

1. **Change the compromised password immediately** from a clean device
2. **Change the password on any other accounts using the same password**
3. **Report to IT/Security immediately**
4. **Monitor your accounts** for unusual activity
5. **Follow your organization's incident response procedures**

## Social Engineering Beyond Email

### Phone-Based (Vishing)

- Never give credentials, MFA codes, or sensitive data over the phone
- Verify the caller by hanging up and calling back using a known number
- IT support will never ask for your password

### SMS-Based (Smishing)

- Do not click links in unexpected text messages
- Banks and services send SMS alerts but never ask for login via text
- Report suspicious SMS to your carrier (forward to 7726/SPAM)

### In-Person Social Engineering

- Challenge unfamiliar visitors, even if they have badges
- Do not hold doors open for people you do not recognize (tailgating)
- Do not leave credentials, access cards, or sensitive documents visible
- Report suspicious behavior to security

### AI-Generated Threats

- AI-generated phishing emails have fewer spelling and grammar errors
- Deepfake voice calls can impersonate executives
- Always verify unusual requests through a second communication channel

## Building a Security Awareness Program

### Program Components

| Component | Frequency | Purpose |
|-----------|-----------|---------|
| Initial onboarding training | At hire | Baseline knowledge |
| Annual refresher training | Yearly | Updated threats and policies |
| Phishing simulations | Monthly | Practical testing |
| Targeted training | After failures | Remediation for those who click |
| Security newsletters | Monthly | Ongoing awareness |
| Incident debriefs | After incidents | Real-world learning |
| Posters and reminders | Ongoing | Environmental reinforcement |

### Program Metrics

- Phishing simulation click rate (target: under 5%)
- Phishing report rate (target: over 70%)
- Training completion rate (target: 100%)
- Time to report (target: under 10 minutes)
- Repeat clicker rate (target: under 2%)

## Quiz Questions

Use these questions for security awareness assessments. Answers are provided for administrators.

### Multiple Choice

**1. You receive an email from your CEO asking you to wire $50,000 to a new vendor immediately. What should you do?**

a) Wire the money -- the CEO asked for it
b) Reply to the email asking for confirmation
c) Call the CEO using a known phone number to verify the request
d) Forward the email to the vendor

**Answer: c)** Always verify unusual financial requests through a separate communication channel.

**2. Which of the following is the BEST way to check if a link is safe?**

a) Click it and see where it goes
b) Hover over the link to preview the URL
c) Copy and paste it into your browser
d) Ask a coworker to click it first

**Answer: b)** Hovering reveals the actual destination without navigating to it.

**3. You receive an email from IT support asking you to send your password to verify your account. What should you do?**

a) Send the password since IT needs it
b) Send the password but change it afterward
c) Report the email as phishing -- legitimate IT will never ask for your password
d) Ignore the email

**Answer: c)** No legitimate IT department or service will ever ask for your password via email.

**4. Which email attachment type poses the HIGHEST risk?**

a) .pdf
b) .docx
c) .exe
d) .jpg

**Answer: c)** Executable files (.exe) can run malicious code directly. However, all attachment types can potentially contain malware.

**5. What is "spear phishing"?**

a) A random mass email sent to thousands of people
b) A targeted phishing email aimed at a specific individual using personal information
c) Phishing that only targets fishermen
d) A type of phone scam

**Answer: b)** Spear phishing uses personal details about the target to appear more convincing.

### True or False

**6. If an email passes your spam filter, it is safe to open.**
**Answer: False.** Spam filters catch most but not all phishing emails.

**7. It is safe to click a link if the display text shows a legitimate URL like "https://microsoft.com".**
**Answer: False.** The display text can be different from the actual URL. Always hover to check.

**8. Two-factor authentication (MFA) completely prevents account compromise from phishing.**
**Answer: False.** MFA significantly reduces risk but advanced attacks (real-time phishing proxies) can bypass some MFA methods.

**9. You should report phishing emails even if you did not click anything.**
**Answer: True.** Reporting helps the security team block the threat for everyone.

**10. AI-generated phishing emails are easy to identify because they always contain spelling errors.**
**Answer: False.** AI-generated phishing is grammatically correct and increasingly difficult to distinguish from legitimate emails.

## Presentation Slides Outline

Use this outline to create a 30-45 minute security awareness presentation:

### Slide 1: Title
- "Phishing Awareness Training"
- Company name, date, presenter

### Slide 2: Why This Matters
- 90% of cyberattacks start with phishing
- Average cost of a breach: $4.76 million
- Real-world examples from the news

### Slides 3-4: Types of Phishing
- Email, spear phishing, whaling, BEC, smishing, vishing
- Brief description and real-world example of each

### Slides 5-8: Phishing Email Examples
- Show 3-4 redacted examples from this guide
- Highlight red flags in each example

### Slides 9-10: The SLAM Method
- Sender, Links, Attachments, Message
- Interactive exercise: show an email, have audience identify red flags

### Slide 11: What to Do
- Do not click, do not reply, do not forward
- Use the report button
- Contact IT/Security

### Slide 12: If You Clicked
- Disconnect, do not enter credentials, report immediately
- Change passwords from a clean device

### Slides 13-14: Beyond Email
- Vishing, smishing, in-person social engineering, QR codes
- AI-generated threats

### Slide 15: Quiz
- 5-10 interactive questions from the quiz section

### Slide 16: Summary and Resources
- Key takeaways
- How to report
- Contact information for IT/Security

## Phishing Simulation Best Practices

- [ ] **Start with easy simulations** and gradually increase difficulty
- [ ] **Never shame or punish employees** who fail simulations
- [ ] **Provide immediate training** after a click (teachable moment)
- [ ] **Vary templates monthly** -- use current events, seasonal themes, and internal scenarios
- [ ] **Track metrics over time** -- measure improvement, not just failure
- [ ] **Get executive buy-in** -- executives should participate in simulations too
- [ ] **Exclude new hires** for the first 30 days (let them complete onboarding training first)
- [ ] **Inform legal and HR** before starting a simulation program
- [ ] **Recognize and reward reporters** -- positive reinforcement works

## Metrics and Measurement

| Metric | Baseline | 6-Month Target | 12-Month Target |
|--------|----------|----------------|-----------------|
| Click rate | 25-30% | 15% | Under 5% |
| Report rate | 10-20% | 40% | Over 70% |
| Training completion | Variable | 95% | 100% |
| Repeat clickers | 10-15% | 5% | Under 2% |

## Additional Resources

- [CISA Phishing Guidance](https://www.cisa.gov/topics/cyber-threats-and-advisories/phishing)
- [KnowBe4 Phishing Resources](https://www.knowbe4.com/phishing)
- [Anti-Phishing Working Group](https://apwg.org/)
- [NIST SP 800-50: IT Security Awareness and Training](https://csrc.nist.gov/publications/detail/sp/800-50/final)

## Contributing

Contributions are welcome. Please open an issue or submit a pull request with additional examples, quiz questions, or training content.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Professional IT Security Services

Need expert help building your security awareness program? **Petronella Technology Group** provides:

- [Managed IT Services](https://petronellatech.com/managed-it-services/) - 24/7 monitoring and management
- [Cybersecurity Assessments](https://petronellatech.com/cybersecurity-assessment/) - Comprehensive security audits
- [Network Security](https://petronellatech.com/cybersecurity/network-security/) - Firewall, IDS/IPS, segmentation
- [AI-Powered Security](https://petronellatech.com/ai/ai-services/) - Next-gen threat detection

**Petronella Technology Group** is a CMMC-RP certified cybersecurity firm in Raleigh, NC. [Contact us](https://petronellatech.com/contact-us/) or call (919) 348-4912.

## About Petronella Technology Group

This training resource is maintained by [Petronella Technology Group, Inc.](https://www.petronellatech.com/) -- a cybersecurity and IT services firm specializing in security awareness training, compliance (CMMC, HIPAA, SOC 2, NIST), and managed IT for businesses across the United States.

- Website: [https://www.petronellatech.com](https://www.petronellatech.com/)
- Book a consultation: [https://book.petronella.ai](https://book.petronella.ai/)
- Phone: [(919) 348-4912](tel:9193484912)
- LinkedIn: [Petronella Technology Group](https://www.linkedin.com/company/petronella-computer-consultants-inc-)
