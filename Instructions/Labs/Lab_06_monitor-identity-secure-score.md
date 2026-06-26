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

1. Sign in to **Microsoft Entra admin center** at **`https://entra.microsoft.com`** as a Global administrator.

    > **Note:** You may be required to set up Microsoft Authenticator during sign-in. Follow the prompts to install and configure the app before continuing.
    
1. In the left navigation menu, under **Entra ID**, select **Identity Secure Score**. This will take you to the Identity Secure Score dashboard.

1. Scroll down to review the list of **recommendations**.  
   These recommendations represent the **improvement actions** for your identity security posture.

1. In contrast to the improvement actions in Microsoft Defender for Cloud and Microsoft Defender XDR, these improvement actions are specific to identity.  This provides a more focused list of potential actions to your security posture management.  Any improvement actions initiated from this list will also provide an impact to your overall tenant security posture. 

#### Task 2 - Execute an improvement action

1. To improve one area of the identity security posture, select **Protect all users with a user risk policy**.
   
1. Review the **Action plan**.

1. Select the link **Follow these steps to create a Conditional Access policy from scratch or by using a template**. Review the steps in the article and then close the tab.

1. In the left navigation menu, expand the **ID Protection**, select **Dashboard**.

1. On the **ID Protection | Dashboard** page, in the left navigation, under **Protect** select **Sign-in risk policy**.

1. On the **ID Protection | Sign-in risk policy** page, in the **Assignments** section,  under **Users**, make sure **All users** is selected.

1. Under **Sign-in risk**, select the **Low and above** link.

1. In the **Sign-in risk** pane, select **Medium and above**, then select **Done**.

1. In the **Controls** section, under **Access**, select **Block access**.

1. In the **Access** pane, select **Allow access** - **Require multi-factor authentication**, then select **Done**.

1. Turn the **Policy enforcement** to **Enabled** (if not done so already), and select **Save**.

1. You have created a Sign-in risk policy that should now increase your Identity Secure Score.  This will take up to 24 hours to take effect in your Identity Secure Score.

1. Review other improvement actions and the steps to create and enable them.
