- IAM

- IAM allows you to manage users and their level of access to the AWS console. It is important to understand IAM and how it works, both for the exam and for administrating a company's AWS account in real life.

- Identity Access Management (IAM) offers the following features:

- Centralized control of your AWS account
- Shared Access to your AWS account
- Granular Permissions
- Idenmtity Federation (Including Active Directory, Facebook, Linkedin, etc)
- Multifactor Authentification
- Provide temporary access for users/devices and services where necessary
- Allows you to set up your own passwors rotation policy
- Integrates with many different AWS services
- Supports PCI DSS Compilance

- Identity Access Management Consists of the following:
    - Users - End users such as people, employees of an organization, etc.
    - Groups - A collection of users. Each user in the group will inherit the permissions of the group
    - Policies - Policies are made up of documents called Policy documents. These documents are in a format called JSON and they give permissions as to what a User/Group/Role is able to do
    - Roles - You create roles and then assign them to AWS Resources.

- IAM is universal. It does not apply to regions at this time.
- The "root account" is simply the account created when first setup your AWS account. It has complete Admin access.
- New Users have NO permissions when first created.
- New Users are assigned Access Key ID & Secret Access Keys when first created.
- These are not the same as a password. You cannot use the Access key ID & Secret Access Key to Login in to the console. You can use this to access AWS via the APIs and Command Line however.
- You only get to view these once. If you lose them, you have to regenerate them. So, save them in a secure location.
- Always setup Multifactor Authentification on your root account.
- You can create and customise your own password rotation policies.

- Roles

- Roles are more secure than storying your access key and secret access key on individual EC2 instances
- Roles are easier to manage
- Roles can be assigned to an EC2 instance after it is created using both the console & command line
- Roles are universal - you can use them in any region