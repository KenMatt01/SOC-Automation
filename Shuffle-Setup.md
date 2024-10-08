# Installing Docker and Docker Compose on Ubuntu Server

*Installing Docker & Docker compose is a prerequisite*<br>
<br>
Step 1: Prepare the system for installation
Before we can start installing docker & docker-compose we need to make sure that the system is up to date. You can do it by running the following commands:
```
sudo apt update
sudo apt upgrade -y
```
Step 2: Download and Install the docker repository
Docker is using an installation repository. to install the repository and use it we need to install the following packages:
```
sudo apt install -y ca-certificates curl gnupg lsb-release
```
After the package installation, we need to add Docker’s GPG Key to our system by running the following commands:
```
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```
Now we can install the docker repository by running the following commands:
```
sudo echo  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
```
Step 3: Installing Docker
You can proceed to install Docker by executing the provided command below. This straightforward command will enable you to initiate the Docker installation process on your system.
```
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
```
Step 4: Installing Docker Compose
To install docker-compose tun the following commands:
```
sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```
To verify that your Docker Compose installation was successful, you can use the following command:
```
docker-compose --version
```

# Installing Shuffle SOAR 

Step1: Make sure you have Docker and docker-compose installed, and that you have a minimum of 2Gb of RAM available.
Step2: Download Shuffle
```
git clone https://github.com/Shuffle/Shuffle
cd Shuffle
```

Step:3 Fix prerequisites for the Opensearch database (Elasticsearch):
```
mkdir shuffle-database                    # Create a database folder
sudo chown -R 1000:1000 shuffle-database  # IF you get an error using 'chown', add the user first with 'sudo useradd opensearch'

sudo swapoff -a                           # Disable swap
```
Step:4 Run docker-compose.
```
docker-compose up -d
```
Step:5 Recommended for Opensearch to work well
```
sudo sysctl -w vm.max_map_count=262144     
```
