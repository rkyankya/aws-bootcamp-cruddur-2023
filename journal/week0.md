# Week 0 — Billing and Architecture

## Required Homework & Tasks

### *Recreate Logical Architectural Deisgn*
The first task is to recreate the logical architecture design from the previous week. This is a good way to get familiar with the tools and the process. The design should be recreated in Lucid Chart. I based my design on the one Andrew Brown was using in his tutorial

[Link to the design](https://lucid.app/lucidchart/b23df7f5-fcac-4476-be9e-339885627b98/edit?viewport_loc=240,-238,2525,1631,0_0&invitationId=inv_474f3ff7-4010-4e24-8ae8-aa1c2bd49b66)

![Logical Architecture Screenshot](//journal/assets/napkin-design.png)

### *Create a new User and Generate AWS Credentials*
The second task is to create a new user called aws-bootcamp and generate AWS credentials. Also created a new IAM group called aws-bootcamp and add the new user to the group. The group should have the following permissions:
- AdministratorAccess

##### User Group
Created User Group called aws-bootcamp and added the new user to the group with the AdministratorAccess policy.
![User Group](//journal/assets/user-group.png)

##### Access Keys
Generated Access Keys for the aws-bootcamp user and downloaded the CSV file.
![Access Keys](//journal/assets/access-keys.png)

##### User enabled for MFA and Consile Access
Enabled MFA for the aws-bootcamp user and enabled console access.
![MFA and Console Access](//journal/assets/mfa-console-access.png)
