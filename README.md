# azdevops-agent-docker

https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops 

Environment variable	Description
AZP_URL	The URL of the Azure DevOps or Azure DevOps Server instance.
AZP_TOKEN	Personal Access Token (PAT) with Agent Pools (read, manage) scope, created by a user who has permission to configure agents, at AZP_URL.
AZP_AGENT_NAME	Agent name (default value: the container hostname).
AZP_POOL	Agent pool name (default value: Default).
AZP_WORK	Work directory (default value: _work).

#token
https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops 

#build

docker build --tag "azp-agent:linux" --file "./azp-agent-linux.dockerfile" . 

#run
docker run -e AZP_URL="<Azure DevOps instance>" -e AZP_TOKEN="<Personal Access Token>" -e AZP_POOL="<Agent Pool Name>" -e AZP_AGENT_NAME="Docker Agent - Linux" --name "azp-agent-linux" azp-agent:linux 
