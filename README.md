# Creating-Organizational-Units-Groups-and-Users
# Active Directory Home Lab: Directory Management

This guide demonstrates how to build and manage the basic hierarchy of a Windows Active Directory environment, including the creation of **Organizational Units (OUs)**, **Groups**, and **Users**.

---

## 1. Creating an Organizational Unit (OU)
Organizational Units are the primary containers used to organize objects within a domain. They allow for more granular control over Group Policy and administrative permissions.

1. Open **Server Manager** and navigate to **Tools** > **Active Directory Users and Computers**.
2. In the console tree, right-click your domain (e.g., `CAPSLOCH`).
3. Select **New** > **Organizational Unit**.
4. In the dialog box, enter a name for your OU (e.g., `USA`).
    * *Note: OUs can be nested. To create a sub-OU, simply right-click an existing OU and repeat these steps.*
5. Click **OK**.

## 2. Adding Groups and Distribution Lists
Groups allow you to manage multiple users at once. You can create these within your new OUs to maintain a clean structure.

1. Right-click your target OU and select **New** > **Group**.
2. Enter the **Group Name**.
3. Select the appropriate **Group Type**:
    * **Security:** Use this for assigning permissions to files, folders, or network resources.
    * **Distribution:** Use this exclusively for email communication lists.
4. Click **OK**.

## 3. Provisioning New Users
Adding users to specific OUs ensures they inherit the correct policies and group memberships.

1. Right-click the desired OU and select **New** > **User**.
2. Fill in the user’s details (First Name, Last Name, and User Logon Name).
3. Click **Next**.
4. Assign a **Password** and select the relevant account settings, such as:
    * *User must change password at next logon.*
    * *Password never expires.*
5. Click **Next**, review the summary, and click **Finish**.

---

**Success!** You have successfully established the foundational structure for your Active Directory environment.
