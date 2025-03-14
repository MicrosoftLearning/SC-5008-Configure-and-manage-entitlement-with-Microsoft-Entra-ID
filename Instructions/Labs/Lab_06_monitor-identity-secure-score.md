---
lab:
    title: 'Lab 6: - Monitor and managed security posture with Identity Secure Score'
    module: 'Module : Deploying access using Microsoft Entra entitlement management'
---

# Lab 6 - Monitor and managed security posture with Identity Secure Score

## Lab scenario

Microsoft Entra Identity Protection provides automated detection and remediation to identity-based risks, and provides data in the portal to investigate potential risks. Microsoft Entra Identity Protection also provides an Identity Secure Score to monitor and improve your identity security posture.  In the same manner as Microsoft Defender XDR and Microsoft Defender for Cloud, Identity Secure Score provides improvement actions and recommendations that can improve your overall security posture for identity in Microsoft Entra ID.  This lab will explore this capability. 

#### Estimated time: 15 minutes

### Exercise 1 - Using Identity Secure Score to monitor and manage identity security posture

#### Task 1 - Review Identity Secure Score and improvement actions

1. Sign in to the [https://entra.microsoft.com](https://entra.microsoft.com) as a Global administrator.

2. Open the **Protection** menu and select **Identity Secure Score**

**NOTE** - This will take you to the Identity Secure Score dashboard.

3. Scroll down to view the **Improvement actions**.

4. In contrast to the improvement actions in Microsoft Defender for Cloud and Microsoft Defender XDR, these improvement actions are specific to identity.  This provides a more focused list of potential actions to your security posture management.  Any improvement actions initiated from this list will also provide an impact to your overall tenant security posture. 

#### Task 2 - Execute an improvement action

1. To improve one area of the identity security posture, select **Enable Microsoft Entra ID Identity Protection sign-in risk policies**.

3. From the menu on the left, open **Identity Protection | Sign-in risk policy**.

4. Select **All users** under **Assignments**.

5. Select **Medium and above** under **Sign-in risk**.

6. Select **Allow** - **Require multi-factor authentication** under **Controls**.

7. Turn the **Policy enforcement** to **Enabled** (if not done so already), and select **Save**.

8. You have created a Sign-in risk policy that should now increase your Identity Secure Score.  This will take up to 24 hours to take affect in your Identity Secure Score.

9. Review other improvement actions and the steps to create and enable them.
