# Week 0 — Billing and Architecture

## Install AWS CLI

I am using Gitpod, so I installed AWS CLI on my Gitpod environment.

Below are the instructions I used to install AWS CLI in our Gitpod workspace and configure it.

- We are going to install AWS CLI when the Gitpod environment launches.
- The bash commands used to install the AWS CLI are referenced from the [AWS CLI Install Documention](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
- We update our ```.gitpod.yml``` file with the following task, such that the installation is done on each startup by itself.

```
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
We can also run these commands individually to perform the install manually.
 

## Logical Architectural Diagram for the Application

I used Lucid Charts to create a logical diagram for our appliaction.

Here's the diagram and the link to [Lucid Chart Document](https://lucid.app/lucidchart/da419696-ad18-407a-b949-016cc2433753/edit?viewport_loc=-1489%2C839%2C2731%2C1139%2C0_0&invitationId=inv_7479a31a-9b5e-4dea-9261-031a10d019db)

![Logical Diagram for Application](/assets/Cruddur-Logical-Diagram.png)
