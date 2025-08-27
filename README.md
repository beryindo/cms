WAJIB UBUNTU 24.04

versi CMS terbaru 4.0.3

**UNTUK DI LOKAL TIDAK PERLU INSTALL L2TP, BISA LANGSUNG KE PROSES INSTALL CMS**

PASTIKAN LOGIN root

INSTALL L2TP untuk TUNNEL CMS
```
apt update
apt upgrade
apt install curl
uname -r
```
cek pastikan TIDAK ada mengandung kata cloud

```
wget https://raw.githubusercontent.com/beryindo/genieacs/refs/heads/main/vpnsetup.sh && chmod +x vpnsetup.sh
```
```
./vpnsetup.sh
```

```
wget -O add_vpn_user.sh https://raw.githubusercontent.com/hwdsl2/setup-ipsec-vpn/master/extras/add_vpn_user.sh
```
```
bash add_vpn_user.sh 'bery' '@Bery212'
```
Tambahkan L2TP Client di Mikrotik anda.

Selanjutnya cek di VPS ppp berapa ada terhubung
```
ip route list
```
misal responsenya seperti ini
```
192.168.42.10 dev ppp0 proto kernel scope link src 192.168.42.1
```
Artinya Mikrotik anda terhubung dengan ppp0. Maka tambahkan route di VPS
```
ip route add 10.0.0.0/24 dev ppp0
```
**10.0.0.0/24** adalah ip lokal modem/onu.


=========================================================================

```
wget https://raw.githubusercontent.com/beryindo/cms/refs/heads/main/install_docker.sh
chmod +x install_docker.sh
./install_docker.sh
```

Jika ada pilihan pilih n saja
