Vagrant.configure("2") do |config|
  config.vm.box = "jonr667/midas_triumf_titan_decayspec"
  config.vm.box_version = "0.4"
  config.vm.hostname = "titan-decayspec"
  config.vm.network "public_network", type: "dhcp", use_dhcp_assigned_default_route: true, bridge: "enp11s0", mac: "080027444CA6"

  config.vm.synced_folder "experiment_data/", "/home/ebit/experiments", owner: "ebit", group: "ebit"

VAGRANT_COMMAND = ARGV[0]
if VAGRANT_COMMAND == "ssh"
  config.ssh.username = 'ebit'
end

config.vm.provision "shell",
    run: "always",
    inline: "dhclient eth1 > /dev/null"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "8192"
    vb.cpus = 4
  end
end
