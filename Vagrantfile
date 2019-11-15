Vagrant.configure("2") do |config|
  config.vm.box = "jonr667/midas_triumf_titan_decayspec"
  config.vm.box_version = "0.2"
  config.vm.network "public_network", type: "dhcp"

VAGRANT_COMMAND = ARGV[0]
if VAGRANT_COMMAND == "ssh"
  config.ssh.username = 'ebit'
end

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
    vb.cpus = 1
  end
end
