---
lab:
  title: 'Lab 5: - Configure Privileged Identity Management for Microsoft Entra roles'
  module: 'Module : Deploying access using Microsoft Entra entitlement management'
  description: The Privileged Identity Management (PIM) service also allows Privileged role administrators to make permanent admin role assignments. Learn to assign a privileged role to users in your company.
  duration: 30 minutes
  level: 300
  islab: true
  primarytopics:
    - Azure
    - Azure Portal
    - Microsoft Entra
    - Microsoft Entra ID
---

# Lab 5: Configure Privileged Identity Management for Microsoft Entra roles

## Lab scenario

A Privileged role administrator can customize Privileged Identity Management (PIM) in their Microsoft Entra organization, including changing the experience for a user who is activating an eligible role assignment. You must become familiar with configuring PIM.

#### Estimated time: 30 minutes

### Exercise 1 - Configure Microsoft Entra role settings

#### Task 1 - Open role settings

Follow these steps to open the settings for a Microsoft Entra role.

1. Sign in to **Microsoft Entra admin center** at **`https://entra.microsoft.com`** as a Global administrator.

    >**Note:** You may be required to set up Microsoft Authenticator during sign-in. Follow the prompts to install and configure the app before continuing.

1. In the left navigation menu, expand the **ID Governance**, select **Privileged Identity Management**.

1. In the **Privileged Identity Management** page, in the left navigation, select **Microsoft Entra roles**.

1. On the **Quick start** page, in the left navigation, select **Settings**.

    ![Screen image displaying the Microsoft Entra roles page with the Settings menu highlighted](./Media/pim-ad-roles-settings.png)

1. Review the list of roles and then, in the **Search by role name**, enter **compliance**.

1. In the results, select **Compliance Administrator**.

1. Review the role setting details information.

#### Task 2 - Require approval to activate

1. In the **Role setting details** page, on the top menu, select **Edit**.

    ![Screen image displaying the top portion of the Role setting details -Compliance Administrator page with Edit highlighted](./Media/pim-edit-compliance-role.png)

1. In the **Edit role setting – Compliance Administrator** page, select the **Require approval to activate** check box.

1. Select **Select approvers**.

1. In the **Select a member** pane, select your administrator account and then select **Select**.

    ![Screen image displaying the edit role settings page and select a member pane with the selected members highlighted](./Media/pim-add-approver.png)

1. Once you have configured the role settings, select **Update** to save your changes.

### Exercise 2 - PIM with Microsoft Entra roles

#### Task 1 - Assign a role

With Microsoft Entra ID, a Global administrator can make permanent Microsoft Entra admin role assignments. These role assignments can be created using the Microsoft Entra admin center, the Azure portal, or using PowerShell commands. The Privileged Identity Management (PIM) service also allows Privileged role administrators to make permanent admin role assignments. Additionally, Privileged role administrators can make users eligible for Microsoft Entra admin roles. An eligible administrator can activate the role when they need it, and then their permissions expire once they're done.

Follow these steps to make a user eligible for a Microsoft Entra admin role.

1. Sign in to **Microsoft Entra admin center** at **`https://entra.microsoft.com`** using a Global Administrator account.

1. Search for and then select **Privileged Identity Management.**

    >**Note**: you can find **Privileged Identity Management**, under the **ID Governance** in the left navigation.

1. In the **Privileged Identity Management** page, in the left navigation, select **Microsoft Entra roles**.

1. On the **Quick start** page, in the left navigation, select **Roles**.

1. On the top menu, select **+ Add assignments**.

    ![Screen image displaying Microsoft Entra roles with Add assignments menu highlighted](./Media/pim-assign-role.png)

1. In the **Add assignments** page, on the **Membership** tab, review the settings.

1. Select the **Select role** menu and then select **Compliance Administrator**.

1. You can use the **Search role by name** filter to help locate a role.

1. Under **Select member(s),** select **No members selected**.

1. In the **Select a member** pane, select **Miriam Graham** and then select **Select**.

1. In the **Add assignments** page, select **Next >**.

