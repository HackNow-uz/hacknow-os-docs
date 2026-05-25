# Muammo hal qilish

## Tizim

### Ekran qora — boot qilmayapti

GRUB menyusida "HackNow OS - Live (Debug)" ni tanlang va xato xabarlarini o'qing.

### Audio ishlamayapti

```bash
# PulseAudio tekshirish
pulseaudio --check
pulseaudio --start

# ALSA tekshirish
aplay -l
alsamixer
```

### Tizim sekin ishlayapti

```bash
# Resurslarni tekshiring
htop
btop

# Disk bo'sh joyini tekshiring
df -h

# Keraksiz paketlarni o'chiring
sudo apt autoremove
```

## Tarmoq

### Internet yo'q

```bash
# NetworkManager tekshiring
nmcli general status
nmcli device status

# DNS tekshiring
cat /etc/resolv.conf
nslookup google.com
```

### VPN'dan keyin internet o'chdi

```bash
# VPN'ni uzib ko'ring
hn-vpn disconnect

# DNS'ni qayta sozlang
sudo systemctl restart NetworkManager
```

## Yordam

- **Telegram:** [t.me/hacknow_uz](https://t.me/hacknow_uz)
- **Email:** hacknow.uz@gmail.com
