# Ko'p beriladigan savollar (FAQ)

## Umumiy

### HackNow OS bepulmi?

Ha, to'liq bepul va ochiq kodli (GPL-3.0).

### Qaysi Debian versiyasiga asoslangan?

Debian 12 (Bookworm) stable.

### Kali Linux o'rniga ishlatsa bo'ladimi?

Ha! HackNow OS xuddi shu toollarni o'z ichiga oladi, qo'shimcha ravishda o'zbek tilida va HackNow platforma integratsiyasi bor.

### Virtual mashinada ishlatasam bo'ladimi?

Ha. VirtualBox, VMware, QEMU/KVM — barchasi ishlaydi. RAM 4GB va disk 30GB tavsiya etiladi.

## O'rnatish

### USB'dan boot qilolmayapman

1. BIOS/UEFI'da Secure Boot'ni o'chiring
2. Boot tartibida USB'ni birinchi qiling
3. UEFI rejimida bo'lsa, "UEFI: USB" ni tanlang

### Installer'da disk ko'rinmayapti

```bash
# Diskni tekshiring
sudo fdisk -l
```
NVMe disklar uchun qo'shimcha firmware kerak bo'lishi mumkin.

### Wi-Fi ishlamayapti

```bash
# Drayverlarni tekshiring
sudo dmesg | grep -i firmware
sudo apt install firmware-iwlwifi   # Intel
sudo apt install firmware-realtek   # Realtek
```

## Toollar

### Metasploit yangilanmayapti

```bash
sudo msfupdate
```

### Burp Suite sekin ishlayapti

Java xotira limitini oshiring:
```bash
# /opt/BurpSuiteCommunity/BurpSuiteCommunity.vmoptions
-Xmx2g
```

### Python tool'ni pipx bilan o'rnatib bo'lmayapti

```bash
pipx ensurepath
pipx install <tool-name>
```

## HackNow platforma

### Login xatosi

```bash
# Token'ni tozalang va qayta kiring
rm ~/.config/hacknow/token
hn-lab-connect login
```

### VPN ulanmayapti

```bash
# OpenVPN log'ini tekshiring
cat /tmp/hn-vpn.log

# DNS ni tekshiring
nslookup lab.hacknow.uz
```

→ [Muammo hal qilish](07-troubleshooting.md)
