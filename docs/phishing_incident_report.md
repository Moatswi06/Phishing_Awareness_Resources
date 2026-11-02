##Phishing Incident Report Checklist

**Companion to phishing_detector.py — Phishing Awareness Resource. Complete one checklist per incident and keep it with your evidence.**

1. Incident Details


• Report ID: ________________


• Date and time received: ________________


• Date and time reported: ________________


• Reported by (name, role, contact): ________________


• Channel (tick one):
    [ ] Email
    [ ] SMS / messaging app (smishing)
    [ ] Phone call (vishing)
    [ ] Social media / other: ________________

    
• Sender name and address / number: ________________
• Subject line or first line of message: ________________
• Suspected type (tick all that apply):
    [ ] Email phishing
    [ ] Spear phishing (personalized)
    [ ] Smishing
    [ ] Business Email Compromise (BEC)
    [ ] Other social engineering: ________________
2. Detector Results
Run the script on the message and record the output. Commands: python phishing_detector.py message.eml, python phishing_detector.py --SMS "text", python phishing_detector.py --url "link", or add --check-tls to test certificates.
[ ] Script run on the message (date/time: ________________)
• Verdict (tick one):
    [ ] Low risk
    [ ] Medium risk
    [ ] High risk
• Score: ________
• Attack type indicators shown (BEC / Smishing / Spear): ________________
• Social engineering tactics detected (urgency, authority, secrecy, etc.): ________________
• Key indicators listed (copy the top three): ________________
[ ] TLS certificate check run (--check-tls) — result: ________________
[ ] Detector output saved with the evidence
[ ] Manual review agrees with the verdict (a low score does not prove a message is safe)
3. What Was Done With the Message?
Tick everything that applies. Any ticked item raises the priority of this incident.
[ ] Nothing — message was not opened or acted on
[ ] Opened the message
[ ] Clicked a link
[ ] Opened or downloaded an attachment
[ ] Entered a username, password, or card details on a linked page
[ ] Shared a one-time code, PIN, or security answer
[ ] Replied to the sender or called a number in the message
[ ] Approved an MFA prompt
[ ] Installed software or granted remote access
[ ] Made or authorized a payment, or changed bank details
[ ] Forwarded the message to others (who: ________________)
Accounts, devices, or money potentially affected: ________________
4. Evidence Preservation
Preserve before deleting or cleaning anything.
[ ] Original message saved as .elm or forwarded as an attachment (keeps full headers)
[ ] Full email headers captured (From, Reply-To, Return-Path, Message-ID, Received, SPF/DKIM/DMARC results)
[ ] Screenshots of the message, linked page, and any call log or SMS thread
[ ] Links recorded as text and not clicked (list: ________________)
[ ] Attachment names and file hashes recorded (do not open)
[ ] Phone numbers, sender IDs, and payment details recorded
[ ] Timeline written down with timestamps
[ ] Evidence stored somewhere access-controlled
5. Containment
[ ] Stopped interacting with the message — no clicks, replies, or downloads
[ ] Affected device disconnected from the network (if a link, attachment, or software was opened)
[ ] Logged out of affected accounts and revoked active sessions
[ ] Compromised accounts locked or disabled by IT
[ ] Sender address, domain, and URLs blocked at the mail filter or firewall
[ ] Message removed from other mailboxes (search and purge by sender or subject)
[ ] Security team or IT notified
[ ] Payment stopped or recall requested, and bank contacted by phone (if money was involved)
6. Eradication
[ ] Passwords changed from a clean device (unique, stored in a password manager)
[ ] Device scanned for malware; unknown apps and browser extensions removed
[ ] Mailbox rules and forwarding addresses reviewed and unauthorized ones removed
[ ] Connected apps and OAuth permissions reviewed and suspicious ones revoked
[ ] API keys, tokens, and service account secrets rotated if exposed
[ ] Device rebuilt from a clean image if it cannot be confirmed clean
[ ] Other systems checked for the same indicators (same sender, links, or file hashes)
7. Recovery
[ ] Files or settings restored from verified clean backups (if altered)
[ ] Accounts and devices reconnected only after cleaning and patching
[ ] Account activity, bank statements, and mobile money monitored for at least 30 days
[ ] Credit or identity monitoring considered if personal data was exposed
[ ] Normal operation confirmed and recorded
[ ] Affected colleagues, customers, or family warned about the same message
8. MFA Audit
[ ] MFA enabled on email, banking, mobile money, and cloud accounts
[ ] Authenticator app, passkey, or security key used instead of SMS codes where possible
[ ] Enrolled devices and recovery methods reviewed; unknown ones removed
[ ] Unrequested MFA prompts identified and reported
[ ] Mobile account PIN or SIM lock set (protects against SIM swapping)
[ ] Backup codes regenerated and stored securely
9. BEC-Specific Checks
Complete if the detector flagged BEC indicators or a payment or bank-detail request was involved.
[ ] Request verified by phone with a number already on file (not one in the message)
[ ] Bank notified and recall attempted for any payment already sent
[ ] Supplier or executive account checked for compromise or spoofing
[ ] Finance team alerted to hold related pending payments
[ ] Look-alike domains registered or in use identified and reported
[ ] Payment-change procedure reinforced (call-back confirmation required)
10. Smishing-Specific Checks
Complete if the incident came by SMS or a messaging app.
[ ] Message reported to the mobile provider (forward to the provider's spam reporting number)
[ ] Sender number blocked and message deleted after evidence was saved
[ ] Any linked site visited or details entered recorded in Section 3
[ ] Bank or mobile money provider contacted if financial details were shared
[ ] SIM swap checked for (sudden loss of signal or unexpected provider messages)
11. Reporting and Notification
[ ] Internal report filed with IT or security
[ ] Management informed (name and time: ________________)
[ ] Phishing reported to the email provider ("report phishing" button)
[ ] Impersonated brand or organization notified
[ ] Bank or financial institution notified (if relevant)
[ ] Police or national cybercrime authority notified (if loss or crime occurred)
[ ] Legal or data-protection duties assessed, including regulator or customer notification if personal data was exposed
[ ] Cyber insurer notified (if applicable)
12. Post-Incident Review
Hold a blameless review within one to two weeks.
• Root cause (how did it reach the user?): ________________
• Detection gap (why did filters miss it?): ________________
• Time to detect: ________  Time to contain: ________  Time to recover: ________
• What worked well: ________________
• What should change: ________________
• Actions:
    [ ] Detector rules updated (e.g., add brands to KNOWN_BRANDS, new keywords, thresholds)
    [ ] Mail filtering and blocking rules updated
    [ ] Awareness training or a phishing simulation scheduled
    [ ] Response procedures updated
    [ ] Reporter thanked (no-blame culture)
13. Sign-Off
• Incident status (tick one):
    [ ] Open
    [ ] Contained
    [ ] Resolved
    [ ] Closed
• Handled by (name, role): ________________
• Reviewed by: ________________
• Date closed: ________________
**Quick reminder: when in doubt, verify through a separate, trusted channel, and report early. Speed limits the damage.**
