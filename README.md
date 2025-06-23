# Manual IP, VPN, and Router Configuration

## Manual Static IP (Linux)
```bash
sudo ip addr add 192.168.1.100/24 dev eth0
sudo ip route add default via 192.168.1.1
```

## Manual Static IP (Windows)
```powershell
netsh interface ip set address "Ethernet" static 192.168.1.100 255.255.255.0 192.168.1.1
```

## VPN Configuration

### OpenVPN (Linux/Windows)
- [Install OpenVPN](https://openvpn.net/community-downloads/)
- Use `.ovpn` config files:
```bash
sudo openvpn --config client.ovpn
```

## Router Configuration

1. **Access Router Panel:** Usually at http://192.168.1.1
2. **Login:** Use admin credentials.
3. **Navigate:** Find LAN/DHCP or WAN settings.
4. **Set Static IP:** Assign fixed IP by MAC address or set static WAN IP.
5. **VPN Setup:** Many routers support OpenVPN, L2TP, or PPTP.

**Reference Guides:**
- [OpenVPN Docs](https://community.openvpn.net/openvpn/wiki/GettingStarted)
- [DD-WRT Wiki (Advanced Routers)](https://wiki.dd-wrt.com/wiki/index.php/Main_Page)
- [TP-Link Static IP Setup](https://www.tp-link.com/us/support/faq/14/)
