# Week 0 — Billing and Architecture

## Required Homework & Tasks

### *Recreate Logical Architectural Deisgn*
The first task is to recreate the logical architecture design from the previous week. This is a good way to get familiar with the tools and the process. The design should be recreated in Lucid Chart. I based my design on the one Andrew Brown was using in his tutorial

[Link to the design](https://lucid.app/lucidchart/b23df7f5-fcac-4476-be9e-339885627b98/edit?viewport_loc=240,-238,2525,1631,0_0&invitationId=inv_474f3ff7-4010-4e24-8ae8-aa1c2bd49b66)

![Logical Architecture Screenshot](//journal/assets/napkin-design.png)

### *Create a new User and Generate AWS Credentials*
The second task is to create a new user called **aws-bootcamp** and generate AWS credentials. Also created a new IAM group called **AWS-Bootcamp** and added the new user to the group. The group has the following permissions:
- ##### AdministratorAccess

##### User Group
Created User Group called **AWS-Bootcamp** and added the new user to the group with the AdministratorAccess policy.
![User Group](//journal/assets/user-group.png)
##### User enabled for MFA and Console Access
Enabled MFA for the *aws-bootcamp* user and enabled console access.
![MFA and Console Access](//journal/assets/mfa-console-access.png)

##### Access Keys
Generated Access Keys for the *aws-bootcamp* user and downloaded the CSV file.
![Access Keys](//journal/assets/access-keys.png)


### Install AWS CLI GitPod

- Installation of the AWS CLI when Gitpod enviroment lanuches.
- Tested AWS CLI to use partial autoprompt mode to make it easier to debug
- Added AWS CLI to Gitpod by adding a script to the `.gitpod.yml` file
- The bash commands used are the same as the [AWS CLI Install Instructions](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

Updated  `.gitpod.yml` to include the following task.

```sh
tasks:
  - name: aws-cli
    env:
      AWS_CLI_AUTO_PROMPT: on-partial
    init: |
      cd /workspace
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
      unzip awscliv2.zip
      sudo ./aws/install
      cd $THEIA_WORKSPACE_ROOT
```

### Set Env Vars

Set these credentials for the current bash terminal
```
export AWS_ACCESS_KEY_ID=""
export AWS_SECRET_ACCESS_KEY=""
export AWS_DEFAULT_REGION=us-east-1
```

For Gitpod to remember these credentials if we relaunch our workspaces
```
gp env AWS_ACCESS_KEY_ID=""
gp env AWS_SECRET_ACCESS_KEY=""
gp env AWS_DEFAULT_REGION=us-east-1
```

### Check that the AWS CLI is working and you are the expected user

```sh
aws sts get-caller-identity
```

You should see something like this:
![Confirmation of AWS CLI and user account](//journal/assets/aws-cli.png)
