Vagrant.configure("2") do |config|

  config.vm.define :clienteFw do |clienteFw|
     clienteFw.vm.box = "bento/centos-7.9"
     clienteFw.vm.network :private_network, ip: "209.191.60.2"
     clienteFw.vm.network :public_network, bridge: "Realtek 8822CE Wireless LAN 802.11ac PCI-E NIC"
     clienteFw.vm.hostname = "clienteFw"
     clienteFw.vm.box_download_insecure = true

  end
  config.vm.define :firewall do |firewall|

    firewall.vm.box = "bento/centos-7.9"
    firewall.vm.network :private_network, ip: "209.191.60.3"
    firewall.vm.network :private_network, ip: "192.168.60.5"
    firewall.vm.network :public_network, bridge: "Realtek 8822CE Wireless LAN 802.11ac PCI-E NIC"
    firewall.vm.network :forwarded_port, guest: 80, host:5567
    firewall.vm.hostname = "firewall"
    firewall.vm.box_download_insecure = true

  end
end
