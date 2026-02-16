# Azure-Cloud-Governance
# 🛡️ Enterprise Cloud Governance & RBAC

## 🎯 Project Objective
Building upon the **17,555 user identities** synchronized from the local domain in Project 2, this project focuses on the implementation of **Cloud Governance** and security. The mission is to establish a secure administrative framework using **Role-Based Access Control (RBAC)**, manage identities via **Security Groups**, and prepare the tenant for advanced security policies.

---

## 🛠️ Technical Stack & Infrastructure
* **Cloud Platform**: Microsoft Entra ID (Free Tier Tenant)
* **Identity Source**: Hybrid-synced identities from `mylab.local`
* **Management Tools**: Entra Admin Center, RBAC Engine

---

## 🚀 Phase 1: Identity Governance & RBAC

### 📋 Task 1: Tiered Administrative Role Assignment
**Objective:** Implement the principle of least privilege by delegating specific cloud permissions to synced identities.

**Detailed Steps:**
1. **Identity Search:** Navigate to **Identity** > **Users** > **All users** and locate the synced identity `bab.gasavo`.
2. **Access Role Menu:** Open the user's profile and select **Assigned roles** from the left-hand navigation pane.
3. **Add Assignment:** Click **+ Add assignments** at the top of the screen.
4. **Role Selection:** Search for and select the **User Administrator** role, then click **Add**.
5. **Verification:** Confirm the role status is "Active" to ensure the user can now manage non-admin accounts and reset passwords.

![RBAC Assignment](https://raw.githubusercontent.com/techboulnp-gif/Azure-Cloud-Governance/main/Phase%201/01_RBAC_Role_Assignment.png)

### 📋 Task 2: Security Group Architecture & License Pivot
**Objective:** Create a centralized management container for the IT staff while documenting infrastructure constraints.

**Detailed Steps:**
1. **Group Creation:** Navigate to **Groups** > **All groups** and click **+ New group**.
2. **Configuration:** Set **Group type** to **Security** and name the group **`IT_Staff_Manual`**.
3. **Licensing Constraint:** Attempted to change **Membership type** to **Dynamic User**.
    * **Note:** This option was unavailable due to the **Entra ID Free** license tier.
4. **Engineering Decision:** To maintain project momentum, the membership type was set to **Assigned** for manual provisioning.

![Group Creation Settings](https://raw.githubusercontent.com/techboulnp-gif/Azure-Cloud-Governance/main/Phase%201/02_Group_Creation_Settings.png)

### 📋 Task 3: Manual Identity Provisioning (The Pilot Group)
**Objective:** Manually link synced identities to the new security container for pilot testing.

**Detailed Steps:**
1. **Open Group Members:** From the `IT_Staff_Manual` group page, select **Members** from the sidebar.
2. **Add Members:** Click **+ Add members**.
3. **Search & Select:** Located and selected 5 specific synced identities: `bab.gasavo`, `baqet.focosi`, `bax.sos`, `bir.cakib`, and `boqaw.doju`.
4. **Selection Verification:** Confirmed all target users appeared in the "Selected" column.

![Membership Selection](https://raw.githubusercontent.com/techboulnp-gif/Azure-Cloud-Governance/main/Phase%201/03_Manual_Group_Membership.png)

### 📋 Task 4: Membership Verification & Integrity Check
**Objective:** Confirm the successful commit of identities to the cloud object.

**Detailed Steps:**
1. **Commitment:** Clicked **Select** to finalize the addition of the 5 users.
2. **Refresh List:** Refreshed the **Members** page to verify the cloud database updated correctly.
3. **Verification Results:** Confirmed that all 5 users, including the User Administrator `bab.gasavo`, are active members of the group.

![Final Membership List](https://raw.githubusercontent.com/techboulnp-gif/Azure-Cloud-Governance/main/Phase%201/04_IT_Staff_Manual_Members_Final.png)

### 📋 Task 5: Delegation of Support Roles (Helpdesk Admin)
**Objective:** Demonstrate a multi-tiered support structure by delegating password management to a separate user tier.

**Detailed Steps:**
1. **Target Identification:** Located the synced identity **`dah.noh`** in the **All users** list.
2. **Role Assignment:** Followed the RBAC process to assign the **Helpdesk Administrator** role.
3. **Functional Delegation:** This creates a second tier of support, where `dah.noh` handles basic support tickets while `bab.gasavo` manages broader user administration.

![Helpdesk Delegation](https://raw.githubusercontent.com/techboulnp-gif/Azure-Cloud-Governance/main/Phase%201/05_Helpdesk_Role_Delegation.png)

---

## 🗺️ Project Roadmap & Portfolio Navigation

### 📍 Current Phase: Cloud Governance & RBAC (In Progress)

This project serves as the final stage of an end-to-end enterprise identity lifecycle.

* **Step 1: On-Premise Active Directory Home Lab (Project 1)** — Establishing the local DC and 17k users. ✅
* **Step 2: Azure Hybrid Identity Lab (Project 2)** — Synchronizing local AD with Entra ID via Entra Connect. ✅
* **Step 3: Cloud Governance & Security (Project 3)** — Implementing RBAC and security policies. 📍

### 🎓 Portfolio Navigation

* [ ⬅️ Previous Project: Azure AD Hybrid Integration ](https://github.com/techboulnp-gif/Azure-Hybrid-Integration)
* [ 🏠 Back to Main Portfolio ](https://github.com/techboulnp-gif)
