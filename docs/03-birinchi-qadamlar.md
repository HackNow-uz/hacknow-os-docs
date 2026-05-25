# Birinchi qadamlar

## Desktop tanishish

HackNow OS **XFCE** desktop muhitini ishlatadi:

- **Yuqori panel** — ilovalar menyusi, tizim tray, soat
- **Ish stoli** — tez kirish ikonkalari
- **Fayl menejeri** — Thunar
- **Terminal** — XFCE Terminal (Ctrl+Alt+T)

## Terminal

Kiberxavfsizlik ishlarining 90% terminal orqali bajariladi. Terminal ochish:

- **Ctrl+Alt+T** — yangi terminal
- **Desktop** → sichqoncha o'ng tugma → "Terminal ochish"

### Foydali buyruqlar

```bash
# Tizim ma'lumotlari
hn-info

# IP manzilni ko'rish
ip a
myip              # Tashqi IP

# Portlarni tekshirish
ports             # ss -tulnp alias

# Tizimni yangilash
hn-update --all
```

## HackNow platformaga ulanish

```bash
# 1. Hisobga kirish
hn-lab-connect login

# 2. Lab ro'yxati
hn-lab-connect status

# 3. Lab ishga tushirish
hn-lab-connect start 42

# 4. VPN ulanish
hn-vpn connect

# 5. Lab'ga SSH
hn-lab-connect ssh 42

# 6. Flag yuborish
hn-submit HN{flag_shu_yerda}
```

## Tool kategoriyalar

| Buyruq | Turi | Tavsif |
|--------|------|--------|
| `nmap` | Razvedka | Port va xizmat skanerlash |
| `sqlmap` | Web | SQL injection avtomatlashtirish |
| `burpsuite` | Web | Web proxy va skaner |
| `wireshark` | Tarmoq | Paket tahlili |
| `john` | Parol | Parol sindirish |
| `metasploit` | Exploit | Exploit framework |
| `ghidra` | Reverse | Reverse engineering |
| `aircrack-ng` | Wireless | Wi-Fi xavfsizlik |

Batafsil: [Tool qo'llanma](04-toollar.md)

## Muhim fayllar va papkalar

```
/opt/hacknow-tools/     — HackNow maxsus toollar
/usr/share/seclists/    — SecLists wordlistlar
/usr/share/wordlists/   → /usr/share/seclists (symlink)
~/.config/hacknow/      — HackNow konfiguratsiya
```

→ [Tool qo'llanma](04-toollar.md)
