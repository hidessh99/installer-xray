
# XRAY BBX
- ***Script XRAY Multi Port 443/80 By RamaGans ID***
- ***SCRIPT UNTUK MEMBUAT SERVER VPN***

#

# FITUR XRAY TLS
- TROJAN WS        : **443**
- TROJAN GRPC      : **443**
- SHADOWSOCKS WS   : **443**
- SHADOWSOCKS GRPC : **443**
- VMESS WS         : **443**
- VMESS GRPC       : **443**
- VLESS WS         : **443**
- VLESS GRPC       : **443**

# FITUR XRAY HTTP
- TROJAN WS        : **80**
- TROJAN GRPC      : **80**
- SHADOWSOCKS WS   : **80**
- SHADOWSOCKS GRPC : **80**
- VMESS WS         : **80**
- VMESS GRPC       : **80**
- VLESS WS         : **80**
- VLESS GRPC       : **80**

# Aplikasi VPN (Android Only)
* Link:
https://github.com/BrebesBlackXploit/XRAY-FOR-ANDROID


# OS 
- Debian 9 (HVM)
- Debian 10
* Berhasil di gunakan di vps aws dan os debian 9 hvm
* untuk vps isp yg lain saya tidak tau, dan os yg lain juga saya tidak tau:v

# Syarat && Bahan Untuk Menggunakan Script Ini
- Wajib Punya VPS
- Wajib Punya Akun Cloudflare
- Wajib Punya Domain Punya Kamu Sendiri
- ***Jika semua syarat dan Bahan sudah terpenuhi ,silahkan di coba script ini***

# Settingan Di Cloudflare
1. Buat VPS Baru
2. Pointing Dulu Domain Kamu, Kalo sudah pernah di pointing
   - Pergi ke dash.cloudflare.com,lalu pilih domain punya kamu, di tab TLS/SSL lalu pilih Overview, di tab TLS/SSL Harus pilih yang FULL
   - FULL (Encrypts end-to-end, using a self signed certificate on the server)✅
   ![settinggambar1](https://raw.githubusercontent.com/fisabiliyusri/XRAY-MANTAP/main/img/settingambar1.jpg)
   ![settinggambar2](https://raw.githubusercontent.com/fisabiliyusri/XRAY-MANTAP/main/img/settingambar2.jpg)
   ![settinggambar3](https://raw.githubusercontent.com/fisabiliyusri/XRAY-MANTAP/main/img/settingambar3.jpg)
   - Lalu pilih Edge Certificates disini kamu harus matikan Always Use HTTPS (Harus Mati/OFF)❌
   ![settinggambar4](https://raw.githubusercontent.com/fisabiliyusri/XRAY-MANTAP/main/img/settingambar4.jpg)
   - Buka tab Network di cloudflare kamu aktifkan WebSocket nya ✅
   ![settinggambar5](https://raw.githubusercontent.com/fisabiliyusri/XRAY-MANTAP/main/img/settingambar5.jpg)
   ![settinggambar6](https://raw.githubusercontent.com/fisabiliyusri/XRAY-MANTAP/main/img/settingambar6.jpg)
3. Setting Di Cloudflare Selesai
# Cara Install Script Nya
- Login ke VPS kamu ( wajib pake user ***root***)
1. MASUK KE VPS LALU KETIK

<p align="center">
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=sudo+su" />
</p>


```
sudo su
```

2. Update Dulu VPS NYA

<p align="center">
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=apt-get+update" />
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=apt-get+upgrade+-y" />
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=update-grub+&&+reboot" />
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=reboot" />
</p>

```
apt-get update && apt-get upgrade -y && update-grub && sleep 2 && reboot
```
- Otomatis Akan Reboot/ Hidupkan Ulang
3. Login Lagi Ke VPS NYA
4. Masukan Nama Domain Kamu, domain harus aktif
- contoh nama domain punya aku,silahkan ganti dengan punya kamu
```
cat >/root/domain <<EOF
mantapxsl.my.id
EOF
```
- ganti mantapxsl.my.id menjadi nama domain punya kamu
```
mkdir -p /etc/xray
cat >/etc/xray/domain <<EOF
mantapxsl.my.id
EOF
```

5. Salin kode di bawah ini dan paste kan ke dalam vps punya kamu
- maka proses install akan berjalan, jangan keluar dari vps
- jika keluar dari vps saat lagi proses install,maka akan gagal
```
wget https://raw.githubusercontent.com/BrebesBlackXploit/xray/main/setup.sh && chmod +x setup.sh && ./setup.sh
```
6. jika sudah selesai,lalu ketik xmenu untuk menampilkan menu
<p align="center">
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=xmenu" />
</p>

```
xmenu
```
7. DONE / SELESAI

# Info Perbaiki / FIX
- ***NOTE***
- jika xray dan nginx mengalami error !
- ketik
```
certv2ray
```
lalu ketik
```
restart-xray
```

# INFO KODE SCRIPT
- xmenu (untuk menampilkan menu
- updatedll (untuk update sc)
- restart-xray (hidupkan ulang xray)
- certv2ray (Perbarui Sertifikat / Update Certificate)

# Contoh Cara Pointing Domain ke Cloudflare
- Link:
```
otw
```
# Cara Pointing Subdomain Secara Otomatis Di Cloudflare Menggunakan Script
- edit dulu script auto-pointing nya
```
nano /usr/bin/auto-pointing
```
- contoh punya aku
- tinggal ubah saja yg cyberpanel1101.xyz menjadi domain punya kamu
```
DOMAIN=cyberpanel1101.xyz
SUB_DOMAIN=onichan-${sub}.cyberpanel1101.xyz
NS_DOMAIN=zerosl-${sub}.cyberpanel1101.xyz
CF_ID=brebesbxx@gmail.com
CF_KEY=1d872b5b696150212fcc866e3452b7cbeaa5e
```
- Lalu ubah juga CF_ID= isi dengan alamat email cloudflare kamu
- CF_KEY= isi dengan YOUR API KEY (GLOBAL API KEY)

# Cara Mendapatkan API KEY CLOUDFLARE
- Link
https://dash.cloudflare.com/profile/api-tokens
- API Keys ,Global API Key, Klik View, Masukan Password kamu, lalu klik View
- nanti muncul Your API Key ,lalu tinggal di salin/copy


