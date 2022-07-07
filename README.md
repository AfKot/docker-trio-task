# Trio-task

This is a Flask application that is set up and configured to work with a database and nginx. Write a docker-compose.yaml that will bring all these services up and allow the app to run on port `80`.

To Setup:

Install Docker by running the following commands:
```
sudo apt-get update
sudo apt install curl -y
curl https://get.docker.com | sudo bash

sudo usermod -aG docker $(whoami)
```

Then restart your VM. (Stop then Start)

Install Compose by running the following commands:
```
sudo apt update

sudo apt install -y curl jq

version=$(curl -s https://api.github.com/repos/docker/compose/releases/latest | jq -r '.tag_name')

sudo curl -L "https://github.com/docker/compose/releases/download/${version}/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose
```

To clear up at the end of your session run:
``` docker-compose down --rmi all ```
