# O'rnatish qo'llanmasi

## 1. ISO yuklab olish

Eng so'nggi versiyani yuklab oling:
- **Rasmiy sayt:** [os.hacknow.uz](https://os.hacknow.uz)

### SHA256 tekshirish

```bash
sha256sum hacknow-os-0.1.iso
# Natijani os.hacknow.uz sahifasidagi hash bilan solishtiring
```

## 2. Bootable USB yaratish

### Linux (dd)

```bash
# USB qurilmangizni aniqlang
lsblk

# ISO'ni yozing (sdX ni o'zingizning USB bilan almashtiring!)
sudo dd if=hacknow-os-0.1.iso of=/dev/sdX bs=4M status=progress
sudo sync
```

### Linux (Balena Etcher)

1. [Balena Etcher](https://etcher.balena.io/) ni yuklab oling
2. ISO faylni tanlang
3. USB qurilmani tanlang
4. "Flash!" tugmasini bosing

### Windows (Rufus)

1. [Rufus](https://rufus.ie/) ni yuklab oling
2. USB qurilmani tanlang
3. ISO faylni tanlang
4. "DD Image" rejimini tanlang
5. "START" tugmasini bosing

## 3. Live rejimda ishga tushirish

1. Kompyuterni USB'dan boot qiling (BIOS/UEFI sozlamalarida boot tartibini o'zgartiring)
2. GRUB menyusidan "HackNow OS - Live" ni tanlang
3. Tizim yuklanadi — foydalanuvchi: `hacknow`, parol: `hacknow`

## 4. Diskka o'rnatish

Live rejimda ishga tushirgandan keyin:

1. Desktop'dagi **"HackNow OS O'rnatish"** ikonkasini bosing
2. Calamares installer ochiladi
3. Qadamlarni bajaring:
   - **Til:** O'zbek / Uzbek
   - **Joylashuv:** Asia → Tashkent
   - **Klaviatura:** Uzbek (yoki English US)
   - **Disk:** "Diskni tozalash" yoki "Qo'lda bo'lish"
   - **Foydalanuvchi:** Ism, login, parol kiriting
   - **Xulosa:** Tekshirib, "O'rnatish" tugmasini bosing
4. O'rnatish tugagach kompyuterni qayta ishga tushiring

## 5. O'rnatishdan keyin

```bash
# Tizimni yangilash
hn-update --all

# HackNow hisobiga kirish
hn-lab-connect login

# Tizim ma'lumotlari
hn-info
```

→ [Birinchi qadamlar](03-birinchi-qadamlar.md)
