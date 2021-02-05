Usage: devcloud list [ --plain ]
       devcloud add NAME [ --system SYSTEM --release RELEASE ]
       devcloud remove NAME
       devcloud clone SOURCE DESTINATION

This script assumes that you
0. install: apt install lxc lxc-templates
1. uncommented "LXC_DHCP_CONFILE=/etc/lxc/dnsmasq.conf" in /etc/default/lxc-net
2. sudo touch /etc/lxc/dnsmasq.conf
3. install yum for centos containers: sudo apt-get install yum
4. add this to /etc/network/interfaces to setup iptables-restore
   pre-up iptables-restore < /etc/iptables.rules
   post-down iptables-save > /etc/iptables.rules

5. remember to run service lxc-net restart after running devcloud add
6. check network port id
