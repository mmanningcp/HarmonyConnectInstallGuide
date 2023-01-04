# Harmony Connect Instal Guide
Update your Linux Repositories and any software running on your system.

    sudo apt-get update || upgrade

Install the nessesary dependancies 

    sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

Download docker gpg key

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add

Verify that you now have the key with the fingerprint

    sudo apt-key fingerprint 0EBFCD88

Add the stable repository

    sudo add-apt-repository \
    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
    $(lsb_release -cs) \
    stable" 

Install the latest version of Docker CE

    sudo apt-get install docker-ce docker-ce-cli containerd.io
