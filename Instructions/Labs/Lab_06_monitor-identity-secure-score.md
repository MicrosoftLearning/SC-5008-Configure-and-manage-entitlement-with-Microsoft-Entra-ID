---
lab:
  title: 'Lab 6: - Monitor and managed security posture with Identity Secure Score'
  module: 'Module : Deploying access using Microsoft Entra entitlement management'
  description: Microsoft Entra Identity Protection provides automated detection and remediation to identity-based risks. Microsoft Entra Identity Protection also provides an Identity Secure Score to monitor and improve your identity security posture. Review your identity platform secure score and remediate issues as needed.
  duration: 15 minutes
  level: 200
  islab: true
  primarytopics:
    - Microsoft Defender
    - Microsoft Defender for Cloud
    - Microsoft Defender XDR
    - Microsoft Entra
    - Microsoft Entra ID
---

# Lab 6 - Monitor and managed security posture with Identity Secure Score

## Lab scenario

Microsoft Entra Identity Protection provides automated detection and remediation to identity-based risks, and provides data in the portal to investigate potential risks. Microsoft Entra Identity Protection also provides an Identity Secure Score to monitor and improve your identity security posture.  In the same manner as Microsoft Defender XDR and Microsoft Defender for Cloud, Identity Secure Score provides improvement actions and recommendations that can improve your overall security posture for identity in Microsoft Entra ID.  This lab will explore this capability. 

#### Estimated time: 15 minutes

### Exercise 1 - Using Identity Secure Score to monitor and manage identity security posture

#### Task 1 - Review Identity Secure Score and improvement actions

1. Sign in to the [https://entra.microsoft.com](https://entra.microsoft.com) as a Global administrator.

2. Open the **Entra ID** menu and select **Identity Secure Score**

    **NOTE** - This will take you to the Identity Secure Score dashboard.

3. Scroll down to view the **Recommendations**.

4. In contrast to the improvement actions in Microsoft Defender for Cloud and Microsoft Defender XDR, these improvement actions are specific to identity.  This provides a more focused list of potential actions to your security posture management.  Any improvement actions initiated from this list will also provide an impact to your overall tenant security posture. 

#### Task 2 - Execute an improvement action

1. To improve one area of the identity security posture, select **Protect all users with a user risk policy**.
   
2. Review the **Action plan**.

3. Select the link **Follow these steps to create a Conditional Access policy from scratch or by using a template**. Review the steps in the article and then close the tab.

4. From the Entra ID menu on the left, open **Conditional Access** and select **+Create new policy**.

5. Name the policy: **User Risk remediation**.

6. Under **Users or Agents (Preview)** select **0 users or agents (Preview)** and then, on the **Include** tab, select **All users**.

7.  On the **Exclude** tab, use the **Users and groups** to exclude **MOD Administrator**

8. Under **Target resources** select **No target resources selected** and then **All resources (formerly 'All cloud apps')**.

9. Under **Conditions** select **0 conditions selected** and then, under **User risk**, select **Not configured**.

10. Under **User risk** select **Configure - Yes** and then the checkboxes for **Medium** and **High** and then select **Done**.

11. Under **Access controls > Grant** select **0 controls selected**, scroll down and select the checkbox for **Require risk remediation**. Read the warning and scroll up to verify that **Require authentication strength > Multifactor authentication** was automatically selected and then scroll down and select the **Select** button. Note that **Access controls > Session** has also been updated to show **Sign-in frequency - Every time**.

12. Under **Enable Policy** select **On** and then select **Create**.

13. You have created a User risk policy that should now increase your Identity Secure Score.  This will take up to 24 hours to take affect in your Identity Secure Score.

14.  From the Entra ID menu on the left, select **Identity Secure Score** to review other improvement actions and the steps to create and enable them.
