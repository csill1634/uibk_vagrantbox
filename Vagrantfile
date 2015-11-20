Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest: 9000, host: 9000

  config.vm.provider "virtualbox" do |vb|
     vb.memory = "2048"
  end

   config.vm.provision "shell", inline: <<-SHELL
	apt-get install --yes python-software-properties
	add-apt-repository ppa:webupd8team/java
	apt-get update -qq
	echo debconf shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
	echo debconf shared/accepted-oracle-license-v1-1 seen true | /usr/bin/debconf-set-selections
	apt-get install --yes oracle-java8-installer
	yes "" | apt-get -f install

   SHELL
end
