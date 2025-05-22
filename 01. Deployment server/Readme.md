## Install kubectl:
- curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.31.2/2024-11-15/bin/linux/amd64/kubectl
- chmod +x ./kubectl
- mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && exportPATH=$HOME/bin:$PATH

## Install eksctl:
- export ARCH=amd64
- export PLATFORM=$(uname -s)_$ARCH
- curl -sLO "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$PLATFORM.tar.gz"
- tar -xzf eksctl_$PLATFORM.tar.gz -C /tmp && rm eksctl_$PLATFORM.tar.gz
- sudo mv /tmp/eksctl /usr/local/bin

## Install Docker
- sudo yum -y insatll docker
- sudo systemctl enable docker
- sudo systemctl start docker
- sudo usermod -a -G docker ec2-user

## Install Node
- curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
- source ~/.bashrc
- nvm install --lts

## Install git 
- sudo yum -y install git

## Install helm
- curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
- chmod 700 get_helm.sh
- ./get_helm.sh
  
