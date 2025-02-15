# Objective
To provide an overview and practical guidance on using Microsoft Defender and related security tools within the Microsoft 365 environment to detect, respond to, and mitigate security threats.

## Skills Learned
- Defender for Office 365: I used Defender for Office 365 to investigate, respond to, and remediate threats. I access it under Email & Collaboration and use the Explorer to review activities like email received, malware, phishing, and campaigns.

- I used Authentication Header and DKIM which helps ensure email authenticity by checking DNS to confirm legitimacy.

- I implemented Data Loss Prevention (DLP) to respond to and alert on data security issues. I access DLP policies through Microsoft 365 Admin Center, specifically under Compliance > Microsoft Purview > Data Loss Prevention Blade > Policies.

- I created DLP policies to protect sensitive information, ensuring it isn't shared incorrectly. There's also possibility to customize policies or use templates, linking them to sensitive info types and classifiers in Communication Compliance.

- I learned that DLP policies are prioritized by order number, with lower numbers having higher priority. Alerts for triggered policies are found in the Alerts Blade under DLP and can be emailed to an admin. I observed that Microsoft integrates DLP alerts with Defender.

- I used Insider Risk Management in Purview to detect, investigate, and take action on potential insider risks. The process involves creating policies, triaging alerts, investigating them, and taking action. Insider Risk Management, needs appropriate licensing, such as the Microsoft 365 E5 Compliance license.

- I used Microsoft Defender for Cloud Apps to monitor cloud services and endpoints, understanding which applications users are utilizing, such as Dropbox, OneDrive, and Salesforce, through the Cloud App Catalog. In Cloud Apps, I also configured policies, using templates to create and manage different policy categories. After creating policies, I review the Activity Log to investigate if any activities have triggered the policies.



