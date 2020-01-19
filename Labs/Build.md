# Azure Pipelines Setup and Administration
In this set of exercises you will add a local build service account, install and configure a new build agent and create a build pipeline to verify the setup.

## Prerequisites
(none?)

## Exercise: Install Build Agent Software
(NOTE: Installing on the Application Tier C: drive, in production instead use a dedicated build server with a separate storage partition for agents.)

### Tasks

1. Browse to Project Settings > Agent Pools and click New Agent. The dialog has a download button and basic instructions for configuring the agent. Download the agent (zip-file).

1. Locate the agent zip-file and extract it to a folder on the root of the C: drive, preferably called ```C:\agent1```.

1. Open an Administrative Command Prompt create a local user account "devopsbuild" for the build service.

1. Configure the build agent using the script config.cmd. Make sure to use the ```--gituseschannel``` parameter so that the Git installation bundled with the agent is getting the server certificates from the local Windows Certificate Stores. Answer yes to running the agent as a service and provide the service user name ("devopsbuild") you created in the previous step.

1. The agent will register and start as a windows service.

## Exercise: Create a Deployment Pool
