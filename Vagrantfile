VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.ssh.insert_key = false
  config.vm.box = 'https://yum.oracle.com/boxes/oraclelinux/latest/ol7-latest.box'
  config.vm.network 'forwarded_port', guest: 1521, host: 1521
  config.vm.network 'forwarded_port', guest: 5500, host: 5500
  config.vm.provision 'shell', path: 'provision.sh'
end
