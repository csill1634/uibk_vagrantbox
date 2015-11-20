# Default Vagrant Box

Referenzumgebung

## How to ##
1. Install Vagrant
2. Copy the Vagrantfile into the target directory
3. `vagrant up`
4. wait (might take some time)
5. `vagrant ssh`
5. `cd /vagrant` (in the box)
6. execute comand(s) on your project (e.g. `./activator run`)

/vagrant is synced to the "outside" folder containing the Vagrantfile.
