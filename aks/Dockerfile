FROM dominikkawczak/aks-helm-teamcity-agent

ARG AZ_USERNAME
ARG AZ_PASSWORD
ARG AZ_TENANT
ARG AKS_RG
ARG AKS_NAME

RUN az login --service-principal -u $AZ_USERNAME -p $AZ_PASSWORD -t $AZ_TENANT; exit 0
RUN az aks get-credentials --resource-group $AKS_RG --name $AKS_NAME;exit 0