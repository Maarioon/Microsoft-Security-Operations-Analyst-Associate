## Security is a major part of deployment, builds and usage. There are different ways of implementing security, either through tools, or via the code base.

## Microsoft Security Copilot
Microsoft Security Copilot is a security assistant that leverages AI to help security analysts detect, investigate, and respond to threats in a more optimized way. It uses sophisticated AI models to process security data, automate mundane tasks and offer intuitive, actionable insights, which improve the security position and operational effectiveness.

## Azure
Microsoft Azure is a cloud offering by Microsoft that provides a number of cloud services like virtual machines, databases, networking, AI and analytics among others. Organizations can use Azure Classic to distribute, develop and run applications, and store with the freedom and flexibility of a large-scale cloud hosting service.

## Microsoft Entra
Microsoft Entra is an all-in-identity and access management offering. It are used to provide access to cloud and on-premises resources, to manage user identities, and to enforce security policies.
and configure single sign-on (SSO), requiring multi-factor authentication (MFA), and access/identity/security governance.It was formerly know as Azure Active directory.

It is a was to monitor, create resources, users, change user permissions, customise domains amongst other, all it's services are to help make work easier.

## Global Administrator Role
Sometimes the role one holds determines the type of access granted for specific tasks or uses. There are different roles, an example is the global administrator role.
The Global Administrator is a privileged role in Microsoft 365 and Azure AD. Users assigned this role have full control over all admin features in all Microsoft services, such as user management, billing, security settings, and service settings. It is usually designated for trusted security personnel who monitor and control settings and services across tenants.

Here is a simple explanation of the above:
Azure – cloud based platform for hosting, managing and building applications.

Microsoft Entra: An identity and access management platform.

Global Administrator: Admin that has access to everything in Microsoft 365 and Azure AD.

This is a project designed to teach to set up permissions and provision capacity for Microsoft Security Copilot in Azure.

Even if you’re a beginner with Azure or Copilot, don’t worry! In this guide you’ll learn everything in super simple, easy to follow steps.

---

## 📚 Table of Contents

- [📖 What is this about?](#-what-is-this-about)
- [🎯 Prerequisites](#-prerequisites)
- [🛠️ Task 1: Set Role Permissions](#️-task-1-set-role-permissions)
- [🚀 Task 2: First Run Experience](#-task-2-first-run-experience)
- [🔍 Task 3: Review Owner Settings](#-task-3-review-owner-settings)
- [📝 Notes](#-notes)

---

##  What is this about?

Before people can start using **Security Copilot**, an admin needs to **provision capacity** and **set permissions**.

**Imagine you have a toy box 🎁, and only people with keys 🔑 can open it and play with the toys.**  
In this case:
- **Copilot** = The toy box  
- **Admins** = People with keys  
- **Permissions** = The keys to open and play  

This guide teaches you how to get those keys and set up your toy box.

---

##  Prerequisites

Before you start, you must have:

 An **Azure subscription**  
 Be an **Azure Owner** or **Contributor** (at least at the resource group level)

---

## 🛠️ Task 1: Set Role Permissions

###  Why is this needed?  

Azure and **Microsoft Entra ID (formerly Azure AD)** are like two different playgrounds 🛝.  
Being a big boss in one playground doesn’t automatically make you a boss in the other.

To manage everything, you need a **special pass (User Access Administrator role)** at the very top (called **root scope (/)**).

---

###  Steps  

1. 🔗 Open the [Azure Portal](https://portal.azure.com)

2. Go to **Microsoft Entra ID** on the left menu.

3. Click **Manage** → then **Properties**.

4. Toggle **Access management for Azure resources** to **Enabled** → Save.

5. Go back to the Azure Portal home page.

6. Click **Subscriptions** → select your subscription (**Woodgrove - GTP Demos (External/Sponsored)**).

7. Select **Access Control (IAM)**.

8. Click **Add role assignment**.

9. Choose:
    - **Role:** Owner  
    - **Members:** Select your name (e.g., Avery Howard)

10. Allow user to assign all roles (except privileged administrator roles, Owner, UAA, RBAC) → Continue.

11. Click **Review + assign** twice.

 Done! You're now the boss 🏆 of your Azure subscription.

---

##  Task 2: First Run Experience

Now, let’s **set up Copilot for the first time**.  
This is like unboxing your new toy 🎁 and setting it up.

---

###  Steps  

1. 🔗 Open [Microsoft Security Copilot](https://security.microsoft.com/copilot)

2. The wizard will appear, guiding you through:

- **Azure subscription:** Choose **Woodgrove - GTP Demos (External/Sponsored)**  
- **Resource group:** Choose **RG-1** or create one  
- **Capacity name:** Leave it as-is  
- **Prompt evaluation location:** Choose your region  
- **Security compute (SCU):** Leave it at **1**  
- **Use overage units:** Turn on/off as you like  

3. Agree to the Terms & Conditions 

4. Click **Continue**.

5. **Help improve Copilot:** Choose On/Off.

6. **Microsoft 365 service data:** No setting here — just read and click **Continue**.

7. **Audit logging (Microsoft Purview):** Choose if you want it or not, then **Continue**.

8. **Copilot access:**  
You can add recommended security roles now or later. Then **Continue**.

9. Click **Finish** 🎉  

---

##  Task 3: Review Owner Settings

Let’s take a quick look at the settings you just made.

### 📋 Steps  

1. Click the **Menu (hamburger icon)** 🍔

2. Go to **Owner Settings**:
   - Check **Help improve Copilot** setting.
   - Check **Audit logging** setting.

3. Return to Menu → **Plugin Settings**:
   - Look for **Accessing data from Microsoft 365 services**
   - Disable and Enable it to see how it affects the plugin list.

4. Check plugin status by:
   - Going back to Security Copilot home
   - Clicking the **sources icon**
   - Look at the **Microsoft Purview plugin** (grayed out if access is disabled)

5. Go to **Role assignment**:
   - Expand **Owner** to see members.
   - Expand **Contributor** to see security roles.

 That’s it! You’re all set.

---

## 📝 Notes  

- This guide uses a simulated environment for demo purposes.
- Replace "Woodgrove - GTP Demos (External/Sponsored)" and "RG-1" with your actual subscription/resource group if needed.
- Always review settings carefully in production environments.

---

##  Final Thought  

**Well done!**  
You’ve successfully set up and configured Microsoft Security Copilot.  
Now you know how to control access, provision capacity, and manage settings like a pro 🚀.

---
