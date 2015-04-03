# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "hashicorp/precise64"
    config.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo apt-get install -y vim curl
      curl -sL https://deb.nodesource.com/setup | sudo bash -
      sudo apt-get install -y nodejs
      sudo npm install -g npm
      npm install -g hubot coffee-script yo generator-hubot
      wget -qO- https://toolbelt.heroku.com/install-ubuntu.sh | sh
    SHELL
    config.vm.provision "file", source: "vimrc", destination: "~/.vimrc"
end
