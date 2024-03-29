# Getting Started with Creating a User Account in an OU

This article describes how to create an individual user and grant policies.

## Prerequisites

You must have OU admin access rights.

.. note:: When a user have multiple accounts, among which one is the admin account. We recommend that the user perform identity and access management operations through the admin account.

## About This Task

The following major steps are involved:

1. Define user roles and design proper access policies for different roles. For example, you might consider to define the **IoT Engineer** role, who is typically responsible for the following operations:

   - Connect devices into EnOS Cloud, including cloud-end configuration such as creating products, provisioning devices, and testing communication.
   - On-site installation of edge devices and connect cables from devices to the edge gateway.

   To perform the operations, this role would need access to the following resources:
   - **Device Connection** related configuration
   - **Edge Gateway** configuration

2. For each specific user role, create a user group to manage access permissions collectively for this role.

3. Create a user account, and add the account into the user group corresponding to the role.

4. Optionally, assign additional access policies for the user when needed.

This example makes the following assumptions:

- The organization that the user belongs to already exist.
- The role of the user, however, does not have corresponding user group created on EnOS.
- The user will be created within its organization.

## Step 1: Create a Policy

1. In the EnOS console, click **IAM > Policies** from the left navigation panel.  

2. Click **New Policy**.

3. Enter the policy name and click **Next**.

4. In the **Grant Permission** page, you can grant access to services<!-- or assets-->. After configurating, user only can see and access to the service that grant access.

  <!-- Service: the services that the user is allowed to access. After configurating, user only can see and access to the service that grant access.
    - Assets: the assets that the user is allowed to access. EnOS supports granting access at 3 levels: individual asset level, asset tree level, and all assets. When assigned access to all assets, the user has access to the data of all assets.
  -->

5. Click **Save** to create the policy.

## Step 2: Create a User Group

In this step, you'll create a user group for the role, and associates the policy that you created in Step 1, which defines the permissions for the user role.

1. In the EnOS console, click **IAM > Groups** from the left navigation panel.

2. In the **Group** page, click **New Group**.

3. Enter a group name that represents the role that you defined and click **Next**.

4. Click **Assign Policies** to assign policies for this group.

5. Click **Save**.

For more information about user group management, see [Creating and managing user groups](managing_groups).


## Step 3: Create a User and Add User into Group

In this step, you'll create the user in the organization, and add the user into the user group that you created in Step 2. This user will then inherit all permissions that are defined by the policies associated to the user group.

1. In the EnOS console, click **IAM > Users** from the left navigation panel.

2. In the **Internal User** tab, click **Create User** and provide proper settings, among these settings:

   - **Send by**
     - other safety way: indicates to send the password in other secure offline approaches.
     - Send by phone: indicates to send the account information via messaging to the registered mobile phone number.
     - Send by email: indicates to send the account information via sending email to the registered email address.
   - **Password**: you can set the initial password, or you can let the system to auto-generate the password for the account.

3. In the **Add User to Groups** tab, click **Add User Group**.

4. In the pop-up window, select the groups that the user belongs to and click **Save**.

5. Click **Save** to confirm the change.


## (Optional) Step 4: Add Additional Policies

If the policies inherited from the user groups are not sufficient, you can add additional policies for the user.
1. In the EnOS Console, click **IAM > Users** from the left navigation panel.  

2. Click the authorize icon |img| to open .

3. In the **Polices** tab, click **Assign Policy** .

4. In the pop-up window, select the policies to assign to this user and click **Save**.

5. Click **Save** to confirm the change.

## What to Do Next
The user will receive account creation notification through the channel as specified in Step 3. The user can then log into EnOS Console with the account information and verify access rights.


.. |img| image:: media/authorize.png

<!--end-->
