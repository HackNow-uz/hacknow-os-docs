# HackNow Platforma Integratsiyasi

## Nima bu?

HackNow OS **HackNow platformasi** (hacknow.uz) bilan bevosita integratsiyalangan.
Platformadagi CTF lablar, mashqlar va musobaqalarga OS ichidan ulaning.

## HackNow CLI Toollar

### hn-lab-connect

Lab muhitiga ulanish uchun asosiy tool.

```bash
# Kirish
hn-lab-connect login

# Lab ishga tushirish
hn-lab-connect start <lab-id>

# Lab holatini ko'rish
hn-lab-connect status

# SSH bilan ulanish
hn-lab-connect ssh <lab-id>

# Lab to'xtatish
hn-lab-connect stop <lab-id>
```

### hn-vpn

Lab tarmoqlariga VPN orqali ulanish.

```bash
# Ulanish
hn-vpn connect

# Holatni tekshirish
hn-vpn status

# Uzish
hn-vpn disconnect
```

### hn-submit

CTF flag yuborish.

```bash
# Flag yuborish
hn-submit HN{flag_text}

# Ma'lum challenge uchun
hn-submit HN{flag_text} 42
```

### hn-update

Tizim va toollarni yangilash.

```bash
hn-update --all      # Hammasi
hn-update --system   # Faqat tizim
hn-update --tools    # Faqat toollar
```

### hn-info

Tizim ma'lumotlari.

```bash
hn-info
```

## CTF oqimi

1. hacknow.uz da challenge tanlang
2. `hn-lab-connect start <id>` bilan lab ishga tushiring
3. `hn-vpn connect` bilan tarmoqqa ulaning
4. Ishlang va bayroqni toping
5. `hn-submit HN{bayroq}` bilan yuboring

→ [FAQ](06-faq.md)
