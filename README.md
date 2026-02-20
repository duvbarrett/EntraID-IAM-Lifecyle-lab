<img width="800" height="418" alt="Image" src="https://github.com/user-attachments/assets/d4fbdf5c-65a8-4be6-86da-5fb70a5b864a" />

# Section 1 Introduction:
Identity and Access Management (IAM) is a critical component of enterprise security. Organizations rely on identity providers such as Microsoft Entra ID to manage user identities, enforce authentication policies, and control access to organizational resources.

In this lab, I configured and administered a Microsoft Entra ID tenant to simulate real-world IAM responsibilities. This environment allowed me to perform identity provisioning, role-based access control, authentication security configuration, and identity administration tasks.

This hands-on experience prepares IAM professionals to manage enterprise identity environments and secure organizational access.

# Section 2: What is Microsoft Entra ID?
Microsoft Entra ID is a cloud-based Identity and Access Management platform that allows organizations to manage user identities, authentication, and authorization. It serves as the central identity provider responsible for controlling access to applications, systems, and organizational resources.

In real world enterprise environments Microsoft Entra ID is used to:

Create and manage user accounts
Assign permissions using Role-Based Access Control (RBAC)
Enforce security policies such as Multi-Factor Authentication (MFA)
Protect privilege accounts using Conditional Access
Automate identity management using PowerShell

# Step 1: Access Microsoft Entra Admin Center
Navigate to:

Microsoft Entra admin center
Edit description
entra.microsoft.com

Sign in using a Microsoft account.

The Microsoft Entra Admin Center is the centralized portal used by IAM administrators to manage identities, roles, authentication methods, and access policies.

Microsoft Entra Admin Center — Identity management portal used by administrators

<img width="1902" height="1063" alt="Image" src="https://github.com/user-attachments/assets/47cc63bc-7aa9-4362-b6fb-994a1e4d56e8" />


# Step 2: Access Tenant Management and Begin Creating a New Entra ID Tenant
In enterprise environments, IAM administrators manage identity environments using tenants. A tenant represents an organization’s identity boundary and contains all users, groups, roles, and access policies.

Before identities can be created and managed, the administrator must access the tenant management section to create or select the appropriate identity environment.

This step stimulates how IAM administrators create and manage identity infrastructures for organizations.

# Step 2.1: Navigate to User Management

From the Microsoft Entra Admin Center homepage:

Click: Entra ID → Users

This opens the identity management interface to create and manage user identities
<img width="812" height="649" alt="Image" src="https://github.com/user-attachments/assets/6fd6dde5-4669-4fe8-9d98-e83a82045ba9" />

User management interface in Microsoft Entra ID used for identity provisioning and lifecycle management

# Step 2.2: Create a New User

Click:

New user → Create new user

This opens the identity provisioning interface.

<img width="517" height="311" alt="Image" src="https://github.com/user-attachments/assets/d38405f9-b05c-4e5e-b16c-1caaf23e683f" />

At this stage, the user provisioning interface has been accessed. This interface allows IAM administrators to create and configure new user identities within the organization’s tenant.

# Step 2.3: Creating a New User Identity
Identity provisioning involves creating a digital identity for a user within the organization’s identity provider. This identity allows the user to authenticate and access organizational resources.

In Microsoft Entra ID, each user identity is defined by User Principal Name (UPN), which uniquely identifies the user within the tenant.

The User Principal Name functions similarily to an email address and is used during authentication.

IAM administrators configure user identities by specifying:

User Principal Name
Display Name
Account Settings
Authentication Configuration
This ensures secure identity creation and proper access management.


User idenity creation form in Microsoft Entra ID. IAM administrators use this interface to provision new user identities and configure authentication settings.

<img width="1148" height="798" alt="Image" src="https://github.com/user-attachments/assets/4e927b33-bbf9-4db8-8a0c-b6efd037bc9a" />

When onboarding a new employee, IAM administrators create a new identitiy within the organization’s indentity provider. This identitiy enables the employee to authenticate and access organizational systems securely.

Each identity is uniquely identified by a User Principal Name (UPN), which serves as the login identifier for authentication.

Press enter or click to view image in full size

Identity provisioning form in Microsoft Entra ID, This interface allows IAM administrators to configure user identity attributes such as User Principal Name, Display Name, and authentication settings.
After accessing the user provisioning interface, the next step is to configure the identity attributes for the new user.

In Microsoft Entra ID, each user identity is uniquely defined by a User Principal Name (UPN). The UPN serves as the user’s authentication identifier and is used during login.

The UPN follows an email format like: username@organizationdomain

Press enter or click to view image in full size

Newly provisioned user identity successfully created in Microsoft Entra ID. This confirms the identity provisioning process was completed.
Step 2.4: Identity Provisioning Complete — User Successfully Created
After reviewing the identity configuration, the new user account was provisioned by selecting Review and Create, followed by Create. Microsoft Entra ID then processed the request and created the identity within the tenant.

The newly created user, John Smith now appears in the Users list. This confirms that the identity provisioning process was successful.

Each user created in Microsoft Entra ID is assigned a unique User Principal Name (UPN), which is used during authentication. The identity can now be assigned roles, granted access to applications, and secured using authentication policies such as Mult-Factor Authentication (MFA).

# Step 3: Role Assignment & Role-Based Access Control (RBAC)
Why Role Assignment Matters in IAM

