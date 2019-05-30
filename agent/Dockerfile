FROM jetbrains/teamcity-agent:latest

RUN sudo apt-get update && sudo apt-get install -y curl apt-transport-https lsb-release gnupg
RUN curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
RUN curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
RUN echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
RUN sudo apt-get update
RUN sudo apt-get install -y kubectl

RUN curl https://raw.githubusercontent.com/kubernetes/helm/master/scripts/get > get_helm.sh
RUN chmod 700 get_helm.sh
RUN ./get_helm.sh