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

## Steps
- Fisrt, we Log in to Microsoft 365 Defender, access the Email & Collaboration section, from the left navigation pane, go to Email & Collaboration under the Threat Management section. This is where all security tools related to email, including Defender for Office 365, are located. We select explorer, now we see a set of predefined categories that allow us to view different types of email threats; All Email Received, Malware, Phishing, Campaigns, Content Malware, URL clicks. In each of these categories, we can filter and analyze emails that were detected by Defender. We can see details like the message subject, sender, detection time, and more.

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/4d7d44285dd6646e00018b28c85c732b31a5f514/Images/Explorer%20exploration.PNG" width="700" />
</p>

- We also ensure that DKIM is configured in our domain’s DNS settings for email authentication - DKIM is an email authentication method that helps validate the legitimacy of incoming emails. We go to the Microsoft 365 Admin Center, In the left pane, under Setup, select Domains, choose the domain you want to check, Look for the DKIM settings for that domain. Ensure that DKIM is enabled, once enabled, DKIM checks will be reflected in Defender for Office 365’s Explorer view, and we’ll see if any incoming email fails the DKIM check.

- To implement Data Loss Prevention (DLP) with Microsoft 365, Open Microsoft Purview from Microsoft 365 Admin Center, Under Solutions, click Compliance, Navigate to the Data Loss Prevention Blade under solutions, click on Policies to start creating or managing your DLP policies. 

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/dce0aa354f4dad50b882f07be80e4cc8cfcafff6/Images/DLP%20navigation.PNG" width="700" />
</p>

- We create a new policy from scratch but there is also the option for editing templates which makes the process easier, select the Create DLP policy button and pick a relevant template. Next, we link DLP Policies to Sensitive Info Types, Under Data Classification, in the Sensitive Info Types section, click Manage sensitive information types and choose or define the specific types of data you want to protect. Under the Communication Compliance section, go to Classifiers, select Sensitive Info Types to define classifiers for your DLP policies, such as Personally Identifiable Information (PII), financial data, etc.

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/ca4f609ed41742169c4b7f1fea180aceeef4e8b8/Images/Creating%20a%20policy.PNG" width="300" />
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/ca4f609ed41742169c4b7f1fea180aceeef4e8b8/Images/GDPR%20policy%20created.PNG" width="300" />
</p>

- When you have multiple Data Loss Prevention (DLP) policies in place, setting the correct policy priority ensures that the most important or sensitive policies take precedence when multiple policies are triggered for the same incident. To set the priority for a specific policy, click on the policy name you want to edit, this will open the policy configuration settings, we will see policy priority and order number. Policy Priority determines which policy should take precedence when more than one policy is triggered by the same incident. Lower order numbers represent higher priority. Adjust the priorities for your policies, click Save to apply the changes.

- Next we set Alerts for DLP Policies. In Microsoft Purview, under Alerts, go to Alerts Blade, review the DLP alerts, which will help you monitor policy violations and incidents. Ensure that DLP incident reports are sent to the admin’s email for ongoing monitoring and action, to do this, configure email notifications in the Alert Settings or DLP Policy Settings. Note: Test DLP policies in a non-production environment before implementing them organization-wide.

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/585d001281b0717ae5b29efe8f925d00166bee36/Images/Alerts%20in%20DLP.PNG" width="700" />
</p>

- We can also view DLP alerts in Microsoft Defender, but we need to link our Microsoft Defender environment with Microsoft Purview, where the DLP policies are managed. Open the Microsoft 365 Admin Center, from the left navigation pane, click on Security to open the Microsoft Defender, navigate to Investigation & Response, click on Incidents & Alerts, click on Incidents and you’ll be able to view all incidents, including alerts from Data Loss Prevention (DLP) policies. We can also filter alerts based on severity, time range, and other conditions and also Investigate the details of each alert to understand what triggered the DLP rule.

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/bc33560ae7150d6f583db968c4374c4678e01050/Images/DLP%20alerts%20from%20microsoft%20defender.PNG" width="700" />
</p>

- To implement Insider Risk Management in Purview, we need the Microsoft 365 E5 Compliance license, and assign the license to your users through the Licenses section in the admin portal - Ensure that your account has the necessary permissions to access and manage these features.

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/ad1aa1f4d47f528b6a7453160157953f7fa31703/Images/Assigning%20licence%20to%20myself.PNG" width="700" />
</p>