Identity provisioning establishes who a user is within an organization. However, identity alone does not determine what the user is allowed to do.

Authorization is controlled through Role-Based Access Control (RBAC).

RBAC is an access control model in which permissions are assigned to predefined roles, and those roles are then assigned to users. This ensures that access is granted based on job responsibilities rather than individual discretion.

# Step 3.1: Accessing the User Profile
After provisioning the user identity, the next step is to review the user profile to validate that the account was created successfully and is active within the tenant.

To assign a role to the newly provisioned identity:

Navigate to: Entra ID → Users → Select the newly created user (John Smith)

This opens the user profile interface, where identity properties, authentication methods, and assigned roles can be managed.

Press enter or click to view image in full size

User identity overview page in Microsoft Entra ID. This interface allows IAM administrators to validate account status and manage roles assignments, group memberships, and authentication configurations.

# Step 3.2: Assigning a Role
Within the user profile:

Select Assigned roles
Click + Add assignments
Search for and select Helpdesk Administrator
Click Add
This assign delegated administrative permissions to the user based on the RBAC model.


Assigning the Helpdesk Admin role to enforce role-based access control and least privilege principles within the tenant
By assigning the Helpdesk Admin role, the identity now has permission to:

Reset user passwords
Force password changes
Perform support level administrator tasks

# Step 4: Enforcing Multi-Factor Authentication (MFA)
While identity provisioning establishes who a user is and RBAC defines what a user can do, authentication security ensures that user access is properly protected.

Multi-Factor Authentication strengthens authentication by requiring an additional verification factor beyond a password.

This reduces the risk of credential compromise and unauthorized access.

MFA supports the principle that passwords alone are insufficient to protect enterprise identities.

Why MFA Matter in IAM

Passwords can be:

Phished
Reused
Brute Forced
Leaked in breaches
MFA introduces a second factor such as:

Authenticator app approval
One time passcode
Hardware token
Biometric verification
This significantly reduces account compromise risk.

# Step 4.1: Navigate to Authentication Methods
In Microsoft Entra Admin Center:

Go to:

Entra ID → Protection → Authentication methods

This section allows IAM administrators to configure how users authenticate within the tenant.

Press enter or click to view image in full size

After provisioning identities and assigning roles, the next step is strengthening authentication controls.

Authentication method policies define which verification methods users may register and use for authentication and password reset.

The configuration supports secure identity governance by limiting acceptable authentication factors.

In this tenant configuration:

Microsoft Authenticator is enabled
Software OATH tokens are enabled
Email OTP is enabled
SMS and Voice authentication are disabled
Disabling weaker authentication methods such as SMS and voice reduces the risk of SIM-swap and social engineering attacks.

This demonstrates a shift toward stronger authentication practices aligned with modern security standards.

# Step 4.2: Understanding MFA Enforcement Through Conditional Access
While authentication methods determine which verification factors are available to users, enforcement of Multi-Factor Authentication (MFA) is typically controlled through Conditional Access policies in enterprise environments.

In Microsoft Entra ID Free, Conditional Access is not available. However, understanding how enforcement works is still critical for IAM professionals.

In enterprise environments, Conditional Access evaluates:

Who is signing in
From where
To which resource
Under what risk conditions
Based on those conditions, policies can require:

Multi-Factor Authentication (MFA)
Device compliance
Authentication strength
Or block access entirely
This policy-driven enforcement model aligns with Zero Trust principles, where access decisions are continuously evaluated rather than implicitly trusted.

# Step 4.3: Evaluating Authentication Strength
Among the enabled authentication methods, Email OTP represents the weakest factor.

Email-based one time passcodes rely on the security of the user’s email account. if an attacker has already compromised the mailbox, the additional verification factor provides limited protection.

Stronger authentication methods such as Microsoft Authenticator or hardware based tokens provide device bound or phishing resistant verification.

IAM administrators should continuously evaluate authentication strength and reduce reliance on weaker factors where feasible.

# Step 5: Identity Lifecycle — Offboarding & Deprovisioning
Why this matters

Most breaches don’t happen because accounts weren/t created securely.

They happen because:

Accounts weren’t disabled when employees left
Privileged roles weren't removed
Access lingered
Orphaned accounts existed
Step 5.1: Remove Role Assignment
Navigate to: Entra ID → Users → John Smith → Assigned roles

Click: Helpdesk Administrator → Remove

Confirm removal.


Press enter or click to view image in full size

Role assignment removed as part of offboarding process to eliminate delegated administrative privileges.

# Step 5.2: Disable the User Account
Go back to: John Smith → Overview

Under: Account status → Click Edit

Toggle: Account enabled → No

Save.

Press enter or click to view image in full size

User account disabled following privilege revocation. This prevents authentication and completes the offboarding process within the identity lifecycle.

# Step 5.3: Identity Deprovisioning: Secure Offboarding
Identity lifecycle management extends beyond onboarding and access assignment. Secure offboarding is critical to preventing unauthorized access after employment termination.

Disbaling the account prevents further authentication attempts while preserving audit history and identity records for governance and compliance purposes.

This shows proper enforcement of identity lifecycle management and access governance principles.

Conclusion: End-to-End Identity Administration
This lab simulated a full identity lifecycly within Microsoft Entra ID, including:

User provisioning
Role assignment using RBAC
Authentication method evaluation
Privilege management
Secure deprovisioning
