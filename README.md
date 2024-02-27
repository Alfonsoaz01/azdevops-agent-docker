# azdevops-agent-docker
[WIP]

https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops 

Environment variable	Description
AZP_URL	The URL of the Azure DevOps or Azure DevOps Server instance.
AZP_TOKEN	Personal Access Token (PAT) with Agent Pools (read, manage) scope, created by a user who has permission to configure agents, at AZP_URL.
AZP_AGENT_NAME	Agent name (default value: the container hostname).
AZP_POOL	Agent pool name (default value: Default).
AZP_WORK	Work directory (default value: _work).

# token
https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops 
![image](https://github.com/Alfonsoaz01/azdevops-agent-docker/assets/91730802/d9249f35-8bb5-4f74-b96b-a80f5fea3a26)

![image](https://github.com/Alfonsoaz01/azdevops-agent-docker/assets/91730802/cf25bfb3-0693-4838-817d-d75701b7095b)


![image](https://github.com/Alfonsoaz01/azdevops-agent-docker/assets/91730802/218e0acc-eb24-4587-8e86-8926e36700f2)

# pool 
![image](https://github.com/Alfonsoaz01/azdevops-agent-docker/assets/91730802/3fd116dc-475a-49bf-ae85-9897c33cfa5f)



# build
open directory : azp-agent-in-docker
docker build --tag "az-agent" --file "./dockerfile" . 

# run
docker run -e AZP_URL="<Azure DevOps instance>" -e AZP_TOKEN="<Personal Access Token>" -e AZP_POOL="<Agent Pool Name>" -e AZP_AGENT_NAME="Docker Agent - Linux" --name "azp-agent-linux" azp-agent:linux 
**Example**
docker run -e AZP_URL="https://dev.azure.com/neworg" -e AZP_TOKEN="secrettoken" -e AZP_POOL="Pool" -e AZP_AGENT_NAME="Docker Agent - Linux" --name "az-agent"

# Result
![image](https://github.com/Alfonsoaz01/azdevops-agent-docker/assets/91730802/e7d130c5-7a33-4d3e-a054-f9ac85f0091c)
 ![image](https://github.com/Alfonsoaz01/azdevops-agent-docker/assets/91730802/0a42a43a-3d10-40dd-8f93-4fce6d7a4f8f)