- After assigning licences to myself, we'll go to Microsoft Defender via Microsoft 365 Defender portal, navigate to Compliance Center to access the policy creation options.
In the Compliance Center, look for Insider Risk Management in the Solutions section on the left-hand menu, click on Insider Risk Management to start managing insider threats. Here, we will create the policies that define the criteria for detecting risky insider behaviors.

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/5c263335ced9b2984e86d6e27a6fe89f7977817e/Images/Creating%20policy%20in%20Insider%20risk%20management.PNG" width="700" />
</p>

- Click on Policies, Create Policy to see existing policies or create new ones, we'll be prompted to configure it with these important details such as Policy Type, Policy Name, Users and Groups, Action Settings, etc. Define the thresholds for when the policy triggers. For example, how many suspicious actions within a certain timeframe would be considered risky? You can also decide on the level of risk (low, medium, high) and the corresponding response. Configure notifications to admins so that the appropriate people or teams are alerted when the policy is triggered. If everything looks good, click on Create Policy.

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/833560f4f2e2fe0211ca675c827587d270feac78/Images/Submit%20policy%20created.PNG" width="700" />
</p>

- To investigate alerts generated by Insider Risk policies in Microsoft Purview and manage the roles for proper access, Open Microsoft Purview , click on the Settings gear icon, find and click on Roles and Scope, within the Roles and Scope section, click on Role Group, from the Role Group list, search for the Insider Risk Management and click it - is the role that controls access to Insider Risk Management menus and features, you’ll see a list of users and groups already assigned to it. This shows you who currently has permissions.

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/f3edb6cf07c3b25321f73f3af5aff296ecd20e23/Images/Adding%20insider%20risk%20management%20role.PNG" width="700" />
</p>

- Click on the Edit button to modify role assignments, in the editing screen, you can add yourself or others by selecting the appropriate user or groups and click Save to update the role assignments. Once saved, check the Insider Risk Management menu, the permissions for the added users should now reflect in the Insider Risk Management section, this will enable you to access and manage Insider Risk policies, view alerts, and take actions.

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/a1d3bf9a413528353de8a8846561a18bd071116d/Images/Adding%20insider%20risk%20management%20role%202.PNG" width="300" />
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/a1d3bf9a413528353de8a8846561a18bd071116d/Images/New%20menu%20items%20in%20IRM.PNG" width="300" />
</p>

- Using Microsoft Defender for Cloud Apps to helps provide visibility into the cloud apps your users are accessing, so you can identify any risky behavior or non-compliant applications. To access Microsoft Defender for Cloud Apps, log in to the Microsoft Defender portal, navigate to the Cloud Apps section by selecting the Cloud Apps blade, inside the Cloud Apps section, you’ll find the Cloud App Catalog, it allows you to search for specific applications such as Dropbox, Salesforce, OneDrive, etc., check if they are in use within your organization, and evaluate their security and compliance posture.

- Next, create policies to define what’s acceptable within your organization. For example, you can create a policy that blocks access to an app if it’s being accessed from an unmanaged device. You can also set Data Loss Prevention (DLP) policies to prevent sensitive data from being uploaded to risky apps or shared inappropriately. To enhance your security posture, integrate Defender for Cloud Apps with other services like Azure AD Conditional Access, Microsoft Defender for Endpoint, and Microsoft Sentinel - integration helps provide a unified security strategy across apps, endpoints, and identity management. 

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/970afb90278b6c11c007494479b6b4e14b0d6ced/Images/Cloud%20apps%20policy%20management.PNG" width="700" />
</p>

- Once alerts are triggered, investigate the activity in the context of the application used and take appropriate action. Actions could include blocking the app, restricting user access, or conducting a deeper investigation into potential breaches or policy violations.

- In our example, we created a File Policy using the "File Share with Personal Email Address" template, and then how to use the Activity Log to investigate any triggered activities. This will help us track file sharing activities that involve personal email addresses and identify any security or policy violations related to file sharing.

<p align="center">
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/e1da503697dd56c9bdaace7741517c18d3b0f31c/Images/Creating%20a%20file%20policy.PNG" width="300" />
  <img src="https://github.com/NgethaWachira/Microsoft-365-Security-and-Compliance-Management/blob/e1da503697dd56c9bdaace7741517c18d3b0f31c/Images/Creating%20a%20file%20policy%202.PNG" width="300" />
</p>

- Review and adjust policies as needed to ensure proper monitoring and enforcement.
