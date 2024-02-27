# azdevops-agent-docker

https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops 

docker build --tag "azp-agent:linux" --file "./azp-agent-linux.dockerfile" . 

docker run -e AZP_URL="<Azure DevOps instance>" -e AZP_TOKEN="<Personal Access Token>" -e AZP_POOL="<Agent Pool Name>" -e AZP_AGENT_NAME="Docker Agent - Linux" --name "azp-agent-linux" azp-agent:linux 
