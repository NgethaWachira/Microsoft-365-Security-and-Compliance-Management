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

## Tools Used
<div>
<img src="https://img.shields.io/badge/-Microsoft%20Defender%20for%20Office%20365-3d5c5c?style=for-the-badge&logo=Microsoft%20Defender&logoColor=white" alt="Microsoft Defender for Office 365">
<img src="https://img.shields.io/badge/-DKIM-aaaa55?style=for-the-badge&logo=Gmail&logoColor=white" alt="DKIM">
<img src="https://img.shields.io/badge/-Microsoft%20365%20Admin%20Center-b3ff1a?style=for-the-badge&logo=Microsoft%20365&logoColor=white" alt="Microsoft 365 Admin Center">
<img src="https://img.shields.io/badge/-Microsoft%20Purview-ff9900?style=for-the-badge&logo=Microsoft%20Purview&logoColor=white" alt="Microsoft Purview">
<img src="https://img.shields.io/badge/-Data%20Loss%20Prevention%20(DLP)-cc6600?style=for-the-badge&logo=Microsoft%20Security&logoColor=white" alt="Data Loss Prevention (DLP)">
<img src="https://img.shields.io/badge/-Communication%20Compliance-993333?style=for-the-badge&logo=Microsoft%20Security&logoColor=white" alt="Communication Compliance">
<img src="https://img.shields.io/badge/-Insider%20Risk%20Management-ff99bb?style=for-the-badge&logo=Microsoft%20Security&logoColor=white" alt="Insider Risk Management">
<img src="https://img.shields.io/badge/-Cloud%20App%20Catalog-df9fbf?style=for-the-badge&logo=Microsoft%20Azure&logoColor=white" alt="Cloud App Catalog">
<img src="https://img.shields.io/badge/-Microsoft%20Defender-660029?style=for-the-badge&logo=Microsoft%20Defender&logoColor=white" alt="Microsoft Defender">
</div>


<p align="center">
  <img src="https://github.com/NgethaWachira/Azure-Security-and-Simulation/blob/670ae5d5cd00a045199063fcee2303e6b30fae0e/Images/Launching%20an%20attack%20simulation.PNG" width="300" />
  <img src="https://github.com/NgethaWachira/Azure-Security-and-Simulation/blob/8d2d52d3bc3c8de99ab8e47cacda47b5ec8010f3/Images/Attack%20email%20payload.PNG" width="300" />
</p>

## Steps
- Fisrt, we Log in to Microsoft 365 Defender, access the Email & Collaboration section, from the left navigation pane, go to Email & Collaboration under the Threat Management section. This is where all security tools related to email, including Defender for Office 365, are located. We select explorer, now we see a set of predefined categories that allow us to view different types of email threats; All Email Received, Malware, Phishing, Campaigns, Content Malware, URL clicks. In each of these categories, we can filter and analyze emails that were detected by Defender. We can see details like the message subject, sender, detection time, and more.

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/4d7d44285dd6646e00018b28c85c732b31a5f514/Images/Explorer%20exploration.PNG" width="700" />
</p>

- We also ensure that DKIM is configured in our domain’s DNS settings for email authentication - DKIM is an email authentication method that helps validate the legitimacy of incoming emails. We go to the Admin Center, In the left pane, under Setup, select Domains. Choose the domain you want to check, Look for the DKIM settings for that domain. Ensure that DKIM is enabled. Once enabled, DKIM checks will be reflected in Defender for Office 365’s Explorer view, and we’ll see if any incoming email fails the DKIM check.






