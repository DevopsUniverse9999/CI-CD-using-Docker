# CI-CD-using-Docker
![Untitled Diagram](https://user-images.githubusercontent.com/122671107/212527794-b064f719-7c4d-4371-993d-403d7057c06a.jpg)

# Our second success which brought fireworks in our hearts....! 
# Use ubuntu 


sudo su <br>
hostname your-name <br>
exec bash <br>
apt-get update <br> 

# Make jenkins instance 

Install jenkins:-<br>
exit <br>
sudo apt-get update <br>

sudo apt-get install openjdk-11-jdk <br>

sudo java -version <br>

sudo curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee \ <br>
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null <br>

sudo echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \ <br>
  /etc/apt/sources.list.d/jenkins.list > /dev/null <br>

sudo apt-get update <br>

sudo apt-get install jenkins <br>

sudo systemctl start jenkins.service <br>

sudo systemctl status jenkins <br>

install git :- <br>
sudo apr-get install git -y <br>
sudo git --version <br>

install docker :- <br>

sudo apt install docker.io -y <br>
sudo usermode -aG docker jenkins   (Add jenkins user to docker ) <br>
sudo systemctl restart jenkins <br>
sudo docket info <br>
sudo mvn -version <br>
cat (Appeared version over the jenkins to get the determined password) <br>

sudo docker  images <br>


Plugins used in jenkins:- sshAgent <br>


# Create a Docker Instance 

sudo apt update <br>
sudo apt install docker.io -y <br>
sudo usermod -aG docker jenkins <br>
sudo docker info <br>
sudo usermod -aG docker ubuntu <br>
clear <br>
exit <br>
docker info <br>
docker version <br>
docker version --format '{{.Server.Version.}}' <br>
sudo docker info <br>
sudo systemctl start docker <br>
sudo docker info <br>
sudo systemctl status docker <br>
