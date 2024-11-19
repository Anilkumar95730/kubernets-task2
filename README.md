# Replication controller
First of create a ec2 instance in in ubuntu with t2 medium.

Switch to root user by the command sudo su -

and update it using command apt update -y

Now install Docker 

             sudo apt install curl wget apt-transport-https -y
             sudo curl -fsSL https://get.docker.com -o get-docker.sh 
             chmod 777 get-docker.sh sh get-docker.sh

# Installation of minikube:

by using this commands:

                   sudo curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
                    sudo mv minikube-linux-amd64 /usr/local/bin/minikube
                    sudo chmod +x /usr/local/bin/minikube
                    sudo minikube version

# installation of kubectl:

             sudo curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl 
             sudo curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256
             sudo echo "$(cat kubectl.sha256) kubectl" | sha256sum --check
             sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
             sudo kubectl version --client --output=yaml 
             chmod +x kubectl
             sudo minikube start --driver=docker --force
# Create the pod commands:
                    kubectl run pod-name --image=image-name 
create yam file 

                 vi anilkumar.yml
![Screenshot 2024-11-18 211007](https://github.com/user-attachments/assets/a07ce09a-f141-4126-aa3d-42699b2e5662)


kubectl create -f anilkumar.yml - by this command if pod is created then the work is done
![Screenshot 2024-11-18 203646](https://github.com/user-attachments/assets/0beb719b-9ee9-4de0-a2dd-4d5aa3f90ac0)