1. On the **Settings** tab, under **Assignment type**, review the available options. For this task, use the default setting, **Eligible**.

    - Eligible assignments require the member of the role to perform an action to use the role. Actions might include performing a multi-factor authentication (MFA) check, providing a business justification, or requesting approval from designated approvers.
    - Active assignments do not require the member to perform any action to use the role. Members assigned as active have the privileges always assigned to the role.

1. Review the remaining settings and then select **Assign**.

#### Task 2 - Log in with Miriam

1. Open a new InPrivate browser window.

1. Connect to **Microsoft Entra admin center** at **`https://entra.microsoft.com`**.

    >**Note**: If it opens with a user logged in, Select on their name in the upper-right corner and select **Sign in as a different account**.

1. Log in as **Miriam**.

    | Field | Value |
    | :--- | :--- |
    | Username | `MiriamG@<<your domain.onmicrosoft.com>>` |
    | Password |  Enter the tenant's admin password(Refer the Lab Resources tab to retrieve the tenant admin password) |

    >**Note**: You may be required to set up Microsoft Authenticator during sign-in. Follow the prompts to install and configure the app before continuing.

    >**Note**: if prompted change your password.

1. In the left navigation menu, under **Entra ID**, select **Users**, then select **All users**.

1. Search for **Miriam** in the list of users and select it.

1. On the **Overview** page, in the left navigation menu, select **Assigned roles**.

1. On the **Miriam Graham | Assigned roles** page, Select **Eligible assignments** tab.

1. Notice that the **Compliance Administrator** role is now available to Miriam.

#### Task 3 - Activate your Microsoft Entra roles

When you need to assume a Microsoft Entra role, you can request activation by opening **My roles** in Privileged Identity Management.

1. From the **Search, resources, services, and docs** bar, look for Privileged.

1. Open the **Privileged Identity Management** page.

1. On the **Privileged Identity Management** page, in the left navigation menu, select **My roles**.

1. In the **My roles** page, review the list of **Eligible assignments**.

    ![Screen image displaying My roles with eligible role assignments highlighted](./Media/pim-my-roles.png)

1. In the **Compliance Administrator** role row, select **Activate**.

    >**Note**: You may be required to complete additional verification (for example, MFA) after selecting **Activate**, depending on the lab environment configuration.

1. In the **Activate - Compliance Administrator** pane, in the **Reason** box, enter a justification like: **This is my justification for activating this role**.

    > **Important Note**: Follow the principle of least privilege. Activate the role only for the time needed.  
    > For example, if the task takes 1.5 hours, set the duration to 2 hours.  
    > If you need to start later, use **Custom activation start time**.

1. Select **Activate**.

#### Task 4 - Assign a role with restricted scope

For certain roles, the scope of the granted permissions can be restricted to a single admin unit, service principal, or application. This procedure is an example of assigning a role that has the scope of an administrative unit.

1. Remember to close out the browser windows for MiriamG, then open the Microsoft Entra admin center with your administrator account.

1. Browse to the **Privileged Identity Management** page, and in the left navigation menu, select **Microsoft Entra roles**.

1. Select **Roles**.

1. In the **Roles** page, on the top menu, select **+ Add assignments**.

1. In the **Add assignments** page, select the **Select role** menu and then select **User administrator**.

1. Select the **Scope type** menu and review the available options. For now, you will use the **Directory** scope type.

    **Tip** - Go to [https://docs.microsoft.com/en-us/azure/active-directory/roles/admin-units-manage](https://docs.microsoft.com/en-us/azure/active-directory/roles/admin-units-manage) for more information about the administrative unit scope type.

1. As you did when assigning a role without a restricted scope, you would add members and complete the settings options. For now, select **Cancel**.

#### Task 5 - Update or remove an existing role assignment

Follow these steps to update or remove an existing role assignment.

1. In the Open **Privileged Identity Management > Microsoft Entra roles** page, in the left navigation, select **Assignments**.

1. In **Assignments** list, for Compliance Administrator, review the options in the **Action** column.

1. Select **Update** and review the options available in the Membership settings pane. When complete, close the pane.

1. Select **Remove**.

1. In the **Remove** dialog box, review the information and then select **Yes**.
