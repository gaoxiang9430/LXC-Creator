### Usage

* devcloud list [ --plain ]
* devcloud add NAME [ --system SYSTEM --release RELEASE ]
* devcloud remove NAME
* devcloud clone SOURCE DESTINATION

### Instructions

1. install: apt install lxc lxc-templates
2. uncommented "LXC_DHCP_CONFILE=/etc/lxc/dnsmasq.conf" in /etc/default/lxc-net
3. sudo touch /etc/lxc/dnsmasq.conf
4. install yum for centos containers: sudo apt-get install yum
5. add this to /etc/network/interfaces to setup iptables-restore
   - pre-up iptables-restore < /etc/iptables.rules
   - post-down iptables-save > /etc/iptables.rules
6. remember to run service lxc-net restart after running devcloud add
7. check network port id
